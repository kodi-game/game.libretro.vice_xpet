cmake_minimum_required(VERSION 3.1)
project(game.libretro.vice)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-vice REQUIRED)

set(VICE_CUSTOM_BINARY ${VICE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} VICE "")

include(CPack)
