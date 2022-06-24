# Digispark 関連のメモ置き場

<h3><div align="right">最終更新：2022/06/24</div></h3>

## 文字列を送信する

前提条件
- `text[]`という配列に送信したい文字列を格納する  
- また、文字列を送信したいときに`sendText()`関数を呼び出す

```cpp
#include <DigiKeyboard.h>

uint8_t text[] = "Hello Arduino";

void setup() {
  //省略:
}

void loop() {
  //省略:
}

void sendText() {
  DigiKeyboard.sendKeyStroke(0);
  DigiKeyboard.delay(5);
  for (uint8_t i = 0; i < sizeof(Text_1) - 1; i++) {
    DigiKeyboard.print(Text_1[i]);
  }
}
```
`DigiKeyboard.sendKeyStroke(0);`はキー送信時の脱落防止のためのおまじないみたいなもので、  
繰り返し回数を`sizeof(Text_1) - 1`にしてるのはヌル終端を除いて送信するためです  
あとは見ての通り

## 複数のキーを同時に使う

```cpp
//ctrl + S:
DigiKeyboard.sendKeySroke(KEY_S, MOD_CTRL_LEFT);

//Alt + F4:
DigiKeyboard.sendKeySroke(KEY_F4, MOD_ALT_LEFT);

//Win + shift + S:
DigiKeyboard.sendKeySroke(KEY_S, MOD_GUI_LEFT | MOD_SHIFT_LEFT);
```

まあ見ての通り、`DigiKeyboard.sendKeySroke(KEY_hoge, MOD_fuga);`という構文です  
ちなみに、`hoge`と`fuga`に当てはまるのは[DigiKeyboard.h](https://github.com/digistump/DigisparkArduinoIntegration/blob/master/libraries/DigisparkKeyboard/DigiKeyboard.h)を見る限り以下の表の通りになります

| hoge | 使うときの文字 | 定義内容 |
|----|----|----|
| A | KEY_A | 4 |
| B | KEY_B | 5 |
| C | KEY_C | 6 |
| X | KEY_X | 27 |
| Y | KEY_Y | 28 |
| Z | KEY_Z | 29 |
| 1 | KEY_1 | 30 |
| 2 | KEY_2 | 31 |
| 9 | KEY_9 | 38 |
| 0 | KEY_0 | 39 |
| Enterキー | KEY_ENTER | 40 |
| Spaceキー | KEY_SPACE | 44 |
| F1 | KEY_F1 | 58 |
| F2 | KEY_F2 | 59 |
| F11 | KEY_F11 | 68 |
| F12 | KEY_F12 | 69 |

| fuga | 使うときの文字 | 定義内容 |
|----|----|----|
| ctrlキー（左） | MOD_CONTROL_LEFT | 1 << 0 |
| shiftキー（左） | MOD_SHIFT_LEFT | 1 << 1 |
| Altキー（左） | MOD_ALT_LEFT | 1 << 2 |
| Windowsキー（左） | MOD_GUI_LEFT | 1 << 3 |
| ctrlキー（右） | MOD_CONTROL_RIGHT | 1 << 4 |
| shiftキー（右） | MOD_SHIFT_RIGHT | 1 << 5 |
| Altキー（右） | MOD_ALT_RIGHT | 1 << 6 |
| Windowsキー（右） | MOD_GUI_RIGHT | 1 << 7 |

<footer><div align="right">© Nch-Lab</div></footer>
