cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  test.c
)

add_executable(paltest_getsysteminfo_test1
  ${SOURCES}
)

add_dependencies(paltest_getsysteminfo_test1 CoreClrPal)

target_link_libraries(paltest_getsysteminfo_test1
  pthread
  m
  CoreClrPal
)
