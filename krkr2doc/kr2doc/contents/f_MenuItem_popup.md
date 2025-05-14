# MenuItem.popup

機能/意味
:   メニュー項目のポップアップ表示

タイプ
:   [MenuItemクラス](f_MenuItem)のメソッド

構文
:   popup(flags, x, y)

引数
:   |  |  |
    | --- | --- |
    | flags | メニューの挙動を表すフラグです。以下の値のビット論理和を指定してください。  tpmLeftButton  tpmRightButton  tpmLeftAlign  tpmCenterAlign  tpmRightAlign  tpmTopAlign  tpmVCenterAlign  tpmBottomAlign  tpmHorizontal  tpmVertical  tpmNoNotify  tpmReturnCmd  tpmRecurse  tpmHorPosAnimation  tpmHorNegAnimation  tpmVerPosAnimation  tpmVerNegAnimation  tpmNoAnimation  これらのフラグの詳細については[MSDNの該当ページ](http://msdn.microsoft.com/library/ja/jpwinui/html/_win32_trackpopupmenu.asp?frame=true)を参照してください。 |
    | x | ウィンドウのクライアント座標上でのx位置を表します。 |
    | y | ウィンドウのクライアント座標上でのy位置を表します。 |

戻り値
:   flagsにtpmReturnCmdが指定されていた場合は、
    選択されたメニュー項目のIDを整数で返します(ただし、現バージョンではこのIDを吉里吉里側から設定することができないため、flagsにtpmReturnCmdを指定することは意味がありません)。
    何も選択されずにキャンセルされた場合は0を返します。

説明
:   メニュー項目をポップアップ表示します。このメソッドは、メニューが閉じられるまで帰ってきません。
    メニューが閉じられるまでの間に他の非同期イベントが発生する可能性があるので注意してください。
    [Window.menu](f_Window_menu)そのものはポップアップできません。
    非表示状態のメニュー項目はポップアップできません。
    [Window.menu](f_Window_menu)の子でないメニューはポップアップできません。