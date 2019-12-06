add_subdirectory(IndexStoreDBTests)
add_subdirectory(ISDBTibsTests)

add_executable(tests
  LinuxMain.swift)
target_link_libraries(tests PRIVATE
  ISDBTestSupport
  IndexStoreDBTests
  ISDBTibsTests)

add_test(NAME check-indexstore-db
  COMMAND tests)
