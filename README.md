# MQL4-Keyboard
Module that manages keyboard operations on the chart.


## Install
1. Download Keyboard.mqh
2. Save the file to /MQL4/Include/mql4_modules/Keyboard/Keyboard.mqh


## Usage
1. Include Keyboard.mqh
2. Pass lparam (this is a OnChartEvent function argument) as an argument to the Keyboard::Key.
3. Keyboard::Key returns which key was pressed.

### Key method
Keyboard::Key tells you which key was pressed.

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
