# Window.onActivateChanged

機能/意味
:   ■拡張イベント：アクティブ状態変更通知

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   onActivateChanged(active, minimize)

引数
:   |  |  |
    | --- | --- |
    | active | 0:非アクティブ化 1:マウスクリック以外でアクティブ化 2:マウスクリックでアクティブ化 |
    | minimize | 0:ウィンドウは最小化されていない それ以外:最小化されている |

戻り値
:   なし (void)

説明
:   ※Window.onActivate や Window.onDeactivate と違うのは、（これは拡張イベント全般に言えることだが）
    System.eventDisabled == true でもイベントコールバックが飛んでくるという点

    例えば System.onDeactivate 時に System.eventDisabled=true（こうすると System.onActivateは
    飛んでこない）にして，このイベント通知で復帰させると「非アクティブ時に動作停止」といった機能を
    追加できるかもしれない（ただしこれはイベントを配信停止するだけなので，前との時間差を見るような
    タイマーを使ったアプリではあまり意味が無い）
    なお，System.eventDisabled=true 時は画面更新すら走らないので，他のウィンドウを上にするなどして
    WM\_PAINT が発生すると画面が崩れる問題がある（後述の OverlayBitmap を使うなどする）