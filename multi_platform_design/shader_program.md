# ShaderProgramクラス

マルチプラットフォーム版ではShaderProgramクラスが追加される。
Android版では、OpenGL ES2.0/3.0で描画が行われ、Windows版ではDirectX11をバックエンドとしたANGLEで OpenGL ES3.0で描画される。
このためシェーダーはGLSLで共通化される。

マルチプラットフォーム版のハードウェアを用いた描画機能では、本体の開発効率や拡張性の観点からシェーダーを内部に持つことは最小限に抑え、TJS2スクリプトと同様にシェーダースクリプトを外部から読み込むことによってより多彩な描画を行える形になっている。

デフォルトで提供されているブレンドモードは、組み込み機能で実現可能なもののみで、吉里吉里2/ZがLayerでもつ多くのブレンド方法はシェーダーによって実現する必要がある。
これらシェーダーは別途スクリプトの形で提供されるので、テクスチャ+シェーダーを引数に持つ描画命令によって使用可能である。
また、トランジションも同じように実現可能となっている。
具体的にはクロスフェードは2つのテクスチャとシェーダーによって実現可能である。
レンダーターゲットを指定することで、描画先をテクスチャとすることが可能なため、そのテクスチャを使うことでこのクロスフェードは実現する。
ユニバーサルトランジションについては、3つのテクスチャとシェーダーによって実現可能である。
さらに拡大縮小の補間方法は、組み込みでは最近傍点とバイリニアのみ提供されるが、シェーダーを用いればLanczosやBicubicをスクリプトで実現できる。

## 内部的な話

ShaderProgramクラスはVertex/Fragmentシェーダーをコンパイル/リンクしたものを格納するクラス。
コンストラクタでコンパイル/リンクは実行され、エラーがあると例外が出るのでログを見て修正する。
シェーダーの入力に使われるパラメータは、TJS2の動的言語特性を活かしメンバに追加されるので、メンバ経由で値の設定が可能(Uniformのみ)。
シェーダープログラムに記述されている変数名取得は、リフレクションを使用し取得する。
Textureなどの指定は決められた予約語としてあらかじめ定めておき、その名前で作る必要がある。
頂点情報となる Attribute 属性値はメンバ経由の設定は出来ず、決められた予約語での設定か、別のMesh2Dクラスによる指定(予定)となる。
ShaderProgramクラスに元々あるメンバ関数やプロパティは必然的にシェーダー内で入力変数名としては使えない(そのため現状は最小限のメンバしか追加していない)。

シェーダー内で定義された入力名として追加されたプロパティに値を設定しておくと、描画時にその値が設定される。
追加されたプロパティは値の設定のみ可能で、取得は出来ない(実装工数上の制限、将来緩和の可能性あり)。
値は保持され続けるので、同じシェーダーを使う場合、描画前に指定したい値に変更しておく必要がある。
プロパティの型は、シェーダースクリプトから取得される。
vec4などはArrayクラスにreal型の配列として受け渡しする。
シェーダーでは構造体や配列も使用可能であるが、現在のところこれらはサポートされていない(実装工数上の制限、将来緩和の可能性あり)。

予約語は、描画実行時に内部的に自動的に設定されるので、明示的に値を設定する必要はない。
ex. s\_tex0 には、1個目の texture id が渡される。
自動的に設定される値は描画命令に依存する(順次マニュアル整備)。

## 有用性

シェーダーがスクリプトから指定出来て、自由に入れ替えられるのなら、従来のようにLayerに機能拡張するためにプラグインを書かなくても、TJS2 スクリプトのみで、従来の CPU 処理するよりも高速に演出の追加が可能になると予測できる。
Layer 相当の機能が現状はないが、Layer/Sprite などを TJS2 スクリプトで実現するために必要な周辺機能を充実させれば、その辺りスクリプトで書けて、従来よりネイティブ(C++)プラグインの出番を少なくできる。
複数 CPU に向けてバイナリを準備する必要のある Android ではスクリプトで機能拡張できるのは、apk サイズ縮小にも役立つ。
また、マルチプラットフォームでも有利。
シェーダー + それを扱う Sprite 等を実現する TJS2 スクリプトをセットで配布すれば、それで演出強化できる。