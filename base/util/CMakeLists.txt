add_library(wcdb_util
  src/error.cpp
  src/file.cpp
  src/path.cpp
  src/rwlock.cpp
  src/spin.cpp
  src/ticker.cpp
)

target_include_directories(wcdb_util
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../abstract/include
)
