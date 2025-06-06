# 吉里吉里Z マルチプラットフォーム版開発/移植時の注意点

従来の吉里吉里Zから変更/追加された機能で注意を要する部分について記述する。

## ファイル名のケースセンシティブについて

従来はファイル名について大文字小文字特に注意する必要はなかったが、Androidのファイルシステムはケースセンシティブであるため、ファイルを置く場所によってその影響を受ける。
XP3にアーカイブ化されたものは従来と同じケースインセンシティブのまま。
その他についてはケースセンシティブ。
プラグインファイル、セーブデータのファイル名、動画ファイル名(現状Assets内に置く仕様)は特に注意が必要。
アーカイブ化せずにAndroidでフォルダ指定して動作確認する場合は全てのファイルがこの影響を受ける。
運用上置き場所などの問題を回避するため、すべて小文字ファイル名とした方が安全である。
AndroidではXP3アーカイブ化されたものしか実行しないのであれば、上述の3つのファイル以外は特に注意は必要ない。

## AndroidではWindowは一つだけでフルスクリーン前提

AndroidではWindowは一つのみ生成可能。
また、フルスクリーン前提となっている。
モーダルウィンドウも使えない。

## メニューを追加する場合

Windowsは伝統的に上側にメニューになっているが、Androidではスワイプインで表示させる時、左側以外はシステムで他に使われているから左側からのスワイプインで表示するしかない。

## ハードウェアを使用した描画

### Window.onDraw内で描画する

ハードウェアを使用した描画は、描画前の設定と描画後のフリップ(スワップ)があるため、onDraw内でのみ描画用Canvasメソッドをコール可能で、他の場所で呼び出した場合意図しない結果となるので注意。
KAG3など従来はタグが呼ばれた時点で即座に描画などしていたが、ハードウェアを使用した描画では状態の変更のみ行い、onDraw内で実際の描画を行う必要がある。

### 内部的に上下反転座標系

OpenGL ES2.0/3.0 での実装なので、内部では上下反転(左下原点)している。
デフォルトのシェーダーではバーテックスシェーダーのortho行列で、左上原点に変換している。
Offscreenクラスを使用して描画を行ったテクスチャは上下反転したバーテックスシェーダーを使用すると、テクスチャが反転してしまうので注意する必要がある。

### 機種依存問題

Windows版では、ANGLEを介し、シェーダーコンパイラ(HLSL)もMSが作っているので互換性はかなり高い(対応有無のみ)と考えられるが、Androidではシェーダーコンパイラ(GLSL)はドライバ実装のため、GPUごと(ドライバごと)に挙動が異なることがあり注意が必要。
また、AndroidではOSバージョンが上がらないとドライバ修正が入らないこともあり、バージョンアップされない端末もあることから、不具合が残ったままの端末も存在する。
GLSLについては、Androidでよくテストする必要がある。
[GLSL機種依存問題](http://dench.flatlib.jp/opengl/glsl)ページはまず一読して、時々チェックする必要がある。

## DrawDeviceの廃止

Android版ではDrawDeviceは廃止されたので、DrawDeviceを自前で作っていた場合は変更が必要になる。
ハードウェアを用いた描画系に書き換えることを推奨。
Windows版のみで互換性を重視し新規追加された描画系を使用しないのであれば、DrawDeviceを使い続けることは可能。
ただし、将来的に廃止の可能性が高いので、早めに移行推奨。