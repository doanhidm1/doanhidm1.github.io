# ImageFunction.copy9Patch

機能/意味
:   9 path を利用した画像コピー(マルチプラットフォーム版以降)

タイプ
:   [ImageFunctionクラス](class_ImageFunction)のメソッド

構文
:   copy9Patch(dst:Bitmap, src:Bitmap) :Rect

引数
:   |  |  |
    | --- | --- |
    | dst | コピー先Bitmap |
    | src | コピー元Bitmap |

戻り値
:   マージン情報

説明
:   9 path ( slice ) を利用した画像コピーを行います。
    返されるマージン情報はRectクラスのオブジェクトです。
    このマージン内にテキストなど描画します。