cmake_minimum_required(VERSION 3.15.1)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake/modules)

project(IndexStoreDB
  LANGUAGES C CXX Swift)
enable_testing()

set(CMAKE_Swift_MODULE_DIRECTORY ${CMAKE_BINARY_DIR}/swift)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED YES)
set(CMAKE_CXX_EXTENSIONS NO)

set(CMAKE_POSITION_INDEPENDENT_CODE YES)

find_package(dispatch CONFIG)
find_package(Foundation CONFIG)
if(BUILD_TESTING)
  find_package(XCTest CONFIG)
endif()

include(SwiftSupport)

add_subdirectory(lib)
add_subdirectory(Sources)
add_subdirectory(cmake/modules)
if(BUILD_TESTING)
  add_subdirectory(Tests)
endif()
