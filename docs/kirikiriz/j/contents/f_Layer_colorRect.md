# Layer.colorRect

機能/意味
:   矩形半透明塗りつぶし

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   colorRect(left, top, width, height, value, opa=255)

引数
:   |  |  |
    | --- | --- |
    | left | 塗りつぶす矩形の左端位置を ( 画像位置における ) ピクセル単位で指定します。 |
    | top | 塗りつぶす矩形の上端位置を ( 画像位置における ) ピクセル単位で指定します。 |
    | width | 塗りつぶす矩形の横幅を ( 画像位置における ) ピクセル単位で指定します。 |
    | height | 塗りつぶす矩形の縦幅を ( 画像位置における ) ピクセル単位で指定します。 |
    | value | 塗りつぶす色や値を指定します。  　この値は、[Layer.face](f_Layer_face) プロパティの値によって意味が変わります。  dfAlpha (またはdfBoth)  : 0xRRGGBB 形式で色を指定してください  dfAddAlpha  : 0xRRGGBB 形式で色を指定してください  dfOpaque (またはdfMain)  : 0xRRGGBB 形式で色を指定してください  dfMask  : マスク(不透明度)の値 ( 0 ～ 255 ) を指定してください  dfProvince  : 領域の値 ( 0 ～ 255 ) を指定してください  　dfOpaque を指定した場合は、マスク情報は無視されます(マスク情報が保持されるか破壊されるかは [Layer.holdAlpha](f_Layer_holdAlpha) プロパティによります)。また、dfMask を指定した場合は、色の情報はそのままになります。  　dfAlpha の場合でかつ opa が負の場合はこの引数は無視されます。 |
    | opa | 塗りつぶす不透明度 ( -255 ～ 0 ～ 255 ) を指定します。  　この引数は、[Layer.face](f_Layer_face) プロパティの値が dfMask や dfProvince の場合は無視されます ( 常に完全不透明 )。  　負の数の指定は [Layer.face](f_Layer_face) が dfAlpha の場合のみに有効で、 この場合は value 引数は無視され、画像から不透明度が取り除かれます ( -255 を指定すると矩形は完全に透明になります )。 |

戻り値
:   なし (void)

説明
:   指定されたレイヤ画像の矩形を指定された方法で塗りつぶします。
    　[Layer.fillRect](f_Layer_fillRect) と異なり、透明度を指定して半透明で塗りつぶすことができます。