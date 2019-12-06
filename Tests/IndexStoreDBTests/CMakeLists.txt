add_library(IndexStoreDBTests
  IndexStoreDBTests.swift
  IndexTests.swift
  LocationScannerTests.swift
  XCTestManifests.swift)
set_target_properties(IndexStoreDBTests PROPERTIES
  INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_Swift_MODULE_DIRECTORY})
target_link_libraries(IndexStoreDBTests PRIVATE
  IndexStoreDB
  XCTest)
