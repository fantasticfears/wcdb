add_library(wcdb_abstract
  src/clause_join.cpp
  src/column.cpp
  src/column_def.cpp
  src/column_index.cpp
  src/column_result.cpp
  src/column_type.cpp
  src/conflict.cpp
  src/constraint_table.cpp
  src/describable.cpp
  src/expr.cpp
  src/foreign_key.cpp
  src/handle.cpp
  src/handle_statement.cpp
  src/module_argument.cpp
  src/order.cpp
  src/order_term.cpp
  src/pragma.cpp
  src/statement.cpp
  src/statement_alter_table.cpp
  src/statement_attach.cpp
  src/statement_create_index.cpp
  src/statement_create_table.cpp
  src/statement_create_virtual_table.cpp
  src/statement_delete.cpp
  src/statement_detach.cpp
  src/statement_drop_index.cpp
  src/statement_drop_table.cpp
  src/statement_explain.cpp
  src/statement_insert.cpp
  src/statement_pragma.cpp
  src/statement_reindex.cpp
  src/statement_release.cpp
  src/statement_rollback.cpp
  src/statement_savepoint.cpp
  src/statement_select.cpp
  src/statement_transaction.cpp
  src/statement_update.cpp
  src/statement_vacuum.cpp
  src/subquery.cpp
  src/value_pragma.cpp
)

target_include_directories(wcdb_abstract
  PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../..
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../util/include
  PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../repair/include
)
target_link_libraries(wcdb_abstract wcdb_util wcdb_repair)
