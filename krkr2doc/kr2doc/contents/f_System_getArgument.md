# System.getArgument

機能/意味
:   コマンドラインオプションの取得

タイプ
:   [Systemクラス](f_System)のメソッド

構文
:   getArgument(name)

引数
:   |  |  |
    | --- | --- |
    | name | 取得するコマンドラインオプション名を指定します。最初に '-' ( ハイフン ) をつけてください ( 例 : '-nosplash' )。 |

戻り値
:   コマンドラインオプションが指定されていればその値、指定されていなければ
    void が返ります。

説明
:   コマンドラインオプションは、
    -name=value
    または
    -name
    　の形式で吉里吉里に渡されている必要があります。前者の場合は値として value が
    返り、前者の場合は値として 'yes' が返ります。

参照
:   [System.setArgument](f_System_setArgument)