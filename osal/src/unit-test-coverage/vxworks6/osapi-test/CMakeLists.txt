
aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} TESTCASE_FILES)
add_executable(osapi-test ${TESTCASE_FILES})
set_target_properties(osapi-test PROPERTIES LINK_FLAGS "${UT_C_FLAGS}")
target_link_libraries(osapi-test ut_osal_osapi ${OSALCOVERAGE_LINK_LIBRARIES})
add_test(osapi-test osapi-test)
