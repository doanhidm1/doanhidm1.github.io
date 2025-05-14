# Base

# メンバ

メソッド
:   [onAfterGUI](func_Base_onAfterGUI) (GUI描画後に呼び出されるイベント )
    [onAfterScene](func_Base_onAfterScene) (シーン描画後に呼び出されるイベント )
    [onAttach](func_Base_onAttach) (オブジェクト生成時やフルスクリーン化などの再構築の後で、 ドライバが初期化された直後に呼ばれるイベント )
    [onBeforeGUI](func_Base_onBeforeGUI) (GUI描画前に呼び出されるイベント )
    [onBeforeScene](func_Base_onBeforeScene) (シーン描画前に呼び出されるイベント )
    [onDetach](func_Base_onDetach) (オブジェクト破棄時や、フルスクリーン化による再構築の前で、 ドライバが破棄される直前に呼ばれるイベント )
    [onEvent](func_Base_onEvent) (Irrlicht からのイベント通知 )

プロパティ
:   [eventMask](prop_Base_eventMask) (イベントマスク。TJS側への呼び返しイベントを指定する。 デフォルトは EMASK\_ATTACH|EMASK\_DETACH )
    [fileSystem](prop_Base_fileSystem) (< ログ環境 (ILoggerクラス）。読み出し専用 )
    [guiEnvironment](prop_Base_guiEnvironment) (< シーンマネージャ(ISceneManagerクラス)。読み出し専用 )
    [logger](prop_Base_logger) (< GUI環境（IGUIEnvironmentクラス）。読み出し専用 )
    [sceneManager](prop_Base_sceneManager) (< ドライバ(IVideoDriverクラス)。読み出し専用 )
    [videoDriver](prop_Base_videoDriver) ( )