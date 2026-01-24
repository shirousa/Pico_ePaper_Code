# Find all source files in a single current directory
# Save the name to DIR_Config_SRCS
# aux_source_directory(. DIR_Config_SRCS)

# Generate the link library
# add_library(Config ${DIR_Config_SRCS})
# target_link_libraries(Config PUBLIC pico_stdlib hardware_spi)

add_library(ePaper_Config INTERFACE)
target_include_directories(ePaper_Config INTERFACE 
	${CMAKE_CURRENT_LIST_DIR}
    )

target_link_libraries(ePaper_Config INTERFACE
    pico_stdlib
    hardware_spi
    )

target_sources(ePaper_Config INTERFACE
	${CMAKE_CURRENT_LIST_DIR}/DEV_Config.c
    )
