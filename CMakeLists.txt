
# The following lines of boilerplate have to be in your project's CMakeLists
# in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)
#them ADF_PATH vao Enviroment windows

execute_process(COMMAND git describe --always --tags --dirty
                OUTPUT_VARIABLE ADF_VER
                OUTPUT_STRIP_TRAILING_WHITESPACE)
add_definitions(-DADF_VER=\"${ADF_VER}\")

if(NOT DEFINED ENV{IDF_PATH})
set(ENV{IDF_PATH} "$ENV{ADF_PATH}/esp-idf/")
endif()
set(EXTRA_COMPONENT_DIRS $ENV{ADF_PATH}/components)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(voip_app)
