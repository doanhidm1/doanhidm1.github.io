# Bitmap.onLoaded

機能/意味
:   非同期読込みが完了した

タイプ
:   [Bitmapクラス](class_Bitmap)のイベント

構文
:   onLoaded(meta, async, error, message)

引数
:   |  |  |
    | --- | --- |
    | meta | 読み込んだ画像のタグ情報です。 |
    | async | 非同期で読み込まれたかどうかです。画像データがキャッシュ内にある場合、 Bitmap.loadAsync 実行中に本イベントが発生します。 |
    | error | 画像読込みでエラーが発生したかどうかです。 |
    | message | エラーメッセージです。エラーが発生した場合、エラーメッセージが渡されます。 |

戻り値
:   なし (void)

説明
:   非同期読込みが完了した時に発生します。
    読み込んだ画像は Layer.copyFromBitmapToMainImage で Layer にコピーできます。
    読込み処理は非同期であるため、読込みが完了した時に、その画像を渡す Layer が既に無効化されている可能性があります。
    本イベントで他のオブジェクトへアクセスする場合は、無効化されていないか確認して下さい。
    もしくは、本イベントが完了するまで対象オブジェクトが無効化されないようにしてください。

参照
:   [Bitmap.loadAsync](func_Bitmap_loadAsync)
    [Layer.copyFromBitmapToMainImage](func_Layer_copyFromBitmapToMainImage)