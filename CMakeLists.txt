cmake_minimum_required(VERSION 3.22)

project(flightlab)

################################################################################

include(FetchContent)
include(GNUInstallDirs)

################################################################################

include(InstallRequiredSystemLibraries)

################################################################################

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

if(WIN32)
    set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG   ${CMAKE_RUNTIME_OUTPUT_DIRECTORY})
    set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE ${CMAKE_RUNTIME_OUTPUT_DIRECTORY})
endif()

set(CMAKE_POSITION_INDEPENDENT_CODE ON)

################################################################################

if(UNIX)
    if(CMAKE_SYSTEM_NAME STREQUAL "Linux")
        add_definitions(-D__linux__)
    endif()
elseif(WIN32)
    add_definitions(-DWIN32)
    add_definitions(-D_WINDOWS)
endif()

if (CMAKE_BUILD_TYPE STREQUAL "Debug")
    add_definitions(-DDEBUG)
    add_definitions(-D_DEBUG)
endif()

################################################################################

if(UNIX)
    set(CMAKE_C_FLAGS "-Wall")
    set(CMAKE_C_FLAGS_DEBUG   "-O0")
    set(CMAKE_C_FLAGS_RELEASE "-O2")
elseif(WIN32)
    set(CMAKE_C_FLAGS_DEBUG   "-W1")
    set(CMAKE_C_FLAGS_RELEASE "-W1 -O2")
endif()

################################################################################

include_directories(./)

################################################################################

add_subdirectory(src)

