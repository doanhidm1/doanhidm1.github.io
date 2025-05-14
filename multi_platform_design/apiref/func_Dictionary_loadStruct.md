# Dictionary.loadStruct

機能/意味
:   ファイルから構造化されたデータの入力を行います

タイプ
:   [Dictionaryクラス](class_Dictionary)のメソッド

構文
:   loadStruct(storage:string, mode:string=null) :Dictionary

引数
:   |  |  |
    | --- | --- |
    | storage | 読み込むファイル名 |
    | mode | ファイルを読み込む際のモード文字列を指定します。   * "o" に続いてオフセットを10進で指定するとファイルのそのバイト位置からの書き込みになります。 |

戻り値
:   読み込んだ Dictionary か Array クラスのオブジェクトを返します。

説明
:   構造化されたデータをファイルから辞書配列、もしくは配列として読み込みます。
    テキスト形式、バイナリ形式の両方で読み込めます。
    クラスメソッドです。

参照
:   [Array.loadStruct](func_Array_loadStruct)