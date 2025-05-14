# VideoOverlay.onFrameUpdate

機能/意味
:   [Windows\*]ビデオフレームが更新された

タイプ
:   [VideoOverlayクラス](class_VideoOverlay)のイベント

構文
:   onFrameUpdate(frame)

引数
:   |  |  |
    | --- | --- |
    | frame | ビデオのフレーム番号 |

戻り値
:   なし (void)

説明
:   ビデオフレームが更新された後に呼び出されるメソッドです。
    引数であるframeは現在表示されているビデオフレームと完全に一致しているとは限りません。
    レイヤ描画モード、ミキサーモード時のみ利用可能です。
    Androidでは発生しません。