# DrawDeviceD3D.DrawDeviceD3D

機能/意味
:   コンストラクタ

タイプ
:   [DrawDeviceD3Dクラス](class_DrawDeviceD3D)のメソッド

構文
:   DrawDeviceD3D(width, height)

引数
:   |  |  |
    | --- | --- |
    | width | 描画領域横幅 |
    | width | 描画領域縦幅 |

戻り値
:   なし (void)

説明
:   縦幅と横幅は従来的機構での primaryLayer の width/height に相当するものです。
    作成されたプライマリレイヤ(複数)はすべてここで指定した領域に対して
    引き延ばし表示されます。
    例:
    drawDevice = new DrawDeviceD3D(800,400);
    base1 = new Layer(this, null); base1.setSize(800,400); // 画面と同じ解像度
    base2 = new Layer(this, null); base1.setSize(400,200); // 画面の半分の解像度
    base3 = new Layer(this, null); base1.setSize(800,200); // 縦だけ解像度半分