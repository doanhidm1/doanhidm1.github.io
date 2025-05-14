# SqliteStatement

Sqliteのステートメントを扱うクラス

# メンバ

メソッド
:   [bind](func_SqliteStatement_bind) (パラメータのバインド @parma params バインドするパラメータ(配列または辞書) )
    [bindAt](func_SqliteStatement_bindAt) (パラメータのバインド @parma value 値 )
    [close](func_SqliteStatement_close) (ステートを閉じる )
    [exec](func_SqliteStatement_exec) (ステートメント実行 )
    [get](func_SqliteStatement_get) (結果の取得。 )
    [getName](func_SqliteStatement_getName) (カラム名の取得 )
    [getType](func_SqliteStatement_getType) (カラムの型の取得 )
    [isNull](func_SqliteStatement_isNull) (カラムのNULL判定 )
    [open](func_SqliteStatement_open) (新規ステートを開く )
    [reset](func_SqliteStatement_reset) (バインド状態のリセット )
    [step](func_SqliteStatement_step) (ステートメントステップ実行 )

プロパティ
:   [columnCount](prop_SqliteStatement_columnCount) (カラム数(読み込み専用) )
    [count](prop_SqliteStatement_count) (データ数(読み込み専用) step の後設定されます )
    [sql](prop_SqliteStatement_sql) (元SQL(読み込み専用) )

定数
:   SQLITE\_INTEGER (カラムの型識別用 )