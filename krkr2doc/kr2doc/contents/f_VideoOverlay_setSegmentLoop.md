# VideoOverlay.setSegmentLoop

機能/意味
:   フレーム間ループの設定

タイプ
:   [VideoOverlayクラス](f_VideoOverlay)のメソッド

構文
:   setSegmentLoop(comeFrame, goFrame)

引数
:   |  |  |
    | --- | --- |
    | comeFrame | ループ移動先フレーム(ループの始端フレーム)。再生がgoFrameに達したとき、再生ヘッドはこのフレームに移動します。 |
    | goFrame | ループ終点フレーム(ループの終端フレーム)。このフレームの1つ前のフレームの表示が終了した時、再生ヘッドはcomeFrameへ移動します。 |

戻り値
:   なし (void)

説明
:   指定されたフレーム間でループ処理を行います。
    ループ終端(goFrame)では、onPeriodイベントが発生します。
    comeFrameのフレームにはムービーファイルにキーフレームを設定しておく必要があります。
    設定されていない場合は、
    ループ終点から始点へ移動時に指定されたフレームに最も近いキーフレームへ再生位置が移動することになります。
    この機能は、SWF再生時には利用できません。

参照
:   [VideoOverlay.cancelSegmentLoop](f_VideoOverlay_cancelSegmentLoop)
    [VideoOverlay.onPeriod](f_VideoOverlay_onPeriod)
    [VideoOverlay.segmentLoopStartFrame](f_VideoOverlay_segmentLoopStartFrame)
    [VideoOverlay.segmentLoopEndFrame](f_VideoOverlay_segmentLoopEndFrame)