# Storages.extractStorageName

機能/意味
:   ストレージ名の抽出

タイプ
:   [Storagesクラス](f_Storages)のメソッド

構文
:   extractStorageName(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | ストレージ名を抽出したいストレージ名を指定します。 |

戻り値
:   ストレージ名が返ります。ストレージ名がなかった場合は空文字列が返ります。

説明
:   指定されたストレージ名から、ストレージ名の部分 ( パスを除く ) を抽出して返します。
    　たとえば "System/hoge.txt" を渡した場合、"hoge.txt" が返ります。

参照
:   [Storages.extractStorageExt](f_Storages_extractStorageExt)
    [Storages.extractStoragePath](f_Storages_extractStoragePath)