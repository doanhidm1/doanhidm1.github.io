# VideoOverlay.setSegmentLoop

機能/意味
:   [Windows\*]フレーム間ループの設定

タイプ
:   [VideoOverlayクラス](class_VideoOverlay)のメソッド

構文
:   setSegmentLoop(comeFrame, goFrame)

引数
:   |  |  |
    | --- | --- |
    | comeFrame | ループ移動先フレーム(ループの始端フレーム)。  再生がgoFrameに達したとき、再生ヘッドはこのフレームに移動します。 |
    | goFrame | ループ終点フレーム(ループの終端フレーム)。  このフレームの1つ前のフレームの表示が終了した時、再生ヘッドはcomeFrameへ移動します。 |

戻り値
:   なし (void)

説明
:   指定されたフレーム間でループ処理を行います。
    ループ終端(goFrame)では、onPeriodイベントが発生します。
    comeFrameのフレームにはムービーファイルにキーフレームを設定しておく必要があります。
    設定されていない場合は、ループ終点から始点へ移動時に指定されたフレームに最も近いキーフレームへ再生位置が移動することになります。

参照
:   [VideoOverlay.cancelSegmentLoop](func_VideoOverlay_cancelSegmentLoop)
    [VideoOverlay.onPeriod](event_VideoOverlay_onPeriod)
    [VideoOverlay.segmentLoopStartFrame](prop_VideoOverlay_segmentLoopStartFrame)
    [VideoOverlay.segmentLoopEndFrame](prop_VideoOverlay_segmentLoopEndFrame)