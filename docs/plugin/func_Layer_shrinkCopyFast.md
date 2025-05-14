# Layer.shrinkCopyFast

機能/意味
:   限定縮小コピー（整数分の一の縮小＆α成分無視で処理）

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   shrinkCopyFast(src, shrink\_x, shrink\_y)

引数
:   |  |  |
    | --- | --- |
    | shrink\_x | 横方向の縮小係数(1 以上） |
    | shrink\_y | 縦方向の縮小係数(1 以上）省略時または 0 の場合は shrink\_x の値を使用 |

戻り値
:   なし (void)

説明
:   透明部分は無視されて常に不透明になる
    右端，下端の 1dot の部分で割り切れない場合の端数分で伸びたように見える場合がある

    ※自分自身のサイズが強制で変更されるので注意
    ⇒ setImageSize(Math.ceil(src.imageWidth / shrink\_x), Math.ceil(src.imageHeight / shrink\_y)) 相当