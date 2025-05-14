# Window.setMaskRegion

機能/意味
:   ウィンドウリージョンをマスクに従って設定

タイプ
:   [Windowクラス](f_Window)のメソッド

構文
:   setMaskRegion(threshold=1)

引数
:   |  |  |
    | --- | --- |
    | threshold | マスクのスレッショルド ( 敷居値 ) を指定します。  　プライマリレイヤのマスク ( レイヤの不透明度の情報 ) のうち、この値よりも大きい部分の形に ウィンドウが切り取られて表示されます。 |

戻り値
:   なし (void)

説明
:   ウィンドウリージョンをプライマリレイヤのマスク ( レイヤの不透明度の情報 ) に従って設定します。
    　ウィンドウを不定形にする事ができます。
    　表示されるプライマリレイヤと、ウィンドウの大きさ、位置がずれないようにするには
    以下のことを行う必要があります。

    * [Window.borderStyle](f_Window_borderStyle) は bsNone に設定します。
    * [Window.innerSunken](f_Window_innerSunken) は false に設定します。
    * [Window.layerLeft](f_Window_layerLeft) および [Window.layerTop](f_Window_layerTop) は 0 に設定します。
    * [Layer.imageLeft](f_Layer_imageLeft) および [Layer.imageTop](f_Layer_imageTop) は 0 に設定します。

参照
:   [Window.removeMaskRegion](f_Window_removeMaskRegion)