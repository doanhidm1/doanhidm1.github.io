# Layer.setPos

機能/意味
:   レイヤ表示位置の設定

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   setPos(left, top, width=void, height=void)

引数
:   |  |  |
    | --- | --- |
    | left | レイヤの ( 親レイヤの表示座標での ) 左端位置をピクセル単位で指定します。  　この値は [Layer.left](f_Layer_left) プロパティでも取得や設定ができます。 |
    | top | レイヤの ( 親レイヤの表示座標での ) 上端位置をピクセル単位で指定します。  　この値は [Layer.top](f_Layer_top) プロパティでも取得や設定ができます。 |
    | width | レイヤの横幅をピクセル単位で指定します。  　この値は [Layer.width](f_Layer_width) プロパティでも取得や設定ができます。  　この引数と height 引数が省略された場合は left 引数と top 引数による位置の変更のみとなります。 |
    | height | レイヤの縦幅をピクセル単位で指定します。  　この値は [Layer.height](f_Layer_height) プロパティでも取得や設定ができます。  　この引数と width 引数が省略された場合は left 引数と top 引数による位置の変更のみと なります。 |

戻り値
:   なし (void)

説明
:   レイヤの表示位置を設定します。