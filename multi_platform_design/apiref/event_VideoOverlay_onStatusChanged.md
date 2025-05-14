# VideoOverlay.onStatusChanged

機能/意味
:   ステータスが変更された

タイプ
:   [VideoOverlayクラス](class_VideoOverlay)のイベント

構文
:   onStatusChanged(status)

引数
:   |  |  |
    | --- | --- |
    | status | ステータス文字列を表します。以下のいずれかです。   * "unload" : メディアが開かれてない * "ready" : メディアの準備が完了している * "play" : メディアは再生中である * "stop" : メディアは停止中である * "pause" : メディアは一時停止中である * "idle" : [Android+]メディアはアイドル中。 * "buffering" : [Android+]メディアはバッファリング中。 * "load error" : [Android+]メディアの読み込みエラー。 * "player error" : [Android+]メディアプレイヤーエラー。 |

戻り値
:   なし (void)

説明
:   このオブジェクトのステータスが変更されたときに発生します。
    ready は、vomMFEVR モード/Androidの時のみ発生します。