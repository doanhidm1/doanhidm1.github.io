# TJS2とKAG

TJS ( TJS2 ) は吉里吉里本体が直接理解できるスクリプト言語で、JavaScript や JAVA ににています。KAG はこの TJS スクリプトで記述されています。
　TJS スクリプトは KAG が理解する ( 抽象的な ) シナリオよりもよりシステム側に近い ( 具体的な ) 記述をすることが可能で、扱いは難しくなりますができることの幅はぐっと広がります。

　KAG には eval emb link if タグなどの exp 属性、各タグの cond 属性、エンティティ ( & 付きのタグの属性 ) などなど、「TJS式」を指定する場面がいくつかあります。
　TJS式を使うと、普通は KAG の裏に隠れている 吉里吉里に比較的簡単にアクセスすることができます。
　また、iscript タグは、TJS2 スクリプトを直接実行することができます。これにより、高度な処理を実行したり、KAGの機能を拡張したりすることができます。

　TJS2 の細かい文法については TJS2 のリファレンスを、吉里吉里本体の機能については吉里吉里２のリファレンスをご覧ください。

# KAG のオブジェクト構造

KAG それ自体は TJS2 スクリプトで記述されているため、( 良くも悪くも ) KAG の内部構造に直接アクセスすることができます。
　KAG の管理するオブジェクトの変数に値を書き込む事などは相当注意したほうが良いですが、KAG 内部の変数を参照してより高度なシナリオ記述に応用することもできます。

KAGWindow クラスのオブジェクト
:   KAGWindow クラス ( MainWindow.tjs に記述 ) は、KAG のウィンドウを管理するためのクラスで、このクラスのオブジェクトがグローバル変数の `kag` としてアクセスできます。
    　たとえば、KAGWindow クラスの `skipMode` という変数 ( 現在どのようなモードでスキップ処理中かが入っている変数 ) にアクセスするには `kag.skipMode` とします。

背景レイヤ
:   背景レイヤは BaseLayer クラス ( GraphicLayer.tjs に記述 ) のオブジェクトです。
    　表画面の背景レイヤは `kag.fore.base`、裏画面の背景レイヤは `kag.back.base` でアクセスできます。

前景レイヤ
:   前景レイヤは CharacterLayer クラス ( GraphicLayer.tjs に記述 ) のオブジェクトです。
    　表画面の前景レイヤは `kag.fore.layers[n]`、裏画面の前景レイヤは `kag.back.layers[n]` でアクセスできます ( n は前景レイヤ番号 0 ～ )。

メッセージレイヤ
:   メッセージレイヤは MessageLayer クラス ( MessageLayer.tjs に記述 ) のオブジェクトです。
    　表画面のメッセージレイヤは `kag.fore.messages[n]`、裏画面のメッセージレイヤは `kag.back.messages[n]` でアクセスできます ( n はメッセージレイヤ番号 0 ～ )。
    　`kag.current` は現在操作対象となっているメッセージレイヤを表します。

メッセージレイヤ内のオブジェクト
:   メッセージレイヤ内に作成した、グラフィカルボタン、エディット、チェックボックスなどにアクセスするにはメッセージレイヤの links を使います。
    　links は配列オブジェクトで、リンク、グラフィカルボタン、エディット、チェックボックスなどが作成された順に、それぞれを管理するオブジェクトへの参照が格納されています。そのうち、グラフィカルボタン、エディット、チェックボックス についてはさらにそのなかの object 変数にアクセスすることによって各クラスのオブジェクトに直接アクセスできます。
    　たとえば、表画面のメッセージレイヤ0に以下のような記述があって、

    `@cm
    @edit length=420 name="f.name"`

    　このエディットにフォーカスを設定する ( キーボードから入力できるようにする ) にはさらに

    `@eval exp="kag.fore.messages[0].links[0].object.focus()"`

    　と記述することができます ( エディットを表示してユーザに入力をすぐに促したいときに便利 )。

効果音バッファ
:   効果音バッファは SESoundBuffer クラス ( SE.tjs に記述 ) のオブジェクトです。
    　`kag.se[n]` でアクセスできます ( n は効果音バッファ番号 0 ～ )。

BGM オブジェクト
:   BGM オブジェクトは BGM クラス ( BGM.tjs に記述 ) のオブジェクトです。
    　`kag.bgm` でアクセスできます。

メニュー
:   メニューオブジェクトには `kag.menu` でアクセスできます。`kag.menu` は
    MenuItem クラスのオブジェクトで、`kag.menu` それ自体はメニューバーを
    示しており、その子に登録されたアイテムがメニューバーに並ぶことになります。
    　メニュー項目は Menus.tjs で作成していていますが、Menus.tjs を直接書き換えると
    KAGシステムのアップデートなどでいちいち書き換えなければならなくなるので、後述するように
    AfterInit.tjs を作成してそこに変更点を記述すると楽です。

# TJS を使うときの注意

KAG が栞に保存しない物に直接手を加えると、KAG が栞を読み込んでもそこの部分を再現できません。
　KAG プラグインの onStore や onRestore をフックして栞に情報を保存するようにすれば問題ないのですが、そうしない場合は注意する必要があります。
　特に Layer クラスに属する描画メソッドなどを使って、KAG の管理する背景レイヤや前景レイヤの内容に変更を加える場合などは注意が必要です。KAG は、レイヤにどのような画像が読み込まれていたかまでは記録しますが、レイヤに加えられた描画や変更までは記録しません。ですので、そのような状態で「栞を保存可能なラベル」を通過し、そこで栞を保存し、その栞を読み出しても、レイヤに加えた変更は再現できないことになります。
　このような場合は、次に「栞を保存可能なラベル」を通過するまでに画像をクリアしたり別の画像を読み込むなどして KAG が管理しきれる状態に戻しておくか、あるいは「栞を保存可能なラベル」を書かない、などで回避することができます。
　TJS を使う場合は、栞との関連について十分注意してください。

# 式中の演算や条件判断、表示に使うもの

`&&` と `||`
:   この二つは演算子で、`&&` は「かつ」を表し、`||` は「または」を表します。
    　たとえば、`f.flag1` が 1 で、かつ、`f.flag2` が 2 の場合、という条件で何かをやりたい場合は、

    `[if exp="f.flag1==1 && f.flag2==1"]`

    　と書くことができます。
    　また、f.flag1 が 1 または 2 または 3 の場合、という条件の場合は、

    `[if exp="f.flag1==1 || f.flag1==2 || f.flag1==3"]`

    　と書くことができます ( f.flag1 が整数ならば `f.flag1>=1 && f.flag1<=3` とも書けますが )。
    　普通の数式で足し算よりもかけ算を優先して計算しないとならないように、`&&` と `||` には優先順位に違いがあって、`&&` の方が優先されます。
    　ですので、たとえば `f.flag1` が 1 の場合で、かつ、`f.flag2` が 3 または 5 のとき、という場合は、

    `[if exp="f.flag1==1 && (f.flag2==3 || f.flag2==5)"]`

    　のように ( ) カッコでくくらなければなりません。

`random` と `intrandom`
:   random は 0 以上 1 未満の実数の乱数となります。

    `例:
    @eval exp="f.ransuu = random"`

    　上記の例のようにすると、f.ransuu には 0 以上 1 未満の実数の乱数が入ります。

    　これに対し、intrandom は指定値以上、指定値以下の整数の乱数を返す関数です。

    書式 : `intrandom(最小値, 最大値)`

    `例:
    @eval exp="f.ransuu = intrandom(0, 5)"`

    　上記の例
    のようにすると 0 以上 5 以下の整数の乱数が f.ransuu に入ります。

`length`
:   length は、文字列の長さを得ることのできるものです。使い方は、文字列の代入された変数の後に . (ドット) を書き、続けて length と書きます。

    `例:
    [if exp="f.namae.length>=8"]名前が長すぎます。[l][jump target=*input][endif]`

    　上記の例では、f.namae の長さが8文字以上だった場合に「名前が長すぎます。」と表示し、\*input ラベルにジャンプします。
    　文字は半角、全角問わず、一文字は一文字として数えられます。これは他の文字列を扱う機能でも同じです。

`substring`
:   substring は、文字列の一部分(部分文字列)を取り出すことのできるものです。
    　使い方は、文字列の代入された変数 ( または文字列を表すもの ) のあとに . (ドット) を書き、続けて

    `substring(切り取り開始位置, 切り取る長さ)`

    　の書式で記述します。切り取り開始位置は 0 が先頭を表します。

    　たとえば、f.furigana 変数の２番目の文字を取り出したい場合、`f.furigana.substring(1, 1)` で取り出すことができます。

    `例:
    @emb exp="f.furigana.substring(1, 1)"`

    　上記の例では、f.furigana 変数の２番目の文字を表示します。

`indexOf`
:   indexOf (インデックス・オブ) は、文字列中の部分文字列が最初に現れる位置を得ることができます。使い方をかえれば、ある文字列中に他の文字列が入っているかどうかを調べることができます。

    書式 : `文字列.indexOf(部分文字列)`

    　たとえば、文字列が `"ABCDEFGHIJKL"` で、部分文字列が `"ABC"` であった場合、`"ABCDEFGHIJKL".indexOf("ABC")` は *0* になります。部分文字列が `"BCD"` の場合は *1*、`"DEF"` の場合は *3* になります。
    　もし、部分文字列が文字列中に現れなかった場合は *-1* になりますので、部分文字列が文字列の一部であるかどうかを判定するには -1 と比較すればいいことになります。

    `例:
    [if exp="'尼屁尻'.indexOf(f.objname)!=-1"]～～[endif]`

    　上記例では、`f.objname` が `"尼" "屁" "尻" "尼屁" "屁尻" "尼屁尻"` のいずれかであった場合に `endif` までを実行します。
    　これを、`"尼屁" "屁尻" "尼屁尻"` では NG にしたい場合 ( `"尼" "屁" "尻"` の場合のみ OK にしたい場合 )、`'尼屁尻'`のそれぞれを `f.objname` 内では現れることのない文字(や記号) で区切ることによって実現できます。
    　たとえば、\v という特殊な制御記号をつかって区切ると、上記の例は

    `[if exp="'尼\v屁\v尻'.indexOf(f.objname)!=-1"]～～[endif]`
    とかくことができます ( \v は通常、f.objname 内には現れないから )。

    　下記例では、f.itemname 内に 'コップ' という文字列が含まれている場合に endif までを実行します。

    `例:
    [if exp="f.itemname.indexOf('コップ')!=-1"]～～[endif]`

正規表現
:   正規表現パターン ( / と / で囲まれた部分 ) を使って正規表現パターンによる文字列の分解や検査を行うことができます。
    　正規表現パターンそのものは Perl の正規表現によく似ています ( 使い方は違いますが正規表現パターンはほぼ互換です )。

    　文字列が目的のパターンに適合しているかどうかを調べるには `test` を使います。

    `例:
    [if exp="/[^0-9]/.test(f.nyuryoku)"]入力された文字に数字以外が混じっています[endif]`

    　上記の例のようにして test を使います。test はパターンに合致すると真を、合致しないと偽を返す関数(正規表現オブジェクトのメソッド)です。上記の例では、`[^0-9]` つまり数字以外が混じっているかどうかを検査する正規表現パターンを用いて、`f.nyuryoku` に数字以外の文字が混じっているかを検査しています。

    　文字列を分解するには `match` を使います。`match` は配列オブジェクトを返します。パターンに合致しなかった場合は配列の要素数 ( `count` ) が 0 になります。それ以外の場合、要素 0 はマッチした部分全体、要素 1 からあとはパターン中の ( ) (カッコ) に対応してマッチした部分が返されます。

    `例:
    [eval exp="f.matched = /([0-9０-９]+)[-－]([0-9０-９]+)/.match(f.input)"]
    [if exp="f.matched.count == 0"]「数値-数値」の形式で入力してください。[jump target=*input][endif]
    [eval exp="f.s1 = str2num(f.matched[1]), f.s2 = str2num(f.matched[2])"]`

    　上記の例では、`f.input` が「数値-数値」の形式に合致しているかをテストして、合致していれば - (ハイフン) の前の部分の `f.s1` に、後の部分を `f.s2` に、数値に変換してから代入しています。

`str2num`
:   str2num は、文字列を数値に変換します。

    書式 : `str2num(文字列または文字列の入った変数)`

    　単項の `+` 演算子と違うのは、`str2num` は、全角の数字であっても数値に変換できるということです。input タグのように、ユーザが全角で数値を入力してしまう可能性のある場合に使用できると思います。数値として認識できない文字列が渡された場合は 0 になります。

    `例:
    [input name="f.kazu" prompt="数値を入力してください"][emb exp="f.kazu=str2num(f.kazu)"]`

`kansuuji` と `kansuuji_simple`
:   `kansuuji` は、指定された数値を漢数字表記にします。`kansuuji_simple` も同様ですが、桁を表す単位をつけません。
    　9223372036854775807 という数値を、`kansuuji` の場合は "九百二十二京三千三百七十二兆三百六十八億五千四百七十七万五千八百七" に、`kansuuji_simple` の場合は "九二二三三七二〇三六八五四七七五八〇七" に変換します。

    `例:
    @emb exp="kansuuji(f.num)"`

    　上記の例では、f.num を漢数字表記にして表示しています。

`number_format`
:   `number_format` は、指定された数値を3桁ごとに , (カンマ) で区切った表記にします。たとえば、9223372036854775807 という数値ならば "9,223,372,036,854,775,807" に変換されます。

    `例:
    @emb exp="number_format(f.num)"`

    　上記の例では、f.num を 3桁ごとにカンマで区切って表示しています。

`Storages.addAutoPath と System.exePath`
:   Storages.addAutoPath は、自動検索パスを追加します。
    　System.exePath は、吉里吉里実行可能ファイルの設置されているフォルダを示します。
    　詳しくは吉里吉里 SDK Help を参照していただきたいのですが、これらを使うとアーカイブやフォルダに自動検索パスを設定できます。
    　自動検索パスは、わざわざフォルダを指定しなくても、ファイルを自動的に見つけてくるための仕組みです。標準では、system image scenario bgimage fgimage bgm sound rule others video のすべてが設定されていますが、Storages.addAutoPath で追加することができます。
    System.exePath は、吉里吉里実行可能ファイルのあるフォルダです。

    　たとえば、吉里吉里実行可能ファイルの直下に cgdata というフォルダがあって、そこの中を自動検索パスに指定したい場合は、

    `[eval exp="Storages.addAutoPath(System.exePath + 'cgdata/')"]`

    　とします ( cgdata の後の二つの / は必ずつけてください )。

    　もし、吉里吉里実行可能ファイルと同じ場所に cgdata.xp3 というアーカイブファイルがあって、このアーカイブ内に自動検索パスを指定したい場合は、

    `[eval exp="Storages.addAutoPath(System.exePath + 'cgdata.xp3>')"]`

    　とします。cgdata.xp3 の後の記号は '>' です。アーカイブ内に検索パスを指定する場合は > で、フォルダ内に検索パスを指定する場合は / です。
    　アーカイブの後の記号は 吉里吉里２ 2.19 beta 14 で '#' から '>' に変更となりました。

`Storages.searchCD`
:   Storages.searchCD は、引数に渡されたボリュームラベルを持つ CD が挿入されたドライブの文字を返します。
    　たとえば、上記 Storages.addAutoPath と組み合わせて、FOO\_BAR\_DISC というボリュームラベルを持つ CD-ROM 内の image というフォルダに自動検索パスを追加したい場合、

    `[eval exp="Storages.addAutoPath(Storages.searchCD('FOO_BAR_DISC') + ':image/')"]`

    　と記述することができます。

    　Stotages.searchCD は、指定されたボリュームラベルを持つ CD が挿入されたドライブが見つからない場合は空文字列を返すので、たとえば指定の CD-ROM がドライブに挿入されていることを確認するために、

    `[if exp="Storages.searchCD('FOO_BAR_DISC') == ''"]CDが挿入されていません[endif]`

    　のように記述することができます。

`System.readRegValue`
:   System.readRegValue では、レジストリに書き込まれた値を読むことができます。たとえば、HKEY\_LOCAL\_MACHINE\SOFTWARE\Dee\kirikiri\installpath を f.installpath に読み込むには、

    `[eval exp="f.installpath = System.readRegValue('HKEY_LOCAL_MACHINE\\SOFTWARE\\Dee\\kirikiri\\installpath')"]`
    　とします。'' で囲まれた中では \ は \\ と記述しなければならないことに注意してください。
    　文字列と数値の値のみを読むことができます。レジストリに値が存在しない場合は void になるので、`===` (識別演算子) を用いて

    `[if exp="f.installpath === void"]インストールされていません[endif]`

    　のような記述をすることができます。

`kag.clickCount`
:   画面上をマウスでクリックするたびに 1 が加算されます。この変数には値を代入してもかまいませんので、0 に設定しておけば、マウスがクリックされたことを、この変数が 0 以外の数値になっていることで知ることができます。

`kag.lastMouseDownX と kag.lastMouseDownY`
:   これらは、最後にマウスがクリックされた座標を表しています。kag.lastMouseDownX は最後にクリックされた X 座標、kag.lastMouseDownY は最後にクリックされた Y 座標です。

`kag.lastWaitTime`
:   wait タグを mode=until で使用したとき、実際に wait タグがまとうとした時間が設定されます。すでにまとうとしていた時間が過ぎていた場合は 0 になりますので、wait タグの直後でこの変数が 0 でないかどうかを判断すれば、処理が追いついているかどうかを判断することができます。
    　ちなみに、クリックなどで wait が中断された場合は、この変数は正確に待っていた時間を表す訳ではありません ( 中断がなかったとした場合の時間を表しています )。

`kag.skipMode`
:   現在のスキップのモードを表す値が入っています。0=スキップなし, 1=クリック待ち記号まで, 2=改ページ待ち記号まで, 3=次の停止まで、となっています。
    　たとえば、声や効果音などをスキップ中には再生したくない場合は、

    `@playse cond="kag.skipMode<=1" storage="hogehoeg.wav"`

    　のように記述することができます。

`kag.autoMode`
:   自動読みすすみの処理中の時に真、それ以外の時に偽になっています。
    　たとえば、声や効果音などの終了を、自動読みすすみの時のみに処理したい場合は、

    `@ws cond="kag.autoMode"`

    　のように記述することができます。

`kag.getBookMarkPageName`
:   `kag.getBookMarkPageName` は、非フリーセーブモードにおいて、引数に指定された番号 ( 0 ～ ) で示された、栞の場所の名前を得ることが出来ます。
    　KAG のメニューからではなく、画面上で栞を示してユーザーにたどる栞を選ばせたいときに使うことが出来ます。
    　`kag.restoreBookMark` と組み合わせて使います。

    `例:
    [locate x=10 y=100][link exp="kag.restoreBookMark(0)"][emb exp="kag.getBookMarkPageName(0)"][endlink]
    [locate x=10 y=130][link exp="kag.restoreBookMark(1)"][emb exp="kag.getBookMarkPageName(1)"][endlink]
    (以下同様)`

`mp`
:   `mp` は、マクロ中にて、マクロに渡された属性が記録された辞書配列を表します。

    `例:
    @macro name=fimg
    @image *
    @eval exp="sf[mp.storage]=1"
    @endmacro`

    　上記の例では、たとえば `@fimg layer=base page=fore storage="bg_03"` と記述された場合、このマクロが実行されている間は `mp.layer` は `'base'`、`mp.page` は `'fore'`、`'mp.storage'` は `'bg_03'` になっています。つまり、マクロに渡された属性を `mp.` の後に指定することによって、その属性の値を得ることができます。
    　このマクロを `@fimg layer=base page=fore storage="bg_03"` として使用した場合、exp タグで `sf[mp.storage]=1` が実行されるため、`sf['bg_03']` が 1 になります。
    　このマクロは、image/img タグの代わりに使うことにより、表示した画像を自動的にシステム変数に記録するマクロとして使用することができます。

`System.getKeyState`
:   `System.getKeyState` は、現在その時点で、指定されたキーが押されているかどうかを判断することができます。

    `例:
    @jump target=*shift_key_pressed cond="System.getKeyState(VK_SHIFT)"
    ; シフトキーが押されていれば、*shift_key_pressed にジャンプする`

    詳しくは吉里吉里２ SDK Help を参照してください。

    　KAG3はゲームパッド(ジョイスティック)からの入力を受け付けますが、ゲームバッドの上に物が乗っかっている、あるいはジョイスティックの軸の調整が不十分という場合には、正常に作品の操作をできない場合があります。
    　作品開始時にゲームパッドのボタンが押されていれば、ユーザに対して警告をすることができます (通常、作品開始時にゲームパッドのボタンが押されていることはなく、押されているとなれば、ユーザの意図しない理由で押されたままになっている可能性が高いため)。
    　USB接続のゲームパッドなどでは下記の例では「押されっぱなし」の検出がうまくいかないかもしれませんので、適宜ドキュメントなどでの補足を推奨します。

    `例:
    @if exp="System.getKeyState(VK_PADANY)"
    @wait time=500
    @if exp="System.getKeyState(VK_PADANY)"
    ; VK_PADANYでは、ゲームパッドのいずれかのボタンが押されている時に真を返す
    ; 500ms(0.5秒間)をすぎてもなお押されているようならばメッセージを表示
    ゲームパッド(ジョイスティック)のボタンが押されたままになっています。
    ゲームパッドの上に物が乗っかっていないか、あるいはジョイスティックの
    軸の調整がされているかを確認してください。
    状況が改善しない場合は、ゲームパッド(ジョイスティック)を抜いてください。
    それでも状況が改善しなければ、ゲームを終了し、「エンジン設定」を起動し、
    「入力-パッド使用可否」の設定を「使用しない」に設定してください。
    [s]
    @endif
    @endif`

# リンクやボタンの exp 属性などに指定するもの

`System.shellExecute`
:   System.shellExecute は、引数に指定されたファイルを開きます。URL を指定するとブラウザが開くので、link タグなどを使ってこの式を実行させれば、Web ページへのリンクなどを作成することが出来ます。

    `例:
    [link exp="System.shellExecute('http://www.yahoo.co.jp/')"]http://www.yahoo.co.jp/[endlink]`

`kag.close` と `kag.shutdown`
:   kag.close は、KAG を終了させます。終了確認を行う設定にしている場合は終了確認があります。
    　kag.shutdown も KAG を終了させますが、終了確認はありません。
    　なお、終了に System.exit() を使用すると、システム変数が保存されずに終了される場合があるので*使用しないでください*。また、これらは eval タグの exp 属性では指定しないでください (代わりに close タグを使用してください)。

    `例:
    [link exp="kag.close()"]終了[endlink]
    [link exp="kag.shutdown()"]終了[endlink]`

`kag.restoreBookMark` と `kag.storeBookMark`
:   kag.restoreBookMark は、非フリーセーブモードにおいて、引数に指定された番号で示された栞をたどります。
    　同様に、kag.storeBookMark は、引数に指定された番号で示された栞を挟みます。
    　ただし、これを直接呼び出すと、[store] タグで栞の使用が禁止されていても栞の操作が出来てしまいます。
    　これらは、成功すると真を、失敗すると偽を返します。
    　例は kag.getBookMarkPageName の物を参照してください。

`kag.loadBookMarkFromFileWithAsk` と `kag.saveBookMarkToFileWithAsk`
:   kag.loadBookMarkFromFileWithAsk は、フリーセーブモードにおいて、ファイル選択ダイアログボックスを表示し、ユーザに栞データを選択させます。ユーザが OK ボタンを押すとその栞から再開します。
    　同様に、kag.saveBookMarkToFileWithAsk は、ファイル選択ダイアログボックスを表示し、栞を保存します。
    　これらは、成功すると真を、ユーザがキャンセルをするか、あるいは失敗すると偽を返します。

    `例:
    [link exp="kag.loadBookMarkFromFileWithAsk()"]栞をたどる[endlink]
    [link exp="kag.saveBookMarkToFileWithAsk()"]栞をはさむ[endlink]`

`kag.callExtraConductor`
:   kag.callExtraConductor は、TJS の制御によって KAG のシナリオをサブルーチンとして呼び出すために用います。このメソッドでシナリオを呼び出すときは、シナリオがクリック待ちや s タグで停止中である必要があります ( kag.inStable や KAG プラグインの onStableStateChanged で知ることができます )。
    　kag.callExtraConductor には引数が３つあります。
    　最初の引数は呼び出すシナリオファイルです。次の引数は呼び出すラベルです。
    　３番目の引数は省略可能ですが、KAG のシナリオから戻ったときに実行する関数/メソッドを指定します。必要ない場合は指定しなくてかまいません。

    `例:
    [button graphic="showhist" exp="kag.callExtraConductor('rclick.ks', '*showhist')"]`

    　これで呼び出すサブルーチンの書き方は、右クリックサブルーチンの書き方に準じます。
    　右クリックサブルーチン中や、すでにこの機能を使って KAG のシナリオを呼び出している最中では、この機能は使用できません。

`kag.se[n].play`
:   効果音バッファの play メソッドは、効果音の再生を開始します。
    　以下の形式で指定します。

    `kag.se[効果音バッファ番号].play(%[storage: 再生する効果音のファイル名, loop: ループするか]);`

    　これをたとえば、以下の例のように link タグの onenter 属性に指定すれば、選択肢の上にマウスカーソルが乗ったときに効果音を発音することができます。

    `例:
    [link target=*foo onenter="kag.se[0].play(%[storage:'select.wav', loop: false])"]選択肢～[endlink]`

    　この例では、効果音バッファ 0 番で select.wav を、ループをせずに再生します。他にも TJS の制御で効果音を鳴らしたいときに便利です。

# 配列

吉里吉里２/KAG3 では配列を簡単に使うことができます。
　配列を使う場合は、最初に `[ ]` を使って配列を宣言しないとなりません。

`例:
[eval exp="f.hairetsu = []"]`

　上記の例では、`f.hairetsu` を配列として使うことを宣言しています。もしすでに `f.hairetsu` が配列だったり、他の数値とか文字列であったとすると `f.hairetsu` の内容は消去されてしまいますので注意してください。
　システム変数などで配列を使いたい場合は、初期状態では変数はすべて void が代入されていると見なされることを利用して、

`例:
[eval exp="sf.hairetsu = [] if sf.hairetsu === void"]`

　とすれば、初回起動時だけ配列を宣言することができます。２回目以降でも配列が消去されることはありません。

　配列に値を代入するには `[ ]` を使います。`[ ]` 内には添え字 ( 要素番号 ) を書きます。添え字は 0 から始まります。

`例:
[eval exp="f.hairetsu[0] = 'zero', f.hairetsu[1] = 'one'"]`

　上記の例では `f.hairetsu[0]` に 'zero' を、`f.hairetsu[1]` に 'one' を代入しています。
　配列の要素数は宣言する必要はありません。必要な大きさまで自動的に拡張されます。配列の要素数を得たり設定したりするには `count` プロパティを用いて `f.hairetsu.count` などとします。

　表示も同様に行えます。

`例:
0 : [emb exp="f.hairetsu[0]"]    1 : [emb exp="f.hairetsu[1]"]`

　２次元配列を用いるのはすこし難しいですが、例だけ挙げておきます。

`@iscript
// １次元目の要素数が 5 の２次元配列を作成する
f.twodim = [] if f.twodim === void; // twodim に１次元目の配列を作成
for(var i = 0; i < 5; i++) f.twodim[i] = [] if f.twodim[i] === void;
// この状態で f.twodim[0] ～ f.twodim[4] がそれぞれ配列なので
// f.twodim[0][3] や f.twodim[4][2] などと指定できる
@endscript

// あるいは、単純にたとえば１次元目の要素数が5の配列を作成するならば
f.twodim = [ [], [], [], [], [] ];
// ( 配列を [] で作成するときにその中に初期要素をカンマで区切って指定できるが、
//   そのときに初期要素として配列を入れ子に指定する )`

# 辞書配列

吉里吉里２/KAG3 では辞書配列も使うことができます。
　辞書配列 ( 連想配列とも呼びます ) とは、名前と、それに対応する値の組を覚えることのできる配列です。
　辞書配列を使う場合は、配列と同じように、最初に `%[ ]` を使って配列を宣言しないとなりません。

`例:
[eval exp="f.dict = %[]"]`

　上記の例では、f.dict を辞書配列として使うことを宣言しています。もしすでに f.hairetsu が辞書配列だったりしたばあいの注意は配列と同じです。

　辞書配列に値を代入するにも `[ ]` を使います ( `%[ ]` ではありません )。`[ ]` 内には「名前」となるものを書きます。

`例:
[eval exp="f.dict['zero'] = 0, f.dict['one'] = 1"]`

　上記の例では `f.dict['zero']` に `0` を、`f.dict['one']` に `1` を代入しています。普通の配列と違うのは文字列を `[ ]` 内に指定することです。

　表示も同様に行えます。

`例:
zero : [emb exp="f.dict['zero']"]    one : [emb exp="f.dict['one']"]`

　ちなみに `[ ]` ではなく `.` を使うこともできます。`f.dict['zero']` は `f.dict.zero` 、`f.dict['one']` は `f.dict.one` と記述することができます ( ただし . の次には「予約語」や「変数名として使えない名前」が来ることはできません )。

　実は KAG の `f` や `sf` といったもの自体も辞書配列で、`f.dict` としたばあいは、辞書配列の中の `'dict'` という名前のついた値にアクセスしていたことになります ( もちろん、`f['dict']` でもアクセスできます )。

# 日付/時刻を得る

現在の日付や時刻を得るには以下のようにします。

`[iscript]
{
    // ↑  endscript の中を {  } で囲むのは この中で宣言された変数を
    // ローカル変数にするため ( そうしないとグローバル変数になる )
    var d = new Date(); // Date クラスのオブジェクトを作成
    // Date クラスのオブジェクトは、作成時に引数に何も指定しなければ
    // 作成時点の現在時刻を保持している
    f.year = d.getYear();  // f.year に 年
    f.month = d.getMonth() + 1; // f.month に 月
    f.date = d.getDate(); // f.date に 日
    f.hours = d.getHours(); // f.hours に 時
    f.minutes = d.getMinutes(); // f.minutes に 分
    f.seconds = d.getSeconds(); // f.seconds に 秒
}
[endscript]`

# process

`kag.process` は、シナリオを指定した位置から実行します。
　最初の引数は読み込むシナリオファイル名です。空文字列を指定すると現在のシナリオファイルが使用されます。
　２番目の引数は、実行を開始するラベルです。空文字列を指定するとシナリオファイルの先頭から実行します。

`例:
kag.process('', '*label2')
kag.process('scenario4.ks', '*label5')`

　たとえシナリオが実行中であろうとも、強制的にそのラベルに飛ぶので注意してください。

# leftClickHook, rightClickHook, keyDownHook

KAG は、左クリックされたとき、右クリックされたとき、キーが押されたときのそれぞれの場合に、登録した関数を呼び出す機能があり、フックと呼んでいます。
　フックは、複数の関数を登録できるように配列になっています。それぞれ `kag.leftClickHook`、`kag.rightClickHook`、`kag.keyDownHook` でアクセスできるようになっています。
　これらに登録した関数で true が返されると、KAG はもともとその機能に割り当てられていた機能を実行しません。たとえば、R キーが押されたとき、keyDownHook に登録された関数が true を返すと、元々の機能である「メッセージ履歴を表示する」の機能は実行されなくなります。

　leftClickHook と rightClickHook には、呼び出される関数に引数はありません。
　leftClickHook は、Enter キーや Space キー等でも発生します。また、マウスで選択肢などをクリックしたときには発生しません。

`例:
@iscript
function myLeftClickHook()
{
    kag.process('', '*label');
    return true;
}
@endscript
@eval exp="kag.leftClickHook.add(myLeftClickHook)"
@s

*label
@eval exp="kag.leftClickHook.remove(myLeftClickHook)"
やあー。
@s`

　上記の例では、クリックされると \*label が実行されます。
　強制的に実行が \*label に移るので注意してください。トランジションや自動移動を実行中等の場合は stoptrans や stopmove タグで実行を停止したほうが安全です。

　keyDownHook は、呼び出される関数には２つ引数が渡されて、一つ目は押されたキーの仮想キーコード、二つ目はそのキーが押されていたときに同時に押されていたシフト系のキーの状態です。詳しくは吉里吉里２ SDK Help を参照してください。

`例:
@iscript
function myKeyDownHook(key, shift)
{
    if(key == #'R')
    {
        // R のキーが押されたら
        kag.process('', '*label');
        return true;
    }
}
@endscript
@eval exp="kag.keyDownHook.add(myKeyDownHook)"
@s

*label
@eval exp="kag.keyDownHook.remove(myKeyDownHook)"
やあー。
@s`

# touchImages

`System.touchImages` は、画像をキャッシュに読み込みます。
　詳しくは 吉里吉里２ドキュメントの System.touchImages をご覧ください。このメソッドは、たとえばなにかのウェイトで時間があいたときを利用して、画像を先読みしておく用途に使えます。
　KAG で使う場合は、前景、背景画像 ( ただし key 属性を指定しないものに限る ) に対して有効です。image や img タグの storage 属性に指定するものと同じ物を storages 引数に配列にして指定してください。
　第２引数は -2\*1024\*1024 あたりを指定しておくと良いようです。
　第３引数には、待つ時間 - 200ms あたりを指定しておくと良いようです。

`例:
@resetwait
@eval exp="System.touchImages(['24_5', '24_4', 'uni', '24'], -2*1024*1024, 800)"
@wait mode=until time=1000`

　ただし、このメソッドは、画像がキャッシュに入るということは保証しないという、不確定的なものです。ですから、絶対に画像を先に読んでおかなければいけない用途には使うべきではありません。そのような用途には後述の assignImages の項で説明する方法を使う方が確実です。

# assignImages

`assignImages` は、レイヤの画像を他のレイヤにコピーします。
　たとえば、

`@eval exp="kag.fore.base.assignImages(kag.fore.layers[0])"`

　とすれば、表前景レイヤ 0 に読み込まれている画像を表背景レイヤにコピーすることができます。
　assignImages は実際には画像のデータをコピーはせず、「コピー元とコピー先の画像が同じになった」という印を付けるだけなので高速です。デモシーンなどで、シーンの途中で画像を読み込むときのタイムロスが問題になるような場合に、あらかじめ画像を非表示の前景レイヤなどに読み込んでおいてから、必要なときに背景レイヤなどにコピーする用途に使えます。

# hact タグの応用

hact タグはメッセージ履歴をクリックしたときに任意の TJS 式を実行できるようにするもので、音声履歴 ( 声つきのゲームなどでメッセージ履歴をクリックしたときにそのメッセージに対応する音声を再生できるようにするもの ) を実装することができます。
　以下は、それを実現するための例で、音声を再生するためのマクロ pv と、音声を停止するためのマクロ sv を定義するものです。

`例:
@iscript
function stopAllVoices()
{
    // 2 ～ 6 のすべての効果音を停止する
    for(var i = 2; i <= 6; i++) kag.se[i].stop();
}
function playVoice(buf, storage)
{
    // 効果音バッファ buf にて storage を再生する
    // KAG がスキップ処理中の場合は処理を行わない
    if(!kag.skipMode)
    {
        stopAllVoices();
        kag.se[buf].play(%[ storage : storage ]);
    }
}
function createHistoryActionExp(buf, storage)
{
    // メッセージ履歴をクリックしたときに実行する TJS 式を生成する
    return "stopAllVoices(), kag.se[" + buf  +"].play(%[ storage : '" + storage + "' ])";
}
@endscript
@macro name=pv
@hact exp="&createHistoryActionExp(mp.b, mp.s)"
@eval exp="playVoice(mp.b, mp.s)"
@endmacro
@macro name=waitvoices
@ws buf=2
@ws buf=3
@ws buf=4
@ws buf=5
@ws buf=6
@endmacro
@macro name=sv
@endhact
@waitvoices cond="kag.autoMode"
@eval exp="stopAllVoices()"
@endmacro`

　createHistoryActionExp 関数では、hact タグの exp 属性に渡すための TJS 式を生成しています。ここで生成した TJS 式が実行されることになります。

　このマクロを使った例は以下のようになります。

`例:
[pv b=2 s=hoge.ogg]ほげ[l][sv][r]
[pv b=3 s=hogera.ogg]ほげら[l][sv][r]
[pv b=4 s=hogemoge.ogg]ほげもげ[p][sv]`

# 初期化時に実行されるスクリプト

KAG はシステムのカスタマイズのために、初期化のいくつかの段階において 任意の TJS スクリプトを実行する機能があります。現バージョンでは以下の方法が用意されています。

Override.tjs
:   このファイルは MainWindow.tjs が読み込まれた後に、もし存在すれば実行されます。初期状態ではこのファイルは存在しないので、新しく作成してください。

AfterInit.tjs
:   すべての初期化が終わり、 first.ks が実行される直前に実行されます。このファイルも初期状態では存在しないので、新しく作成してください。

「追加の設定」
:   Config.tjs 内には、いくつか「◆ ウィンドウや動作の追加の設定」など、「追加の設定」を記述できるところがあります。そこに記述した内容は Config.tjs の実行される各段階で実行されます。

# メニューのカスタマイズ

メニュー項目に、たとえば、単純な on/off だけの設定項目を追加するには、AfterInit.tjs に以下のような内容を書きます。

`例:
kag.menu.insert(kag.optionsMenu =
    new KAGMenuItem(this, "効果(&G)", 0, void, false), 2);
kag.optionsMenu.stopRecur = true;

kag.optionsMenu.add(
    kag.doTransMenuItem = new KAGMenuItem(
        this,
        "画面切り替えを行う(&T)",
        0,
        function(sender) { sf.dotrans = sender.checked = !sf.dotrans; },
        false));

if(sf.dotrans === void) sf.dotrans = true;
kag.doTransMenuItem.checked = sf.dotrans;

kag.optionsMenu.add(
    kag.playSEItem = new KAGMenuItem(
        this,
        "効果音を再生する(&S)",
        0,
        function(sender) { sf.playse = sender.checked = !sf.playse; },
        false));

if(sf.playse === void) sf.playse = true;
kag.playSEItem.checked = sf.playse;`

　`kag.menu.insert(kag.optionsMenu = new KAGMenuItem(this, "効果(&G)", 0, void, false), 2);` では、KAG のメニューバーに「効果」メニューを挿入しています。kag.optionMenu がその「効果」メニューのオブジェクトになります。insert メソッドの第２引数は、メニュー項目を挿入する位置です。
　次の行ではそのオブジェクトの stopRecur を true に設定していますが、これは kag.internalSetMenuAccessibleAll で不必要なメニューアイテムの検索を行わないようにするためです。

　その kag.optioneMenu に、add メソッドで子のメニュー項目を作成しています。

　KAGMenuItem の第４引数は、メニューアイテムがクリックされたときに実行する式を指定します。

　`if(sf.dotrans === void) sf.dotrans = true;` では、sf.dotrans が void ( つまり、何も値が無い状態 ) の時に、初期値を入れています。`kag.doTransMenuItem.checked = sf.dotrans;` では、メニューアイテムのチェックの初期状態を設定しています。システム変数に記録しているため、プログラムを終了しても次回に設定が引き継がれます。

　あとは sf.dotrans や sf.playse に現在のメニューの状態が記録されているので、

`@playse storage="kon.wav" cond="sf.playse"`
　のようにして使用することができます。

　応用でいろいろできると思います。

# KAG用プラグインを書く

KAGPlugin クラス のサブクラスを作り、KAG に登録することで KAG の機能を拡張するプラグインを作ることができます。
　サンプルが KAG の配布ファイルとともに配布されていると思うので参照してみてください。