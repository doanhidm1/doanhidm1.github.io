# BinaryStream.setFilter

機能/意味
:   フィルタDLLを設定する

タイプ
:   [BinaryStreamクラス](class_BinaryStream)のメソッド

構文
:   setFilter(dll)

引数
:   |  |  |
    | --- | --- |
    | dll | 対象のDLLファイル（voidの場合は設定解除） |

戻り値
:   なし (void)

説明
:   copy/compress/decompressのデータに対して外部DLLを使用したフィルタを設定します
    elm.filter に関数名を指定た場合に，このDLL中の下記の形式でエクスポートされた関数をフィルタとして使用します
    void (\_\_stdcall \*FilterProc)(uint32 hash, uint64 offset, void \*buffer, uint32 length);