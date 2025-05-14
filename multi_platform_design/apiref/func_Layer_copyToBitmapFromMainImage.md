# Layer.copyToBitmapFromMainImage

機能/意味
:   Bitmap への画像のコピー

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   copyToBitmapFromMainImage(dest)

引数
:   |  |  |
    | --- | --- |
    | dest | コピー先の Bitmap オブジェクトを指定します。 |

戻り値
:   なし (void)

説明
:   dest で指定した Bitmap オブジェクトへレイヤのメイン画像をコピーします。
    画像サイズはコピー元のレイヤの画像サイズと同一になります。
    コピーといっても、実際は「同じ画像を二つ以上のレイヤで共有している」という状態になるだけなのでこのメソッドはほとんど実行時間がかかりません。

参照
:   [Layer.copyFromBitmapToMainImage](func_Layer_copyFromBitmapToMainImage)