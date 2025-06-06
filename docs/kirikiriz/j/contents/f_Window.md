# Window

Window クラスは、ウィンドウを管理するためのクラスです。

# メンバ

コンストラクタ
:   [Window](f_Window_Window)

メソッド
:   [add](f_Window_add) ( 管理オブジェクトの追加 )
    [bringToFront](f_Window_bringToFront) ( ウィンドウを最前面に移動 )
    [close](f_Window_close) ( ウィンドウを閉じる )
    [getMouseVelocity](f_Window_getMouseVelocity) ( マウス座標移動速度の取得(1.1.0以降) )
    [getTouchPoint](f_Window_getTouchPoint) ( タッチ座標の取得 )
    [getTouchVelocity](f_Window_getTouchVelocity) ( タッチ座標移動速度の取得(1.1.0以降) )
    [hideMouseCursor](f_Window_hideMouseCursor) ( マウスカーソルを一時的に隠す )
    [postInputEvent](f_Window_postInputEvent) ( 入力イベントの生成 )
    [registerMessageReceiver](f_Window_registerMessageReceiver) ( メッセージ受信関数の登録/登録削除 )
    [remove](f_Window_remove) ( 管理オブジェクトの削除 )
    [removeMaskRegion](f_Window_removeMaskRegion) ( ウィンドウリージョンの解除 )
    [resetMouseVelocity](f_Window_resetMouseVelocity) ( マウス座標移動速度計測のリセット(1.1.0以降) )
    [setInnerSize](f_Window_setInnerSize) ( クライアントサイズの設定 )
    [setMaskRegion](f_Window_setMaskRegion) ( ウィンドウリージョンをマスクに従って設定 )
    [setMaxSize](f_Window_setMaxSize) ( ウィンドウの最大サイズの設定 )
    [setMinSize](f_Window_setMinSize) ( ウィンドウの最小サイズの設定 )
    [setPos](f_Window_setPos) ( ウィンドウ位置の設定 )
    [setSize](f_Window_setSize) ( ウィンドウサイズの設定 )
    [setZoom](f_Window_setZoom) ( レイヤ拡大倍率の設定 )
    [showModal](f_Window_showModal) ( モーダルでウィンドウを表示 )
    [update](f_Window_update) ( ウィンドウ内容の強制的な描画 )

プロパティ
:   [HWND](f_Window_HWND) ( ウィンドウハンドル )
    [borderStyle](f_Window_borderStyle) ( ウィンドウ外見 )
    [caption](f_Window_caption) ( ウィンドウのキャプション )
    [displayOrientation](f_Window_displayOrientation) ( ディスプレイの向き(1.1.0以降) )
    [displayRotate](f_Window_displayRotate) ( ディスプレイの回転角度(1.1.0以降) )
    [drawDevice](f_Window_drawDevice) ( 描画デバイス )
    [enableTouch](f_Window_enableTouch) ( タッチイベント有効/無効 )
    [focusable](f_Window_focusable) ( フォーカスを取得可能か )
    [focusedLayer](f_Window_focusedLayer) ( フォーカスを持っているレイヤオブジェクト )
    [fullScreen](f_Window_fullScreen) ( フルスクリーンかどうか )
    [height](f_Window_height) ( ウィンドウの縦幅 )
    [hintDelay](f_Window_hintDelay) ( ヒント表示待ち時間 )
    [imeMode](f_Window_imeMode) ( デフォルトのIMEモード )
    [innerHeight](f_Window_innerHeight) ( クライアント領域の縦幅 )
    [innerWidth](f_Window_innerWidth) ( クライアント領域の横幅 )
    [left](f_Window_left) ( ウィンドウの左端位置 )
    [mainWindow](f_Window_mainWindow) ( メインウィンドウ )
    [maxHeight](f_Window_maxHeight) ( ウィンドウの最大の縦幅 )
    [maxWidth](f_Window_maxWidth) ( ウィンドウの最大の横幅 )
    [minHeight](f_Window_minHeight) ( ウィンドウの最小の縦幅 )
    [minWidth](f_Window_minWidth) ( ウィンドウの最小の横幅 )
    [mouseCursorState](f_Window_mouseCursorState) ( マウスカーソル表示状態 )
    [primaryLayer](f_Window_primaryLayer) ( プライマリレイヤオブジェクト )
    [stayOnTop](f_Window_stayOnTop) ( 常に最上位に表示するかどうか )
    [top](f_Window_top) ( ウィンドウの上端位置 )
    [touchPointCount](f_Window_touchPointCount) ( タッチ数 )
    [touchRotateThreshold](f_Window_touchRotateThreshold) ( マルチタッチ回転閾値 )
    [touchScaleThreshold](f_Window_touchScaleThreshold) ( マルチタッチ拡大閾値 )
    [trapKey](f_Window_trapKey) ( キー入力をトラップするか )
    [useMouseKey](f_Window_useMouseKey) ( マウスキーを使用するかどうか )
    [visible](f_Window_visible) ( ウィンドウが表示されているかどうか )
    [waitVSync](f_Window_waitVSync) ( 垂直同期待ち )
    [width](f_Window_width) ( ウィンドウの横幅 )
    [zoomDenom](f_Window_zoomDenom) ( レイヤ拡大倍率(分母) )
    [zoomNumer](f_Window_zoomNumer) ( レイヤ拡大倍率(分子) )

イベント
:   [onActivate](f_Window_onActivate) ( ウィンドウがアクティブになったとき )
    [onClick](f_Window_onClick) ( ウィンドウがクリックされた )
    [onCloseQuery](f_Window_onCloseQuery) ( ウィンドウを閉じる確認 )
    [onDeactivate](f_Window_onDeactivate) ( ウィンドウが非アクティブになったとき )
    [onDisplayRotate](f_Window_onDisplayRotate) ( 画面が回転されたとき(1.1.0以降) )
    [onDoubleClick](f_Window_onDoubleClick) ( ウィンドウがダブルクリックされた )
    [onFileDrop](f_Window_onFileDrop) ( ファイルがドロップされた )
    [onHintChanged](f_Window_onHintChanged) ( ヒントの状態が変化したとき )
    [onKeyDown](f_Window_onKeyDown) ( キーが押された )
    [onKeyPress](f_Window_onKeyPress) ( 文字が入力された )
    [onKeyUp](f_Window_onKeyUp) ( キーが離された )
    [onMouseDown](f_Window_onMouseDown) ( マウスのボタンが押された )
    [onMouseEnter](f_Window_onMouseEnter) ( マウスが入ってきた )
    [onMouseLeave](f_Window_onMouseLeave) ( マウスが出ていった )
    [onMouseMove](f_Window_onMouseMove) ( マウスが移動した )
    [onMouseUp](f_Window_onMouseUp) ( マウスのボタンが離された )
    [onMouseWheel](f_Window_onMouseWheel) ( マウスホイールが回転した )
    [onMultiTouch](f_Window_onMultiTouch) ( マルチタッチ状態が変化した )
    [onPopupHide](f_Window_onPopupHide) ( ポップアップウィンドウを閉じる )
    [onResize](f_Window_onResize) ( ウィンドウのサイズが変化した )
    [onTouchDown](f_Window_onTouchDown) ( 画面がタッチされた )
    [onTouchMove](f_Window_onTouchMove) ( 指が移動した )
    [onTouchRotate](f_Window_onTouchRotate) ( 回転操作した )
    [onTouchScaling](f_Window_onTouchScaling) ( 拡大操作した )
    [onTouchUp](f_Window_onTouchUp) ( 画面から指が離された )