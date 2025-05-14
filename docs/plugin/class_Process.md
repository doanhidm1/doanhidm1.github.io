# Process

外部アプリを機動してその終了を待つ機構を提供します。

# メンバ

メソッド
:   [commandExecute](func_Process_commandExecute) (コンソール出力取得つきコマンドラインプログラムの実行 )
    [execute](func_Process_execute) (バックグラウンドでの外部プログラムの実行 )
    [onExecuted](func_Process_onExecuted) (イベント:シェル実行終了 )
    [onOutput](func_Process_onOutput) (イベント:コンソール出力 )
    [sendSignal](func_Process_sendSignal) (Ctrl+Cイベントの送信(experimental:すべての環境で動作するとは限りません) )
    [terminate](func_Process_terminate) (実行中の外部プログラムの強制終了 )

プロパティ
:   [status](prop_Process_status) (現在の状態 )