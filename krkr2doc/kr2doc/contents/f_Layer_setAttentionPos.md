# Layer.setAttentionPos

機能/意味
:   注視位置の指定

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   setAttentionPos(left, top)

引数
:   |  |  |
    | --- | --- |
    | left | 注視する ( このレイヤの表示座標における ) x 座標値をピクセル単位で指定します。  　この値は [Layer.attentionLeft](f_Layer_attentionLeft) プロパティでも設定／取得する事ができます。 |
    | top | 注視する ( このレイヤの表示座標における ) x 座標値をピクセル単位で指定します。  　この値は [Layer.attentionTop](f_Layer_attentionTop) プロパティでも設定／取得する事ができます。 |

戻り値
:   なし (void)

説明
:   注視位置を指定します。注視位置とは通常カレット ( キーボードからの文字入力位置を
    示すためにテキストエディタなどで点滅する棒 ) の位置に設定します。IME の未確定文字はこの注視位置に
    表示されます。

参照
:   [Layer.useAttention](f_Layer_useAttention)