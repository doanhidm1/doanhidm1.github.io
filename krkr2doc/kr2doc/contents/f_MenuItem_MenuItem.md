# MenuItem.MenuItem

機能/意味
:   MenuItem オブジェクトの構築

タイプ
:   [MenuItemクラス](f_MenuItem)のコンストラクタ

構文
:   MenuItem(window, caption='')

引数
:   |  |  |
    | --- | --- |
    | window | このメニュー項目を作成するウィンドウを指定します。 |
    | caption | メニュー項目のキャプション (表示する文字列) を指定します。  　[MenuItem.caption](f_MenuItem_caption) プロパティで設定/取得できます。 |

戻り値
:   なし (void)

説明
:   MenuItem クラスのオブジェクトを構築します。
    　作成したメニュー項目を親メニュー項目に追加するには、親メニュー項目の
    [MenuItem.add](f_MenuItem_add) メソッドを使います。