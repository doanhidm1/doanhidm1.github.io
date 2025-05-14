# Zip.add

機能/意味
:   アーカイブにファイルを追加します

タイプ
:   [Zipクラス](class_Zip)のメソッド

構文
:   add(srcfile, destfile, commpressLevel, password)

引数
:   |  |  |
    | --- | --- |
    | srcfile | 追加するファイル（吉里吉里ストレージ名） |
    | destfile | アーカイブ中での名前(アーカイブ内パス名） |
    | deflateLevel | 圧縮レベル 0(無圧縮) ～ 9(最大圧縮) 省略時は 6になる |
    | password | 暗号化パスワード指定 |

戻り値
:   追加に成功したら true

説明