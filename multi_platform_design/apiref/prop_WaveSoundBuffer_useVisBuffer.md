# WaveSoundBuffer.useVisBuffer

機能/意味
:   視覚化用バッファを使用するかどうか

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のプロパティ

説明
:   視覚化用バッファを使用するかどうか表します。
    値を設定することもできます。
    真を指定すると視覚化用バッファが利用可能になり、WaveSoundBuffer.getVisBuffer メソッドが利用可能になります。
    デフォルトでは偽になっています。
    真を指定すると偽を指定したときよりも多くのメモリと CPU 時間を消費するようになるので注意してください。