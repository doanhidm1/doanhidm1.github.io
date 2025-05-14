# BinaryStream.copy

機能/意味
:   別のストレージからデータをコピー

タイプ
:   [BinaryStreamクラス](class_BinaryStream)のメソッド

構文
:   copy(storage, elm)

引数
:   |  |  |
    | --- | --- |
    | storage | コピー元のストレージ（現在開いているストレージと同じ場合は例外） |
    | elm | 動作指定用の辞書（in/out）内容は下記：（省略時は単純コピー，[out]なし） offset :[in] コピー元ストレージの読み込み開始オフセット（省略時先頭） length :[in] コピー元ストレージの最大読み込みサイズ（省略時ファイルサイズ）  filter :[in] フィルタ処理を行う関数名（省略時はフィルタ処理なし） fparam :[in] フィルタに渡すパラメータ値(int)  nocopy :[in] trueを指定すると出力を書き込まない（省略時はfalse，hashのみ取得したい場合などに指定） md5 :[in] trueを指定すると出力のMD5ダイジェストを返す  hash :[out]読み込んだファイルのハッシュ値（Adler32） read :[out]読み込んだバイト数 digest :[out]書き込んだデータのMD5ダイジェスト（octet） ※md5がtrueの場合にのみ有効 |

戻り値
:   書き込んだバイト数

説明
:   対象ストレージのoffsetからlength分の内容が，現在のストリームのポジションから書き込まれます
    フィルタの詳細は setFilter() の説明を参照してください