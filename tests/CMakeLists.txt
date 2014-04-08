set(CppUTest_DIR ${PROJECT_SOURCE_DIR}/deps/cpputest)

include_directories(${CppUTest_DIR}/include)
file(GLOB SOURCES *.cpp)

add_executable(unit ${SOURCES})
add_definitions(-Wall -Werror -g -ggdb)
target_link_libraries(unit src CppUTest CppUTestExt)

add_custom_target(
    unit-tests
    COMMAND ${PROJECT_SOURCE_DIR}/build/tests/unit
    DEPENDS unit)
