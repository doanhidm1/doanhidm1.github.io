# PhaseVocoder

WaveSoundBuffer.PhaseVocoder クラスは、このインスタンスを WaveSoundBuffer.filters に登録して使用するためのフィルタで、Phase Vocoder (位相ボコーダ) の機能を提供します。
Phase Vocoder では、再生速度を保ったままでの音程の変更 (ピッチ・シフタ) や、音程を保ったままでの再生速度の変更 (タイム・シフタ) を行うことができます。

# メンバ

コンストラクタ
:   [PhaseVocoder](func_PhaseVocoder_PhaseVocoder) (PhaseVocoder オブジェクトの構築 )

メソッド

プロパティ
:   [interface](prop_PhaseVocoder_interface) (インターフェースオブジェクトを取得 )
    [overlap](prop_PhaseVocoder_overlap) (オーバーラップカウント )
    [pitch](prop_PhaseVocoder_pitch) (周波数軸方向のスケール )
    [time](prop_PhaseVocoder_time) (時間軸方向のスケール )
    [window](prop_PhaseVocoder_window) (ウィンドウサイズ )

イベント