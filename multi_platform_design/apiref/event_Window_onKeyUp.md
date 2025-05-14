# Window.onKeyUp

機能/意味
:   キーが離された

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onKeyUp(key, shift)

引数
:   |  |  |
    | --- | --- |
    | key | 離されたキーの仮想キーコードの値です。 |
    | shift | キーが離された時に同時に押されていたシフト系のキーやマウスのボタンの状態です。  以下の値のビット OR による組み合わせになります。   * ssAlt : ALT キーが押されていた * ssShift : SHIFT キーが押されていた * ssCtrl : CTRL キーが押されていた * ssLeft : マウスの左ボタンが押されていた * ssMiddle : マウスの中ボタンが押されていた * ssRight : マウスの右ボタンが押されていた |

戻り値
:   なし (void)

説明
:   キーが離された時に発生します。