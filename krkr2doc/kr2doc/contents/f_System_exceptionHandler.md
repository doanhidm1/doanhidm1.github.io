# System.exceptionHandler

機能/意味
:   捕捉されなかった例外のためのハンドラ関数

タイプ
:   [Systemクラス](f_System)のプロパティ (読み書き可能)

説明
:   捕捉されなかった例外 (どこにも捕捉されずに吉里吉里本体に渡された例外) を処理する関数を表します。
    　null を指定すると、デフォルトの動作になります。
    　デフォルトの動作とは、

    1. 非同期イベントの配信を停止する ([System.eventDisabled](f_System_eventDisabled) を 真 に設定)
    2. ログをファイルに出力開始する ([Debug.logAsError](f_Debug_logAsError) を呼ぶ)
    3. エラーを通知するダイアログボックスを表示し、スクリプトエディタでその箇所を示す

    　です。
    　ハンドラ関数は引数を一つ取り、それが例外オブジェクトになります。
    　ハンドラ関数が指定されないか、あるいはハンドラ関数が null であるか、あるいはハンドラ関数が偽を返すと、デフォルトの動作が行われます。
    　ハンドラ関数が真を返すと上記のデフォルトの動作は行われません。
    　ハンドラ関数を実行中に非同期イベントが発生する可能性を考慮してください。吉里吉里本体が非同期イベントを処理できてしまうと、例外ハンドラを実行中に再び予期せぬ例外が発生する可能性があります。これを避けるため、通常、ハンドラ関数内でなにかを待つような処理をする場合 (吉里吉里が非同期イベントを処理する機会がある場合 )、非同期イベントの発生を停止させます。
    `例:
    System.exceptionHandler = function (e)
    {
        // どこにも捕捉されない例外がシステム側で捕捉された場合、この関数が
        // 呼ばれる。e は例外オブジェクト。
        if(e instanceof "ConductorException")
        {
            // コンダクタの投げた例外の場合
            Debug.logAsError(); // ログのファイルへの書き出し動作の開始など
            var event_disabled = System.eventDisabled;
            System.eventDisabled = true;
                // エラーの理由を表示させている間にイベントが発生すると
                // やっかいなのでいったんイベント発生を停止させる
            System.inform(e.message);
            System.eventDisabled = event_disabled;
                // イベントを発生するかどうかを元の状態に
            return true; // true を返すと本体側で例外の処理は行わなくなる
        }
        else
        {
            return false; // false を返すと通常の例外処理
        }
    };`

参照
:   [System.eventDisabled](f_System_eventDisabled)
    [Debug.logAsError](f_Debug_logAsError)