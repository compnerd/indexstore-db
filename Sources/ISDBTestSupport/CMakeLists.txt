add_library(ISDBTestSupport
  SourceFileCache.swift
  TestLocationScanner.swift
  TestLocation.swift
  TestSources.swift
  TibsTestWorkspace.swift
  XCTestAssertions.swift)
set_target_properties(ISDBTestSupport PROPERTIES
  INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_Swift_MODULE_DIRECTORY})
target_link_libraries(ISDBTestSupport PUBLIC
  IndexStoreDB
  XCTest)
