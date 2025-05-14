# Sqlite.Sqlite

機能/意味
:   コンストラクタ

タイプ
:   [Sqliteクラス](class_Sqlite)のメソッド

構文
:   Sqlite(database, readonly)

引数
:   |  |  |
    | --- | --- |
    | database | データベースファイル |
    | readonly | 読み込み専用で開く |

戻り値
:   なし (void)

説明
:   ※読み込み専用時は吉里吉里のファイル機構が使われます。そうでない場合はOSの機構を使います。