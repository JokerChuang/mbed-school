# 第 2 章：認識 GPIO

## 電子零件介紹

準備材料如下：

1. ARM mbed LPC 1768 開發版
2. 麵包板 x 1
3. 紅色導線 x 1，黑色導線 x 1
4. LED x 1

![圖 2.1：本章節使用的零件](http://i.imgur.com/5iD2ehn.jpg)

圖 2.1：本章節使用的零件

## LED 通電測試

依照以下步驟進行 LED 通電測試：

![圖 2.2：將 LPC 1768 開發版插上麵包板](http://i.imgur.com/2Nx0FSh.jpg)

圖 2.2：將 LPC 1768 開發版插上麵包板

![圖 2.3：LED 有兩支針腳，一長一短，長的接正極，短的接負極](http://i.imgur.com/GzFrp2W.jpg)

圖 2.3：LED 有兩支針腳，一長一短，長的接正極，短的接負極

![圖 2.4：紅色導線一端接到 LPC 1768 開發版 3.3v Regulated Out 的針腳，另一端接到麵包板上的正極](http://i.imgur.com/mJZWmMH.jpg)

圖 2.4：紅色導線一端接到 LPC 1768 開發版 3.3v Regulated Out 的針腳，另一端接到麵包板上的正極

![圖 2.5：黑色導線一端接到 LPC 1768 開發版 GND 的針腳，另一端接到麵包板上的負極](http://i.imgur.com/aszlXqG.jpg)

圖 2.5：黑色導線一端接到 LPC 1768 開發版 GND 的針腳，另一端接到麵包板上的負極

![圖 2.6：LED 針腳長端插上麵包板正極，短端插上麵包板負極](http://i.imgur.com/3Duw0rK.jpg)

圖 2.6：LED 針腳長端插上麵包板正極，短端插上麵包板負極

![圖 2.7：LED 點亮，測試成功](http://i.imgur.com/Iom5KME.jpg)

圖 2.7：LED 點亮，測試成功

## 實習：以 DigitalOut 控制 LED 

![圖 2.8：將 LPC 1768 開發版 插上麵包板](http://i.imgur.com/2Nx0FSh.jpg)

圖 2.8：將 LPC 1768 開發版 插上麵包板

![圖 2.9：紅色導線一端接到 LPC 1768 開發版 GND 針腳，另一端接到麵包板上的正極](http://i.imgur.com/LT0xdWQ.jpg)

圖 2.9：紅色導線一端接到 LPC 1768 開發版 GND 針腳，另一端接到麵包板上的正極

![圖 2.10：LED 針腳長端插上 PwmOut 21~26 任意一個針腳，針腳短端插上麵包板正極](http://i.imgur.com/99qiOYr.jpg)

圖 2.10：LED 針腳長端插上 PwmOut 21~26 任意一個針腳，針腳短端插上麵包板正極

4. 撰寫程式碼

```
#include "mbed.h"

DigitalOut myled(p21);

int main() {
    wait(0.8);
    
    while(1) {    
        myled = 1;
        wait(0.2);
        myled = 0;
        wait(0.2);
    }
}

```

本範例程式下載網址：

```

https://developer.mbed.org/users/mbedschool/code/ch2_mbed_led_control/

```

![圖 2.11：測試成功](http://i.imgur.com/GV3hZjz.jpg)

圖 2.11：測試成功

## 延伸練習

![圖 2.12：LED 瓢蟲](http://i.imgur.com/zo38TF0.jpg)

圖 2.12：LED 瓢蟲

試著做看看吧！