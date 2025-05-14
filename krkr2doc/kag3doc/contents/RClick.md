# 右クリックサブルーチンとは

マウスの右クリックで呼び出される KAG のサブルーチンです。
　右クリックによってセーブ/ロードの画面を表示させたりするのに用います。

# とりあえず例

右クリックサブルーチンを作るには rclick タグを用います。このタグによって、右クリックをされたときに指定のサブルーチンを呼び出すか、あるいは、指定のラベルにジャンプするかを指定できます。

　たとえば、rlick.ks に以下の内容を書いたとします。

`例:
*rclick
@rclick jump=true storage="rclick.ks" target="*exit" enabled=true
@current layer=message1
@layopt layer=message0 page=fore visible=false
@layopt layer=message1 page=fore visible=true
@er
ここは右クリックルーチン内です。
[s]

*exit
@layopt layer=message1 page=fore visible=false
@layopt layer=message0 page=fore visible=true
@current layer=message0
@rclick call=true storage="rclick.ks" target="*rclick" enabled=true
@return`

　これで、たとえば、first.ks には以下の行を記述します。

`@rclick call=true storage="rclick.ks" target="*rclick" enabled=true`

　すると、右クリックで rclick.ks の \*rclick が呼ばれるようになります。
　上記の例の rclick.ks では、まず右クリックがされたら \*exit にジャンプするように設定しています。これにより、右クリックサブルーチン内で右クリックを行えば元に戻ることができます。
　メッセージレイヤ0 を非表示にしています。これにより、メッセージレイヤ0 になにか選択肢が表示されていても選択肢を選択できなくすることができます。
　メッセージレイヤ1 を表示状態にし、そこに「ここは右クリックルーチン内です。」と表示し、そこで停止します。

# 難しい例

右クリックサブルーチンとしては複雑な例を挙げますが、メッセージ履歴を見たり、セーブ・ロードができたりするものです。

`例:
*sub1
@tempsave
; ↑一時的に状態を保存
@history output=false
; ↑メッセージ履歴への出力を無効に
@mapdisable layer=0 page=fore
; ↑クリッカブルマップをもし使っている場合はこのようにして無効化する
@backlay
@layopt layer=message1 page=back visible=true
; ↑このサブルーチン内ではメッセージレイヤ1を使う
@layopt layer=message0 page=back visible=false
@current layer=message1 page=back
@position left=0 top=0 width=640 height=480
@eval exp="f.r_first=true"
; ↑このルーチンに入ったときにだけトランジションを行うように
;
*menu
@er
@nowait
[link target=*hide]メッセージを消す[endlink][r]
[link target=*history]メッセージ履歴を見る[endlink][r]
[link target=*load]栞をたどる[endlink][r]
[link target=*save]栞をはさむ[endlink][r]
[link target=*gotostart]最初に戻る[endlink][r]
[link target=*ret]戻る[endlink][r]
@endnowait
@current layer=message1 page=fore
@if exp="f.r_first"
@trans time=500 rule=trans1 vague=128
@wt
@endif
@eval exp="f.r_first=false"
@s

*ret
; サブルーチンから戻る
@tempload bgm=false se=false backlay=true
@trans time=500 rule=trans1 vague=128
@wt
@return

*hide
; メッセージを消す
@hidemessage
@jump target=*menu

*history
; メッセージ履歴を見る
@showhistory
@jump target=*menu

*load
; 栞をたどる
; emb exp= .... については [TJSをもっと使うために](TJSTips) を参照
@er
@nowait
[link target=*lt0][emb exp="kag.getBookMarkPageName(0)"][endlink][r]
[link target=*lt1][emb exp="kag.getBookMarkPageName(1)"][endlink][r]
[link target=*lt2][emb exp="kag.getBookMarkPageName(2)"][endlink][r]
[link target=*lt3][emb exp="kag.getBookMarkPageName(3)"][endlink][r]
[link target=*lt4][emb exp="kag.getBookMarkPageName(4)"][endlink][r]
[link target=*menu]戻る[endlink][r]
@endnowait
@s

*lt0
@load place=0 ask=true
@jump target=*menu
*lt1
@load place=1 ask=true
@jump target=*menu
*lt2
@load place=2 ask=true
@jump target=*menu
*lt3
@load place=3 ask=true
@jump target=*menu
*lt4
@load place=4 ask=true
@jump target=*menu

*save
; 栞をはさむ
; emb exp= .... については [TJSをもっと使うために](TJSTips) を参照
@er
@nowait
[link target=*st0][emb exp="kag.getBookMarkPageName(0)"][endlink][r]
[link target=*st1][emb exp="kag.getBookMarkPageName(1)"][endlink][r]
[link target=*st2][emb exp="kag.getBookMarkPageName(2)"][endlink][r]
[link target=*st3][emb exp="kag.getBookMarkPageName(3)"][endlink][r]
[link target=*st4][emb exp="kag.getBookMarkPageName(4)"][endlink][r]
[link target=*menu]戻る[endlink][r]
@endnowait
@s

*st0
@save place=0 ask=true
@jump target=*menu
*st1
@save place=1 ask=true
@jump target=*menu
*st2
@save place=2 ask=true
@jump target=*menu
*st3
@save place=3 ask=true
@jump target=*menu
*st4
@save place=4 ask=true
@jump target=*menu

*gotostart
; 「最初に戻る」
@gotostart ask=true
@jump target=*menu`

　このほか、栞データにサムネイル画像を保存する場合は若干の注意がありますので locksnapshot と unlocksnapshot タグを参照してください。