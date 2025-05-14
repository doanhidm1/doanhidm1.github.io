# WaveSoundBuffer

WaveSoundBuffer クラスは、PCMの再生を管理するクラスです。
WaveSoundBuffer クラスでは、ループチューナ で作成した .sli ファイルを読み込み、処理することができます。
詳しくはループチューナの説明をご覧ください。

# メンバ

コンストラクタ
:   [WaveSoundBuffer](func_WaveSoundBuffer_WaveSoundBuffer) (WaveSoundBuffer オブジェクトの構築 )

メソッド
:   [fade](func_WaveSoundBuffer_fade) (フェードを開始する )
    [freeDirectSound](func_WaveSoundBuffer_freeDirectSound) (DirectSound の解放 )
    [getVisBuffer](func_WaveSoundBuffer_getVisBuffer) (視覚化用データの取得 )
    [open](func_WaveSoundBuffer_open) (メディアを開く )
    [play](func_WaveSoundBuffer_play) (メディアを再生する )
    [stop](func_WaveSoundBuffer_stop) (メディアを停止する )
    [stopFade](func_WaveSoundBuffer_stopFade) (フェードを停止する )

プロパティ
:   [bits](prop_WaveSoundBuffer_bits) (量子化ビット数 )
    [channels](prop_WaveSoundBuffer_channels) (チャンネル数 )
    [filters](prop_WaveSoundBuffer_filters) (フィルタ配列 )
    [flags](prop_WaveSoundBuffer_flags) (フラグ )
    [frequency](prop_WaveSoundBuffer_frequency) (サンプリング周波数 )
    [globalFocusMode](prop_WaveSoundBuffer_globalFocusMode) (フォーカスモード )
    [globalVolume](prop_WaveSoundBuffer_globalVolume) (大域音量 )
    [labels](prop_WaveSoundBuffer_labels) (ラベル )
    [looping](prop_WaveSoundBuffer_looping) (ループ再生を行うかどうか )
    [pan](prop_WaveSoundBuffer_pan) (パン )
    [paused](prop_WaveSoundBuffer_paused) (一時停止状態かどうか )
    [position](prop_WaveSoundBuffer_position) (再生位置 )
    [samplePosition](prop_WaveSoundBuffer_samplePosition) (再生位置 )
    [status](prop_WaveSoundBuffer_status) (ステータス )
    [totalTime](prop_WaveSoundBuffer_totalTime) (メディアの再生時間 )
    [useVisBuffer](prop_WaveSoundBuffer_useVisBuffer) (視覚化用バッファを使用するかどうか )
    [volume](prop_WaveSoundBuffer_volume) (音量 )
    [volume2](prop_WaveSoundBuffer_volume2) (第２音量 )

イベント
:   [onFadeCompleted](event_WaveSoundBuffer_onFadeCompleted) (フェードが終了した )
    [onLabel](event_WaveSoundBuffer_onLabel) (ラベルを通過した )
    [onStatusChanged](event_WaveSoundBuffer_onStatusChanged) (ステータスが変更された )