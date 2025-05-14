# VideoOverlay

VideoOverlay クラスは、MPEG I や WMV、H.264、theora などを表示するため表示領域を作成するクラスです。
吉里吉里のレイヤに表示を行うこともできます。
theora を再生するには krdstheora.dll が必要になります。
レイヤでの再生を除き、オーバーレイによる再生では、VideoOverlay クラスの表示領域は、すべてのレイヤよりも手前に表示され、透過することはできません。
レイヤでの再生は、オーバーレイでの再生に比べ、再生時のプロセッサの負荷は高くなる傾向にあります。
Androidでは常に最前面表示されるオーバーレイと等価なモードに限定されます。
また再生可能なフォーマットも機種に依存します。
H.246 が再生できる端末が多いようです。
Androidでは動画ファイルはassets内に格納します。

# メンバ

コンストラクタ
:   [VideoOverlay](func_VideoOverlay_VideoOverlay) (VideoOverlay オブジェクトの構築 )

メソッド
:   [cancelPeriodEvent](func_VideoOverlay_cancelPeriodEvent) ([Windows\*]指定フレームでのイベント発生の解除 )
    [cancelSegmentLoop](func_VideoOverlay_cancelSegmentLoop) ([Windows\*]フレーム間ループの解除 )
    [close](func_VideoOverlay_close) (メディアを閉じる )
    [open](func_VideoOverlay_open) (メディアを開く )
    [pause](func_VideoOverlay_pause) (一時停止 )
    [play](func_VideoOverlay_play) (再生開始 )
    [prepare](func_VideoOverlay_prepare) ([Windows\*]再生準備 )
    [resetMixingLayer](func_VideoOverlay_resetMixingLayer) ([Windows+]ミキシング対象レイヤの設定解除 )
    [rewind](func_VideoOverlay_rewind) (巻き戻し )
    [selectAudioStream](func_VideoOverlay_selectAudioStream) ([Windows\*]音声ストリームの選択 )
    [setBounds](func_VideoOverlay_setBounds) ([Windows\*]再生矩形の位置とサイズを指定 )
    [setMixingLayer](func_VideoOverlay_setMixingLayer) ([Windows+]ミキシング対象レイヤの設定 )
    [setPeriodEvent](func_VideoOverlay_setPeriodEvent) ([Windows\*]指定フレームでのイベント発生の指定 )
    [setPos](func_VideoOverlay_setPos) ([Windows\*]再生矩形の左上位置を指定 )
    [setSegmentLoop](func_VideoOverlay_setSegmentLoop) ([Windows\*]フレーム間ループの設定 )
    [setSize](func_VideoOverlay_setSize) ([Windows\*]再生矩形のサイズを指定 )
    [stop](func_VideoOverlay_stop) (再生停止 )

プロパティ
:   [audioBalance](prop_VideoOverlay_audioBalance) ([Windows\*]音声バランス(パニング) )
    [audioVolume](prop_VideoOverlay_audioVolume) (音声ボリューム )
    [brightness](prop_VideoOverlay_brightness) ([Windows+]ビデオの輝度 )
    [brightnessDefaultValue](prop_VideoOverlay_brightnessDefaultValue) ([Windows+]ビデオの輝度既定値 )
    [brightnessRangeMax](prop_VideoOverlay_brightnessRangeMax) ([Windows+]ビデオの輝度レンジ最大値 )
    [brightnessRangeMin](prop_VideoOverlay_brightnessRangeMin) ([Windows+]ビデオの輝度レンジ最小値 )
    [brightnessStepSize](prop_VideoOverlay_brightnessStepSize) ([Windows+]ビデオの輝度増減ステップ値 )
    [contrast](prop_VideoOverlay_contrast) ([Windows+]ビデオのコントラスト )
    [contrastDefaultValue](prop_VideoOverlay_contrastDefaultValue) ([Windows+]ビデオのコントラスト既定値 )
    [contrastRangeMax](prop_VideoOverlay_contrastRangeMax) ([Windows+]ビデオのコントラストレンジ最大値 )
    [contrastRangeMin](prop_VideoOverlay_contrastRangeMin) ([Windows+]ビデオのコントラストレンジ最小値 )
    [contrastStepSize](prop_VideoOverlay_contrastStepSize) ([Windows+]ビデオのコントラスト増減ステップ値 )
    [enabledAudioStream](prop_VideoOverlay_enabledAudioStream) ([Windows\*]再生対象音声ストリーム番号 )
    [fps](prop_VideoOverlay_fps) ([Windows\*]フレームレート )
    [frame](prop_VideoOverlay_frame) ([Windows]現在のフレーム )
    [height](prop_VideoOverlay_height) ([Windows\*]再生矩形の縦幅 )
    [hue](prop_VideoOverlay_hue) ([Windows+]ビデオの色相 )
    [hueDefaultValue](prop_VideoOverlay_hueDefaultValue) ([Windows+]ビデオの色相既定値 )
    [hueRangeMax](prop_VideoOverlay_hueRangeMax) ([Windows+]ビデオの色相レンジ最大値 )
    [hueRangeMin](prop_VideoOverlay_hueRangeMin) ([Windows+]ビデオの色相レンジ最小値 )
    [hueStepSize](prop_VideoOverlay_hueStepSize) ([Windows+]ビデオの色相増減ステップ値 )
    [layer1](prop_VideoOverlay_layer1) ([Windows\*]描画レイヤ指定1 )
    [layer2](prop_VideoOverlay_layer2) ([Windows\*]描画レイヤ指定2 )
    [left](prop_VideoOverlay_left) ([Windows\*]再生矩形の左端位置 )
    [loop](prop_VideoOverlay_loop) ([Windows\*]ループ再生をするかどうか )
    [mixingMovieAlpha](prop_VideoOverlay_mixingMovieAlpha) ([Windows+]ビデオの透明度 )
    [mixingMovieBGColor](prop_VideoOverlay_mixingMovieBGColor) ([Windows+]ビデオの背景色 )
    [mode](prop_VideoOverlay_mode) ([Windows\*]オーバーレイorレイヤ描画の指定 )
    [numberOfAudioStream](prop_VideoOverlay_numberOfAudioStream) ([Windows\*]音声ストリーム数 )
    [numberOfFrame](prop_VideoOverlay_numberOfFrame) ([Windows\*]全フレーム数 )
    [originalHeight](prop_VideoOverlay_originalHeight) ([Windows\*]ビデオの実際の高さ )
    [originalWidth](prop_VideoOverlay_originalWidth) ([Windows\*]ビデオの実際の幅 )
    [periodEventFrame](prop_VideoOverlay_periodEventFrame) ([Windows\*]ピリオドイベントフレーム )
    [playRate](prop_VideoOverlay_playRate) ([Windows\*]再生速度 )
    [position](prop_VideoOverlay_position) (再生位置 )
    [saturation](prop_VideoOverlay_saturation) ([Windows+]ビデオの彩度 )
    [saturationDefaultValue](prop_VideoOverlay_saturationDefaultValue) ([Windows+]ビデオの彩度既定値 )
    [saturationRangeMax](prop_VideoOverlay_saturationRangeMax) ([Windows+]ビデオの彩度レンジ最大値 )
    [saturationRangeMin](prop_VideoOverlay_saturationRangeMin) ([Windows+]ビデオの彩度レンジ最小値 )
    [saturationStepSize](prop_VideoOverlay_saturationStepSize) ([Windows+]ビデオの彩度増減ステップ値 )
    [segmentLoopEndFrame](prop_VideoOverlay_segmentLoopEndFrame) ([Windows\*]セグメントループの開始フレーム )
    [segmentLoopStartFrame](prop_VideoOverlay_segmentLoopStartFrame) ([Windows\*]セグメントループの開始フレーム )
    [top](prop_VideoOverlay_top) ([Windows\*]再生矩形の上端位置 )
    [totalTime](prop_VideoOverlay_totalTime) (合計時間 )
    [visible](prop_VideoOverlay_visible) (可視かどうか )
    [width](prop_VideoOverlay_width) ([Windows\*]再生矩形の横幅 )

イベント
:   [onFrameUpdate](event_VideoOverlay_onFrameUpdate) ([Windows\*]ビデオフレームが更新された )
    [onPeriod](event_VideoOverlay_onPeriod) ([Windows\*]Periodイベントが発生した )
    [onStatusChanged](event_VideoOverlay_onStatusChanged) (ステータスが変更された )