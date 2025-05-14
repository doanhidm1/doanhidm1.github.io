# Window.onHintChanged

機能/意味
:   ヒントの状態が変化したとき

タイプ
:   [Windowクラス](f_Window)のイベント

構文
:   onHintChanged(text, x, y, isshow)

引数
:   |  |  |
    | --- | --- |
    | text | ヒントに表示する文字列が渡されます。 |
    | x | ヒント表示X軸座標値が渡されます。 |
    | y | ヒント表示Y軸座標値が渡されます。 |
    | isshow | ヒントを表示するか、非表示にするかが渡されます。 |

説明
:   ヒントの状態が変化したときに呼び出されるイベント関数を表します。
    　表示/非表示に従いヒントの表示を行います。
    　ヒントをレイヤで表示する場合は、そのレイヤのマウスメッセージが無視されるように [Layer.hitThreshold](f_Layer_hitThreshold) を256に設定します。
    　また、[Layer.ignoreHintSensing](f_Layer_ignoreHintSensing) もtrueを指定します。

参照
:   [Window.hintDelay](f_Window_hintDelay)
    [Layer.ignoreHintSensing](f_Layer_ignoreHintSensing)
    [Layer.hitThreshold](f_Layer_hitThreshold)