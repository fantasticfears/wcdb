cmake_minimum_required (VERSION 3.8.10)
project(WCDB)

set(CMAKE_CXX_STANDARD 11)

execute_process(
  COMMAND make -f Makefile.preprocessed
  WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/../sqlcipher
)

add_subdirectory(abstract)
add_subdirectory(core)
add_subdirectory(util)
add_subdirectory(repair)
