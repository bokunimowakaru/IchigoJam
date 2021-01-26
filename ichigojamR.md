# IchigoJam Risc-V ファームウェアの書き込み

## デバイス側  

### Wio Lite RSIC-V  
	https://www.seeedstudio.com/Wio-Lite-RISC-V-GD32VF103-p-4293.html

##### 接続方法  

	J3 (16pin)
	pin 14: PA10_UART0_RX_D0
	pin 15: PA9_UART0_TX_D1
	pin 16: GND

##### 書き込み方法  

	BOOT0スイッチを「1」にして書き込み、「0」で動作。  

### Longan Nano  


--------------------------------------------------------------------------------

## 書き込み側  

### Windows  

	Windows用 stm32flash.exe
	https://github.com/IchigoJam/stm32flash
	stm32flash.exe -w ichigojam-r.bin -g 0 -e 112 -b 115200 /dev/ttyS2
	※COM3のとき

### Linux  

	$ git clone https://github.com/IchigoJam/stm32flash
	$ cd stm32flash
	$ make
	$ wget https://ichigojam.github.io/ichigojam-r-1.5b01.zip
	$ unzip ichigojam-r-1.5b01.zip
	$ ./stm32flash -w ichigojam-r.bin -g 0 -e 112 -b 115200 /dev/ttyUSB0

### petit15term  

	$ cd
	$ git clone https://bokunimo.net/git/petit15term
	$ cd petit15term
	$ make
	$ ./petit15term

--------------------------------------------------------------------------------

# git.bokunimo.com GitHub Pages site
[http://git.bokunimo.com/](http://git.bokunimo.com/)  

## IchigoJam GitHub Pages site
[http://git.bokunimo.com/IchigoJam/](http://git.bokunimo.com/IchigoJam/)  

--------------------------------------------------------------------------------

## 参考文献

IchigoJam BASIC 1.5β1、USBキーボード対応 RISC-V版 IchigoJam Rβ 出荷スタート！  
https://fukuno.jig.jp/3103

GitHub IchigoJam/doc  
https://github.com/IchigoJam/doc
