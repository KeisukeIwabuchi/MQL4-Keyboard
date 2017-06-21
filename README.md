# MQL4-Keyboard
チャート上でのキーボード操作を管理するためのモジュール


## Install
1. Keyboard.mqhをダウンロード
2. データフォルダを開き、/MQL4/Includes/mql4_modules/Keyboard/Keyboard.mqhとして保存


## Usage
1. Keyboard.mqhを読み込む
2. Keyboard::KeyにOnChartEventのlparamを渡す
3. 押されたキーが返ってくる

### Keyメソッド
キーが押された際にKeyメソッドを実行してlparamを渡すと、どのキーが押されたのかを返す。

```cpp
void OnChartEvent(const int id, 
                  const long& lparam,  
                  const double& dparam,
                  const string& sparam
                  ) 
{
   if(id==CHARTEVENT_KEYDOWN) { 
      Comment(Keyboard::Key(lparam));
   }
}
```
