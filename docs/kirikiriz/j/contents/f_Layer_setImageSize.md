# Layer.setImageSize

機能/意味
:   レイヤ画像サイズの設定

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   setImageSize(width, height)

引数
:   |  |  |
    | --- | --- |
    | width | レイヤ画像の横幅をピクセル単位で指定します。  　この値は [Layer.imageWidth](f_Layer_imageWidth) プロパティでも取得や設定ができます。 |
    | height | レイヤ画像の縦幅をピクセル単位で指定します。  　この値は [Layer.imageHeight](f_Layer_imageHeight) プロパティでも取得や設定ができます。 |

戻り値
:   なし (void)

説明
:   レイヤ画像サイズを指定します。
    　サイズが拡張される場合は、レイヤの表示サイズは変更されませんが、サイズが縮小
    される場合はレイヤの表示サイズも縮小されます。