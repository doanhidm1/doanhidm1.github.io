# System

System クラスは 吉里吉里本体や、吉里吉里が実行されている環境に関する情報を取得したり、設定したりするためのクラスです。このクラスからオブジェクトを作成することはできません。

# メンバ

コンストラクタ
:   なし

メソッド
:   [addContinuousHandler](f_System_addContinuousHandler) ( Continuous ハンドラの追加 )
    [assignMessage](f_System_assignMessage) ( メッセージ割り当ての変更 )
    [createAppLock](f_System_createAppLock) ( 二重起動のチェック )
    [createUUID](f_System_createUUID) ( UUID 文字列の生成 )
    [doCompact](f_System_doCompact) ( メモリのコンパクト化 )
    [exit](f_System_exit) ( 吉里吉里の同期終了 )
    [getArgument](f_System_getArgument) ( コマンドラインオプションの取得 )
    [getKeyState](f_System_getKeyState) ( キー状態の取得 )
    [getTickCount](f_System_getTickCount) ( ティックカウントの取得 )
    [inform](f_System_inform) ( メッセージの表示 )
    [inputString](f_System_inputString) ( 文字列の入力 )
    [readRegValue](f_System_readRegValue) ( レジストリの読み込み )
    [removeContinuousHandler](f_System_removeContinuousHandler) ( Continuous ハンドラの削除 )
    [setArgument](f_System_setArgument) ( コマンドラインオプションの設定 )
    [shellExecute](f_System_shellExecute) ( ファイル/プログラムの実行 )
    [terminate](f_System_terminate) ( 吉里吉里の非同期終了 )
    [toActualColor](f_System_toActualColor) ( 色定数の実際の色の取得 )
    [touchImages](f_System_touchImages) ( 画像のキャッシュへの読み込み )

プロパティ
:   [appDataPath](f_System_appDataPath) ( ユーザのホームディレクトリのパス )
    [dataPath](f_System_dataPath) ( データ保存場所のパス )
    [desktopHeight](f_System_desktopHeight) ( デスクトップ高さ )
    [desktopLeft](f_System_desktopLeft) ( デスクトップ左端位置 )
    [desktopTop](f_System_desktopTop) ( デスクトップ上端位置 )
    [desktopWidth](f_System_desktopWidth) ( デスクトップ幅 )
    [drawThreadNum](f_System_drawThreadNum) ( 描画に使用するスレッドの数 )
    [eventDisabled](f_System_eventDisabled) ( イベント配信が停止されているかどうか )
    [exceptionHandler](f_System_exceptionHandler) ( 捕捉されなかった例外のためのハンドラ関数 )
    [exeName](f_System_exeName) ( 吉里吉里本体のパス )
    [exePath](f_System_exePath) ( 吉里吉里本体のあるフォルダのパス )
    [exitOnWindowClose](f_System_exitOnWindowClose) ( メインウィンドウが閉じたときに終了するかどうか )
    [graphicCacheLimit](f_System_graphicCacheLimit) ( 画像キャッシュ制限 )
    [onActivate](f_System_onActivate) ( アプリケーションがアクティブになったとき )
    [onDeactivate](f_System_onDeactivate) ( アプリケーションが非アクティブになったとき )
    [osName](f_System_osName) ( OS 名 )
    [personalPath](f_System_personalPath) ( マイドキュメントのパス )
    [platformName](f_System_platformName) ( プラットフォーム名 )
    [screenHeight](f_System_screenHeight) ( 画面高さ )
    [screenWidth](f_System_screenWidth) ( 画面幅 )
    [title](f_System_title) ( タイトル )
    [versionInformation](f_System_versionInformation) ( バージョン情報文字列 )
    [versionString](f_System_versionString) ( バージョン文字列 )

イベント
:   なし