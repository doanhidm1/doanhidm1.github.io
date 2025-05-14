# Window.onDisplayRotate

機能/意味
:   画面が回転されたとき

タイプ
:   [Windowクラス](class_Window)のイベント

構文
:   onDisplayRotate(orientation, angle, bpp, width, height)

引数
:   |  |  |
    | --- | --- |
    | orientation | 画面の向き( orientation ) です。以下のいずれかの値になります。oriUnknown (取得失敗/不明), oriPortrait(縦向き), oriLandscape(横向き) |
    | angle | 角度です。角度 ( angle ) は、0、90、180、270、-1 のいずれかで、取得できなかった時は-1となります。  角度は、そのデバイスデフォルトからの回転角なので、縦向きのデバイスでは縦向きで0となります。  通常のデバイスだと、横向きで0が多ようです。  縦向きが0になるのは最近の8インチタブレットなどで、縦向きが標準の向きとなっているものです。  Androidでは常に-1が返ります。  必要であれば別途Windows.displayRotateで取得します。 |
    | bpp | bits per pixel です。Androidではdpi値が返ります。 |
    | width | 画面の幅です。  Androidでは常に0が返ります。  必要であれば別途取得します。 |
    | height | 画面の高さです。  Androidでは常に0が返ります。  必要であれば別途取得します。 |

戻り値
:   なし (void)

説明
:   画面が回転されたときに呼び出されるイベント関数を表します。

参照
:   [Window.displayOrientation](prop_Window_displayOrientation)
    [Window.displayRotate](prop_Window_displayRotate)