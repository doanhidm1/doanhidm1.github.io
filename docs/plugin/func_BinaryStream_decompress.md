# BinaryStream.decompress

機能/意味
:   別のストレージからデータを展開しつつコピー

タイプ
:   [BinaryStreamクラス](class_BinaryStream)のメソッド

構文
:   decompress(storage, elm)

引数
:   |  |  |
    | --- | --- |
    | storage | コピー元のストレージ（現在開いているストレージと同じ場合は例外） |
    | elm | 動作指定用の辞書（in/out）内容は copy() と同じ |

戻り値
:   書き込んだバイト数

説明
:   対象ストレージを zlib/inflate で展開しつつ，現在のストリームのポジションから書き込みます
    展開に失敗すると例外が発生します
    フィルタ関数は展開後のバイナリに対して適用されます
    hash[out] は展開後／フィルタ後のバイナリに対して計算されます