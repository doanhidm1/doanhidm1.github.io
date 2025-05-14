# 監視式について

監視式は、実行中に Shift + F3 を押すことにより表示することができます。
　監視式では簡単に多くの式の結果を一度に確認することができます。
　また、一定時間ごとに結果の表示を更新させることもできます。
　ちなみに式の結果は変更があったときに自動的に更新されるわけではありません。手動で表示を更新するか、あるいは一定時間ごとに自動的に更新させる必要があります。イベントハンドラ中での変数の変化を追従して表示することもできません。イベントハンドラを実行中に表示更新の時間が来たとしても、すべてのイベントハンドラから吉里吉里本体に制御が戻ったときに表示が更新されます。

# 画面の説明

![ExprWatch.png](ExprWatch.png)

右クリックメニューの説明です。

![NewExprIcon.png](NewExprIcon.png) 新規の式
:   監視式を新しく追加します。

![DeleteIcon.png](DeleteIcon.png) 削除
:   選択されている監視式を削除します。

式の編集
:   選択されている監視式を編集します。

![UpdateIcon.png](UpdateIcon.png) 更新
:   結果を更新します。

![AutoUpdateIcon.png](AutoUpdateIcon.png) 自動更新
:   結果表示を一定時間ごとに自動的に更新しします。

自動更新の間隔
:   自動更新を行う間隔を設定します。

![ControllerIcon.png](ControllerIcon.png) コントローラ
:   [コントローラ](Controller) を表示します。

![ScriptEditorIcon.png](ScriptEditorIcon.png) スクリプトエディタ
:   [スクリプトエディタ](ScriptEditor) を表示します。

![ConsoleIcon.png](ConsoleIcon.png) コンソール
:   [コンソール](Console) を表示します。