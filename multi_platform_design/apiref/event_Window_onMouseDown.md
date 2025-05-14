# Window.onMouseDown

機能/意味
:   [Windows\*]マウスのボタンが押された

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onMouseDown(x, y, button, shift)

引数
:   |  |  |
    | --- | --- |
    | x | マウスのボタンが押された位置の x 座標 ( クライアント座標での ) の値です。 |
    | y | マウスのボタンが押された位置の y 座標 ( クライアント座標での ) の値です。 |
    | button | 押されたマウスボタンです。  以下のいずれかの値になります。   * mbLeft : マウスの左ボタンが押された * mbMiddle : マウスの中ボタンが押された * mbRight : マウスの右ボタンが押された * mbX1 : マウスのサイドキー第1ボタンが押された * mbX2 : マウスのサイドキー第2ボタンが押された |
    | shift | マウスボタンが押されたときに同時に押されていたシフト系のキーの状態です。  以下の値のビット OR による組み合わせになります。   * ssAlt : ALT キーが押されていた * ssShift : SHIFT キーが押されていた * ssCtrl : CTRL キーが押されていた |

戻り値
:   なし (void)

説明
:   マウスボタンが押された時に発生します。

参照
:   [Window.onClick](event_Window_onClick)