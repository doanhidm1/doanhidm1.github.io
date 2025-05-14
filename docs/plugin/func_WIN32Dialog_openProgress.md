# WIN32Dialog.openProgress

機能/意味
:   プログレスダイアログを表示する

タイプ
:   [WIN32Dialogクラス](class_WIN32Dialog)のメソッド

構文
:   openProgress(id, window, dsapp, breathe)

引数
:   |  |  |
    | --- | --- |
    | id | プログレスバーのダイアログアイテムID（progressValueプロパティで更新される対象） |
    | window | [optional] オーナーwindow (void=オーナーなし,null=Application) |
    | dsapp | [optional] プログレス表示中はアプリケーションウィンドウを無効にするか |
    | breathe | [optional] progressValueのsetterでbreatheするかどうか |

戻り値
:   成功したらtrue

説明
:   プログレスダイアログのstyleにはWS\_VISIBLEを指定しないこと
    閉じるときは必ず closeProgress() を使用すること
    プログレス表示の場合，onInit以外のコールバックは来ないので注意