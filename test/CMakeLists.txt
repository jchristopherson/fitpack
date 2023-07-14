include("${PROJECT_SOURCE_DIR}/cmake/helper.cmake")

set(fitpack_test_sources
    test.f90
    fitpack_curve_tests.f90
    fitpack_test_data.f90
    fitpack_tests.f90
)

add_executable(fitpack_tests ${fitpack_test_sources})
link_library(fitpack_tests ${PROJECT_NAME} ${PROJECT_INCLUDE_DIR})
add_test(
    NAME fitpack_tests
    WORKING_DIRECTORY ${CMAKE_LIBRARY_OUTPUT_DIRECTORY}
    COMMAND $<TARGET_FILE:fitpack_tests>
)