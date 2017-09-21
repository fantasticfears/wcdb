add_library(wcdb_repair
  src/sqliterk_output.cpp
  src/sqliterk.c
  src/sqliterk_api.c
  src/sqliterk_btree.c
  src/sqliterk_column.c
  src/sqliterk_crypto.c
  src/sqliterk_os.c
  src/sqliterk_pager.c
  src/sqliterk_util.c
  src/sqliterk_values.c
)

target_include_directories(wcdb_repair PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
