# RegExp.exec

機能/意味
:   引数に指定した文字列に正規表現パターンマッチングを行い、マッチした結果を含む配列を返します

タイプ
:   [RegExpクラス](class_RegExp)のメソッド

構文
:   exec(text:string) :Array

引数
:   |  |  |
    | --- | --- |
    | text | 文字列 |

戻り値
:   パターンにマッチしない場合、配列の要素数は 0 になります。
    マッチした場合、要素 0 (最初の要素) はマッチした部分全体、それ以降の要素は各マッチ部分 ( 正規表現パターン中の ( ) で指定した部分 ) が入っています。

説明
:   このメソッドはこのオブジェクトの各プロパティの値を更新します。