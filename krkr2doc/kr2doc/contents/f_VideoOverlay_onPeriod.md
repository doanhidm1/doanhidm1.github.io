# VideoOverlay.onPeriod

機能/意味
:   Periodイベントが発生した

タイプ
:   [VideoOverlayクラス](f_VideoOverlay)のイベント

構文
:   onPeriod(type)

引数
:   |  |  |
    | --- | --- |
    | type | Periodイベントのタイプを表します。  　以下のいずれかです。  perLoop :  (通常の)ループの終端に達した  perSegLoop :  セグメントループの終端に達した  perPeriod :  setPeriodEvent メソッドで指定されたフレームに達した  perPrepare :  prepare メソッドによる再生準備が完了した |

説明
:   ループの終端や、 setPeriodEventによって指定されたフレームに達した場合、または prepare メソッドにより再生準備が完了した場合に呼び出されるメソッドです。
    ループの終端や、 setPeriodEvent によって指定されたフレームに達した場合にこのイベントが呼ばれる時点では、再生状況によっては、すでに再生位置が指定された位置を超えている場合があります。現在の実際の再生位置を取得するには frame プロパティを参照してください。
    この機能は、SWF再生時には利用できません。

参照
:   [VideoOverlay.setPeriodEvent](f_VideoOverlay_setPeriodEvent)
    [VideoOverlay.prepare](f_VideoOverlay_prepare)
    [VideoOverlay.frame](f_VideoOverlay_frame)