# VideoOverlay.setPeriodEvent

機能/意味
:   指定フレームでのイベント発生の指定

タイプ
:   [VideoOverlayクラス](f_VideoOverlay)のメソッド

構文
:   setPeriodEvent(eventFrame)

引数
:   |  |  |
    | --- | --- |
    | eventFrame | onPeriodイベントを発生させるフレームを指定します。 |

戻り値
:   なし (void)

説明
:   指定したフレームでonPeriodイベントを発生させます。
    onPeriodイベントは、一度発生すると解除されます。再び発生させたい場合は再度このメソッドで設定してください。

参照
:   [VideoOverlay.cancelPeriodEvent](f_VideoOverlay_cancelPeriodEvent)
    [VideoOverlay.onPeriod](f_VideoOverlay_onPeriod)