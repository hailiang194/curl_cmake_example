cmake_minimum_required(VERSION 3.16)
project(CurlGet)

set(BUILD_CURL_EXE OFF)
set(BUILD_SHARED_LIBS OFF)

add_subdirectory(vendors/curl)

add_executable(CurlGet src/main.cpp)

target_link_libraries(CurlGet PRIVATE libcurl)