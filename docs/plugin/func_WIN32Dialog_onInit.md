# WIN32Dialog.onInit

機能/意味
:   WM\_INITDIALOG のコールバック

タイプ
:   [WIN32Dialogクラス](class_WIN32Dialog)のメソッド

構文
:   onInit(msg, wparam, lparam)

引数
:   |  |  |
    | --- | --- |
    | msg | DlgProc のメッセージ == WM\_INITDIALOG |
    | wparam | DlgProc のWPARAM |
    | lparam | DlgProc のLPARAM |

戻り値
:   なし (void)

説明
:   コールバックはownerに対して呼ばれるので注意してください
    owner.onInitが未定義なら何もしません。