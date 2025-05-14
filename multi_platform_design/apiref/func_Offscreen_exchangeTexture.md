# Offscreen.exchangeTexture

機能/意味
:   フレームバッファに設定されているテクスチャとTextureクラスが指すテクスチャを入れ替える。

タイプ
:   [Offscreenクラス](class_Offscreen)のメソッド

構文
:   exchangeTexture(texture:Texture)

引数
:   |  |  |
    | --- | --- |
    | texture | 交換するTextureクラスのインスタンス。 |

戻り値
:   なし (void)

説明
:   交換するテクスチャのサイズは合わせておかないと例外となる。
    カラーフォーマットもRGBAとする必要がある。
    レンダリング途中での入れ替えも行わない方がいいかもしれない(要確認)。
    クロスフェードなどで両方に描画する必要がない場合、以前の画像をTextureとして取り出し、新しいTextureに差し替えることでオーバーヘッドを減らせる。