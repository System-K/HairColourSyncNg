# CMake build for the SKSE-Hotfixes Linux/clang-cl toolchain (upstream builds with HairColourSyncNg.vcxproj).
cmake_minimum_required(VERSION 3.21)
project(HairColourSyncNg LANGUAGES CXX)
find_package(CommonLibSSE CONFIG REQUIRED)
add_library(HairColourSyncNg SHARED dllmain.cpp plugin.cpp)
target_compile_features(HairColourSyncNg PRIVATE cxx_std_23)
target_link_libraries(HairColourSyncNg PRIVATE CommonLibSSE::CommonLibSSE psapi)
