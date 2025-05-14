# SqliteThread

sqliteのスレッド実行サポート

# メンバ

コンストラクタ
:   [SqliteThread](func_SqliteThread_SqliteThread)

メソッド
:   [abort](func_SqliteThread_abort) (実行処理を中止させます。 )
    [onProgress](func_SqliteThread_onProgress) (更新処理経過 )
    [onStateChange](func_SqliteThread_onStateChange) (状態変更 )
    [select](func_SqliteThread_select) (検索処理をバックグランドで実行する。 )
    [update](func_SqliteThread_update) (更新処理をバックグランドでトランザクション実行する。 )

プロパティ
:   [errorCode](prop_SqliteThread_errorCode) (エラーコード )
    [progressUpdateCount](prop_SqliteThread_progressUpdateCount) (onProgress で呼び出す頻度指定 )
    [selectResult](prop_SqliteThread_selectResult) (select取得データ(配列) )
    [state](prop_SqliteThread_state) (実行ステート )

定数
:   DONE (処理完了 )
    INIT (初期状態 )
    WORKING (処理中 )