# Storages.getPlacedPath

機能/意味
:   ストレージの検索、拡張子指定版

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   getPlacedPath(storage, extlist)

引数
:   |  |  |
    | --- | --- |
    | storage | 検索したいストレージ名を指定します。 |
    | extlist | 拡張子リスト。"|"で区切って拡張子を列挙する。例.".tlg|.png|.jpg|.bmp" |

戻り値
:   発見された場所が統一ストレージ名で返ります。
    見つからなかった場合は空文字列が返ります。

説明
:   storage で指定されたストレージを自動検索パスから検索します。
    storageに拡張子が付いている場合は、拡張子を取り除いてからリストの拡張子が付与されます。

参照
:   [Storages.getFullPath](func_Storages_getFullPath)
    [Storages.isExistentStorage](func_Storages_isExistentStorage)