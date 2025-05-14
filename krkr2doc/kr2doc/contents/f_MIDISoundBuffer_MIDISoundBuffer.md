# MIDISoundBuffer.MIDISoundBuffer

機能/意味
:   MIDISoundBuffer オブジェクトの構築

タイプ
:   [MIDISoundBufferクラス](f_MIDISoundBuffer)のコンストラクタ

構文
:   MIDISoundBuffer(owner)

引数
:   |  |  |
    | --- | --- |
    | owner | イベントの発生先を指定します。 |

戻り値
:   なし (void)

説明
:   MIDISoundBuffer クラスのオブジェクトを構築します。
    　イベントが発生すると owner で指定したオブジェクトの action メソッドを呼び出します。owner に null を指定すると action メソッドは呼ばれません。通常は [Window](f_Window) クラスのオブジェクトを owner に指定します。