# isAlpha()

ここは`isAlpha()` 関数のページです

# 説明

渡された文字が数字かどうかを解析します  
`thisChar`が数字である場合`true`を返します

# 構文

`isAlpha(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

数字である場合：`true`  
数字でない場合：`false`  

# サンプルコード

```cpp
if (isDigit(myChar)) {  // myChar が数字かどうかを判断
  Serial.println("The character is a digit");
}
else {
  Serial.println("The character is not a digit");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/isdigit/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
