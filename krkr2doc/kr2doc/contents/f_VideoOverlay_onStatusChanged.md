# VideoOverlay.onStatusChanged

機能/意味
:   ステータスが変更された

タイプ
:   [VideoOverlayクラス](f_VideoOverlay)のイベント

構文
:   onStatusChanged(status)

引数
:   |  |  |
    | --- | --- |
    | status | ステータス文字列を表します。  　以下のいずれかです。  "unload" :  メディアが開かれてない  "play" :  メディアは再生中である  "stop" :  メディアは停止中である  "pause" :  メディアは一時停止中である |

説明
:   このオブジェクトのステータスが変更されたときに発生します。
    SWF再生時には再生の停止や一時停止に関する機能は利用できません。