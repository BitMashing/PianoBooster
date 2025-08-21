cmake_minimum_required(VERSION 3.10)

# Force C++17 for Qt6 compatibility
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Use Qt6 instead of Qt5
set(QT_PACKAGE_NAME Qt6)

if(COMMAND cmake_policy)
    cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

# set project's name
PROJECT( pianobooster )

add_compile_options(-std=c++17 -Wno-deprecated-declarations)
add_compile_definitions(GL_SILENCE_DEPRECATION)


ADD_SUBDIRECTORY(src build)
