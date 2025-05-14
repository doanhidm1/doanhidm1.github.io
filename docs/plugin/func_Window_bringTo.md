# Window.bringTo

機能/意味
:   ウィンドウの Zオーダーを変更する

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   bringTo(win, activate)

引数
:   |  |  |
    | --- | --- |
    | win | Windowオブジェクトまたは規定文字列または数値 Windowオブジェクトなら，そのウィンドウの後ろに置かれる 文字列の場合，"bottom" "notopmost" "top" "topmost" のいずれか（HWND\_\*相当）cf. SetWindowPos API 数値の場合，ウィンドウハンドルと見なすか，HWND\_\* マクロの値を直指定する #define HWND\_TOP ((HWND)0) #define HWND\_BOTTOM ((HWND)1) #define HWND\_TOPMOST ((HWND)-1) #define HWND\_NOTOPMOST ((HWND)-2) |
    | activate | アクティブ状態にするかどうかのフラグ trueにしてもアプリケーション自体はアクティブになりません（タスクバーの点滅などおこりません） |

戻り値
:   なし (void)

説明