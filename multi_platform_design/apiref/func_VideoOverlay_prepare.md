# VideoOverlay.prepare

機能/意味
:   [Windows\*]再生準備

タイプ
:   [VideoOverlayクラス](class_VideoOverlay)のメソッド

構文
:   prepare()

引数

戻り値
:   なし (void)

説明
:   メディアの1フレーム目を指定されているレイヤーに描画し、描画終了時にonPeriodイベントを発生させます。
    prepareメソッド コール後の再生は、onPeriodイベントを待機してから行ってください。

参照
:   [VideoOverlay.onPeriod](event_VideoOverlay_onPeriod)