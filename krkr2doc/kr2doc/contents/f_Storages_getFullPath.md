# Storages.getFullPath

機能/意味
:   完全な統一ストレージ名の取得

タイプ
:   [Storagesクラス](f_Storages)のメソッド

構文
:   getFullPath(path)

引数
:   |  |  |
    | --- | --- |
    | path | 完全な統一ストレージ名にしたいストレージ名を指定します。 |

戻り値
:   完全な統一ストレージ名

説明
:   path で指定されたストレージ名を完全な統一ストレージ名に変換します。
    　冗長なパスアクセス ( たとえば system/flags/../data/ など ) はすべて圧縮されます。
    　カレントメディア、カレントフォルダが指定されていなければ、補完します。

参照
:   [Storages.getPlacedPath](f_Storages_getPlacedPath)