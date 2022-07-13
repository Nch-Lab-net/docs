# isAscii()

ここは`isAscii()` 関数のページです

# 説明

文字がASCII文字かどうかを解析します  
`thisChar`がASCII文字である場合`true`を返します

# 構文

`isAscii(thisChar)`

# パラメータ

`thisChar`：任意の文字。データ型は`char`

# 返り値

ASCII文字である場合：`true`
ASCII文字でない場合：`false`

# サンプルコード

```cpp
if (isAscii(myChar)) {  // myChar がASCII文字かどうかを判断
  Serial.println("The character is Ascii");
}
else {
  Serial.println("The character is not Ascii");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/isascii/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
