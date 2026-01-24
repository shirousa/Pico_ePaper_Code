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
    ePaper_examples_2in7
    )

# ===

add_library(ePaper_examples_2in7 INTERFACE)
target_include_directories(ePaper_examples_2in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_examples_2in7 INTERFACE
    Config
    )

target_sources(ePaper_examples_2in7 INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/EPD_2in7_test.c
    )
