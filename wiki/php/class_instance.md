# GizumoFAQ

## 【Question】
クラスとインスタンスの関係性がよくわかりません

## 【Answer】
クラスは「設計図」、インスタンスは「実体」です。

### 【原因】

#### 【クラスとインスタンス】
クラスとインスタンスの違いを調べると、

> クラスは「設計図」、インスタンスは「実体」です。

という説明がよく出てきます。
ただ、この説明を聞いてもあまり良くわからないという方も多いと思います。
そこで、今回は、たい焼きに例えて説明をしていこうと思います！

---

まず、クラスは「 **たい焼きの金型** 」、インスタンスは「 **たい焼き自体** 」だと思ってください。

この **金型** （クラス）に **具材** (引数)を入れて、 **たい焼き** （インスタンス）を作ること（new）を「 **インスタンス化** 」と言います。

では、 **金型** （クラス）を作ることでプログラミングにおいてどんなメリットがあるのかをみていきましょう。

---

たい焼きの **金型** を作っておけば、 **小麦粉** と **あんこ** を入れれば「 **あんこたい焼き** 」。 **小麦粉** と **カスタード** を入れれば「 **カスタードたい焼き** 」を作ることができます。

これをコードにしてみると右の画像のようになります。

**たい焼き** を作る工程に **1000行** 必要だったとしても、一旦 **金型** を作っておけば、 **具材** （引数）を変えるだけで、色々な **たい焼き** を量産できますね！

![クラスあり](https://res.cloudinary.com/gizumo-inc/image/upload/v1669970979/curriculums/GizumoFAQ/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2022-11-26_18.53.28.png)

では、 **金型** がないとどうなるのか見ていきましょう。

**金型** がないので、 **3つ**のたい焼きを作るとしても、全て **0** から形を作っていかないといけません。

これをコードにしてみると、 **1つ** のたい焼きを作るのに **1000行** 必要だとすると、 **3つ** 作る為には **3000行** 必要になってしまいます。

![クラスなし](https://res.cloudinary.com/gizumo-inc/image/upload/v1669970986/curriculums/GizumoFAQ/%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88_2022-11-26_18.53.58.png)

プログラミングにおいて、 **インスタンス化** しないで、 **クラス** をそのまま使おうとする人がいます。

ただ、これは「 **たい焼きをください** 」と言って「 **たい焼きの金型** 」を渡されるようなものです。

 **クラス** を使用する際には、必ず **インスタンス化** をして、 **インスタンス** にしないと使えない理由はこれになります。


