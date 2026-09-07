# Find all source files in a single current directory
# Save the name to DIR_ePaper_SRCS
# aux_source_directory(. DIR_ePaper_SRCS)

# include_directories(../Config)

# Generate the link library
# add_library(ePaper ${DIR_ePaper_SRCS})
# target_link_libraries(ePaper PUBLIC Config)

add_library(ePaper INTERFACE)

target_link_libraries(ePaper INTERFACE
    ePaper_1in54_V2
    ePaper_2in7
    ePaper_2in13_V2
    ePaper_2in13_V3
    ePaper_2in13_V4
    ePaper_2in13b_V3
    ePaper_2in13b_V4
    ePaper_2in13bc
    ePaper_2in13d
    ePaper_2in66
    ePaper_2in66b
    ePaper_2in7_V2
    ePaper_2in9_V2
    ePaper_2in9b_V3
    ePaper_2in9b_V4
    ePaper_2in9bc
    ePaper_2in9d
    ePaper_3in7
    ePaper_4in2
    ePaper_4in2_V2
    ePaper_4in2b_V2
    ePaper_4in2b_V2_old
    ePaper_5in65f
    ePaper_5in83_V2
    ePaper_5in83b_V2
    ePaper_7in5_V2
    ePaper_7in5_V2_old
    ePaper_7in5b_V2
    ePaper_7in5b_V2_old
    )

# ===

add_library(ePaper_1in54_V2 INTERFACE)
target_include_directories(ePaper_1in54_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_1in54_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_1in54_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_1in54_V2.c
    )

# ===

add_library(ePaper_2in7 INTERFACE)
target_include_directories(ePaper_2in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in7 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in7.c
    )

# ===

add_library(ePaper_2in13_V2 INTERFACE)
target_include_directories(ePaper_2in13_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13_V2.c
    )

# ===

add_library(ePaper_2in13_V3 INTERFACE)
target_include_directories(ePaper_2in13_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13_V3 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13_V3.c
    )

# ===

add_library(ePaper_2in13_V4 INTERFACE)
target_include_directories(ePaper_2in13_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13_V4 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13_V4.c
    )

# ===

add_library(ePaper_2in13b_V3 INTERFACE)
target_include_directories(ePaper_2in13b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13b_V3 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13b_V3.c
    )

# ===

add_library(ePaper_2in13b_V4 INTERFACE)
target_include_directories(ePaper_2in13b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13b_V4 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13b_V4.c
    )

# ===

add_library(ePaper_2in13bc INTERFACE)
target_include_directories(ePaper_2in13bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13bc INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13bc.c
    )

# ===

add_library(ePaper_2in13d INTERFACE)
target_include_directories(ePaper_2in13d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in13d INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in13d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in13d.c
    )

# ===

add_library(ePaper_2in66 INTERFACE)
target_include_directories(ePaper_2in66 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in66 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in66 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in66.c
    )

# ===

add_library(ePaper_2in66b INTERFACE)
target_include_directories(ePaper_2in66b INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in66b INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in66b INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in66b.c
    )

# ===

add_library(ePaper_2in7_V2 INTERFACE)
target_include_directories(ePaper_2in7_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in7_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in7_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in7_V2.c
    )

# ===

add_library(ePaper_2in9_V2 INTERFACE)
target_include_directories(ePaper_2in9_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in9_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in9_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9_V2.c
    )

# ===

add_library(ePaper_2in9b_V3 INTERFACE)
target_include_directories(ePaper_2in9b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in9b_V3 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in9b_V3 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9b_V3.c
    )

# ===

add_library(ePaper_2in9b_V4 INTERFACE)
target_include_directories(ePaper_2in9b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in9b_V4 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in9b_V4 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9b_V4.c
    )

# ===

add_library(ePaper_2in9bc INTERFACE)
target_include_directories(ePaper_2in9bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in9bc INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in9bc INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9bc.c
    )

# ===

add_library(ePaper_2in9d INTERFACE)
target_include_directories(ePaper_2in9d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_2in9d INTERFACE
    ePaper_Config
    )

target_sources(ePaper_2in9d INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in9d.c
    )

# ===

add_library(ePaper_3in7 INTERFACE)
target_include_directories(ePaper_3in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_3in7 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_3in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_3in7.c
    )

# ===

add_library(ePaper_4in2 INTERFACE)
target_include_directories(ePaper_4in2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_4in2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_4in2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2.c
    )

# ===

add_library(ePaper_4in2_V2 INTERFACE)
target_include_directories(ePaper_4in2_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_4in2_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_4in2_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2_V2.c
    )

# ===

add_library(ePaper_4in2b_V2 INTERFACE)
target_include_directories(ePaper_4in2b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_4in2b_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_4in2b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2b_V2.c
    )

# ===

add_library(ePaper_4in2b_V2_old INTERFACE)
target_include_directories(ePaper_4in2b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_4in2b_V2_old INTERFACE
    ePaper_Config
    )

target_sources(ePaper_4in2b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_4in2b_V2_old.c
    )

# ===

add_library(ePaper_5in65f INTERFACE)
target_include_directories(ePaper_5in65f INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_5in65f INTERFACE
    ePaper_Config
    )

target_sources(ePaper_5in65f INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_5in65f.c
    )

# ===

add_library(ePaper_5in83_V2 INTERFACE)
target_include_directories(ePaper_5in83_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_5in83_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_5in83_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_5in83_V2.c
    )

# ===

add_library(ePaper_5in83b_V2 INTERFACE)
target_include_directories(ePaper_5in83b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_5in83b_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_5in83b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_5in83b_V2.c
    )

# ===

add_library(ePaper_7in5_V2 INTERFACE)
target_include_directories(ePaper_7in5_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_7in5_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_7in5_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5_V2.c
    )

# ===

add_library(ePaper_7in5_V2_old INTERFACE)
target_include_directories(ePaper_7in5_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_7in5_V2_old INTERFACE
    ePaper_Config
    )

target_sources(ePaper_7in5_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5_V2_old.c
    )

# ===

add_library(ePaper_7in5b_V2 INTERFACE)
target_include_directories(ePaper_7in5b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_7in5b_V2 INTERFACE
    ePaper_Config
    )

target_sources(ePaper_7in5b_V2 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5b_V2.c
    )

# ===

add_library(ePaper_7in5b_V2_old INTERFACE)
target_include_directories(ePaper_7in5b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_7in5b_V2_old INTERFACE
    ePaper_Config
    )

target_sources(ePaper_7in5b_V2_old INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_7in5b_V2_old.c
    )
