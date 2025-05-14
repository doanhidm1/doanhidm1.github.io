# Window.onDisplayRotate

機能/意味
:   画面が回転されたとき(1.1.0以降)

タイプ
:   [Windowクラス](f_Window)のイベント

構文
:   onDisplayRotate(orientation, angle, bpp, width, height)

引数
:   |  |  |
    | --- | --- |
    | orientation | 画面の向き( orientation ) です。  　以下のいずれかの値になります。  　oriUnknown (取得失敗/不明), oriPortrait(縦向き), oriLandscape(横向き) |
    | angle | 角度です。  　角度 ( angle ) は、0、90、180、270、-1 のいずれかで、取得できなかった時は-1となります。  　角度は、そのデバイスデフォルトからの回転角なので、縦向きのデバイスでは縦向きで0となります。  　通常のデバイスだと、横向きで0が多ようです。  　縦向きが0になるのは最近の8インチタブレットなどで、縦向きが標準の向きとなっているものです。 |
    | bpp | bits per pixel です。 |
    | width | 画面の幅です。 |
    | height | 画面の高さです。 |

説明
:   画面が回転されたときに呼び出されるイベント関数を表します。

参照
:   [Window.displayOrientation](f_Window_displayOrientation)
    [Window.displayRotate](f_Window_displayRotate)