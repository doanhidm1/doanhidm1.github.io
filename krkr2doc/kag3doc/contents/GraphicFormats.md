# 各画像形式の特徴

吉里吉里/KAG はいろいろな画像形式を使うことができますが、それぞれ特徴があります。

BMP 画像
:   吉里吉里では、無圧縮の BMP のみサポートしています。吉里吉里で使う BMP は RLE 圧縮できませんし、配布するときに圧縮をしようとしてもあまり圧縮率があがらないので、容量という点では大きくなりますが、読み込みが一番高速です。

JPEG 画像
:   JPEG は、(普通は) 不可逆圧縮という圧縮の方法を行います。その特性上、いったん圧縮すると展開しても完全に元の画像に戻りません。具体的には画像のシャープさが失われ、画像の輪郭や鋭いエッジの周りにゴミが出ます。しかし、圧縮率がよく、写真取り込みや風景画などの自然画像では不可逆圧縮の特性によるゴミなどはほとんど目立たないので、背景画像や一枚絵に向いています。前景画像の保存にはあまり向いていません ( マスク画像をもし JPEG で保存するときはグレースケールにしてください )。

Portable Network Graphic 画像 ( PNG 画像 )
:   JPEG とは違い、可逆圧縮を行います。圧縮によってデータサイズは JPEG ほどは小さくはならないのですが、画質は圧縮を行っても劣化しません。CG に適しています。一つの画像中にアルファチャンネル ( 透過度 ) の情報を持たせることができます。
    　また、レイヤトランジション に使うルール画像も PNG での圧縮がいいでしょう。

Entis Rasterized Image format 画像 ( ERI 画像 )
:   主にフルカラー画像用途ですが、可逆圧縮にしてはかなりの高圧縮率での圧縮 ( PNG の 5 ～ 7 割ほどのサイズ ) と、その圧縮率にしては高速な展開が特徴です。一つの画像中にアルファチャンネル ( 透過度 ) の情報を持たせることができます。

TLG5 画像
:   TLG5 画像の拡張子は .tlg です ( .tlg5 ではありません )。場所によっては単に TLG と呼んでいる場所もあるかと思います。
    　フルカラーの画像にのみ対応しています。可逆圧縮を行います。一つの画像中にアルファチャンネル ( 透過度 ) の情報を持たせることができます。
    　圧縮率はさほど高くなく、ファイルサイズは PNG の 3 割増しぐらいのサイズになりますが、高速に展開できるという特徴があります。PNG の４～５倍ほどの速度で画像を展開することができます。

TLG6 画像
:   TLG6 画像の拡張子は TLG5 と同じく .tlg です ( .tlg6 ではありません )。吉里吉里２ Version 2.21 beta 3 から使用可能になった画像形式で、高い圧縮率と高速な展開速度が特徴です。サイズは PNG より 1～4割ほど小さく、展開速度は PNG の２倍以上高速です。PNGのようにグレースケールやパレット付きの画像を扱うことはできませんが、フルカラーの画像や、アルファチャンネルつきフルカラーの画像ならば PNG の代用として使用できます。
    　フルカラーの画像にのみ対応しています。可逆圧縮を行います。一つの画像中にアルファチャンネル ( 透過度 ) の情報を持たせることができます。

# 各画像形式の比較

展開速度
:   各フォーマットを展開速度的に比較すると大体以下のようになります。

    　(早い) BMP > TLG5 > JPEG > TLG6 > ERI > PNG (遅い)

    　ちなみに BMP は標準では Releaser は「圧縮する」に分類しますが、この圧縮を行うと展開速度は ERI ぐらいの速度になります。速度が重要な場合は Releaser では「圧縮しない」に分類したほうが良いでしょう。
    　ただし BMP はファイルサイズが大きくなります。最近の PC のハードディスクからの読み込みならばあまり差は無いかと思いますが、古い HDD や CD-ROM からの読み込みなどでは、ファイルサイズが小さい方が読み込み速度が速いことがあるので注意が必要です。

サイズ
:   各フォーマットの圧縮後のサイズを比較すると大体以下のようになります ( もちろん画像や圧縮率の設定によっても変わってきます )。

    　(大きい) BMP > TLG5 > PNG > ERI > TLG6 > JPEG (小さい)

画質
:   画質は JPEG のみが不可逆圧縮で他は可逆圧縮なので、以下のようになります。

    　(高い) BMP = PNG = ERI = TLG5 = TLG6 > JPEG (悪い)

# 用途別の選定

背景画像
:   ファイルサイズを気にしないのならば BMP がもっとも高速で、しかも画質の劣化がありません。
    　それについで TLG5 が高速で、ファイルサイズはあんまり気にならないけど、画質も損ないたくないし、まるっきり圧縮しないのも能がない、というときは TLG5 が良いでしょう。
    　ファイルサイズはもうちょっと気になるが、画質は損ないたくないならば TLG6、ERI か PNG が良いでしょう。
    　ファイルサイズがひどく気になり、画質は劣化しても仕方ないならば JPEG が良いでしょう。

前景画像(立ち絵など)
:   これも背景画像と同じことが言えます。
    　ただし JPEG は一つのファイルでは透過情報を扱えないため、メイン/マスク分離形式で扱う必要があります。

デモシーン中での画像
:   特に動的な表現を多様するデモシーンなどでは、展開速度が高速な BMP を用いると良いでしょう( ただしファイルサイズと読み込み時間については上で説明したとおりです )。
    　しかし BMP は大きくなるので、TLG5 で圧縮するというのも良いでしょう。TLG5 は高速に展開できるのでこのような用途には使いやすいと思います。
    　画質を気にしなくて良いならば、JPEG もよい選択肢です。JPEG の展開は思いのほか高速で、大体 ERI や PNG の半分以下の時間で展開することができます。また、動的な表現に用いる場合は画質の劣化はほとんど気にならないでしょう。

# アルファチャネルの効用

吉里吉里はアルファチャネル(透過度)を持った画像を前景画像として扱うことができます。従来用いられてきたカラーキーによる透過では、完全に透過するか、あるいは完全に不透明かの二つの状態しか扱うことができません。
　アルファチャネルを用いることにより、透明部分と不透明部分のエッジをなめらかに背景と合成したり、画像中に半透明の部分を作ることができます。

![kiri_a.png](kiri_a.png)![kiri_aa.png](kiri_aa.png)
カラーキーによる透過とアルファチャネルによる透過

　左がカラーキー、右がアルファチャネルによる透過です。
　透明部分とのエッジを拡大してみるとわかると思います。また、右側ではリボンを半透明にすることができています。

# 画像フォーマットコンバータ

吉里吉里 SDK 付属の画像フォーマットコンバータ ( krkrtpc.exe ) を用いると、画像を簡単に変換することができます。入力には Photoshop データ (PSD) も用いることができます。これにより、Photoshop データから簡単に吉里吉里用の前景画像を作成することが可能です。また、吉里吉里独自の圧縮形式である TLG5/TLG6 にも、このツールで変換を行うことができます。
　詳しくは、吉里吉里 SDK ヘルプをご覧ください。

Note

　現バージョンでは ERI の入力/出力には未対応です。