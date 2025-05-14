[Topへ](index)

# 画像処理機能

吉里吉里Z がサポートする画像処理機能ついて記載。

### 目次

[諸元](#spec)
[合成演算](#blend_mode)

諸元

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| 合成 演算 | 不透明 | 乗算合成 | Photoshop互換 覆い焼き(リニア)合成(加算合成) | Photoshop互換 ハードライト合成 | Photoshop互換 比較(明)合成 |
| アルファ合成 | 覆い焼き合成 | Photoshop互換 焼き込み(リニア)合成(減算合成) | Photoshop互換 ソフトライト合成 | Photoshop互換 比較(暗)合成 |
| 加算アルファ合成 | 比較(明)合成 | Photoshop互換 乗算合成 | Photoshop互換 覆い焼きカラー合成 | Photoshop互換 差の絶対値合成 |
| 加算合成 | 比較(暗)合成 | Photoshop互換 スクリーン合成 | Photoshop V.5.x以下互換 覆い焼きカラー合成 | Photoshop V.5.x以下互換 差の絶対値合成 |
| 減算合成 | スクリーン乗算合成 | Photoshop互換 オーバーレイ合成 | Photoshop互換 焼き込みカラー合成 | Photoshop互換 除外合成 |

合成演算

| No. | 種類 | 式 | 説明 |
| --- | --- | --- | --- |
| 1 | 不透明 | result = src | アルファチャンネルを参照せずに合成を行います |
| 2 | アルファ合成 | result = blend(dest, src, α) | アルファ合成を行います。  透過を行う際のもっとも基本的なタイプです。 |
| 3 | 加算アルファ合成 | result = min(1.0, dest × ( 1.0 - α ) + src) | 加算アルファ合成を行います。 |
| 4 | 加算合成 | result = min(1.0, dest × ( 1.0 - α ) + src) | 加算合成を行います。光彩の表現に適しています。  11.Photoshopにおける「覆い焼き(リニア)」に相当しますが、本合成ではアルファは無視されます。  中性色 (重ね合わせても変化のない色) は黒です。 |
| 5 | 減算合成 | result = max(0.0, dest + src - 1.0)  ※ result = dest - src と違うのは src が反転しないかするかの違いだけです。 | 減算合成を行います。αは無視されます。  中性色は白です。 |
| 6 | 乗算合成 | result = dest × src | 乗算合成を行います。  αは無視されます。  中性色は白です。 |
| 7 | 覆い焼き合成 | result = min(1.0, dest ÷ ( 1.0 - src ) ) | 覆い焼き合成を行います。  光に照らされたものの表現に適しています。  αは無視されます。  中性色は黒です。 |
| 8 | 比較(明)合成 | result = max(dest, src) | 「比較(明)」合成を行います。  αは無視されます。  中性色は黒です。 |
| 9 | 比較(暗)合成 | result = min(dest, src) | 「比較(暗)」合成を行います。  αは無視されます。  中性色は白です。 |
| 10 | スクリーン乗算合成 | result = 1.0 - ( 1.0 - dest ) × ( 1.0 - src ) | 「スクリーン乗算」合成を行います。  αは無視されます。  中性色は黒です。 |
| 11 | Photoshop互換 覆い焼き(リニア)合成 (加算合成) | result = blend(dest, min(1.0, dest + src), α) | Photoshop互換の「覆い焼き(リニア)」合成(加算合成)を行います。  4.加算合成と違い、αは無視されません。  中性色は黒です。 |
| 12 | Photoshop互換 焼き込み(リニア)合成 (減算合成) | result = blend(dest, max(0.0, dest + src - 1.0), α) | Photoshop互換の「焼き込み(リニア)」合成(減算合成)を行います。  5.減算合成と違い、αは無視されません。  中性色は白です。 |
| 13 | Photoshop互換 乗算合成 | result = blend(dest, dest × src, α) | Photoshop互換の「乗算」合成を行います。  6.乗算合成と違い、αは無視されません。  中性色は白です。 |
| 14 | Photoshop互換 スクリーン合成 | result = blend(dest, 1.0 - (1.0 - dest) × (1.0 - src), α) | Photoshop互換の「スクリーン」合成を行います。  10.スクリーン乗算合成と違い、αは無視されません。  中性色は黒です。 |
| 15 | Photoshop互換 オーバーレイ合成 | result = blend(dest, overlay(dest, src), α)  ここで overlay(a, b) =  a × b × 2.0 ( a < 0.5 のとき)  1.0 - (1.0 - a) × (1.0 - b) × 2.0 (それ以外のとき) | Photoshop互換の「オーバーレイ」合成を行います。  中性色は50%灰色です。 |
| 16 | Photoshop互換 ハードライト合成 | result = blend(dest, hardlight(dest, src), α)  ここで hardlight(a, b) =  a × b × 2.0 (b < 0.5 のとき)  1.0 - (1.0 - a) × (1.0 - b) × 2.0 (それ以外のとき) | Photoshop互換の「ハードライト」合成を行います。  中性色は50%灰色です。 |
| 17 | Photoshop互換 ソフトライト合成 | result = blend(dest, softlight(dest, src), α)  ここで softlight(a, b) =   後でLatexで書いた式を貼り付ける | Photoshop互換の「ソフトライト」合成を行います。  中性色は50%灰色です。 |
| 18 | Photoshop互換 覆い焼きカラー合成 | result = blend(dest, min(1.0, dest ÷ ( 1.0 - src ) ), α) | Photoshop互換の「覆い焼きカラー」合成を行います。  ltDodge と違い、αは無視されません。  中性色は黒です。 |
| 19 | Photoshop Ver.5.x以下互換 覆い焼きカラー合成 | result = min(1.0, dest ÷ ( 1.0 - src × α) ) | Photoshopのバージョン 5.x 以下と互換の「覆い焼きカラー」合成を行います。  18.Photoshop互換覆い焼きカラー合成とは式が若干異なります。  中性色は黒です。 |
| 20 | Photoshop互換 焼き込みカラー合成 | result = blend(dest, max(0.0, 1.0 - (1.0 - dest) ÷ src), α) | Photoshop互換の「焼き込みカラー」合成を行います。  中性色は白です。 |
| 21 | Photoshop互換 比較(明)合成 | result = blend(dest, max(dest, src), α) | Photoshop互換の「比較(明)」合成を行います。  8.比較(明)合成と違い、αは無視されません。  中性色は黒です。 |
| 22 | Photoshop互換 比較(暗)合成 | result = blend(dest, min(dest, src), α) | Photoshop互換の「比較(暗)」合成を行います。  9.比較(暗)合成と違い、αは無視されません。  中性色は白です。 |
| 23 | Photoshop互換 差の絶対値合成 | result = blend(dest, abs(dest - src), α) | Photoshop互換の「差の絶対値」合成を行います。  中性色は黒です。 |
| 24 | Photoshop Ver.5.x以下互換 差の絶対値合成 | result = abs(dest - src × α) | Photoshopのバージョン 5.x 以下と互換の「差の絶対値」合成を行います。  23.Photoshop互換差の絶対値合成とは式が若干異なります。  中性色は黒です。 |
| 25 | Photoshop互換 除外合成 | result = blend(dest, dest + src - 2.0 × src × dest, α) | Photoshop互換の「除外」合成を行います。  中性色は黒です。 |