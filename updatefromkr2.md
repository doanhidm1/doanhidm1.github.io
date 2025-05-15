[Topへ](index)

# 吉里吉里Zでの吉里吉里2からの変更点一覧

以下の変更点は初期正式版についてのものです。
それ以降のバージョンによってさらに変更が加えられている可能性があります。
1.0 以降の更新内容については、[更新履歴](olderversions)を参照してください。

変更

1. Visual Studio でビルドできるように変更。

C++Builder5 でビルドしてた吉里吉里2 を Visual C++ 2012 でビルドできるように各種変更を行った。

2. VCL 依存部分を Win32 API 呼び出し処理へ変更。

VC では、VCL を利用できないため、通常の Win32 API を使用する処理へ変更。
ある程度等価な処理となっているが、同じ実装ではないため細部の動作は異なる部分がある。
VCL では、不可視のメインウィンドウがアプリケーション(ウィンドウ)として機能し、他のウィンドウはその子として動く。
吉里吉里2 内では、最初に作られたウィンドウがメインウィンドウとして扱われるが、内部には不可視のアプリケーション(ウィンドウ)が存在している(た)。
吉里吉里Z では、VCL を書き換えると共に、この不可視のアプリケーション(ウィンドウ)は存在しなくなっている。
このためアプリケーションの挙動で細部が異なる箇所が存在する。
アプリケーションとして扱われるもののうちいくつかは最初に作られた吉里吉里内のメインウィンドウが相当する。
アプリケーションのイベントでアクティブ/非アクティブはメインウィンドウのものとなる。

3. Direct3D7 を Direct3D9 へ変更。

Direct3D7 によって描画されていたものは Direct3D9 へ書き換えられている。
それに伴い次の変更が行われている。

4. フルスクリーン化処理を DrawDevice で行うように変更。

DirectDraw によるフルスクリーン化は、Windows8 でいくつか問題を引き起こしていたようなので、この部分は変更する必要があり、Direct3D9 では Direct3D Device がフルスクリーン化を担当するということもあり、フルスクリーン化処理は DrawDevice 側で処理する実装とした。
上述のように Direct3D9 化に伴い、フルスクリーン化は API/DirectDraw から API/Direct3D9 へと変更になり、設定はオプションではなく DrawDevice 依存となった。

5. KAGParser クラスをプラグインに変更。

元々プラグインの方が良いと思えるクラスだったので、プラグインに移動した。
このプラグインは互換性のために作成した。

6. Menu クラスをプラグインに変更。

Menu を非推奨とするにあたり、プラグインに移動した。
今後メニューを使わない実装にすることを推奨。

7. 各種依存ライブラリを更新。

VCプロジェクト作成時に最新バージョンに更新した。

8. 正規表現エンジンを鬼車へ変更。

boost の少し古いバージョンのものであったので、鬼車へと変更した。

9. コンソールへの出力をコマンドラインへの出力へ変更、デバッグ時はデバッグ出力へも出力。

コンソール削除に伴いコマンドラインへ出力するように変更した。
デバッグ時は、デバッグ出力で見られた方がデバッグしやすいため、デバッグビルドではデバッグ出力へも出力するようにした。

10. Font クラスを生成できるように変更。

Layer.font としてのみ存在していたが、独立して生成できるようにした。

11. ツールチップ処理の仕様変更。

VCL のツールチップは、コモンコントロールのツールチップではなく独自実装と言うことで、コモンコントロールに置き換えるか、同じように実装するか検討し、イベントを発生させて Layer として描画可能な形に変更した。
Layer.hint を設定し、カーソルが一定時間停止しヒント表示タイミングになると [Window.onHintChanged](docs/kirikiriz/j/contents/f_Window_onHintChanged) イベントが発生する。
カーソル停止時間は、[Window.hintDelay](docs/kirikiriz/j/contents/f_Window_hintDelay) で指定可能。
ヒントを描画するレイヤーには [Layer.ignoreHintSensing](docs/kirikiriz/j/contents/f_Layer_ignoreHintSensing) を有効にして、ヒント表示を無視させる。
これで onHintChanged で isshow が true の時、ヒントを最前面レイヤーに描画し、ヒントレイヤーはマウスメッセージは無視されるように設定すれば従来と同じような表示が出来る。
isshow が false でイベントが来たら非表示にする。
[GitHub にサンプル](https://github.com/jin1016/krkrz/blob/last_64bit_merge/script/Sample/tooltip/startup.tjs)を上げている。

12. ゲームパッドの有効/無効をデバッグオプション化。

組み込みのゲームパッドサポートはない方が良い場合もあるので、オプションのみでなくコンパイルオプションで無効化してしまえるようにした。
DISABLE\_EMBEDDED\_GAME\_PAD を指定すると無効化される。

13. JPEG デコード時 LLM を使用するのを標準に。

吉里吉里2 では、品質が標準の時 AAN が使われていたが、AAN だと低品質なので LLM を標準とした。
吉里吉里Z では JPEG の読込みは吉里吉里2 よりもかなり高速化しており、IDCT のアルゴリズムを AAN から LLM へ変更しても吉里吉里2 より高速にデコードされる。
LLM の方が一般的に使われているはずなので、吉里吉里で表示すると汚いと言う状況は少なくなると考えられる。

14. TJS2 スクリプトのデフォルト文字コードを UTF-8 に変更。

UTF-8 の方が一般化していると言うことで、Shift-JIS から変更。
TVP\_TEXT\_READ\_ANSI\_MBCS を付けてコンパイルすれば従来通り Shift-JIS をデフォルトとする。
Plugin用公開関数の TVPCreateTextStreamForReadByEncoding の第3引数にエンコーディング指定可能。
"Shift\_JIS" か "UTF-8" のどちらかを指定する。
また、オプションの"-readencoding"で"Shift\_JIS" か "UTF-8" のどちらかを指定することでデフォルトを変更できる。
[Scripts.textEncoding](docs/kirikiriz/j/contents/f_Scripts_textEncoding) で "Shift\_JIS" か "UTF-8" のどちらかの指定も可能。
プラグインの KAGParser もこの設定に従う。
プラグインで TVPCreateTextStreamForReadByEncoding を呼び出している箇所を変更すれば、任意のエンコーディングで読み込む。

15. ソースコード埋め込み文字列をリソースへ移動。

エラーメッセージ等直接ソースコードに記述されていた文字列をリソースへ移動し、日本語と英語で分離。
メッセージからリソースやソースコードはスクリプトで自動生成するようにしたので、他環境実装時持っていきやすくなっている。
Messages.xlsx に記述し、gentext.bat で生成される。
ライセンス文はリソースの license.txt に記述されている。

16. コンパイル後バイナリに結合していたオプションをリソースに移動。

従来 tvpwin32.exe に optionarea.bin を末尾に結合し、krkr.eXe として、実行時末尾のバイナリを読み取っていたものをリソースに埋め込む形に変更。
オプションは optionarea.txt に改行区切りで記述する。
一般的な構造となったためウィルス駆除ソフト等で誤検出が減ることが期待できる。

17. マルチディスプレイ対応に伴いスクリーンサイズ等が返す値を変更。

従来プライマリーディスプレイの値を常に返すようになっていたが、複数のディスプレイを考慮した値を返すように変更。
[System.screenWidth](docs/kirikiriz/j/contents/f_System_screenWidth) /
[screenHeight](docs/kirikiriz/j/contents/f_System_screenHeight) は、メインウィンドウがあるモニタのサイズを返す。メインウィンドウが作られる前はプライマリモニタのサイズで返す。
[System.desktopLeft](docs/kirikiriz/j/contents/f_System_desktopLeft) /
[desktopTop](docs/kirikiriz/j/contents/f_System_desktopTop) /
[desktopWidth](docs/kirikiriz/j/contents/f_System_desktopWidth) /
[desktopHeight](docs/kirikiriz/j/contents/f_System_desktopHeight) は、メインウィンドウがあるモニタの作業領域を返す。メインウィンドウがない時は、プライマリモニタの作業領域を返す。

18. フォント選択ダイアログをスクリプト化。

本体から削除し win32dialog.dll + スクリプトによる実装に変更。
スクリプトは [GitHub](https://github.com/krkrz/krkrz/tree/master/script/Krkr2Compat) にある。

19. 文字入力ダイアログをスクリプト化。

本体から削除し win32dialog.dll + スクリプトによる実装に変更。
スクリプトは [GitHub](https://github.com/krkrz/krkrz/tree/master/script/Krkr2Compat) にある。

20. 起動時ファイル選択ダイアログをフォルダ選択ダイアログへ変更。

VCL を使った独自のダイアログだったものを、フォルダ選択ダイアログへ変更した。

21. 起動時ファイル選択をデバッグオプションで無効化可能に変更。

最終リリース版ではない方がよい機能なので、無効化可能にした。
TVP\_DISABLE\_SELECT\_XP3\_OR\_FOLDER を定義することで無効化する。

22. マルチバイトコードからワイド(UNICODE)バイトコードへ変更。

NT 系のみサポートとするので、ワイド(UNICODE)バイトコードに変更した。

23. -waitvsync のプロパティ化

コマンドラインオプションの-waitvsyncは廃止し、[Window.waitVSync](docs/kirikiriz/j/contents/f_Window_waitVSync)に変更した。
これはWindowごとにD3DDeviceを持ち、垂直同期待ちがそのデバイスに依存するため。

24. PassThroughDrawDevice を BasicDrawDevice へ変更。

DirectDraw / Direct3D / GDI をベンチマークし、いずれかで描画を行っていた PassThroughDrawDevice を廃止し、Direct3D9 で描画を行う BasicDrawDevice を追加した。
DrawDevice は BasicDrawDevice が標準となる。
Direct3D9 以外で描画を行いたい場合はプラグインによる追加が必要となる。

25. オプション説明をJSON化、リソースへ移動。

独自フォーマットであったオプション説明ファイルをJSONに変更した。
また、ファイルをリソースへ移動し、プラグインからの読込みも公開関数からリソースに変更した。
option\_desc\_ja.json にて指定可能。
-userconf で起動された時、このファイルにしたがって設定項目が表示される。

26. 2GB を超える XP3 ファイルに対応。

吉里吉里2 では読込み時にエラーが出ていたものを修正して 2GB 超の XP3 ファイルを読めるようにした。

27. Windowの再生成排除。

吉里吉里2 ではフルスクリーン化時ボーダースタイル変更時に、ウィンドウが作り直されていたが、吉里吉里Z では作り直しが行われなくなった。
そのため TVP\_WM\_DETACH と TVP\_WM\_ATTACH が呼ばれる機会はほとんどなくなった。
フルスクリーン化/ウィンドウ化のタイミングを知るために、フルスクリーン変更前に TVP\_WM\_FULLSCREEN\_CHANGING が、変更後に TVP\_WM\_FULLSCREEN\_CHANGED が呼ばれるようになった。(フルスクリーンかどうか判定するものではないことに注意)

28. プラグイン公開関数の増減。

以下の公開関数が追加された。
TVPCreateTextStreamForReadByEncoding
TVPSetDefaultReadEncoding
TVPGetDefaultReadEncoding
TVPRegisterAcceleratorKey
TVPUnregisterAcceleratorKey
TVPDeleteAcceleratorKeyTable
TVPEnsureDirect3DObject
TVPGetDirect3DObjectNoAddRef
TVPChBlurMulCopy
TVPChBlurAddMulCopy
TVPChBlurCopy

以下の公開関数が削除された。
TVPMIDIOutData
TVPEnsureDirectDrawObject
TVPGetDirectDrawObjectNoAddRef
TVPGetDirectDraw7ObjectNoAddRef
TVPGetDDPrimarySurfaceNoAddRef
TVPSetDDPrimaryClipper
TVPReleaseDDPrimarySurface

削除

1. コンソール削除

最終的にリリースされるものに含まれていない方が良いので削除。

2. コントローラー削除

最終的にリリースされるものに含まれていない方が良いので削除。

3. MIDI / CDDA / Pad クラス削除

現状を考えるとレガシー機能であるとの判断から削除。

4. Win9X 系メソッド削除

XP以降のみ対応としたので、それ以前をサポートするための API を削除。

5. DirectDraw 描画処理を削除

ドライバの DirectDraw サポート状況が怪しくなってきていることと古いAPIであるので削除。

6. ERI フォーマットのサポートを削除

現状では取り立てて使用する意味を見出せないので削除。

7. Window クラスのいくつかのメソッドを削除。

削除されるメソッド/プロパティは以下の通り。
Window.layerLeft / Window.layerTop / Window.setLayerPos
Window.innerSunken
Window.showScrollBars
Window.beginMove

8. Layer クラスの obsolete メソッドを削除。

以前から obsolete で新しいメソッドへの置き換えが推奨されていたので削除。
削除されるメソッドは以下の通り。
Layer.affineBlend
Layer.affinePile
Layer.blendRect
Layer.pileRect
Layer.stretchBlend
Layer.stretchPile

9. マウスカーソルの内 Windows 標準でサポートされないものを削除。

C++Builder 標準ではあっても、Windows 標準でないものは削除。
削除されるカーソルは crDrag、crNoDrop、crHSplit、crVSplit、crMultiDrag、crSQLWait、crAppStart、crHBeam 。
必要な場合は、自前でリソースを追加する必要がある。
また、他のアイコンも C++ Builder とは少し見た目が異なる。
[サポートされているカーソルはこちら](docs/kirikiriz/j/contents/MouseCursors)(画像は吉里吉里2のまま)

10. krflash.dll の削除

krflash.dll は同梱されなくなった。
吉里吉里2 のものを持ってくれば動く可能性はあるが公式にはサポートしない。
flashPlayer プラグインへの移行を推奨。

追加

1. マルチタッチ機能のサポート。

マルチタッチをサポートするデバイスが有効の場合、タッチが有効になる。
1点のみのタッチがサポートされているような場合、マウス入力と同じように扱っても問題ないと考えられるため、タッチは有効にならない。
タッチ処理ではなく、常にマウスと同じように処理したい場合は、[Window.enableTouch](docs/kirikiriz/j/contents/f_Window_enableTouch)をfalseにして、タッチを無効化する必要がある。

2. Bitmap/ImageFunction/Rect クラス追加。

画像のみを保持するLayerクラスが欲しいという要望からBitmapクラスを新設。
それに伴いLayerから分離して必要な機能を実装するためにImageFunctionとRectクラスを追加。

3. Octet.unpack と Array.pack の追加。

吉里吉里2 で予定されていたものの追加されていない機能と思われる。
これによりバイナリファイルの読込み、書き出しが行いやすくなる。
[オクテット列に対する操作](docs/tjs2/j/contents/octet) と
[Array クラス](docs/tjs2/j/contents/array) を参照のこと。

4. -startup="xxx" により任意スクリプトからの起動を可能に。

テスト等で指定できた方が便利であるため追加。
詳細は[コマンドラインオプション](docs/kirikiriz/j/contents/CommandLine)参照のこと。

5. 5ボタンマウスの「戻る」「進む」キーサポート。

Windows 2000 以降で追加され、使用可能であるため追加。
[Window.onMouseDown](docs/kirikiriz/j/contents/f_Window_onMouseDown) 等で使用可能に。

6. バックグラウンドでの画像読込み機能サポート。

今までの同期読込みでは画像を更新しながら読み込んだ時に、表示が読込み時止まると言う問題があったため追加。
非同期読込みによって表示の更新を止めずに次の画像の読込みが可能になった。
非同期読込みは [Bitmap.loadAsync](docs/kirikiriz/j/contents/f_Bitmap_loadAsync) によって行う。

7. TJS2 クラスの継承をネイティブ( C++ ) で記述可能に。

C++ でも TJS2 クラスの継承を記述できた方が良いため追加。

8. drawGlyph を追加し外字を描画しやすくした。

任意の字形を文字列に埋め込んで描画しやすくするために追加。
[Layer.drawGlyph](docs/kirikiriz/j/contents/f_Layer_drawGlyph) /
[ImageFunction.drawGlyph](docs/kirikiriz/j/contents/f_ImageFunction_drawGlyph) で描画できる。

9. PNG/JPEG/TLG 保存機能の追加。

読込みが出来るので、それと対になるように保存も追加。
本体で BMP/PNG/JPEG/TLG の読み書きが出来るようになり便利に。
[Layer.saveLayerImage](docs/kirikiriz/j/contents/f_Layer_saveLayerImage) / [Bitmap.save](docs/kirikiriz/j/contents/f_Bitmap_save) の type 引数でBitmap以外の形式指定が可能になった。

10. FreeType での文字描画追加。

吉里吉里2 では GDI による文字描画のみだったが、FreeType による描画もサポートした。
[Font.rasterizer](docs/kirikiriz/j/contents/f_Font_rasterizer) で指定可能。
GDI よりも綺麗な文字描画が期待できる。

11. ログハンドラの追加。

ログをスクリプトで表示可能にするためログハンドラを追加。
[Debug.addLoggingHandler](docs/kirikiriz/j/contents/f_Debug_addLoggingHandler) /
[removeLoggingHandler](docs/kirikiriz/j/contents/f_Debug_removeLoggingHandler) /
[getLastLog](docs/kirikiriz/j/contents/f_Debug_getLastLog) によって処理可能。

12. 文字列の実描画範囲取得メソッドの追加。

フォントによって綺麗に指定位置へ描画することが困難な場合もあるため文字列の実描画範囲取得メソッドを追加した。
[Font.getGlyphDrawRect](docs/kirikiriz/j/contents/f_Font_getGlyphDrawRect) で取得可能。

13. 取消線とアンダーラインの実装。

吉里吉里2 では未実装となっていた取消線とアンダーラインを実装した。
これによって取消線やアンダーラインを含む文字を描画できる。
[Font.strikeout](docs/kirikiriz/j/contents/f_Font_strikeout) /
[underline](docs/kirikiriz/j/contents/f_Font_underline) で指定可能。

14. Opusサウンドフォーマットのサポート。

Vorbis より高圧縮率の [Opusサウンドフォーマット](http://opus-codec.org/) を kropus.dll にてサポートした。
短い音でもファイルサイズが小さくなるため、効果音などにも利用しやすい。
また、音声に最適化された圧縮方法も持っているため、台詞などで効果を発揮する。

15. 吉里吉里デバッガ同梱。

従来別配布となっていた吉里吉里デバッガを同梱し、デバッガ有効化バイナリも含めるようにした。
TJS2 スクリプトのデバッグがより行いやすくなる。

16. スクリプト例外発生時起動エディタ指定追加。

例外発生時に Pad を使用して表示されていたものを削除したため、それに変わるものとして任意のエディタを指定可能とした。
-exceptionexe と -exceptionarg で指定可能。
詳細は[コマンドラインオプション](docs/kirikiriz/j/contents/CommandLine)参照のこと。