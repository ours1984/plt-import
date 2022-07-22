cmake_minimum_required(VERSION 3.5)

project(pltimport)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

function(print var)
  message(STATUS "${var} = ${${var}}")
endfunction()

aux_source_directory(. DIR_SRCS)

print(DIR_SRCS)

add_executable(pltimport
    ${DIR_SRCS}
)

target_link_libraries(pltimport
    -lm
)