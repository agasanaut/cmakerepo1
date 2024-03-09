cmake_minimum_required(VERSION 3.10)
project(AdditionLibrary)

set(CMAKE_CXX_STANDARD 17)

# Set source files
set(SOURCE_FILES addition.cpp)

# Create the shared library
add_library(AdditionLibrary SHARED ${SOURCE_FILES})

# Set the library name and version
set_target_properties(AdditionLibrary PROPERTIES
    VERSION 1.0
    SOVERSION 1
)

# Install the library
install(TARGETS AdditionLibrary
    LIBRARY DESTINATION /home/tejnxt/github/cmakerepo1/lib
)

