# Storages.chopStorageExt

機能/意味
:   ストレージ名の拡張子の切り落とし

タイプ
:   [Storagesクラス](f_Storages)のメソッド

構文
:   chopStorageExt(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | 拡張子部分を切り落としたいストレージ名を指定します。 |

戻り値
:   拡張子部分が切り落とされたストレージ名が返ります。

説明
:   指定されたストレージ名から拡張子の部分を切り落として返します。
    　たとえば "file://home/dee/hoge.txt" を渡した場合、"file://home/dee/hoge" が返
    ります。

参照
:   [Storages.extractStorageExt](f_Storages_extractStorageExt)