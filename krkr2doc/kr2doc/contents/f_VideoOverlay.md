# VideoOverlay

VideoOverlay クラスは、MPEG I や WMV、 SWF (Macromedia Flash) などを表示するため表示領域を作成するクラスです。また、WMV/MPEG I 再生時は、吉里吉里のレイヤに表示を行うことができます。
　WMV/MPEG I を再生するときは、吉里吉里実行可能ファイルと同じ場所に、krmovie.dll が必要になります。
　SWF を再生する場合は、吉里吉里実行可能ファイルと同じ場所に krflash.dll が必要になります。
　SWF では、いくつかのメソッドやプロパティが使用できない可能性があります。

　レイヤでの再生を除き、WMV/MPEG I のオーバーレイによる再生や Flash の再生では、VideoOverlay クラスの表示領域は、すべてのレイヤよりも手前に表示され、透過することはできません。
　レイヤでの再生は、オーバーレイでの再生に比べ、再生時のプロセッサの負荷は高くなる傾向にあります。

# メンバ

コンストラクタ
:   [VideoOverlay](f_VideoOverlay_VideoOverlay)

メソッド
:   [cancelPeriodEvent](f_VideoOverlay_cancelPeriodEvent) ( 指定フレームでのイベント発生の解除 )
    [cancelSegmentLoop](f_VideoOverlay_cancelSegmentLoop) ( フレーム間ループの解除 )
    [close](f_VideoOverlay_close) ( メディアを閉じる )
    [open](f_VideoOverlay_open) ( メディアを開く )
    [pause](f_VideoOverlay_pause) ( 一時停止 )
    [play](f_VideoOverlay_play) ( 再生開始 )
    [prepare](f_VideoOverlay_prepare) ( 再生準備 )
    [resetMixingLayer](f_VideoOverlay_resetMixingLayer) ( ミキシング対象レイヤの設定解除 )
    [rewind](f_VideoOverlay_rewind) ( 巻き戻し )
    [selectAudioStream](f_VideoOverlay_selectAudioStream) ( 音声ストリームの選択 )
    [setBounds](f_VideoOverlay_setBounds) ( 再生矩形の位置とサイズを指定 )
    [setMixingLayer](f_VideoOverlay_setMixingLayer) ( ミキシング対象レイヤの設定 )
    [setPeriodEvent](f_VideoOverlay_setPeriodEvent) ( 指定フレームでのイベント発生の指定 )
    [setPos](f_VideoOverlay_setPos) ( 再生矩形の左上位置を指定 )
    [setSegmentLoop](f_VideoOverlay_setSegmentLoop) ( フレーム間ループの設定 )
    [setSize](f_VideoOverlay_setSize) ( 再生矩形のサイズを指定 )
    [stop](f_VideoOverlay_stop) ( 再生停止 )

プロパティ
:   [audioBalance](f_VideoOverlay_audioBalance) ( 音声バランス(パニング) )
    [audioVolume](f_VideoOverlay_audioVolume) ( 音声ボリューム )
    [brightness](f_VideoOverlay_brightness) ( ビデオの輝度 )
    [brightnessDefaultValue](f_VideoOverlay_brightnessDefaultValue) ( ビデオの輝度既定値 )
    [brightnessRangeMax](f_VideoOverlay_brightnessRangeMax) ( ビデオの輝度レンジ最大値 )
    [brightnessRangeMin](f_VideoOverlay_brightnessRangeMin) ( ビデオの輝度レンジ最小値 )
    [brightnessStepSize](f_VideoOverlay_brightnessStepSize) ( ビデオの輝度増減ステップ値 )
    [contrast](f_VideoOverlay_contrast) ( ビデオのコントラスト )
    [contrastDefaultValue](f_VideoOverlay_contrastDefaultValue) ( ビデオのコントラスト既定値 )
    [contrastRangeMax](f_VideoOverlay_contrastRangeMax) ( ビデオのコントラストレンジ最大値 )
    [contrastRangeMin](f_VideoOverlay_contrastRangeMin) ( ビデオのコントラストレンジ最小値 )
    [contrastStepSize](f_VideoOverlay_contrastStepSize) ( ビデオのコントラスト増減ステップ値 )
    [enabledAudioStream](f_VideoOverlay_enabledAudioStream) ( 再生対象音声ストリーム番号 )
    [fps](f_VideoOverlay_fps) ( フレームレート )
    [frame](f_VideoOverlay_frame) ( 現在のフレーム )
    [height](f_VideoOverlay_height) ( 再生矩形の縦幅 )
    [hue](f_VideoOverlay_hue) ( ビデオの色相 )
    [hueDefaultValue](f_VideoOverlay_hueDefaultValue) ( ビデオの色相既定値 )
    [hueRangeMax](f_VideoOverlay_hueRangeMax) ( ビデオの色相レンジ最大値 )
    [hueRangeMin](f_VideoOverlay_hueRangeMin) ( ビデオの色相レンジ最小値 )
    [hueStepSize](f_VideoOverlay_hueStepSize) ( ビデオの色相増減ステップ値 )
    [layer1](f_VideoOverlay_layer1) ( 描画レイヤ指定1 )
    [layer2](f_VideoOverlay_layer2) ( 描画レイヤ指定2 )
    [left](f_VideoOverlay_left) ( 再生矩形の左端位置 )
    [loop](f_VideoOverlay_loop) ( ループ再生をするかどうか )
    [mixingMovieAlpha](f_VideoOverlay_mixingMovieAlpha) ( ビデオの透明度 )
    [mixingMovieBGColor](f_VideoOverlay_mixingMovieBGColor) ( ビデオの背景色 )
    [mode](f_VideoOverlay_mode) ( オーバーレイorレイヤ描画の指定 )
    [numberOfAudioStream](f_VideoOverlay_numberOfAudioStream) ( 音声ストリーム数 )
    [numberOfFrame](f_VideoOverlay_numberOfFrame) ( 全フレーム数 )
    [periodEventFrame](f_VideoOverlay_periodEventFrame) ( ピリオドイベントフレーム )
    [playRate](f_VideoOverlay_playRate) ( 再生速度 )
    [position](f_VideoOverlay_position) ( 再生位置 )
    [saturation](f_VideoOverlay_saturation) ( ビデオの彩度 )
    [saturationDefaultValue](f_VideoOverlay_saturationDefaultValue) ( ビデオの彩度既定値 )
    [saturationRangeMax](f_VideoOverlay_saturationRangeMax) ( ビデオの彩度レンジ最大値 )
    [saturationRangeMin](f_VideoOverlay_saturationRangeMin) ( ビデオの彩度レンジ最小値 )
    [saturationStepSize](f_VideoOverlay_saturationStepSize) ( ビデオの彩度増減ステップ値 )
    [segmentLoopEndFrame](f_VideoOverlay_segmentLoopEndFrame) ( セグメントループの開始フレーム )
    [segmentLoopStartFrame](f_VideoOverlay_segmentLoopStartFrame) ( セグメントループの開始フレーム )
    [top](f_VideoOverlay_top) ( 再生矩形の上端位置 )
    [totalTime](f_VideoOverlay_totalTime) ( 合計時間 )
    [visible](f_VideoOverlay_visible) ( 可視かどうか )
    [width](f_VideoOverlay_width) ( 再生矩形の横幅 )

イベント
:   [onCallbackCommand](f_VideoOverlay_onCallbackCommand) ( コールバックコマンドが発生した )
    [onFrameUpdate](f_VideoOverlay_onFrameUpdate) ( ビデオフレームが更新された )
    [onPeriod](f_VideoOverlay_onPeriod) ( Periodイベントが発生した )
    [onStatusChanged](f_VideoOverlay_onStatusChanged) ( ステータスが変更された )