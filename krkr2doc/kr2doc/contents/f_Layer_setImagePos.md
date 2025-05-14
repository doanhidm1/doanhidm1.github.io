# Layer.setImagePos

機能/意味
:   レイヤ画像オフセットの設定

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   setImagePos(left, top)

引数
:   |  |  |
    | --- | --- |
    | left | レイヤに表示する画像の左端位置 ( x オフセット ) をピクセル単位で指定します。  　この値は [Layer.imageLeft](f_Layer_imageLeft) プロパティでも取得や設定ができます。 |
    | top | レイヤに表示する画像の上端位置 ( y オフセット ) をピクセル単位で指定します。  　この値は [Layer.imageTop](f_Layer_imageTop) プロパティでも取得や設定ができます。 |

戻り値
:   なし (void)

説明
:   レイヤ画像オフセットを指定します。
    　レイヤ画像サイズはレイヤ表示サイズより大きくすることができますが、すべてを表示する
    ことはできませんので、このメソッドや [Layer.imageLeft](f_Layer_imageLeft) や [Layer.imageTop](f_Layer_imageTop) プロパティで表示オフセットを指定することになります。
    　オフセットは、 0 か、負の数値になります。