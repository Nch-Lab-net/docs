# isLowerCase()

ここは`isLowerCase()` 関数のページです

# 説明

渡された文字が子文字かどうかを解析します  
`thisChar`が子文字である場合`true`を返します

# 構文

`isLowerCase(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

子文字である場合：`true`  
子文字でない場合：`false`  

# サンプルコード

```cpp
if (isLowerCase(myChar)) {  // myChar が子文字かどうかを判断
  Serial.println("The character is lower case");
}
else {
  Serial.println("The character is not lower case");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/islowercase/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
