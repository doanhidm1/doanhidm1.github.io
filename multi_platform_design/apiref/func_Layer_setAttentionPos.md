# Layer.setAttentionPos

機能/意味
:   注視位置の指定

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   setAttentionPos(left, top)

引数
:   |  |  |
    | --- | --- |
    | left | 注視する ( このレイヤの表示座標における ) x 座標値をピクセル単位で指定します。  この値は Layer.attentionLeft プロパティでも設定／取得する事ができます。 |
    | top | 注視する ( このレイヤの表示座標における ) x 座標値をピクセル単位で指定します。  この値は Layer.attentionTop プロパティでも設定／取得する事ができます。 |

戻り値
:   なし (void)

説明
:   注視位置を指定します。
    注視位置とは通常カレット ( キーボードからの文字入力位置を示すためにテキストエディタなどで点滅する棒 ) の位置に設定します。
    IME の未確定文字はこの注視位置に表示されます。

参照
:   [Layer.useAttention](prop_Layer_useAttention)