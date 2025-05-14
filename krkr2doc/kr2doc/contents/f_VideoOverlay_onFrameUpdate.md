# VideoOverlay.onFrameUpdate

機能/意味
:   ビデオフレームが更新された

タイプ
:   [VideoOverlayクラス](f_VideoOverlay)のイベント

構文
:   onFrameUpdate(frame)

引数
:   |  |  |
    | --- | --- |
    | frame | ビデオのフレーム番号 |

説明
:   ビデオフレームが更新された後に呼び出されるメソッドです。
    引数であるframeは現在表示されているビデオフレームと完全に一致しているとは限りません。
    レイヤ描画モード、ミキサーモード時のみ利用可能です。
    この機能は、SWF再生時には利用できません。