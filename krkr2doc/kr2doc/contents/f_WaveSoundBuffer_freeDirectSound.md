# WaveSoundBuffer.freeDirectSound

機能/意味
:   DirectSound の解放

タイプ
:   [WaveSoundBufferクラス](f_WaveSoundBuffer)のメソッド

構文
:   freeDirectSound()

引数
:   なし

戻り値
:   なし (void)

説明
:   DirectSound を解放します。すべての WaveSoundBuffer クラスのオブジェクトは停止状態に
    なります。
    　DirectSound と WaveMapper ( MCI 等 ) による再生を同時に行えない環境などで DirectSound を
    解放するためにこのメソッドを使います。
    　このメソッドは WaveSoundBuffer クラス上にしか存在しません (WaveSoundBufferから作られたオブジェクト上にこのメソッドはありません)。使用する際は WaveSoundBuffer.freeDirectSound(); としてください。