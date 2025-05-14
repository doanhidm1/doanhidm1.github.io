# CDDASoundBuffer.CDDASoundBuffer

機能/意味
:   CDDASoundBuffer オブジェクトの構築

タイプ
:   [CDDASoundBufferクラス](f_CDDASoundBuffer)のコンストラクタ

構文
:   CDDASoundBuffer(owner)

引数
:   |  |  |
    | --- | --- |
    | owner | イベントの発生先を指定します。 |

戻り値
:   なし (void)

説明
:   CDDASoundBuffer クラスのオブジェクトを構築します。
    　イベントが発生すると owner で指定したオブジェクトの action メソッドを呼び出します。owner に null を指定すると action メソッドは呼ばれません。通常は [Window](f_Window) クラスのオブジェクトを owner に指定します。