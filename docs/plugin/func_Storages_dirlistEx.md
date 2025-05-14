# Storages.dirlistEx

機能/意味
:   指定ディレクトリのファイル一覧と詳細情報を取得する

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   dirlistEx(dir)

引数
:   |  |  |
    | --- | --- |
    | dir | ディレクトリ名 |

戻り値
:   ファイル情報一覧が格納された配列\n[ %[ name:ファイル名, size, attrib, mtime, atime, ctime ], ... ]\ndirlistと違いnameにおいてフォルダの場合の末尾"/"追加がないので注意(attribで判定のこと)

説明