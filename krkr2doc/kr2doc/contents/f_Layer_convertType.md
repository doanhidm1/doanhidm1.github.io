# Layer.convertType

機能/意味
:   レイヤ画像表現形式の変換

タイプ
:   [Layerクラス](f_Layer)のメソッド

構文
:   convertType(from)

引数
:   |  |  |
    | --- | --- |
    | from | 変換元となる描画方式タイプを指定します。 |

戻り値
:   なし (void)

説明
:   レイヤ画像の形式を変換します。
    　このメソッドは、ltAlpha (dfAlpha) と ltAddAlpha (dfAddAlpha) のように、「レイヤの画像表現形式が異なるが同様の表現が可能なタイプ」間での画像表現形式の変換を行います。
    　たとえば、ltAlpha で表示しているレイヤのタイプをそのまま ltAddAlpha に変更しただけでは、アルファチャンネルと色情報の扱いが異なるので正常に表示されません。そのため、このメソッドを用い、dfAlpha から dfAddAlpha に変換を行う必要があります。
    　このメソッドでは、変換先の画像表現形式は [Layer.face](f_Layer_face) プロパティで指定した描画方式に対応した形式になります ([Layer.type](f_Layer_type)で指定するレイヤタイプではなくて、描画方式であることに注意してください )。
    　from 引数には、変換元の画像表現形式に対応する描画方式(dfで始まる定数; [Layer.face](f_Layer_face)参照)を指定します。from 引数には dfAuto は指定できません。
    　現在サポートされている変換は、dfAlpha→dfAddAlpha と dfAddAlpha→dfAlpha の変換です。dfAddAlpha→dfAlphaでは、変換により色情報が失われる場合があります。
    　このメソッドは、描画クリップ矩形の影響を受けません ( 常にレイヤ画像全体が影響を受けます )。