# BinaryStream.compress

機能/意味
:   別のストレージからデータを圧縮しつつコピー

タイプ
:   [BinaryStreamクラス](class_BinaryStream)のメソッド

構文
:   compress(storage, elm)

引数
:   |  |  |
    | --- | --- |
    | storage | コピー元のストレージ（現在開いているストレージと同じ場合は例外） |
    | elm | 動作指定用の辞書（in/out）内容は copy() と同じものに加えて下記： comp\_lv :[in] zlibによる圧縮レベル（1～9）省略時，またはelmそのものの指定がない場合は 9 |

戻り値
:   書き込んだバイト数

説明
:   対象ストレージを zlib/deflate で圧縮しつつ，現在のストリームのポジションから書き込みます
    フィルタ関数は圧縮前のバイナリに対して適用されます