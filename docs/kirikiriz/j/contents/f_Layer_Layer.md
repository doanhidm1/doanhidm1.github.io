# Layer.Layer

機能/意味
:   Layer オブジェクトの構築

タイプ
:   [Layerクラス](f_Layer)のコンストラクタ

構文
:   Layer(window, parent)

引数
:   |  |  |
    | --- | --- |
    | window | このレイヤを保有することになるウィンドウ ( [Window](f_Window) クラスの オブジェクト ) を指定します。  　ウィンドウはいったん決定したら変更することはできません。 |
    | parent | このレイヤの親となるレイヤを指定します。  　null を指定するとプライマリレイヤになります。  　プライマリレイヤはウィンドウに一つのみ存在することができ、また、レイヤを用いる場合は かならず一つ存在しなければならない、すべてのレイヤの親となるレイヤです。  　ただし、描画デバイス ( [Window.drawDevice](f_Window_drawDevice) で設定可能) によっては、ウィンドウが 複数のプライマリレイヤを持つことができる物があります。  　レイヤの親は、[Layer.parent](f_Layer_parent) プロパティで変更することができます。 |

戻り値
:   なし (void)

説明
:   Layer クラスのオブジェクトを構築します。
    　Layer クラスは非表示の状態で構築されます。