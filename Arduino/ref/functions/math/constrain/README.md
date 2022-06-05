# constrain()

ここは`constrain()` 関数のページです

# 説明

値が範囲内に収まるようにします

# 構文

`constrain(x, a, b)`

# パラメータ

`x`：決められた範囲内に収まるようにしたい値。すべてのデータ型を使えます  
`a`：指定する範囲の下限。すべてのデータ型を使えます  
`b`：指定する範囲の上限。すべてのデータ型を使えます  

# 返り値

`a ≦ x ≦ b`の場合`x`  
`x ＜ a`の場合`a`  
`b ＜ x`の場合`b`

# サンプルコード

このコードではセンサの値が10から150に収まるように操作しています

```cpp
sensVal = constrain(sensVal, 10, 150);
```

# 注意点

constrain関数の実装の都合上、括弧内で他の関数を実行するのは避けてください。思わぬ結果を招くことがあります

# 関連



# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/math/constrain/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
