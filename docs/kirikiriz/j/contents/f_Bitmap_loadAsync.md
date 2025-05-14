# Bitmap.loadAsync

機能/意味
:   画像の非同期読み込み

タイプ
:   [Bitmapクラス](f_Bitmap)のメソッド

構文
:   loadAsync(image)

引数
:   |  |  |
    | --- | --- |
    | image | 読み込む画像ストレージを指定します。  　ここで指定するファイル名は拡張子を含んだものになることに注意してください。  　拡張子がないとファイルが見つからずエラーとなります。 |

戻り値
:   なし (void)

説明
:   画像を非同期で読み込みます。
    　読込みの完了は [Bitmap.onLoaded](f_Bitmap_onLoaded) で受け取れます。
    　非同期読込み中か否かは [Bitmap.loading](f_Bitmap_loading) で確認できます。
    　非同期読込み中は [Bitmap.loading](f_Bitmap_loading) 以外のメンバへアクセスすると例外が発生します。
    　[Bitmap.onLoaded](f_Bitmap_onLoaded) の説明も確認してください。

参照
:   [Bitmap.onLoaded](f_Bitmap_onLoaded)
    [Bitmap.loading](f_Bitmap_loading)
    [Layer.copyFromBitmapToMainImage](f_Layer_copyFromBitmapToMainImage)