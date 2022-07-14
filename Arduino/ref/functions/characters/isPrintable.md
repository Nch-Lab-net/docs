# isPrintable()

ここは`isPrintable()` 関数のページです

# 説明

渡された文字が印刷可能（`serial.print()`等）かどうかを解析します。出力可能であれば空白であっても印刷可能となります  
`thisChar`が印刷可能な場合`true`を返します

# 構文

`isPrintable(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

印刷可能である場合：`true`  
印刷可能でない場合：`false`  

# サンプルコード

```cpp
if (isPrintable(myChar)) {  // myChar が印刷可能かどうかを判断
  Serial.println("The character is printable");
}
else {
  Serial.println("The character is not printable");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/isprintable/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
