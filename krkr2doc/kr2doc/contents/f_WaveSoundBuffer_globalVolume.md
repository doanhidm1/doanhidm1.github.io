# WaveSoundBuffer.globalVolume

機能/意味
:   大域音量

タイプ
:   [WaveSoundBufferクラス](f_WaveSoundBuffer)のプロパティ (読み書き可能)

説明
:   大域音量 (マスターボリューム)を表します。値を設定することもできます。
    　この音量は、すべての WaveSoundBuffer に影響します。
    　0 ～ 100000 の数値で指定し、 0 が完全ミュート、100000 が 100% の音量となります。デフォルトの値は 100000 です。
    　このプロパティは WaveSoundBuffer クラス上にしか存在しません (WaveSoundBufferから作られたオブジェクト上にこのプロパティはありません)。使用する際は WaveSoundBuffer.globalVolume としてください。