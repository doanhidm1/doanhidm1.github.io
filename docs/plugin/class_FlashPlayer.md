# FlashPlayer

FlashPlayerクラス
FlashPlayerをレイヤ上で再生制御するオブジェクトです。

## ExternalInterface機能

### ◇TJSメソッドのActionScriptからの呼び出し

オブジェクトの任意のメソッドが、再生中の swfの ActionScriptから ExternalInterface で呼び出し可能です

```

-----------------------------------------------------------
import flash.external.ExternalInterface;
trace(ExternalInterface.call("tjsFunction", 10, "test"));
-----------------------------------------------------------

```

吉里吉里側で例外が発生して呼び出しに失敗しても ActionScript 側では
例外になりませんので注意してください。
例外情報は getLastTJSError() で取得可能です。

### ◇ActionScriptメソッドのTJSからの呼び出し

callFunction() で､ExternalInterface で公開されている
ActionScript メソッドを呼び出しできます。

```

ActionScriptでの関数の準備
-----------------------------------------------------------
import flash.external.ExternalInterface;
// 呼び出しメソッド
function flashFunction(a:Number, b:String):String {
return StringUtil.substitute("{0}:{1}", a, b);
}
// 登録
ExternalInterface.addCallback("flashFunction", flashFunction);
-----------------------------------------------------------

TJSからの呼び出し
-----------------------------------------------------------
var flash = new FlashPlayer(100,100);
flash.initMovie("sample.swf");
Debug.message(flash.callFunction("flashFunction", 1, "test"));
-----------------------------------------------------------

```

呼び出しに失敗すると例外になります。

# メンバ

コンストラクタ
:   [FlashPlayer](func_FlashPlayer_FlashPlayer)

メソッド
:   [back](func_FlashPlayer_back) ( )
    [callFunction](func_FlashPlayer_callFunction) (Flash の ExternalInterface 登録されたメソッドを呼び出します。 )
    [clearMovie](func_FlashPlayer_clearMovie) (動画情報を完全にクリアする )
    [disableLocalSecurity](func_FlashPlayer_disableLocalSecurity) ( )
    [doKeyDown](func_FlashPlayer_doKeyDown) (キーダウンの通知 )
    [doKeyUp](func_FlashPlayer_doKeyUp) (キーアップの通知 )
    [doMouseDown](func_FlashPlayer_doMouseDown) (マウスキーおしさげ通知 )
    [doMouseEnter](func_FlashPlayer_doMouseEnter) (マウスが領域に入った通知 )
    [doMouseLeave](func_FlashPlayer_doMouseLeave) (マウスが領域から出た通知 )
    [doMouseMove](func_FlashPlayer_doMouseMove) (マウス移動通知 )
    [doMouseUp](func_FlashPlayer_doMouseUp) (マウスキーおしあげ通知 )
    [doMouseWheel](func_FlashPlayer_doMouseWheel) (マウスホイール通知 )
    [draw](func_FlashPlayer_draw) (レイヤに対して現在の描画内容を出力する。レイヤのサイズが小さい場合はトリミングされます )
    [enforceLocalSecurity](func_FlashPlayer_enforceLocalSecurity) ( )
    [forward](func_FlashPlayer_forward) ( )
    [getFrameLoaded](func_FlashPlayer_getFrameLoaded) ( )
    [getLastTJSError](func_FlashPlayer_getLastTJSError) (TJS呼び出しエラーの取得。 )
    [getVariable](func_FlashPlayer_getVariable) ( )
    [gotoFrame](func_FlashPlayer_gotoFrame) ( )
    [hitTest](func_FlashPlayer_hitTest) (指定された座標の位置に対する入力をうけつけるかどうかを返します )
    [initMovie](func_FlashPlayer_initMovie) (指定した吉里吉里のファイルを動画として初期化する )
    [isPlaying](func_FlashPlayer_isPlaying) ( )
    [loadMovie](func_FlashPlayer_loadMovie) (ムービーをロードする )
    [onFrameUpdate](func_FlashPlayer_onFrameUpdate) (描画内容が更新された場合に呼び出されるイベント )
    [onFSCommand](func_FlashPlayer_onFSCommand) (FSCommandイベントの通知 )
    [onProgress](func_FlashPlayer_onProgress) (Progressイベントの通知 )
    [onReadyStateChange](func_FlashPlayer_onReadyStateChange) (ReadyStateChangeイベントの通知 )
    [pan](func_FlashPlayer_pan) ( )
    [play](func_FlashPlayer_play) ( )
    [rewind](func_FlashPlayer_rewind) ( )
    [setSize](func_FlashPlayer_setSize) (プレイヤーサイズの変更 )
    [setVariable](func_FlashPlayer_setVariable) ( )
    [setZoomRect](func_FlashPlayer_setZoomRect) ( )
    [stop](func_FlashPlayer_stop) ( )
    [stopPlay](func_FlashPlayer_stopPlay) ( )
    [tCallFrame](func_FlashPlayer_tCallFrame) ( )
    [tCallLabel](func_FlashPlayer_tCallLabel) ( )
    [tCurrentFrame](func_FlashPlayer_tCurrentFrame) ( )
    [tCurrentLabel](func_FlashPlayer_tCurrentLabel) ( )
    [tGetProperty](func_FlashPlayer_tGetProperty) ( )
    [tGetPropertyNum](func_FlashPlayer_tGetPropertyNum) ( )
    [tGotoFrame](func_FlashPlayer_tGotoFrame) ( )
    [tGotoLabel](func_FlashPlayer_tGotoLabel) ( )
    [tPlay](func_FlashPlayer_tPlay) ( )
    [tSetProperty](func_FlashPlayer_tSetProperty) ( )
    [tSetPropertyNum](func_FlashPlayer_tSetPropertyNum) ( )
    [tStopPlay](func_FlashPlayer_tStopPlay) ( )
    [zoom](func_FlashPlayer_zoom) ( )

プロパティ
:   [alighMode](prop_FlashPlayer_alighMode) ( )
    [allowScriptAccess](prop_FlashPlayer_allowScriptAccess) ( )
    [backgroundColor](prop_FlashPlayer_backgroundColor) ( )
    [base](prop_FlashPlayer_base) ( )
    [bgColor](prop_FlashPlayer_bgColor) ( )
    [currentFrame](prop_FlashPlayer_currentFrame) (RO )
    [deviceFont](prop_FlashPlayer_deviceFont) ( )
    [embedMovie](prop_FlashPlayer_embedMovie) ( )
    [flashVars](prop_FlashPlayer_flashVars) ( )
    [flashVersion](prop_FlashPlayer_flashVersion) (RO )
    [frameNum](prop_FlashPlayer_frameNum) ( )
    [loop](prop_FlashPlayer_loop) ( )
    [menu](prop_FlashPlayer_menu) ( )
    [movie](prop_FlashPlayer_movie) ( )
    [movieData](prop_FlashPlayer_movieData) ( )
    [percentLoaded](prop_FlashPlayer_percentLoaded) (RO )
    [playing](prop_FlashPlayer_playing) ( )
    [profile](prop_FlashPlayer_profile) ( )
    [profileAddress](prop_FlashPlayer_profileAddress) ( )
    [profilePort](prop_FlashPlayer_profilePort) ( )
    [quality](prop_FlashPlayer_quality) ( )
    [quality2](prop_FlashPlayer_quality2) ( )
    [readyState](prop_FlashPlayer_readyState) (RO )
    [sAlign](prop_FlashPlayer_sAlign) ( )
    [scale](prop_FlashPlayer_scale) ( )
    [scaleMode](prop_FlashPlayer_scaleMode) ( )
    [seamlessTabbing](prop_FlashPlayer_seamlessTabbing) ( )
    [swRemote](prop_FlashPlayer_swRemote) ( )
    [totalFrames](prop_FlashPlayer_totalFrames) (RO )