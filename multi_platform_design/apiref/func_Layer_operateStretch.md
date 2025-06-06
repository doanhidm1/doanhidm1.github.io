# Layer.operateStretch

機能/意味
:   拡大縮小演算合成

タイプ
:   [Layerクラス](class_Layer)のメソッド

構文
:   operateStretch(dleft, dtop, dwidth, dheight, src, sleft, stop, swidth, sheight, mode=omAuto, opa=255, type=stNearest, option=1)

引数
:   |  |  |
    | --- | --- |
    | dleft | 重ね合わせ先の矩形の左端位置を ( 重ね合わせ先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | dtop | 重ね合わせ先の矩形の上端位置を ( 重ね合わせ先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | dwidth | 重ね合わせ先の矩形の横幅を ( 重ね合わせ先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | dheight | 重ね合わせ先の矩形の縦幅を ( 重ね合わせ先レイヤの画像位置における ) ピクセル単位で指定します。 |
    | src | 重ね合わせ元のレイヤオブジェクトを指定します。  Bitmap クラスのオブジェクトも指定可能です。 |
    | sleft | 重ね合わせる矩形の左端位置を ( 重ね合わせ元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | stop | 重ね合わせる矩形の上端位置を ( 重ね合わせ元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | swidth | 重ね合わせる矩形の横幅を ( 重ね合わせ元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | sheight | 重ね合わせる矩形の縦幅を ( 重ね合わせ元レイヤの画像位置における ) ピクセル単位で指定します。 |
    | mode | 演算のモードを指定します。   * omAuto が指定された場合は演算元レイヤのLayer.typeプロパティに従って演算の種類が自動的に決定されます。 * omPsNormal が指定された場合はPhotoshop互換のアルファ合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsAdditive が指定された場合はPhotoshop互換の覆い焼き(リニア)合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsSubtractive が指定された場合はPhotoshop互換の焼き込み(リニア)合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsMultiplicative が指定された場合はPhotoshop互換の乗算合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsScreen が指定された場合はPhotoshop互換のスクリーン合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsOverlay が指定された場合はPhotoshop互換のオーバーレイ合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsHardLight が指定された場合はPhotoshop互換のハードライト合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsSoftLight が指定された場合はPhotoshop互換のソフトライト合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsColorDodge が指定された場合はPhotoshop互換の覆い焼きカラー合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsColorDodge5 が指定された場合はPhotoshopのバージョン5.x 以下と互換の覆い焼きカラー合成が行われます(stNearestとstFastLinear以外で実装)。 * somPsColorBurn が指定された場合はPhotoshop互換の焼き込みカラー合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsLighten が指定された場合はPhotoshop互換の比較(明)合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsDarken が指定された場合はPhotoshop互換の比較(暗)合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsDifference が指定された場合はPhotoshop互換の差の絶対値合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsDifference5 が指定された場合はPhotoshopのバージョン 5.x 以下と互換の差の絶対値合成が行われます(stNearestとstFastLinear以外で実装)。 * omPsExclusion が指定された場合はPhotoshop互換の除外合成が行われます(stNearestとstFastLinear以外で実装)。 * omAdditive が指定された場合は加算合成が行われます(stNearestとstFastLinear以外で実装)。 * omSubtractive が指定された場合は減算合成が行われます(stNearestとstFastLinear以外で実装)。 * omMultiplicative が指定された場合は乗算合成が行われます(stNearestとstFastLinear以外で実装)。 * omDodge が指定された場合は覆い焼き合成が行われます(stNearestとstFastLinear以外で実装)。 * omDarken が指定された場合は比較(暗)合成が行われます(stNearestとstFastLinear以外で実装)。 * omLighten が指定された場合は比較(明)合成が行われます(stNearestとstFastLinear以外で実装)。 * omScreen が指定された場合はスクリーン乗算合成が行われます(stNearestとstFastLinear以外で実装)。 * omAlpha が指定された場合はアルファ合成が行われます。 * omAddAlpha が指定された場合は加算アルファ合成が行われます。この場合は、転送先の Layer.face プロパティが dfOpaque かつ Layer.holdAlpha プロパティが偽のとき、type 引数に stFastLinear を指定することにより線形補間が可能です。 * omOpaque が指定された場合は src のアルファ情報は無視され、src は常に完全不透明であると見なされます。この場合は、転送先の Layer.face プロパティが dfOpaque かつ Layer.holdAlpha プロパティが偽のとき、type 引数に stFastLinear を指定することにより線形補間が可能です。 |
    | opa | 演算の強度 ( 0 ～ 255 ) を指定します。 |
    | type | 拡大縮小のタイプを指定します。   * stNearest : 最近傍点法が用いられます * stFastLinear : 低精度の線形補間が用いられます(一部実装) * stSemiFastLinear : 固定小数線形補間が用いられます(1.3以降) * stLinear : 線形補間が用いられます(1.3以降実装変更) * stFastCubic : 固定小数３次元補間が用いられます(1.3以降) * stCubic : ３次元補間が用いられます(1.3以降実装変更) * stFastLanczos2 : 固定小数Lanczos補間の範囲4x4が用いられます(1.3以降) * stLanczos2 : Lanczos補間の範囲4x4が用いられます(1.3以降) * stFastLanczos3 : 固定小数Lanczos補間の範囲6x6が用いられます(1.3以降) * stLanczos3 : Lanczos補間の範囲6x6が用いられます(1.3以降) * stFastSpline16 : 固定小数スプライン補間4x4が用いられます(1.3以降) * stSpline16 : スプライン補間4x4が用いられます(1.3以降) * stFastSpline36 : 固定小数スプライン補間6x6が用いられます(1.3以降) * stSpline36 : スプライン補間6x6が用いられます(1.3以降) * stFastAreaAvg : 固定小数面積平均縮小が用いられます。拡大は出来ません(1.3以降) * stAreaAvg : 面積平均縮小が用いられます。拡大は出来ません(1.3以降) * stFastGaussian : 固定小数ガウス補間4x4が用いられます(1.3以降) * stGaussian : ガウス補間4x4が用いられます(1.3以降) * stFastBlackmanSinc : 固定小数Blackman-Sinc補間8x8が用いられます(1.3以降) * stBlackmanSinc : Blackman-Sinc補間8x8が用いられます(1.3以降)   速度は stNearest > stFastLinear > stLinear > stCubic の順に高速ですが、画質は速度が速ければ速いタイプほど低画質になります。  stCubic 以降の補間方法は十分高画質で好みの差とも言えます。  ただし、ガウス補間についてはぼやけたような画質になります。stFastLinear と他の線形補間(stSemiFastLinear と stLinear)の差は縮小時に大きく出ます。  stFastLinear は、常に周囲4画素を参照するのに対して、stSemiFastLinear、stLinear は、縮小時は等倍時の影響範囲が4画素となるような範囲、つまりより広い範囲の画素を参照し補間するためより高画質です(アルゴリズム的には本来の線形補間です)。  stFastLinear に対しては、stRefNoClip をビット論理和で追加指定することができ、この場合は、コピーするビットマップの領域外を参照して色を合成することを許可します。  これを指定しない場合は、転送元ビットマップの周囲に余裕があったとしても、転送元ビットマップの範囲外を参照することはありません(範囲外の色はもっとも近い位置にある範囲内のピクセルの色と見なされます)。 |
    | option | ３次元補間時のシャープネスです。  他の補間方法では現在のところ意味を持ちません。  シャープネスの値をプラス方向に大きくするとぼやけていき、マイナス方向に大きくしていくとシャープになっていきます。 |

戻り値
:   なし (void)

説明
:   指定された重ね合わせ元レイヤの矩形を、重ね合わせ先 ( メソッドを実行するレイヤ ) の矩形に演算合成します。
    重ね合わせ元矩形と重ね合わせ先矩形のサイズが異なる場合は拡大または縮小が行われます。
    mode に omAuto を指定した場合は、演算元レイヤのLayer.typeプロパティに従って演算の種類が自動的に決定されます。