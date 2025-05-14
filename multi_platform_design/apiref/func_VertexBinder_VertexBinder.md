# VertexBinder.VertexBinder

機能/意味
:   コンストラクタ

タイプ
:   [VertexBinderクラス](class_VertexBinder)のメソッド

構文
:   VertexBinder(vertex:VertexBuffer, stride:int=0, componentCount:int=4, offset:int=0, normalize:bool=false)

引数
:   |  |  |
    | --- | --- |
    | vertex | 関連付けるVertexBuffer |
    | stride | 頂点ごとのストライドをバイト数で指定します。XY座標をfloat型で渡すのであればsizeof(float)\*2なので、8を指定します。 |
    | componentCount | 頂点要素数を渡します。XY座標を渡すのであれば2を指定します。RGBAカラーなら4です。 |
    | offset | VertexBufferの先頭からのオフセットをバイト数で指定します。一つのVertexBufferで複数の頂点情報を格納している場合に使用します。 |
    | normalize | 正規化するかどうかを指定します。trueの場合、非float型の時[-1.0～0.0～1.0]の間に正規化されシェーダーに送られます。 |

戻り値
:   なし (void)

説明