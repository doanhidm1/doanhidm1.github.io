# Layer.assignImages

機能/意味
:   画像のコピー

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   assignImages(src)

引数
:   |  |  |
    | --- | --- |
    | src | コピー元のレイヤを指定します。 |

戻り値
:   なし (void)

説明
:   src で指定したレイヤの、メイン画像、マスク画像、領域画像をすべてコピーします。
    画像サイズはコピー元のレイヤの画像サイズと同一になります。
    それ以外の情報はコピーしません。
    コピーといっても、実際は「同じ画像を二つ以上のレイヤで共有している」という状態になるだけなのでこのメソッドはほとんど実行時間がかかりません。