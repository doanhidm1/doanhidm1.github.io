# WIN32Dialog.open

機能/意味
:   ダイアログを開く

タイプ
:   [WIN32Dialogクラス](class_WIN32Dialog)のメソッド

構文
:   open(window)

引数
:   |  |  |
    | --- | --- |
    | window | 親ウィンドウ(吉里吉里の Window クラス)，省略時またはvoid時は親なし |

戻り値
:   なし (void)

説明
:   あらかじめ makeTemplate でダイアログテンプレートが生成されているか
    または loadResource でダイアログリソースの読み込んでいること
    makeTemplate より loadResource のデータ優先されるので注意