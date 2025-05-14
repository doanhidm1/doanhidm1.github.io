# CDDASoundBuffer.fade

機能/意味
:   フェードを開始する

タイプ
:   [CDDASoundBufferクラス](f_CDDASoundBuffer)のメソッド

構文
:   fade(to, time, delay=0)

引数
:   |  |  |
    | --- | --- |
    | to | 到達させる音量を指定します。  　音量の指定については [CDDASoundBuffer.volume](f_CDDASoundBuffer_volume) プロパティを参照して ください。 |
    | time | フェードにかける時間を ms 単位で指定します。 |
    | delay | フェード開始までの待ち時間を ms 単位で指定します。 |

戻り値
:   なし (void)

説明
:   フェード ( 連続的な音量の変化 ) を開始します。