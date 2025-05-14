# バージョン情報ダイアログとは

よくソフトウェアの「ヘルプ - バージョン情報」ででてくるウィンドウです。KAG の場合はこれを KAG のシナリオファイルで書くことができます。
　使用するには、`Config.tjs` の `helpMenu.visible` と `helpAboutMenuItem.visible` をともに true に設定する必要があります。
　また、バージョン情報ダイアログのサイズは `aboutWidth` と `aboutHeight` で指定したサイズになります。
　バージョン情報ダイアログに表示する KAG シナリオファイルは `about.ks` という名前になります。

　通常は、バージョン情報の内容を書いた画像を背景に表示するだけでも十分ですが、作り方によっては凝ったものも作れると思います。

# about.ks の制限

about.ks は通常の KAG シナリオにはない制限があります。
　下に記した以外の制限もあります ( Config.tjs の設定のほとんどに従わない等 )。

BGM、効果音、ビデオなど
:   基本的に使用できますが、効果音バッファの数は 1 つに固定されます。ムービー(AVI や SWF など) は使用できません。

メッセージレイヤ
:   メッセージレイヤの数は 1 つに固定されます。メッセージ履歴は表示できません。メッセージレイヤ0は初期状態で表示されていますが、サイズは不定ですので、非表示にするか、position タグで位置やサイズを指定してから使ってください。

# バージョン情報ダイアログの例

単純に背景に画像を表示するだけの例です。

`@title name="このソフトについて"
@layopt layer=message0 page=fore visible=false
@image storage=about.png layer=base page=fore
@s`

　もうちょっと複雑で、メッセージレイヤに情報をトランジションを使って表示するものです。また、サポートページを link タグで作成したリンクをクリックすることで開くことができるようにしています。また、「閉じる」をクリックするとダイアログを閉じることができるようにしています。

`@title name="このソフトについて"
@rclick enabled=false
@clickskip enabled=false
@position left=0 top=0 width=320 height=200 color=0xffffff opacity=255 marginl=0 margint=0 marginr=0 marginb=0
@style align=center
@font size=24 shadow=false color=0
@wait time=200
@nowait
@backlay
@current page=back
吉里吉里２
[emb exp="System.versionString"]
@trans method=crossfade time=500
@wt
KAG3
[emb exp="kagVersion"]
@trans method=crossfade time=500
@wt
[font size=12]ダウンロードページ
[link hint="クリックするとダウンロードページを開きます" exp="System.shellExecute('http://kikyou.info/tvp/')"]http://kikyou.info/tvp/[endlink]
@trans method=crossfade time=500
@wt
[link target=*exit]閉じる[endlink]
@trans method=crossfade time=500
@wt
@s
*exit
@close`