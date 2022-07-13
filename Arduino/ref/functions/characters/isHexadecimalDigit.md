# isHexadecimalDigit()

ここは`isHexadecimalDigit()` 関数のページです

# 説明

渡された文字が16進数の数字（0 ~ 9, A ~ F）かどうかを解析します  
`thisChar`が16進数の数字である場合`true`を返します

# 構文

`isHexadecimalDigit(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

16進数での数字である場合：`true`  
16進数での数字でない場合：`false`  

# サンプルコード

```cpp
if (isHexadecimalDigit(myChar)) {  // myChar が16進数の数字かどうかを判断
  Serial.println("The character is a hexadecimal digit");
}
else {
  Serial.println("The character is not a hexadecimal digit");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/isHexadecimalDigit/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
