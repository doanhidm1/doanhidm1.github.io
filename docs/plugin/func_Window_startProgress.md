# Window.startProgress

機能/意味
:   プログレス処理を開始する。 吉里吉里が実行ブロック中でも正常に表示継続します。

タイプ
:   [Windowクラス](class_Window)のメソッド

構文
:   startProgress(init)

引数
:   |  |  |
    | --- | --- |
    | init | 初期化データ(辞書) |

戻り値
:   なし (void)

説明
:   プログレスバー初期化パラメータ
    progressBarEnable: プログレスバーを表示するかどうか(デフォルト:true)
    progressBarStyle: プログレスバーのスタイル (デフォルト:なし)
    progressBarLeft: プログレスバー表示位置X (デフォルト:自動センタリング)
    progressBarTop: プログレスバー表示位置Y (デフォルト:自動センタリング)
    progressBarWidth: プログレスバー横幅 (デフォルト:ウインドウ横幅の 1/3)
    progressBarHeight: プログレスバー縦幅 (デフォルト:ウインドウ縦幅の 1/10)
    progressBarColor: プログレスバー色 0xRRGGBB (デフォルト:デフォルト色)
    progressBarBackColor: プログレスバー背景色 0xRRGGBB (デフォルト:デフォルト色)

    キャンセルボタン初期化パラメータ
    cancelButtonEnable: キャンセルボタンを表示するかどうか(デフォルト:true)
    cancelButtonCaption: キャンセルボタンに表示するテキスト(デフォルト:Cancel)
    cancelButtonLeft: キャンセルボタン表示位置X (デフォルト:自動センタリング)
    cancelButtonTop: キャンセルボタン表示位置Y (デフォルト:下から heightの３倍の位置)
    cancelButtonWidth: キャンセルボタン横幅 (デフォルト:テキスト文字数\*12+8)
    cancelButtonHeight: キャンセルボタン縦幅 (デフォルト:20)

    背景画像初期化パラメータ(未実装)
    backGround: 背景指定 レイヤ：レイヤの画像を直接参照 数値:該当色で塗りつぶし デフォルト:なし

    メッセージ初期化パラメータ(未実装)
    messages: メッセージ情報またはその配列
    left: 表示座標X
    top: 表示座標Y
    text: 初期表示テキスト
    size: 表示サイズ
    color: 表示カラー
    shadowColor: 影色
    shadowDistanceX: 影のずれ指定
    shadowDistanceY: 影のずれ指定
    font: フォント指定
    fontStyle: フォントスタイル