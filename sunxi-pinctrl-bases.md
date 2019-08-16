
## sunxi-h5 pin group offsets

```c
#define PA_BASE	0
#define PB_BASE	32
#define PC_BASE	64
#define PD_BASE	96
#define PE_BASE	128
#define PF_BASE	160
#define PG_BASE	192
#define PH_BASE	224
#define PI_BASE	256
#define PL_BASE	352
#define PM_BASE	384
#define PN_BASE	416
```

Pin# | Name                 | Linux gpio |   Pin# |   Name               |   Linux gpio
-----|----------------------|------------|--------|----------------------|--------------------------
1    |   SYS_3.3V           |            |   2    |   VDD_5V             |   
3    |   I2C0_SDA / GPIOA12 |            |   4    |   VDD_5V             |   
5    |   I2C0_SCL / GPIOA11 |            |   6    |   GND                |   
7    |   GPIOG11            | 203 ->     |   8    |   UART1_TX / GPIOG6  |   198
9    |   GND                |            |   10   |   UART1_RX / GPIOG7  |   199
11   |   UART2_TX / GPIOA0  |   0        |   12   |   GPIOA6             |   6
13   |   UART2_RTS / GPIOA2 |   2        |   14   |   GND                |   
15   |   UART2_CTS / GPIOA3 |   3        |   16   |   UART1_RTS / GPIOG8 |   200
17   |   SYS_3.3V           |            |   18   |   UART1_CTS / GPIOG9 |   201
19   |   SPI0_MOSI / GPIOC0 |   64       |   20   |   GND                |   
21   |   SPI0_MISO / GPIOC1 |   65       |   22   |   UART2_RX / GPIOA1  |   1
23   |   SPI0_CLK / GPIOC2  |   66       |   24   |   SPI0_CS / GPIOC3   |   67 
