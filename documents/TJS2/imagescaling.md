# 画像拡大縮小フィルタ

吉里吉里Zでは画像の拡大縮小方法に2で使われていたニアレストネイバーとバイリニア、バイキュービック以外にも色々なフィルタが追加された。

## 拡大縮小フィルタ

* ニアレストネイバー
* バイリニア
* バイキュービック
* Lanczos2
* Lanczos3
* Spline16
* Spline36
* 面積平均(縮小のみ)
* Gaussian
* BlackmanSinc

吉里吉里2 では、バイキュービックはかなり遅くて使いづらかったが、現在の吉里吉里Zでは高速化され、どのフィルタでも使用できる程度の速度になっている。

※ 参考画像 : 別サイトの画像
![参考画像](../img/resample_20140404.png "実行結果サンプル")

### [このドキュメントのライセンス](../LICENSE)