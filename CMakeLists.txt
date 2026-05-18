cmake_minimum_required(VERSION 3.15)
project(mathlib VERSION 1.0 LANGUAGES CXX)

add_library(mathlib src/mathlib.cpp)
target_include_directories(mathlib PUBLIC include)
target_compile_definitions(mathlib PRIVATE PKG_VERSION="${PROJECT_VERSION}")

set_target_properties(mathlib PROPERTIES PUBLIC_HEADER "include/mathlib.h")
install(TARGETS mathlib)
