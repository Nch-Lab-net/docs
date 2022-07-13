# isAlphaNumeric()

ここは`isAlphaNumeric()` 関数のページです

# 説明

渡された文字（char）が文字・数字（Alpha・Number）かどうかを解析します  
`thisChar`が文字・数字（Alpha・Number）である場合`true`を返します

# 構文

`isAlphaNumeric(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

文字・数字（Alpha・Number）である場合：`true`  
文字・数字（Alpha・Number）でない場合：`false`

# サンプルコード

```cpp
if (isAlphaNumeric(myChar)) { // myChar が文字・数字かを判断
  Serial.println("The character is alphanumeric");
}
else {
  Serial.println("The character is not alphanumeric");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ]()を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
