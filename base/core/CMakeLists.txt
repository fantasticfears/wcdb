add_library(wcdb_core
  src/config.cpp
  src/core_base.cpp
  src/database.cpp
  src/database_config.cpp
  src/database_file.cpp
  src/database_repair_kit.cpp
  src/database_sql.cpp
  src/database_transaction.cpp
  src/handle_pool.cpp
  src/handle_recyclable.cpp
  src/statement_recyclable.cpp
  src/transaction.cpp
)

target_include_directories(wcdb_core
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../abstract/include
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../repair/include
)
target_link_libraries(wcdb_core wcdb_util wcdb_abstract wcdb_repair)
