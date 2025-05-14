# WIN32Dialog.onCommand

機能/意味
:   WM\_COMMAND のコールバック

タイプ
:   [WIN32Dialogクラス](class_WIN32Dialog)のメソッド

構文
:   onCommand(msg, wparam, lparam)

引数
:   |  |  |
    | --- | --- |
    | msg | DlgProc のメッセージ == WM\_COMMAND |
    | wparam | DlgProc のWPARAM |
    | lparam | DlgProc のLPARAM |

戻り値
:   なし (void)

説明
:   コールバックはownerに対して呼ばれるので注意してください。
    owner.onCommandが未定義なら何もしません。