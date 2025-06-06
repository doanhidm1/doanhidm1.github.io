# はじめに

KAG は Kirikiri Adventure Game の略です。吉里吉里でアドベンチャーゲームやノベルゲームを作るためのスクリプトです。
　KAG それ自体は、吉里吉里が理解できる TJS(2) スクリプト言語で書いてありますが、KAG が理解するファイルは、シナリオファイルという、文章中に「タグ」(指令) を書き込んだテキストファイルです。
　シナリオファイル作りは、テキストエディタ上での作業が主となります。敷居はすこし高いかも知れません。しかし、たとえば、HTML をテキストエディタでじかに書くことのできる人であれば、すぐになじめると思います。

　標準で用意されたタグのみを使用してもそこそこのことはできますが、KAG 自体が TJS スクリプトで書いてあるため、これを改造したり、またはシナリオファイル中に TJS スクリプトを書き込んで直接吉里吉里本体に働きかければ、より別の動作や別の機能を拡張する事ができます。これは 吉里吉里/KAG の大きな特徴の一つです。

Note

　KAG 3 以降に対応する吉里吉里本体は 吉里吉里２です。吉里吉里２は吉里吉里１に似せてほぼ１から作り直した吉里吉里で、それに伴い KAG も新しく書き直したものが KAG 3 です。KAG 3 は KAG 3 未満の KAG とシナリオレベルでの互換性を持っていますが、KAG 3 未満のプロジェクトを移植する場合はいくつかの注意点があります。[KAG 3 未満からの移植と KAG 3 での新機能](PortFromOldKAG) をご覧ください。

Note

　吉里吉里本体は TJS というスクリプト言語を解釈することができます。その TJS というスクリプト言語で書かれた KAG は、KAG 用に書かれたシナリオファイルを解釈することができるという構造になっています。そのため、ここでは、とくに KAG に限定して物事を言うときは「KAG」と、また吉里吉里本体に限定して言うときは「吉里吉里」、また両方に関わることであれば「吉里吉里/KAG」という言い方をすることにします。
　また、TJS スクリプトと KAG シナリオの区別を付けるため、TJS スクリプトを記述したものは「スクリプト」あるいは「スクリプトファイル」、KAG シナリオを記述したものは「シナリオ」あるいは「シナリオファイル」という言い方をすることにします。

# どんなゲームを作れるのか

KAG は元々アドベンチャーゲームを作るためのスクリプトですので、アドベンチャーゲームを作ることができます(当たり前か)。
　アドベンチャーゲームといってもいろいろありますが、KAG では主に文章を表示し、文章中に設定された選択肢をたどることで物語が分岐する、というタイプのアドベンチャーゲームを作ることができます。

# このドキュメントの著作権等

このドキュメントの文章やほとんどの画像の著作権は W.Dee が保有します。引用は許可無く行ってかまいませんが、このドキュメント中で使用している画像には他の方の著作物が含まれるため、画像そのものを流用したり、画像を含む引用を行う場合は W.Dee に連絡を取ってください。

サポートやダウンロードは以下のページで行っております
吉里吉里/KAG ダウンロードページ : <http://kikyou.info/tvp/>