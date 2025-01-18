cmake_minimum_required(VERSION 3.10) # Adjust if needed

project(LabVector)

# Set include directories
include_directories(
    .
)

# Source files
set(SOURCE_FILES
    testVector.cpp
)

# Add executable
add_executable(LabVector ${SOURCE_FILES})

# Target-specific options (optional)
if(CMAKE_BUILD_TYPE MATCHES Debug)
    # Debug-specific options
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g -O0")
endif()

if(CMAKE_BUILD_TYPE MATCHES Release)
    # Release-specific options
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -DNDEBUG")
endif()
