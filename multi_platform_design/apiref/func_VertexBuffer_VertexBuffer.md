# VertexBuffer.VertexBuffer

機能/意味
:   頂点配列を指定して頂点バッファを作ります

タイプ
:   [VertexBufferクラス](class_VertexBuffer)のメソッド

構文
:   VertexBuffer(data:Array, dataType:int, updateType:int, isIndex:bool=false)

引数
:   |  |  |
    | --- | --- |
    | data | 頂点配列。バッファサイズはこの配列の要素数×データ型サイズ。 |
    | dataType | データの型。dtByte/dtUByte/dtShort/dtUShort/dtInt/dtFloat |
    | updateType | データ更新頻度。utStream/utStatic/utDynamic |
    | isIndex | インデックスバッファかどうか。頂点バッファならfalse |

戻り値
:   なし (void)

説明