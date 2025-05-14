# Canvas.flush

機能/意味
:   描画をフラッシュする

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   flush()

引数

戻り値
:   なし (void)

説明
:   描画を反映したいrenderTargetを入れ替える場合などに使われます。
    onDraw中にrenderTargetを入れ替えると、内部的にflushは呼ばれるので、明示的な呼び出しは不要です。