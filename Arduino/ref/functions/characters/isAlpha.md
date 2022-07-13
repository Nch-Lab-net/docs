# isAlpha()

ここは`isAlpha()` 関数のページです

# 説明

渡された文字（char）が文字（Alpha）であるかどうかを解析します  
`thisChar`が文字（Alpha）である場合`true`を返します

# 構文

`isAlpha(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

文字（Alpha）である場合：`true`  
文字（Alpha）でない場合：`false`  

# サンプルコード

```cpp
if (isAlpha(myChar)) {  // myChar が文字かどうかを判断
  Serial.println("The character is a letter");
}
else {
  Serial.println("The character is not a letter");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/isalpha/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
