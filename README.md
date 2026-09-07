# Pico_ePaper_Code
## waveshare electronics
![waveshare_logo.png](waveshare_logo.png)

## 中文：
微雪电子 Pico-ePaper 系列驱动代码，支持C和Python

更多资料请在官网搜索相关产品：
> https://www.waveshare.net or https://www.waveshare.net/wiki
***
## English:
Waveshrae Pico-ePaper series drivers code, Support C and Python.

For more information, please search on the official website:
> https://www.waveshare.com or https://www.waveshare.com/wiki/Main_Page

***
## 日本語：このフォークについて

このリポジトリは [waveshareteam/Pico_ePaper_Code](https://github.com/waveshareteam/Pico_ePaper_Code) のフォークで、`c/` 配下の CMake ビルド構成を作り直しています。upstream 本家は現時点(フォーク後)で変更が無いため、本家との差分はそのまま以下の内容です。

### 何を変えたか

1. **CMake をデバイス単位で細かくビルド・リンクできるように再構成**
   従来は `aux_source_directory` で `c/lib/e-Paper` 配下の全ドライバ(約30機種分)を1つの `ePaper` ライブラリにまとめてビルドし、`c/main.c` のコメントアウトで使うデバイスを切り替える方式でした。
   これを、デバイスごとの `INTERFACE` ライブラリに分割しました。必要なデバイスだけを選んで `target_link_libraries()` すれば、そのデバイスのソースだけがコンパイル対象になります。

   ```cmake
   # 例: 1.54inch V2 と 2.7inch のデモだけをリンクしたい場合
   add_subdirectory(path/to/this-repo/c)

   target_link_libraries(YourExecutable
       ePaper_1in54_V2          # デバイスドライバ (lib/e-Paper)
       ePaper_examples_2in7     # デモコード一式 (examples) -- GUI/Fonts/共通画像データも自動で付いてくる
   )
   ```

   命名規則:
   - `ePaper_<component>` … `ePaper_Config` / `ePaper_GUI` / `ePaper_Fonts`(共通部品)
   - `ePaper_<device>` … `ePaper_1in54_V2` などデバイスドライバ本体(`lib/e-Paper`)
   - `ePaper_examples_<device>` … `ePaper_examples_2in7` などデモ・使用例コード(`examples`)

   このリポジトリの `c/` 自体はもう実行ファイルを生成しません(`pico_sdk_init()` や `add_executable` は含みません)。外側に自分のプロジェクトを1つ用意し、`pico_sdk_init()` → `add_subdirectory(path/to/this-repo/c)` → 上記のように `target_link_libraries()` する使い方を想定しています。

2. **1.54inch V2 (`EPD_1in54_V2`) ドライバを追加**
   本家未収録だった 1.54inch V2 e-Paper 用のドライバ(`EPD_1in54_V2.c` / `.h`)を追加しました。

### 検証状況

- 静的検証: 全デバイスの `target_sources` / `target_link_libraries` の参照整合性(ファイル実在・ターゲット解決)をスクリプトでチェック済み
- 実ビルド検証: CMake + Ninja + ARM GNU Toolchain + Pico SDK を使い、`ePaper_1in54_V2` と `ePaper_examples_2in7` を選んでリンクする外部プロジェクトで実際に `compile` → `link` まで成功を確認済み(警告・エラー0件)。他デバイスのソースがビルドに巻き込まれないことも確認済み
- 各ディスプレイの実機での表示動作そのもの(ハードウェア検証)は未実施です

### 移行状況

`lib/e-Paper` の全29ドライバ、`examples` の全27デモを上記の個別ライブラリ形式に移行済みです。

***
## English: About this fork

This repository is a fork of [waveshareteam/Pico_ePaper_Code](https://github.com/waveshareteam/Pico_ePaper_Code) that rebuilds the CMake build setup under `c/`. Upstream has not moved since this fork was created, so the diff against upstream is exactly what's described below.

### What changed

1. **Restructured CMake so each device can be built and linked individually**
   Previously, `aux_source_directory` swept every driver in `c/lib/e-Paper` (~30 devices) into a single `ePaper` library, and `c/main.c` selected which one to build by commenting/uncommenting lines.
   This has been split into one `INTERFACE` library per device. Pick only the device(s) you need in `target_link_libraries()`, and only that device's sources get compiled.

   ```cmake
   # Example: link only the 1.54inch V2 driver and the 2.7inch demo
   add_subdirectory(path/to/this-repo/c)

   target_link_libraries(YourExecutable
       ePaper_1in54_V2          # device driver (lib/e-Paper)
       ePaper_examples_2in7     # demo code (examples) -- pulls in GUI/Fonts/shared image data automatically
   )
   ```

   Naming convention:
   - `ePaper_<component>` — shared pieces: `ePaper_Config` / `ePaper_GUI` / `ePaper_Fonts`
   - `ePaper_<device>` — device driver itself, e.g. `ePaper_1in54_V2` (`lib/e-Paper`)
   - `ePaper_examples_<device>` — demo/usage-example code, e.g. `ePaper_examples_2in7` (`examples`)

   `c/` no longer produces an executable on its own (no `pico_sdk_init()` or `add_executable()` in it). It's meant to be consumed from an outer project of your own: `pico_sdk_init()` → `add_subdirectory(path/to/this-repo/c)` → `target_link_libraries()` as shown above.

2. **Added the 1.54inch V2 (`EPD_1in54_V2`) driver**
   Added the driver (`EPD_1in54_V2.c` / `.h`) for the 1.54inch V2 e-Paper display, which wasn't in upstream.

### Verification status

- Static check: scripted verification that every device's `target_sources` / `target_link_libraries` references resolve (files exist, targets are defined)
- Real build check: using CMake + Ninja + ARM GNU Toolchain + Pico SDK, an external project linking only `ePaper_1in54_V2` and `ePaper_examples_2in7` compiled and linked cleanly (0 warnings/errors), and no other device's sources were pulled into the build
- Actual on-device display behavior has not been verified (no hardware testing)

### Migration status

All 29 drivers in `lib/e-Paper` and all 27 demos in `examples` have been migrated to the per-device library form described above.