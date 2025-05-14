# VideoOverlay.selectAudioStream

機能/意味
:   [Windows\*]音声ストリームの選択

タイプ
:   [VideoOverlayクラス](class_VideoOverlay)のメソッド

構文
:   selectAudioStream(streamNumber)

引数
:   |  |  |
    | --- | --- |
    | streamNumber | 音声ストリーム番号を指定します。 |

戻り値
:   なし (void)

説明
:   指定した音声ストリーム番号を有効にします。
    音声ストリームを複数含まないビデオでは使用できません。
    Androidでは常に0を返し、設定しても意味はありません。

参照
:   [VideoOverlay.numberOfAudioStream](prop_VideoOverlay_numberOfAudioStream)
    [VideoOverlay.enabledAudioStream](prop_VideoOverlay_enabledAudioStream)