# sq()

ここは`sq()` 関数のページです

# 説明

数値の二乗を計算します

# 構文

`sq(x)`

# パラメータ

`x`：二乗を計算させたい数字。すべてのデータ型が使えます  

# 返り値

$ x^2 $
の計算結果。データ型は`double`

# 注意点

`sq()`関数の実装の都合上、括弧内で他の関数を実行すると予期しない結果になることがあります

このコードでは誤った結果になります

```cpp
int inputSquared = sq(Serial.parseInt());  // これは避けて下さい
```

代わりに以下のコードを使用して下さい

```cpp
int input = Serial.parseInt();  // 他の関数を括弧の外で実行する
int inputSquared = sq(input);
```

# 関連

[double](./../../../constant/double)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/math/sq/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
