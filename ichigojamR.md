# IchigoJam Risc-V ファームウェアの書き込み

--------------------------------------------------------------------------------

## デバイス側  

--------------------------------------------------------------------------------

### Wio Lite RSIC-V  
	https://www.seeedstudio.com/Wio-Lite-RISC-V-GD32VF103-p-4293.html

##### UART 接続方法  

	J3 (16 pin)
	pin 14: RXD : PA10_UART0_RX_D0
	pin 15: TXD : PA9_UART0_TX_D1
	pin 16: GND : GND

##### 書き込み方法  

	BOOT0スイッチを「1」にして書き込み、「0」で動作。  

##### I2C 接続方法  

	J4 (12 pin)
	pin 10: SDA : PB7_D5
	pin  5: SCL : PB6_D12
	pin  2: GND : GND

--------------------------------------------------------------------------------

### Longan Nano  

##### UART 接続方法  

	P2 (8 pin)
	pin  3: RXD : GD_UART0_RX
	pin  2: TXD : GD_UART0_TX
	pin  1: GND : GND

##### 書き込み方法  

	BOOT0スイッチを押しながらRESET。  

##### VIDEO 接続方法  

	P4 (18 pin) pin10 = N/A
	pin 18: GND         : GND
	pin 12: VIDEO2/COPI : GD_PB5	# 映像(100Ω)
	pin 11: VIDEO1/CIPO : GD_PB4	# 同期(470Ω)

##### I2C 接続方法  

	J4 (12 pin)
	pin 18: GND : GND
	pin 14: SDA : GD_PB7
	pin 13: SCL : GD_PB6

--------------------------------------------------------------------------------

## 書き込み側  

--------------------------------------------------------------------------------

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

[IchigoJam BASIC 1.5β1、USBキーボード対応 RISC-V版 IchigoJam Rβ 出荷スタート！]
(https://fukuno.jig.jp/3103)  

[GitHub IchigoJam/doc]
(https://github.com/IchigoJam/doc)  

[GitHub IchigoJam/doc/IchigoJam-R-pins.csv]
(https://github.com/IchigoJam/doc/blob/master/IchigoJam-R-pins.csv)

--------------------------------------------------------------------------------
