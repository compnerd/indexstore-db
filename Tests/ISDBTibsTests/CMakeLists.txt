add_library(ISDBTibsTests
  MiscTests.swift
  OutputFileMapTests.swift
  TibsBuildTests.swift
  TibsCompilationDatabaseTests.swift
  TibsManifestTests.swift
  TibsResolutionTests.swift
  XCTestManifests.swift)
set_target_properties(ISDBTibsTests PROPERTIES
  INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_Swift_MODULE_DIRECTORY})
target_link_libraries(ISDBTibsTests PRIVATE
  ISDBTibs
  XCTest)
