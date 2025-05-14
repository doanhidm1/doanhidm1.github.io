# SimpleDevice.SimpleDevice

機能/意味
:   コンストラクタ

タイプ
:   [SimpleDeviceクラス](class_SimpleDevice)のメソッド

構文
:   SimpleDevice(window, width, height)

引数
:   |  |  |
    | --- | --- |
    | window | 親になるウインドウ |
    | width | バックバッファ横幅。レンダーターゲットを使う場合は 2の階乗サイズにする必要があります。 |
    | height | バックバッファ縦幅。レンダーたーガットを使う場合は 2の階乗サイズにする必要があります。 |
    | useRender | レンダーターゲットを使う場合は true。レンダーターゲットはα透過します。  生成した時点では Irrlichtのデバイスは存在しません。 生成後の最初のイベント処理前に初期化されて、 ドライバ、シーンマネージャ、GUIが扱えるようになります。 処理は onAttach() イベントを待ってから行う必要があります。 |

戻り値
:   なし (void)

説明