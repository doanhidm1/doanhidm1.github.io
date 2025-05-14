# Storages.isExistentStorage

機能/意味
:   ストレージの存在確認

タイプ
:   [Storagesクラス](f_Storages)のメソッド

構文
:   isExistentStorage(storage)

引数
:   |  |  |
    | --- | --- |
    | storage | 存在を確認したいストレージ名を指定します。 |

戻り値
:   存在を確認できれば真、なければ偽が返ります。

説明
:   storage で指定したストレージが存在するかどうかを確認します。getPlacedPath を用いるよりは高速
    です。

参照
:   [Storages.getPlacedPath](f_Storages_getPlacedPath)