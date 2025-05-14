# BitmapLayerTreeOwner

BitmapLayerTreeOwner クラスは、レイヤーツリーを保持し、描画結果を Bitmap クラスで取得できるクラスです。
Layer クラスのコンストラクタの第一引数に window の代わりに渡すことで、それら Layer の描画結果を Bitmap クラスとして画像で取得できます。
描画結果の Bitmap を Texture に転送することで Layer 描画系を Canvas で使用できるようになります。

# メンバ

コンストラクタ
:   [BitmapLayerTreeOwner](func_BitmapLayerTreeOwner_BitmapLayerTreeOwner) (BitmapLayerTreeOwner オブジェクトの構築 )

メソッド
:   [clearDirtyRect](func_BitmapLayerTreeOwner_clearDirtyRect) (更新矩形情報をクリアする )
    [fireClick](func_BitmapLayerTreeOwner_fireClick) (クリックをレイヤに通知します(使用非推奨) )
    [fireDisplayRotate](func_BitmapLayerTreeOwner_fireDisplayRotate) (画面が回転されたことをレイヤに通知します )
    [fireDoubleClick](func_BitmapLayerTreeOwner_fireDoubleClick) (ダブルクリックをレイヤに通知します(使用非推奨) )
    [fireKeyDown](func_BitmapLayerTreeOwner_fireKeyDown) (キーが押されたことをレイヤに通知します )
    [fireKeyPress](func_BitmapLayerTreeOwner_fireKeyPress) (文字が入力されたことをレイヤに通知します )
    [fireKeyUp](func_BitmapLayerTreeOwner_fireKeyUp) (キーが離されたことをレイヤに通知します )
    [fireMouseDown](func_BitmapLayerTreeOwner_fireMouseDown) (マウス押下をレイヤに通知します )
    [fireMouseMove](func_BitmapLayerTreeOwner_fireMouseMove) (マウス移動をレイヤに通知します )
    [fireMouseOutOfWindow](func_BitmapLayerTreeOwner_fireMouseOutOfWindow) (マウスがWindow外に出たことをレイヤに通知します )
    [fireMouseUp](func_BitmapLayerTreeOwner_fireMouseUp) (マウス押下をレイヤに通知します )
    [fireMouseWheel](func_BitmapLayerTreeOwner_fireMouseWheel) (マウスのホイール回転をレイヤに通知します )
    [fireMultiTouch](func_BitmapLayerTreeOwner_fireMultiTouch) (マルチタッチ状態変化をレイヤに通知します )
    [fireRecheckInputState](func_BitmapLayerTreeOwner_fireRecheckInputState) (必要なら1秒間隔で呼び出します。 )
    [fireReleaseCapture](func_BitmapLayerTreeOwner_fireReleaseCapture) (マウスキャプチャ解除をレイヤに通知します )
    [fireTouchDown](func_BitmapLayerTreeOwner_fireTouchDown) (タッチされたことをレイヤに通知します )
    [fireTouchMove](func_BitmapLayerTreeOwner_fireTouchMove) (タッチが移動されたことをレイヤに通知します )
    [fireTouchRotate](func_BitmapLayerTreeOwner_fireTouchRotate) (回転操作されたことをレイヤに通知します )
    [fireTouchScaling](func_BitmapLayerTreeOwner_fireTouchScaling) (拡大操作されたことをレイヤに通知します )
    [fireTouchUp](func_BitmapLayerTreeOwner_fireTouchUp) (タッチが離されたことをレイヤに通知します )

プロパティ
:   [height](prop_BitmapLayerTreeOwner_height) (高さ(readonly) )
    [layerTreeOwnerInterface](prop_BitmapLayerTreeOwner_layerTreeOwnerInterface) (LTOインターフェイス、内部使用(readonly) )
    [primaryLayer](prop_BitmapLayerTreeOwner_primaryLayer) (プライマリレイヤ(readonly) )
    [width](prop_BitmapLayerTreeOwner_width) (幅(readonly) )

イベント
:   [onChangeLayerImage](event_BitmapLayerTreeOwner_onChangeLayerImage) (Layer 画像が更新された )
    [onDisableAttentionPoint](event_BitmapLayerTreeOwner_onDisableAttentionPoint) (Layer から注視位置の指定解除された )
    [onGetCursorPos](event_BitmapLayerTreeOwner_onGetCursorPos) (Layer からカーソル位置取得が呼び出された )
    [onReleaseMouseCapture](event_BitmapLayerTreeOwner_onReleaseMouseCapture) (Layer からマウスキャプチャ解除が呼び出された )
    [onResetImeMode](event_BitmapLayerTreeOwner_onResetImeMode) (IMEモードがリセットされた )
    [onResizeLayer](event_BitmapLayerTreeOwner_onResizeLayer) (プライマリレイヤーのサイズが変更された )
    [onSetAttentionPoint](event_BitmapLayerTreeOwner_onSetAttentionPoint) (Layer から注視位置の指定が呼び出された )
    [onSetCursorPos](event_BitmapLayerTreeOwner_onSetCursorPos) (Layer からカーソル位置設定が呼び出された )
    [onSetHintText](event_BitmapLayerTreeOwner_onSetHintText) (Layer からヒントテキスト設定が呼び出された )
    [onSetImeMode](event_BitmapLayerTreeOwner_onSetImeMode) (IMEモードが設定された )
    [onSetMouseCursor](event_BitmapLayerTreeOwner_onSetMouseCursor) (Layer からカーソル設定が呼び出された )