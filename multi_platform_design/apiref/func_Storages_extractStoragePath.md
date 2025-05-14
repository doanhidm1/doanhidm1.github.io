# Storages.extractStoragePath

機能/意味
:   ストレージ名のパスの抽出

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   extractStoragePath(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | パスを抽出したいストレージ名を指定します。 |

戻り値
:   パスが返ります。パスがなかった場合は空文字列が返ります。

説明
:   指定されたストレージ名から、パスの部分を抽出して返します。
    たとえば "file://home/dee/hoge.txt" を渡した場合、"file://home/dee/" が返ります。

参照
:   [Storages.extractStorageExt](func_Storages_extractStorageExt)
    [Storages.extractStorageName](func_Storages_extractStorageName)