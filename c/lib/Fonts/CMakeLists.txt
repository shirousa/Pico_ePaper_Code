# Find all source files in a single current directory
# Save the name to DIR_Fonts_SRCS
# aux_source_directory(. DIR_Fonts_SRCS)

# Generate the link library
# add_library(Fonts ${DIR_Fonts_SRCS})

add_library(ePaper_Fonts INTERFACE)
target_include_directories(ePaper_Fonts INTERFACE
	${CMAKE_CURRENT_LIST_DIR})

target_sources(ePaper_Fonts INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/font8.c
	${CMAKE_CURRENT_LIST_DIR}/font12.c
	${CMAKE_CURRENT_LIST_DIR}/font12CN.c
	${CMAKE_CURRENT_LIST_DIR}/font16.c
	${CMAKE_CURRENT_LIST_DIR}/font20.c
	${CMAKE_CURRENT_LIST_DIR}/font24.c
	${CMAKE_CURRENT_LIST_DIR}/font24CN.c
    )
