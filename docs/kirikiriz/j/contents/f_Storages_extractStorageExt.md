# Storages.extractStorageExt

機能/意味
:   ストレージ名の拡張子の抽出

タイプ
:   [Storagesクラス](f_Storages)のメソッド

構文
:   extractStorageExt(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | 拡張子部分を抽出したいストレージ名を指定します。 |

戻り値
:   拡張子部分が返ります。拡張子部分は . (ドット)も含みます。拡張子が
    なかった場合は空文字列が返ります。

説明
:   指定されたストレージ名から拡張子の部分を抽出して返します。

参照
:   [Storages.extractStorageName](f_Storages_extractStorageName)
    [Storages.extractStoragePath](f_Storages_extractStoragePath)
    [Storages.chopStorageExt](f_Storages_chopStorageExt)