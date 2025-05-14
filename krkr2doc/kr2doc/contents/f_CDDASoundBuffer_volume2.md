# CDDASoundBuffer.volume2

機能/意味
:   第２音量

タイプ
:   [CDDASoundBufferクラス](f_CDDASoundBuffer)のプロパティ (読み書き可能)

説明
:   再生する音量を表します。値を設定することができます。
    　[CDDASoundBuffer.volume](f_CDDASoundBuffer_volume) プロパティと違うのは、このプロパティは
    [CDDASoundBuffer.fade](f_CDDASoundBuffer_fade) メソッドでも変化しないということです。
    　最終的な音量は、volume プロパティとこのプロパティの積で決定されます。volume プロパティが
    100000 ( 100% ) で volume2 プロパティも 100000 ( 100% ) ならば 100% × 100% = 100% で
    100% の音量で再生されます。volume プロパティが 50000 ( 50% ) で volume2 プロパティが 75000 ( 75% ) ならば
    50% × 75% = 37.5% で 37.5 % の音量で再生されます。