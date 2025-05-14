# SqliteThread.select

機能/意味
:   検索処理をバックグランドで実行する。

タイプ
:   [SqliteThreadクラス](class_SqliteThread)のメソッド

構文
:   select(sql, params)

引数
:   |  |  |
    | --- | --- |
    | sql | 実行するSQL |
    | params | バインドするパラメータ(配列または辞書) |

戻り値
:   処理が開始されたら true

説明
:   結果は内部に蓄積されて完了後に引き渡されます。