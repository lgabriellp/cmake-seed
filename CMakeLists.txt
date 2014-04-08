cmake_minimum_required(VERSION 2.8)
project(seed)

add_subdirectory(deps/cpputest)
add_subdirectory(src)
add_subdirectory(tests)

get_cmake_property(_variableNames VARIABLES)
foreach (_variableName ${_variableNames})
    message(STATUS "${_variableName}=${${_variableName}}")
endforeach()
