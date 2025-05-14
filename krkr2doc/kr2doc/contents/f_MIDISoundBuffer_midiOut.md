# MIDISoundBuffer.midiOut

機能/意味
:   任意の MIDI データの出力

タイプ
:   [MIDISoundBufferクラス](f_MIDISoundBuffer)のメソッド

構文
:   midiOut(data)

引数
:   |  |  |
    | --- | --- |
    | data | 出力する MIDI データをオクテット形式で指定します。 |

戻り値
:   なし (void)

説明
:   任意の MIDI データを出力します。
    　データ中に ff 00 が入っていると、その時点で 50ms のウェイトが入ります。