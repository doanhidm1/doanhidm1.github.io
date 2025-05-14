# Window.onTouchRotate

機能/意味
:   回転操作した

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onTouchRotate(startangle, currentangle, distance, cx, cy, flag)

引数
:   |  |  |
    | --- | --- |
    | startangle | マルチタッチが開始された時のラジアン角度です。 |
    | currentangle | イベント発生時のタッチのラジアン角度です。 |
    | distance | イベント発生時のタッチのピクセル距離です。 |
    | cx | 中心位置の x 座標 ( クライアント座標での ) の値です。 |
    | cy | 中心位置の y 座標 ( クライアント座標での ) の値です。 |
    | flag | マルチタッチ状態フラグです。  0x01 : マルチタッチが開始された最初のイベントに設定されています。 |

戻り値
:   なし (void)

説明
:   タッチパネル上でマルチタッチによって回転操作した時に発生します。