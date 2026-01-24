# Find all source files in a single current directory
# Save the name to DIR_ePaper_SRCS
# aux_source_directory(. DIR_ePaper_SRCS)

# include_directories(../Config)

# Generate the link library
# add_library(ePaper ${DIR_ePaper_SRCS})
# target_link_libraries(ePaper PUBLIC Config)

add_library(ePaper INTERFACE)
target_include_directories(ePaper INTERFACE
	ePaper_1in54_V2
    )

target_link_libraries(ePaper INTERFACE
    ePaper_1in54_V2
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
