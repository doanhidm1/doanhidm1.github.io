# RegExp.last

機能/意味
:   最後に test あるいは exec メソッドが実行された RegExp クラスのインスタンスです

タイプ
:   [RegExpクラス](class_RegExp)のプロパティ

説明
:   例 :
     `if(/pat(\d+)/.test(target)) { return RegExp.last.matches[1]; }`