# Layer.copyToBitmapFromMainImage

機能/意味
:   Bitmap への画像のコピー

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   copyToBitmapFromMainImage(dest)

引数
:   |  |  |
    | --- | --- |
    | dest | コピー先の [Bitmap](f_Bitmap) オブジェクトを指定します。 |

戻り値
:   なし (void)

説明
:   dest で指定した Bitmap オブジェクトへレイヤのメイン画像をコピーします。
    　画像サイズはコピー元のレイヤの画像サイズと同一になります。
    　コピーといっても、実際は「同じ画像を二つ以上のレイヤで共有している」という状態になるだけなので
    このメソッドはほとんど実行時間がかかりません。

参照
:   [Layer.copyFromBitmapToMainImage](f_Layer_copyFromBitmapToMainImage)