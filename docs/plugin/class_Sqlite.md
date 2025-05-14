# Sqlite

Sqliteクラス

# メンバ

コンストラクタ
:   [Sqlite](func_Sqlite_Sqlite)

メソッド
:   [begin](func_Sqlite_begin) (トランザクションの開始 )
    [commit](func_Sqlite_commit) (トランザクションのコミット )
    [exec](func_Sqlite_exec) (SQLを実行する。 )
    [execValue](func_Sqlite_execValue) (値取得用にSQLを実行する。 )
    [rollback](func_Sqlite_rollback) (トランザクションのロールバック )

プロパティ
:   [errorCode](prop_Sqlite_errorCode) (直前のコマンド実行のエラーコード )
    [errorMessage](prop_Sqlite_errorMessage) (直前のコマンド実行のエラーメッセージ )
    [lastInsertRowId](prop_Sqlite_lastInsertRowId) (直前の挿入の行ID )

定数
:   SQLITE\_ABORT (Callback routine requested an abort )
    SQLITE\_AUTH (Authorization denied )
    SQLITE\_BUSY (The database file is locked )
    SQLITE\_CANTOPEN (Unable to open the database file )
    SQLITE\_CONSTRAINT (Abort due to constraint violation )
    SQLITE\_CORRUPT (The database disk image is malformed )
    SQLITE\_DONE (sqlite3\_step() has finished executing )
    SQLITE\_EMPTY (Database is empty )
    SQLITE\_ERROR (SQL error or missing database )
    SQLITE\_FORMAT (Auxiliary database format error )
    SQLITE\_FULL (Insertion failed because database is full )
    SQLITE\_INTERNAL (Internal logic error in SQLite )
    SQLITE\_INTERRUPT (Operation terminated by sqlite3\_interrupt() )
    SQLITE\_IOERR (Some kind of disk I/O error occurred )
    SQLITE\_LOCKED (A table in the database is locked )
    SQLITE\_MISMATCH (Data type mismatch )
    SQLITE\_MISUSE (Library used incorrectly )
    SQLITE\_NOLFS (Uses OS features not supported on host )
    SQLITE\_NOMEM (A malloc() failed )
    SQLITE\_NOTADB (File opened that is not a database file )
    SQLITE\_NOTFOUND (NOT USED. Table or record not found )
    SQLITE\_OK (Successful result )
    SQLITE\_PERM (Access permission denied )
    SQLITE\_PROTOCOL (NOT USED. Database lock protocol error )
    SQLITE\_RANGE (2nd parameter to sqlite3\_bind out of range )
    SQLITE\_READONLY (Attempt to write a readonly database )
    SQLITE\_ROW (sqlite3\_step() has another row ready )
    SQLITE\_SCHEMA (The database schema changed )
    SQLITE\_TOOBIG (String or BLOB exceeds size limit )