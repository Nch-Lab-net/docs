# isControl()

ここは`isControl()` 関数のページです

# 説明

渡された文字が制御文字かどうかを解析します  
`thisChar`が制御文字である場合`true`を返します

# 構文

`isControl(thisChar)`

# パラメータ

`thisChar`：任意の文字（char）。データ型は`char`

# 返り値

制御文字である場合：`true`  
制御文字でない場合：`false`  

# サンプルコード

```cpp
if (isControl(myChar)) {  // myChar が制御文字かどうかを判断
  Serial.println("The character is a control character");
}
else {
  Serial.println("The character is not a control character");
}
```

# 関連

[char](./../../../constant/char)  
[if()](./../../../structure/control_structure/if)  
[while()](./../../../structure/control_structure/while)  
[read()](./../../Communication/Serial/read)  

# 出典

このページは[Arduino公式のページ](https://www.arduino.cc/reference/en/language/functions/characters/iscontrol/)を翻訳したものです（一部意訳を含みます）

[一覧に戻る](https://docs.nchlab.net/Arduino/ref/)  
