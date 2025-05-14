# Layer.copyFromBitmapToMainImage

機能/意味
:   Bitmap からの画像のコピー

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   copyFromBitmapToMainImage(src)

引数
:   |  |  |
    | --- | --- |
    | src | コピー元の Bitmap オブジェクトを指定します。 |

戻り値
:   なし (void)

説明
:   src で指定した Bitmap オブジェクトからレイヤのメイン画像へ画像をコピーします。
    画像サイズはコピー元のBitmap オブジェクトの画像サイズと同一になります。
    コピーといっても、実際は「同じ画像を二つ以上のレイヤで共有している」という状態になるだけなのでこのメソッドはほとんど実行時間がかかりません。

参照
:   [Layer.copyToBitmapFromMainImage](func_Layer_copyToBitmapFromMainImage)