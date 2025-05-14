# WaveSoundBuffer.PhaseVocoder

WaveSoundBuffer.PhaseVocoder クラスは、このインスタンスを [WaveSoundBuffer.filters](f_WaveSoundBuffer_filters) に登録して使用するためのフィルタで、Phase Vocoder (位相ボコーダ) の機能を提供します。
　Phase Vocoder では、再生速度を保ったままでの音程の変更 (ピッチ・シフタ) や、音程を保ったままでの再生速度の変更 (タイム・シフタ) を行うことができます。

# メンバ

コンストラクタ
:   [PhaseVocoder](f_WaveSoundBuffer.PhaseVocoder_PhaseVocoder)

メソッド
:   なし

プロパティ
:   [interface](f_WaveSoundBuffer.PhaseVocoder_interface) ( インターフェースオブジェクトを取得 )
    [overlap](f_WaveSoundBuffer.PhaseVocoder_overlap) ( オーバーラップカウント )
    [pitch](f_WaveSoundBuffer.PhaseVocoder_pitch) ( 周波数軸方向のスケール )
    [time](f_WaveSoundBuffer.PhaseVocoder_time) ( 時間軸方向のスケール )
    [window](f_WaveSoundBuffer.PhaseVocoder_window) ( ウィンドウサイズ )

イベント
:   なし