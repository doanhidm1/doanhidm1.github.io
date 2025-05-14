# Storages.searchPath

機能/意味
:   パスの検索

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   searchPath(filename, searchpath)

引数
:   |  |  |
    | --- | --- |
    | filename | 検索対象ファイル名 |
    | searchpath | 検索対象パス（ローカル表記(c:\～等)で";"区切り，省略時はシステムのデフォルト検索パス） |

戻り値
:   見つからなかった場合はvoid，見つかった場合はファイルのフルパス(file://./～)

説明