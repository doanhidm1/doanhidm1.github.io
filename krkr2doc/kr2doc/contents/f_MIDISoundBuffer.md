# MIDISoundBuffer

MIDISoundBuffer クラスは、MIDIの再生を管理するクラスです。

# メンバ

コンストラクタ
:   [MIDISoundBuffer](f_MIDISoundBuffer_MIDISoundBuffer)

メソッド
:   [fade](f_MIDISoundBuffer_fade) ( フェードを開始する )
    [midiOut](f_MIDISoundBuffer_midiOut) ( 任意の MIDI データの出力 )
    [open](f_MIDISoundBuffer_open) ( メディアを開く )
    [play](f_MIDISoundBuffer_play) ( メディアを再生する )
    [stop](f_MIDISoundBuffer_stop) ( メディアを停止する )
    [stopFade](f_MIDISoundBuffer_stopFade) ( フェードを停止する )

プロパティ
:   [looping](f_MIDISoundBuffer_looping) ( ループ再生を行うかどうか )
    [paused](f_MIDISoundBuffer_paused) ( 一時停止状態かどうか )
    [position](f_MIDISoundBuffer_position) ( 再生位置 )
    [status](f_MIDISoundBuffer_status) ( ステータス )
    [totalTime](f_MIDISoundBuffer_totalTime) ( メディアの再生時間 )
    [volume](f_MIDISoundBuffer_volume) ( 音量 )
    [volume2](f_MIDISoundBuffer_volume2) ( 第２音量 )

イベント
:   [onFadeCompleted](f_MIDISoundBuffer_onFadeCompleted) ( フェードが終了した )
    [onStatusChanged](f_MIDISoundBuffer_onStatusChanged) ( ステータスが変更された )