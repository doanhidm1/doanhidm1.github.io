[Topへ](index)

# ファイルフォーマット

吉里吉里Z がサポートするファイルフォーマットついて記載。

### 目次

[ファイルフォーマット](#fileformat)

ファイルフォーマット

| 種類 | 形式 | 拡張子 | 説明 |
| --- | --- | --- | --- |
| 静止画像 | Windows ビットマップ (Bitmap) | .bmp | 無圧縮形式のみサポート。 |
| JPEG | .jpg | 読み込み時精度を指定可能。  設定可能な値は 'high' (高い), 'normal' (標準), 'low' (低い) のいずれか。  デフォルトは'normal'。  low はIDCTに固定小数点(整数)AAN、色差拡大補間なし。  normal はIDCTに固定小数点(整数)LLM、色差拡大補間あり。  high はIDCTに浮動小数点AAN、色差拡大補間あり。  指定方法については[起動オプション -jpegdec (JPEG画像デコード精度)](../kirikiriz/j/contents/CommandLine#id47)を参照のこと。 |
| Portable Network Graphic (PNG) | .png | αチャンネルや透明色指定に対応。 |
| TLG5 | .tlg | 吉里吉里独自形式。  展開速度が高速(PNGの4倍速程度)なのが特徴。  [画像フォーマットコンバータ](../kirikiriz/j/contents/TPC)で変換可能。 |
| TLG6 | .tlg | 吉里吉里独自形式。  PNGやTLG5よりも圧縮率は高いが、TLG5の倍ほど展開に時間がかかります。  ただ、それでもPNGの2倍速程度なので高速です。  [画像フォーマットコンバータ](../kirikiriz/j/contents/TPC)で変換可能。 |
| その他 | .\* | Susie-plugin による拡張が可能。 |
| 音声 | WAVE | .wav | 無圧縮WAVE形式をサポート。 |
| Ogg Vorbis | .ogg | 要wuvorbis.dllプラグイン |
| その他 | .\* | プラグインにより拡張可能。 |
| 動画 | MPEG I | .mpg .mpeg .mpv .m1v .dat | MPEG Iのみサポート。  MPEG2などそれ以降は非サポート。  要 krmovie.dll。  再生機にWindows Media Player 6.4以降、  またはDirectX 7以降がインストールされていること。 |
| Windows Media Video (WMV) | .wmv | 要 krmovie.dll。  再生機にWindows Media Player 9以降がインストールされていること。 |
| AVI | .avi | 非公式サポート。  要 krmovie.dll。  Codecなどの問題により再生出来ないことなどがあり、公式サポートは行わない。 |
| アニメーション | ASD ファイル | .asd | 吉里吉里独自形式。  KAG3 でサポートされる。  AnimationLayer.tjsのコメント、もしくは[吉里吉里2/KAG3のアニメーション](http://homepage1.nifty.com/gutchie/KAG3Animation)を参照のこと |
| アーカイブ | XP3 | .xp3 | 吉里吉里独自形式。  [Releaser](../kirikiriz/j/contents/Releaser)にて作成する。 |
| その他 | .\* | プラグインにより拡張可能。 |
| フォント | レンダリング済みフォント | .tft | 吉里吉里独自形式。  [レンダリング済みフォントデータ作成ツール](../kirikiriz/j/contents/FontMaker)にて生成する |
| TrueType/OpenType フォント | .ttf .otf | 非公式サポート。  システムにフォントをインストールすることなく使える。  要[addFont.dll](../../src/plugins/win32/addFont/index)。Windows2000/XP/Vista のみ対応。 |