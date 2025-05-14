# System.setIconicPreview

機能/意味
:   Vista以降のタスクバーやAlt+TABでのサムネイル表示を強制的にアプリケーションアイコン表示にする

タイプ
:   [Systemクラス](class_System)のメソッド

構文
:   setIconicPreview(iconic)

引数
:   |  |  |
    | --- | --- |
    | iconic | trueならサムネイルの代わりにアイコンを表示する／falseなら設定解除 |

戻り値
:   成功したかどうか（XP以前では常に失敗）

説明
:   ※ アプリケーションウィンドウに DWMWA\_FORCE\_ICONIC\_REPRESENTATION が設定される