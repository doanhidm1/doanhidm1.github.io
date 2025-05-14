# DrawDevice.DrawDevice

機能/意味
:   コンストラクタ

タイプ
:   [DrawDeviceクラス](class_DrawDevice)のメソッド

構文
:   DrawDevice(width, height)

引数
:   |  |  |
    | --- | --- |
    | width | バックバッファ横幅 |
    | width | バックバッファ縦幅 縦幅と横幅は従来的機構での primaryLayer の width/height に相当するものです。 作成されたプライマリレイヤ(複数)はすべてここで指定した領域に対して 引き延ばし表示されます。 例: drawDevice = new Irrlicht.DrawDevice(800,400); base1 = new Layer(this, null); base1.setSize(800,400); // 画面と同じ解像度 base2 = new Layer(this, null); base1.setSize(400,200); // 画面の半分の解像度 base3 = new Layer(this, null); base1.setSize(800,200); // 縦だけ解像度半分  生成した時点では Irrlichtのデバイスは存在しません。 DrawDevice としての描画処理開始時 (SetTargetWindow 呼び出し時)に初期化されて、 ドライバ、シーンマネージャ、GUIが扱えるようになります。 処理は onAttach() イベントを待ってから行う必要があります。 |

戻り値
:   なし (void)

説明