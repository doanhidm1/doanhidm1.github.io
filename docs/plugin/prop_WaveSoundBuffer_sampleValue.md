# WaveSoundBuffer.sampleValue

機能/意味
:   サンプル値の取得（新方式）

タイプ
:   [WaveSoundBufferクラス](class_WaveSoundBuffer)のプロパティ

説明
:   getVisBuffer(buf, sampleCount, 1, sampleAhead)でサンプルを取得し，
    (value/32768)^2の最大値を取得します。(0～1の実数で返ります)
    ※このプロパティを読み出すと暗黙でuseVisBuffer=trueに設定されます