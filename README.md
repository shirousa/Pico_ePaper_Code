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
## このフォークについて (Differences from upstream)

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