# tTJS とは

TJS2 スクリプトエンジンのクラスです。このクラスのオブジェクトを通して TJS2 を操作することができます。

# コンストラクタ

tTJS のコンストラクタに引数はありません。
　tTJS のオブジェクトは自動変数として作成できません。かならず new 演算子を用いて作成する必要があります。
　作成直後の 参照カウンタは 1 になっています。これはそのまま Release メソッドを呼べば tTJS のオブジェクトが解放されると言うことです。

# デストラクタ

tTJS のデストラクタは保護部にあり、アクセスできません。
　tTJS のオブジェクトを解放するには Release メソッドを使ってください。
　また、tTJS のオブジェクトを解放する前には Shutdown メソッドを呼ぶことが推奨されます。

# AddRef

void tTJS::AddRef()

　TJS2 スクリプトエンジンの参照カウンタをインクリメントします。

# Release

void tTJS::Release()

　TJS2 スクリプトエンジンの参照カウンタをデクリメントします。
　参照カウンタが 0 になれば tTJS オブジェクトは解放されます。

# Shutdown

void tTJS::Shutdown()

　スクリプトエンジンのシャットダウンを行います。

　TJS2 スクリプトエンジンを解放するとき、Release メソッドの前にこのメソッドを呼ぶことを推奨します。

# GetGlobal

iTJSDispatch2 \* tTJS::GetGlobal()

　global オブジェクトを取得します。[iTJSDispatch2 インターフェース](interface) 型のオブジェクトが返されます。
　このメソッドは global オブジェクトを返すとき、その参照カウンタをインクリメントします。

# GetGlobalNoAddRef

iTJSDispatch2 \* tTJS::GetGlobalNoAddRef()

　global オブジェクトを取得します。GetGlobal と違うのは、global オブジェクトの参照カウンタをインクリメントしないと言うことです。

# SetConsoleOutput

void tTJS::SetConsoleOutput(iTJSConsoleOutput \*console);

　コンソールの出力先を指定します。
　コンソールは、TJS2 の出すエラーメッセージなどが出力されるところです。

以下の引数があります。

console
:   コンソールの出力先を定義する、iTJSConsoleOutput 型のオブジェクトを指定します。
    　iTJSConsoleOutput 型は tjs.h に定義されている基本抽象クラスで、以下のメソッドがあります。

    void iTJSConsoleOutput::ExceptionPrint(const tjs\_char \*msg)
    :   例外に関する情報を出力するためのメソッドです。msg がメッセージを表します。

    void iTJSConsoleOutput::Print(const tjs\_char \*msg)
    :   その他の情報を出力するためのメソッドです。msg がメッセージを表します。

# GetConsoleOutput

tTJSConsoleOutput \* tTJS::GetConsoleOutput() const

　コンソールの出力先を取得します。

# OutputToConsole

void tTJS::OutputToConsole(const tjs\_char \*msg) const

　コンソールに文字列を出力します。msg は出力するメッセージです。

# OutpuExceptionToConsole

void tTJS::OutpuExceptionToConsole(const tjs\_char \*msg) const

　コンソールに例外の文字列を出力します。msg は出力するメッセージです。

# OutputToConsoleWithCentering

void tTJS::OutputToConsoleWithCentering(const tjs\_char \*msg, tjs\_uint width) const

　コンソールに文字列をセンタリングして出力します。msg は出力するメッセージで、width は横幅です。
　横幅よりも出力するメッセージの文字数が少ない場合は、指定した横幅の中央にセンタリングして出力します
( ただしすべての文字の幅を同一であると見なすため、全角が混じると崩れた表示になります )

# OutputToConsoleSeparator

void tTJS::OutputToConsoleSeparator(const tjs\_char \*text, tjs\_uint count) const

　text で示された区切り記号を、count 個、コンソールに出力します。

# Dump

void tTJS::Dump(tjs\_uint width = 80) const

　TJS2 の状態をコンソールに出力します。
　各スクリプトブロック中の仮想マシンコードの逆アセンブル結果などが表示されます。
　width には出力する横幅を指定します。

# ExecScript

void tTJS::ExecScript(
    const tjs\_char \*script,
    tTJSVariant \*result = NULL,
    iTJSDispatch2 \*context = NULL,
    const tjs\_char \*name = NULL,
    tjs\_int lineofs = 0
    )

void tTJS::ExecScript(
    const ttstr &script,
    tTJSVariant \*result = NULL,
    iTJSDispatch2 \*context = NULL,
    const tjs\_char \*name = NULL,
    tjs\_int lineofs = 0
    )

　スクリプトを実行します。

　以下の引数があります。

const tjs\_char \*script

const ttstr &script
:   実行するスクリプトを指定します。

tTJSVariant \*result
:   結果を受け取るための tTJSVariant 型の変数へのポインタを指定します。
    　NULL も指定できますが、NULL の場合は結果を受け取ることができません。

iTJSDispatch2 \*context
:   このスクリプトが実行されるコンテキストを指定します。
    　NULL を指定すると、スクリプトは global コンテキスト上で実行されます。
    　通常は NULL を指定しますが、スクリプトを特定のコンテキストで実行したい場合はそのコンテキストとなるオブジェクトを指定してください。

const tjs\_char \*name
:   スクリプトの名前を指定します。通常、そのスクリプトのファイル名を指定します。
    　例外の通知の際にどこのスクリプトで例外が起こったかを知らせたりする目的で使用されます。

tjs\_int lineofs
:   スクリプト中の、そのスクリプトの始まった行(0～)を指定します。
    　KAGシナリオ中に埋め込まれたTJSスクリプトのように、他のドキュメント中にTJSスクリプトが埋め込まれる場合に、そのTJSスクリプトの開始行を指定します。
    　例外の通知の際にどこのスクリプトで例外が起こったかを知らせたりする目的で使用されます。

# EvalExpression

void tTJS::EvalExpression(
    const tjs\_char \*expression,
    tTJSVariant \*result = NULL,
    iTJSDispatch2 \*context = NULL,
    const tjs\_char \*name = NULL
    tjs\_int lineofs = 0
    )

void tTJS::EvalExpression(
    const ttstr &expression,
    tTJSVariant \*result = NULL,
    iTJSDispatch2 \*context = NULL,
    const tjs\_char \*name = NULL
    tjs\_int lineofs = 0
    )

　式を評価します。
　引数については ExecScript を参照してください。

　if 演算子のように式の結果を得ることができない演算子の場合、その結果を得ようとして result に非 NULL を指定すると例外が発生します。この場合は result には NULL を指定する必要があります。

# SetPPValue

void tTJS::SetPPValue(const tjs\_char \*name, const tjs\_int32 value)

　条件コンパイル用の変数を設定します。name は変数の名前、value は設定する値です。

# GetPPValue

tjs\_int32 tTJS::GetPPValue(const tjs\_char \*name)

　条件コンパイル用の変数を取得します。name は変数の名前です。変数が見つからなかった場合は 0 が帰ります。

# DoGarbageCollection

tjs\_int32 tTJS::DoGarbageCollection()

　ガベージコレクションを行います。TJS2 が保持しているキャッシュをクリアしたり、未処理のクリーンアップ処理を完了させます。