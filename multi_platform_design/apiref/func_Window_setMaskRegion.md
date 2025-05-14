# Window.setMaskRegion

機能/意味
:   [Windows+]ウィンドウリージョンをマスクに従って設定

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   setMaskRegion(threshold=1)

引数
:   |  |  |
    | --- | --- |
    | threshold | マスクのスレッショルド ( 敷居値 ) を指定します。  プライマリレイヤのマスク ( レイヤの不透明度の情報 ) のうち、この値よりも大きい部分の形にウィンドウが切り取られて表示されます。 |

戻り値
:   なし (void)

説明
:   ウィンドウリージョンをプライマリレイヤのマスク ( レイヤの不透明度の情報 ) に従って設定します。
    ウィンドウを不定形にする事ができます。
    表示されるプライマリレイヤと、ウィンドウの大きさ、位置がずれないようにするには以下のことを行う必要があります。
    Window.borderStyle は bsNone に設定します。
    Layer.imageLeft および Layer.imageTop は 0 に設定します。

参照
:   [Window.removeMaskRegion](func_Window_removeMaskRegion)