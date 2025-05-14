# Layer.joinFocusChain

機能/意味
:   フォーカスチェーンに参加するか

タイプ
:   [Layerクラス](f_Layer)のプロパティ (読み書き可能)

説明
:   フォーカスチェーンに参加するかどうかを表します。
    　真を指定するとフォーカスチェーンに参加し、[Layer.prevFocusable](f_Layer_prevFocusable) などに
    現れるようになったり、TAB キーなどでそのレイヤにフォーカスを移動したりできるように
    なります。
    　偽を指定するとフォーカスチェーンには参加しませんが、フォーカスを [Layer.focus](f_Layer_focus) メソッドなどで受け取ることはできます。