# Find all source files in a single current directory
# Save the name to DIR_examples_SRCS
# aux_source_directory(. DIR_examples_SRCS)

# include_directories(../lib/Config)
# include_directories(../lib/GUI)
# include_directories(../lib/e-Paper)

# # Generate the link library
# add_library(examples ${DIR_examples_SRCS})
# target_link_libraries(examples PUBLIC Config)


add_library(ePaper_examples INTERFACE)
target_include_directories(ePaper_examples INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples INTERFACE
    ePaper_examples_2in13_V2
    ePaper_examples_2in13_V3
    ePaper_examples_2in13_V4
    ePaper_examples_2in13b_V3
    ePaper_examples_2in13b_V4
    ePaper_examples_2in13bc
    ePaper_examples_2in13d
    ePaper_examples_2in66
    ePaper_examples_2in66b
    ePaper_examples_2in7
    ePaper_examples_2in7_V2
    ePaper_examples_2in9_V2
    ePaper_examples_2in9b_V3
    ePaper_examples_2in9b_V4
    ePaper_examples_2in9bc
    ePaper_examples_2in9d
    ePaper_examples_3in7
    ePaper_examples_4in2
    ePaper_examples_4in2_V2
    ePaper_examples_4in2b_V2
    ePaper_examples_4in2b_V2_old
    ePaper_examples_5in65f
    ePaper_examples_5in83_V2
    ePaper_examples_5in83b_V2
    ePaper_examples_7in5_V2
    ePaper_examples_7in5_V2_old
    ePaper_examples_7in5b_V2
    ePaper_examples_7in5b_V2_old
    )

# ===

# Shared bitmap data (ImageData.c) used by every device demo via EPD_Test.h
add_library(ePaper_examples_common INTERFACE)
target_include_directories(ePaper_examples_common INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_sources(ePaper_examples_common INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/ImageData.c
    )

# ===

add_library(ePaper_examples_2in13_V2 INTERFACE)
target_include_directories(ePaper_examples_2in13_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13_V2
    )

target_sources(ePaper_examples_2in13_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13_V2_test.c
    )

# ===

add_library(ePaper_examples_2in13_V3 INTERFACE)
target_include_directories(ePaper_examples_2in13_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13_V3 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13_V3
    )

target_sources(ePaper_examples_2in13_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13_V3_test.c
    )

# ===

add_library(ePaper_examples_2in13_V4 INTERFACE)
target_include_directories(ePaper_examples_2in13_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13_V4 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13_V4
    )

target_sources(ePaper_examples_2in13_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13_V4_test.c
    )

# ===

add_library(ePaper_examples_2in13b_V3 INTERFACE)
target_include_directories(ePaper_examples_2in13b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13b_V3 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13b_V3
    )

target_sources(ePaper_examples_2in13b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13b_V3_test.c
    )

# ===

add_library(ePaper_examples_2in13b_V4 INTERFACE)
target_include_directories(ePaper_examples_2in13b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13b_V4 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13b_V4
    )

target_sources(ePaper_examples_2in13b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13b_V4_test.c
    )

# ===

add_library(ePaper_examples_2in13bc INTERFACE)
target_include_directories(ePaper_examples_2in13bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13bc INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13bc
    )

target_sources(ePaper_examples_2in13bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13bc_test.c
    )

# ===

add_library(ePaper_examples_2in13d INTERFACE)
target_include_directories(ePaper_examples_2in13d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in13d INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in13d
    )

target_sources(ePaper_examples_2in13d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13d_test.c
    )

# ===

add_library(ePaper_examples_2in66 INTERFACE)
target_include_directories(ePaper_examples_2in66 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in66 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in66
    )

target_sources(ePaper_examples_2in66 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in66_test.c
    )

# ===

add_library(ePaper_examples_2in66b INTERFACE)
target_include_directories(ePaper_examples_2in66b INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in66b INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in66b
    )

target_sources(ePaper_examples_2in66b INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in66b_test.c
    )

# ===

add_library(ePaper_examples_2in7 INTERFACE)
target_include_directories(ePaper_examples_2in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in7 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in7
    )

target_sources(ePaper_examples_2in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in7_test.c
    )

# ===

add_library(ePaper_examples_2in7_V2 INTERFACE)
target_include_directories(ePaper_examples_2in7_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in7_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in7_V2
    )

target_sources(ePaper_examples_2in7_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in7_V2_test.c
    )

# ===

add_library(ePaper_examples_2in9_V2 INTERFACE)
target_include_directories(ePaper_examples_2in9_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in9_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in9_V2
    )

target_sources(ePaper_examples_2in9_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9_V2_test.c
    )

# ===

add_library(ePaper_examples_2in9b_V3 INTERFACE)
target_include_directories(ePaper_examples_2in9b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in9b_V3 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in9b_V3
    )

target_sources(ePaper_examples_2in9b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9b_V3_test.c
    )

# ===

add_library(ePaper_examples_2in9b_V4 INTERFACE)
target_include_directories(ePaper_examples_2in9b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in9b_V4 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in9b_V4
    )

target_sources(ePaper_examples_2in9b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9b_V4_test.c
    )

# ===

add_library(ePaper_examples_2in9bc INTERFACE)
target_include_directories(ePaper_examples_2in9bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in9bc INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in9bc
    )

target_sources(ePaper_examples_2in9bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9bc_test.c
    )

# ===

add_library(ePaper_examples_2in9d INTERFACE)
target_include_directories(ePaper_examples_2in9d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in9d INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_2in9d
    )

target_sources(ePaper_examples_2in9d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9d_test.c
    )

# ===

add_library(ePaper_examples_3in7 INTERFACE)
target_include_directories(ePaper_examples_3in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_3in7 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_3in7
    )

target_sources(ePaper_examples_3in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_3in7_test.c
    )

# ===

add_library(ePaper_examples_4in2 INTERFACE)
target_include_directories(ePaper_examples_4in2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_4in2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_4in2
    )

target_sources(ePaper_examples_4in2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2_test.c
    )

# ===

add_library(ePaper_examples_4in2_V2 INTERFACE)
target_include_directories(ePaper_examples_4in2_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_4in2_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_4in2_V2
    )

target_sources(ePaper_examples_4in2_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2_V2_test.c
    )

# ===

add_library(ePaper_examples_4in2b_V2 INTERFACE)
target_include_directories(ePaper_examples_4in2b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_4in2b_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_4in2b_V2
    )

target_sources(ePaper_examples_4in2b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2b_V2_test.c
    )

# ===

add_library(ePaper_examples_4in2b_V2_old INTERFACE)
target_include_directories(ePaper_examples_4in2b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_4in2b_V2_old INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_4in2b_V2_old
    )

target_sources(ePaper_examples_4in2b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2b_V2_test_old.c
    )

# ===

add_library(ePaper_examples_5in65f INTERFACE)
target_include_directories(ePaper_examples_5in65f INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_5in65f INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_5in65f
    )

target_sources(ePaper_examples_5in65f INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_5in65f_test.c
    )

# ===

add_library(ePaper_examples_5in83_V2 INTERFACE)
target_include_directories(ePaper_examples_5in83_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_5in83_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_5in83_V2
    )

target_sources(ePaper_examples_5in83_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_5in83_V2_test.c
    )

# ===

add_library(ePaper_examples_5in83b_V2 INTERFACE)
target_include_directories(ePaper_examples_5in83b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_5in83b_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_5in83b_V2
    )

target_sources(ePaper_examples_5in83b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_5in83b_V2_test.c
    )

# ===

add_library(ePaper_examples_7in5_V2 INTERFACE)
target_include_directories(ePaper_examples_7in5_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_7in5_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_7in5_V2
    )

target_sources(ePaper_examples_7in5_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5_V2_test.c
    )

# ===

add_library(ePaper_examples_7in5_V2_old INTERFACE)
target_include_directories(ePaper_examples_7in5_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_7in5_V2_old INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_7in5_V2_old
    )

target_sources(ePaper_examples_7in5_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5_V2_test_old.c
    )

# ===

add_library(ePaper_examples_7in5b_V2 INTERFACE)
target_include_directories(ePaper_examples_7in5b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_7in5b_V2 INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_7in5b_V2
    )

target_sources(ePaper_examples_7in5b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5b_V2_test.c
    )

# ===

add_library(ePaper_examples_7in5b_V2_old INTERFACE)
target_include_directories(ePaper_examples_7in5b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_7in5b_V2_old INTERFACE
    ePaper_Config
    ePaper_GUI
    ePaper_Fonts
    ePaper_examples_common
    ePaper_7in5b_V2_old
    )

target_sources(ePaper_examples_7in5b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5b_V2_test_old.c
    )
