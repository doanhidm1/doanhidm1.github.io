# Layer.releaseCapture

機能/意味
:   マウスイベントキャプチャの解除

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   releaseCapture()

引数
:   なし

戻り値
:   なし (void)

説明
:   マウスイベントキャプチャを解除します。
    　マウスイベントキャプチャとは、最初にマウスボタンを押下した位置にあったレイヤのみに、マウスボタンを放すまでずっとマウスイベントが占有的に送られる機能です。
    　このメソッドは、この機能を解除し、通常のマウスイベントの処理状態に戻します。
    　このメソッドを実行すると、同じウィンドウに属しているレイヤのマウスキャプチャは、たとえメソッドを実行するレイヤとキャプチャの対象となっているレイヤが異なっていても解除されます。
    　このメソッドはキャプチャ状態でない場合は何もしません。