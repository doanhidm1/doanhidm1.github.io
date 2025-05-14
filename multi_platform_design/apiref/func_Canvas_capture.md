# Canvas.capture

機能/意味
:   現在の描画内容全体をBitmap/Texture/Offscreenにキャプチャ

タイプ
:   [Canvasクラス](class_Canvas)のメソッド

構文
:   capture(dest, front:bool=true)

引数
:   |  |  |
    | --- | --- |
    | dest | キャプチャ先Bitmap/Texture/Offscreen |
    | front | front bufferからのキャプチャかback bufferからのキャプチャかの指定。trueでfront、falseでback |

戻り値
:   なし (void)

説明
:   ビットマップのサイズはスクリーンサイズに補正
    Texture/Offscreenの場合は変更されない