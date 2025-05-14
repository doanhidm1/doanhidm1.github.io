# Layer.onTouchScaling

機能/意味
:   拡大操作した

タイプ
:   [Layerクラス](f_Layer)のイベント

構文
:   onTouchScaling(startdistance, currentdistance, cx, cy, flag)

引数
:   |  |  |
    | --- | --- |
    | startdistance | マルチタッチが開始された時のピクセル距離です。 |
    | currentdistance | イベント発生時のタッチのピクセル距離です。 |
    | cx | 中心位置の x 座標 ( クライアント座標での ) の値です。 |
    | cy | 中心位置の y 座標 ( クライアント座標での ) の値です。 |
    | flag | マルチタッチ状態フラグです。  0x01 : マルチタッチが開始された最初のイベントに設定されています。 |

説明
:   タッチパネル上でマルチタッチによって拡大操作した時に発生します。
    　このイベントが発生するのは、フォーカスのあるレイヤです。