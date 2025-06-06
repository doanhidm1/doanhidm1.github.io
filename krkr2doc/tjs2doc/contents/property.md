# プロパティ

プロパティとは、変数と同じように扱うことができるが、実際はメソッド呼び出しと同様に、セッター ( setter ) とゲッター ( getter ) の呼び出しを伴うものです。セッターやゲッターを、プロパティハンドラと呼ぶ場合があります。

　構文は以下の通りです。

`property 識別子
{
    setter(引数)
    {
        // ここにセッターの内容
    }

    getter()
    {
        // ここにゲッターの内容
        return 式; // ゲッターとして返す値
    }
}`

　setter と getter は、逆の順番で書かれていてもかまいません。
　この property を記述したクラスや、グローバルのメンバとしてこのプロパティは登録されますが、この識別子からの値の取得はゲッター、値の設定はセッターを通して行われます。これらのセッターとゲッターは、メソッド同様に様々な内容を書くことができます。セッターは setter に続く ( ) 内に、値を受け取る変数を引数として書きます。ゲッターは return ステートメントにて値を返します。

　getterのあとの () は省略できます。

　一つの識別子に対し、セッターとゲッターの両方を書けば、読み書きの両方が可能なプロパティになります。一方しか書かない場合、たとえばゲッターしか書かない場合は、読み出し専用のプロパティとなり、書き込みはエラーになります。

`例:
    var value;

    property property1 // プロパティ 'property1' を宣言
    {
        setter(v)
        {
            // セッターはただ一つだけの引数をとる
            value=v; // 引数 v を処理する

            inform("value set.");
        }

        getter
        {
            // propset と同じ識別子 'property1' のゲッターを宣言
            // ゲッターに引数はない
            inform("value get.");
            return value; // 戻り値として返す
        }
    }

    property1=5; // property1 への代入は、セッターが呼ばれる
    property1++; // このような式では、ゲッターが呼ばれ、
                 // 次にセッターが呼ばれて値が設定される
}`

　プロパティも変数や関数やクラス同様、オーバーライドできます。

# プロパティオブジェクト

プロパティ自身も一つのオブジェクトです。しかし、なんらかのオブジェクトに登録されている場合は、普通のアクセス方法ではプロパティハンドラが呼ばれるだけであり、プロパティオブジェクトそのものにはアクセスできません。
　プロパティオブジェクトそのものを取り出すには `&` 演算子を使います。取り出したプロパティオブジェクトはローカル変数に入れることが出来ます。
　また、`&` 演算子を使ってプロパティオブジェクトを登録することもできます。

`例:
    property prop // プロパティ prop を宣言
    {
        (略)
    }

{
    var p = &prop; // プロパティオブジェクトを得てローカル変数に入れる

    &object.property1 = p; // p を object の property1 として登録する
}`

　`&` 演算子を使うと、ゲッターやセッターは呼ばれずにプロパティオブジェクトそのものにアクセスする事ができます。`&` 演算子を使わなければ通常のプロパティへのアクセスとなります。

　ローカル変数として取り出したプロパティオブジェクトは、オブジェクトに登録しなくとも、`*` 演算子を用いてプロパティハンドラを呼び出すことができます。

`例:
    property prop // プロパティ prop を宣言
    {
        (略)
    }

{
    var p = &prop; // プロパティオブジェクトを得てローカル変数に入れる

    *p = 30; // setter を呼び出し 30 を設定する
    func(*p); // getter を呼び出し値を取得し、func に渡す
}`

Note

上記のように var 変数にプロパティオブジェクトをとる場合は、変数はローカル変数にしてください。これは、プロパティオブジェクトはいったんオブジェクトに登録されると、プロパティオブジェクトとしてではなくプロパティとしてゲッターやセッターを介した動作をするようになるためです。つまり、ローカル変数ではなく、グローバル変数(＝globalのメンバ)やオブジェクトのメンバにプロパティオブジェクトを登録してしまうと、普通のプロパティと同じように振る舞うようになります。もちろんこのようにしてグローバル変数やオブジェクトのメンバに登録したプロパティオブジェクトを取り出すために & 演算子を使うのはかまいません。

プロパティオブジェクトに対して instanceof 演算子を "Property" を伴って使用した場合は真になります(上記の例で言うと、&prop instanceof "Property" は真)。