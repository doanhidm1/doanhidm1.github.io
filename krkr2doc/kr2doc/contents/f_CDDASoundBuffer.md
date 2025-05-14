# CDDASoundBuffer

CDDASoundBuffer クラスは、CD-DAの再生を管理するクラスです。

# メンバ

コンストラクタ
:   [CDDASoundBuffer](f_CDDASoundBuffer_CDDASoundBuffer)

メソッド
:   [fade](f_CDDASoundBuffer_fade) ( フェードを開始する )
    [open](f_CDDASoundBuffer_open) ( メディアを開く )
    [play](f_CDDASoundBuffer_play) ( メディアを再生する )
    [stop](f_CDDASoundBuffer_stop) ( メディアを停止する )
    [stopFade](f_CDDASoundBuffer_stopFade) ( フェードを停止する )

プロパティ
:   [looping](f_CDDASoundBuffer_looping) ( ループ再生を行うかどうか )
    [paused](f_CDDASoundBuffer_paused) ( 一時停止状態かどうか )
    [position](f_CDDASoundBuffer_position) ( 再生位置 )
    [status](f_CDDASoundBuffer_status) ( ステータス )
    [totalTime](f_CDDASoundBuffer_totalTime) ( メディアの再生時間 )
    [volume](f_CDDASoundBuffer_volume) ( 音量 )
    [volume2](f_CDDASoundBuffer_volume2) ( 第２音量 )

イベント
:   [onFadeCompleted](f_CDDASoundBuffer_onFadeCompleted) ( フェードが終了した )
    [onStatusChanged](f_CDDASoundBuffer_onStatusChanged) ( ステータスが変更された )