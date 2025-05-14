# Texture.Texture

機能/意味
:   ミップマップ生成版コンストラクタ

タイプ
:   [Textureクラス](class_Texture)のメソッド

構文
:   Texture(sizelist:Array, filename:string, type=stFastAreaAvg, typeopt:real=1)

引数
:   |  |  |
    | --- | --- |
    | sizelist | ミップマップを生成するサイズを配列で幅、高さの組み合わせで指定します。 |
    | filename | 画像ファイル名 |
    | type | 縮小アルゴリズムを指定します。ImageFunction.operateStretch の type か Layer.operateStretch の type 引数と同じです。 |
    | typeopt | ３次元補間時のシャープネスです。他の補間方法では現在のところ意味を持ちません。 |

戻り値
:   なし (void)

説明