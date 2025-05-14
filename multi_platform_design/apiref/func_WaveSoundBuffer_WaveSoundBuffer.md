# WaveSoundBuffer.WaveSoundBuffer

機能/意味
:   WaveSoundBuffer オブジェクトの構築

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のメソッド

構文
:   WaveSoundBuffer(owner)

引数
:   |  |  |
    | --- | --- |
    | owner | イベントの発生先を指定します。 |

戻り値
:   なし (void)

説明
:   WaveSoundBuffer クラスのオブジェクトを構築します。
    イベントが発生すると owner で指定したオブジェクトの action メソッドを呼び出します。
    owner に null を指定すると action メソッドは呼ばれません。
    通常は Window クラスのオブジェクトを owner に指定します。