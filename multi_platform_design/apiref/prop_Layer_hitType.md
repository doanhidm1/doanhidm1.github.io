# Layer.hitType

機能/意味
:   当たり判定のタイプ

タイプ
:   [Layerクラス](class_Layer)のプロパティ

説明
:   マウスイベントの当たり判定のタイプを表します。
    値を設定することもできます。
    htProvince を指定すると、領域画像において 0 以外の領域のみマウスイベントを受け取るようになります。
    htMask を指定すると、マスク(不透明度)画像の値が、Layer.hitThreshold プロパティで指定した値以上の場合のみマウスイベントを受け取るようになります。
    受け取られなかったマウスイベントは、より奥のレイヤで処理されます。
    初期状態では htMask となっています。