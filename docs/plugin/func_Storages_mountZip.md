# Storages.mountZip

機能/意味
:   zipファイルをファイルシステムとして mount します

タイプ
:   [Storagesクラス](class_Storages)のメソッド

構文
:   mountZip(name, zipfile)

引数
:   |  |  |
    | --- | --- |
    | name | ドメイン名 |
    | zipfile | マウントするZIPファイル名 |

戻り値
:   マウントに成功したら true

説明
:   zip://ドメイン名/ファイル名 でアクセス可能になります。読み込み専用になります。