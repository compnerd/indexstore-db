add_library(ISDBTibs
  Data.swift
  JSONCompilationDatabase.swift
  Makefile.swift
  OutputFileMap.swift
  Process.swift
  TibsBuilder.swift
  TibsManifest.swift
  TibsResolvedTarget.swift
  TibsToolchain.swift)
set_target_properties(ISDBTibs PROPERTIES
  INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_Swift_MODULE_DIRECTORY})
# FIXME(compnerd) should these be public?
target_link_libraries(ISDBTibs PUBLIC
  Foundation)
