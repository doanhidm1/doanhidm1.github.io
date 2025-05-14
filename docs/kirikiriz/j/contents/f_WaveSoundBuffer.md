# WaveSoundBuffer

WaveSoundBuffer クラスは、PCMの再生を管理するクラスです。
　WaveSoundBuffer クラスでは、[ループチューナ](LoopTuner) で作成した .sli ファイルを読み込み、処理することができます。詳しくはループチューナの説明をご覧ください。

# メンバ

コンストラクタ
:   [WaveSoundBuffer](f_WaveSoundBuffer_WaveSoundBuffer)

メソッド
:   [fade](f_WaveSoundBuffer_fade) ( フェードを開始する )
    [freeDirectSound](f_WaveSoundBuffer_freeDirectSound) ( DirectSound の解放 )
    [getVisBuffer](f_WaveSoundBuffer_getVisBuffer) ( 視覚化用データの取得 )
    [open](f_WaveSoundBuffer_open) ( メディアを開く )
    [play](f_WaveSoundBuffer_play) ( メディアを再生する )
    [stop](f_WaveSoundBuffer_stop) ( メディアを停止する )
    [stopFade](f_WaveSoundBuffer_stopFade) ( フェードを停止する )

プロパティ
:   [bits](f_WaveSoundBuffer_bits) ( 量子化ビット数 )
    [channels](f_WaveSoundBuffer_channels) ( チャンネル数 )
    [filters](f_WaveSoundBuffer_filters) ( フィルタ配列 )
    [flags](f_WaveSoundBuffer_flags) ( フラグ )
    [frequency](f_WaveSoundBuffer_frequency) ( サンプリング周波数 )
    [globalFocusMode](f_WaveSoundBuffer_globalFocusMode) ( フォーカスモード )
    [globalVolume](f_WaveSoundBuffer_globalVolume) ( 大域音量 )
    [labels](f_WaveSoundBuffer_labels) ( ラベル )
    [looping](f_WaveSoundBuffer_looping) ( ループ再生を行うかどうか )
    [pan](f_WaveSoundBuffer_pan) ( パン )
    [paused](f_WaveSoundBuffer_paused) ( 一時停止状態かどうか )
    [position](f_WaveSoundBuffer_position) ( 再生位置 )
    [samplePosition](f_WaveSoundBuffer_samplePosition) ( 再生位置 )
    [status](f_WaveSoundBuffer_status) ( ステータス )
    [totalTime](f_WaveSoundBuffer_totalTime) ( メディアの再生時間 )
    [useVisBuffer](f_WaveSoundBuffer_useVisBuffer) ( 視覚化用バッファを使用するかどうか )
    [volume](f_WaveSoundBuffer_volume) ( 音量 )
    [volume2](f_WaveSoundBuffer_volume2) ( 第２音量 )

イベント
:   [onFadeCompleted](f_WaveSoundBuffer_onFadeCompleted) ( フェードが終了した )
    [onLabel](f_WaveSoundBuffer_onLabel) ( ラベルを通過した )
    [onStatusChanged](f_WaveSoundBuffer_onStatusChanged) ( ステータスが変更された )