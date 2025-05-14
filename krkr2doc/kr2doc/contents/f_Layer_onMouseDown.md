# Layer.onMouseDown

機能/意味
:   マウスのボタンが押された

タイプ
:   [Layerクラス](f_Layer)のイベント

構文
:   onMouseDown(x, y, button, shift)

引数
:   |  |  |
    | --- | --- |
    | x | マウスのボタンが押された位置の x 座標 ( レイヤの表示座標での ) の値です。 |
    | y | マウスのボタンが押された位置の y 座標 ( レイヤの表示座標での ) の値です。 |
    | button | 押されたマウスボタンです。以下のいずれかの値になります。  mbLeft : マウスの左ボタンが押された  mbMiddle : マウスの中ボタンが押された  mbRight : マウスの右ボタンが押された |
    | shift | マウスボタンが押されたときに同時に押されていたシフト系のキーの状態です。 以下の値のビット OR による組み合わせになります。  ssAlt : ALT キーが押されていた  ssShift : SHIFT キーが押されていた  ssCtrl : CTRL キーが押されていた |

説明
:   マウスボタンが押された時に発生します。

参照
:   [Layer.onClick](f_Layer_onClick)