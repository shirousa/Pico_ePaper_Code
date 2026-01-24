# Find all source files in a single current directory
# Save the name to DIR_GUI_SRCS
# aux_source_directory(. DIR_GUI_SRCS)

# include_directories(../Config)

# Generate the link library
# add_library(GUI ${DIR_GUI_SRCS})
# target_link_libraries(GUI PUBLIC Config)

add_library(ePaper_GUI INTERFACE)
target_include_directories(ePaper_GUI INTERFACE
	${CMAKE_CURRENT_LIST_DIR})

target_link_libraries(ePaper_GUI INTERFACE
    ePaper_Config
    )

target_sources(ePaper_GUI INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/GUI_Paint.c
    )
