---
sidebar_position: 1
description: "Detailed hardware information for ROCK 5B/5B+"
---

# Hardware Interface Description

## Chip block diagram

<img src="/img/rock5b/rk3588-block-diagram.webp" alt="rk3588 system diagram" width="700" />

## Physical photographs

<Tabs queryString="versions">
    <TabItem value="ROCK 5B">
        <img src="/img/rock5b/rock-5b-overview-v1-45.webp" alt="rock 5b overview" width="700" />
    </TabItem>
    <TabItem value="ROCK 5B+">
        <img src="/img/rock5b/rock5b-plus-overview.webp" alt="rock 5b+ overview" width="700" />
    </TabItem>
</Tabs>

## Interface details

### eMMC

<div className='gpio_style'>

|       Name       | Pin# | Pin# |    Name    |
| :--------------: | :--: | :--: | :--------: |
|       GND        |  1   |  34  |    GND     |
|     EMMC_D5      |  2   |  33  |  eMMC_D6   |
|       GND        |  3   |  32  |    GND     |
|     EMMC_D4      |  4   |  31  |  eMMC_D7   |
|       GND        |  5   |  30  |    GND     |
|     EMMC_D0      |  6   |  29  |  eMMC_D1   |
|       GND        |  7   |  28  |    GND     |
|     EMMC_CLK     |  8   |  27  |  eMMC_D2   |
|       GND        |  9   |  26  |    GND     |
|     EMMC_D3      |  10  |  25  |  eMMC_CMD  |
|       GND        |  11  |  24  |    GND     |
|    EMMC_RSTN     |  12  |  23  | VCC_3V3_S3 |
|       GND        |  13  |  22  | VCC_3V3_S3 |
|       GND        |  14  |  21  | VCC_1V8_S3 |
| eMMC_DATA_STROBE |  15  |  20  | VCC_1V8_S3 |
|       GND        |  16  |  19  |    GND     |
|       GND        |  17  |  18  |    GND     |
|                  |      |      |    GND     |
|       GND        |  35  |      |    GND     |
|       GND        |  36  |      |    GND     |
|       GND        |  37  |      |    GND     |
|       GND        |  38  |      |    GND     |
|       GND        |  39  |      |    GND     |
|       GND        |  40  |      |    GND     |
|       GND        |  41  |      |    GND     |
|       GND        |  42  |      |    GND     |
|       GND        |  43  |      |    GND     |
|       GND        |  44  |      |    GND     |
|       GND        |  45  |      |    GND     |
|       GND        |  46  |      |    GND     |
|       GND        |  47  |      |    GND     |
|       GND        |  48  |      |    GND     |
|       GND        |  49  |      |    GND     |

</div>

### FAN Header

### GPIO

- GPIO Voltage

| GPIO       | Voltage | MAX   |
| ---------- | ------- | ----- |
| All GPIO   | 3.3V    | 3.63V |
| SARADC_IN4 | 3.3V    | 1.8V  |

- GPIO Pinout

<Tabs queryString="versions">
    <TabItem value="ROCK 5B">
        <div className='gpio_style' style={{ overflow :"auto"}} >

        | GPIO number |  Function8  |  Function7   |  Function6   |  Function5  |   Function4   |  Function3  | Function2  | Function1 |               Pin#               |              Pin#               | Function1  | Function2  | Function3  |                 Function4                 |  Function5  |  Function6   |  Function7   | Function8 | GPIO number |
        | :---------: | :---------: | :----------: | :----------: | :---------: | :-----------: | :---------: | :--------: | :-------: | :------------------------------: | :-----------------------------: | :--------: | :--------: | :--------: | :---------------------------------------: | :---------: | :----------: | :----------: | :-------: | :---------: |
        |             |             |              |              |             |               |             |            |   +3.3V   | <div className='yellow'>1</div>  |  <div className='red'>2</div>   |   +5.0V    |            |            |                                           |             |              |              |           |             |
        |     139     |             |              | I2S1_SDO2_M0 | I2C7_SDA_M3 | UART8_CTSN_M0 | PWM15_IR_M1 |            | GPIO4_B3  |  <div className='green'>3</div>  |  <div className='red'>4</div>   |   +5.0V    |            |            |                                           |             |              |              |           |             |
        |     138     |             |              | I2S1_SDO1_M0 | I2C7_SCL_M3 | UART8_RTSN_M0 |  PWM14_M1   |            | GPIO4_B2  |  <div className='green'>5</div>  | <div className='black'>6</div>  |    GND     |            |            |                                           |             |              |              |           |             |
        |     115     |             | SPI1_CS1_M1  |              | I2C8_SDA_M4 | UART7_CTSN_M1 | PWM15_IR_M0 |            | GPIO3_C3  |  <div className='green'>7</div>  | <div className='green'>8</div>  |  GPIO0_B5  |            |            | <div className='orange'>UART2_TX_M0</div> | I2C1_SCL_M0 | I2S1_MCLK_M1 |              |           |     13      |
        |             |             |              |              |             |               |             |            |    GND    |  <div className='black'>9</div>  | <div className='green'>10</div> |  GPIO0_B6  |            |            | <div className='orange'>UART2_RX_M0</div> | I2C1_SDA_M0 | I2S1_SCLK_M1 |              |           |     14      |
        |     113     |             | SPI1_CLK_M1  |              |             |  UART7_RX_M1  |             |            | GPIO3_C1  | <div className='green'>11</div>  | <div className='green'>12</div> |  GPIO3_B5  |            |  PWM12_M0  |                UART3_TX_M1                |             | I2S2_SCLK_M1 |              |           |     109     |
        |     111     |             | SPI1_MOSI_M1 |              | I2C3_SCL_M1 |               |             |            | GPIO3_B7  | <div className='green'>13</div>  | <div className='black'>14</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     112     |             | SPI1_MISO_M1 |              | I2C3_SDA_M1 |  UART7_TX_M1  |             |            | GPIO3_C0  | <div className='green'>15</div>  | <div className='green'>16</div> |  GPIO3_A4  |            |            |                                           |             |              |              |           |     100     |
        |             |             |              |              |             |               |             |            |   +3.3V   | <div className='yellow'>17</div> | <div className='green'>18</div> |  GPIO4_C4  |            |  PWM5_M2   |                                           |             |              | SPI3_MISO_M0 |           |     148     |
        |     42      |             | SPI0_MOSI_M2 |              |             |  UART4_RX_M2  |             |            | GPIO1_B2  | <div className='green'>19</div>  | <div className='black'>20</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     41      |             | SPI0_MISO_M2 |              |             |               |             |            | GPIO1_B1  | <div className='green'>21</div>  | <div className='green'>22</div> | SARADC_IN4 |            |            |                                           |             |              |              |           |             |
        |     43      |             | SPI0_CLK_M2  |              |             |  UART4_TX_M2  |             |            | GPIO1_B3  | <div className='green'>23</div>  | <div className='green'>24</div> |  GPIO1_B4  |            |            |                UART7_RX_M2                |             |              | SPI0_CS0_M2  |           |     44      |
        |             |             |              |              |             |               |             |            |    GND    | <div className='black'>25</div>  | <div className='green'>26</div> |  GPIO1_B5  |            |            |                UART7_TX_M2                |             |              | SPI0_CS1_M2  |           |     45      |
        |     150     |             | SPI3_CLK_M0  |              | I2C0_SDA_M1 |               | PWM7_IR_M3  |            | GPIO4_C6  |  <div className='blue'>27</div>  | <div className='blue'>28</div>  |  GPIO4_C5  |            |  PWM6_M2   |                                           | I2C0_SCL_M1 |              | SPI3_MOSI_M0 |           |     149     |
        |     63      |             |              |              |             | UART1_CTSN_M1 | PWM15_IR_M3 |            | GPIO1_D7  | <div className='green'>29</div>  | <div className='black'>30</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     47      | SPDIF_TX_M0 |              |              |             |  UART1_RX_M1  |  PWM13_M2   |            | GPIO1_B7  | <div className='green'>31</div>  | <div className='green'>32</div> |  GPIO3_C2  |            |  PWM14_M0  |               UART7_RTSN_M1               | I2C8_SCL_M4 |              | SPI1_CS0_M1  |           |     114     |
        |     103     |             |              |              |             |               |   PWM8_M0   |            | GPIO3_A7  | <div className='green'>33</div>  | <div className='black'>34</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     110     |             |              | I2S2_LRCK_M1 |             |  UART3_RX_M1  |  PWM13_M0   |            | GPIO3_B6  | <div className='green'>35</div>  | <div className='green'>36</div> |  GPIO3_B1  |            |  PWM2_M1   |                UART2_TX_M2                |             |              |              |           |     105     |
        |             |             |              |              |             |               |             |            | GPIO0_A0  | <div className='green'>37</div>  | <div className='green'>38</div> |  GPIO3_B2  |            | PWM3_IR_M1 |                UART2_RX_M2                |             | I2S2_SDI_M1  |              |           |     106     |
        |             |             |              |              |             |               |             |            |    GND    | <div className='black'>39</div>  | <div className='green'>40</div> |  GPIO3_B3  |            |            |                UART2_RTSN                 |             | I2S2_SDO_M1  |              |           |     107     |

        </div>
    </TabItem>
    <TabItem value="ROCK 5B+">
        <div className='gpio_style' style={{ overflow :"auto"}} >

        | GPIO number |  Function8  |  Function7   |  Function6   |  Function5  |   Function4   |  Function3  | Function2  | Function1 |               Pin#               |              Pin#               | Function1  | Function2  | Function3  |                 Function4                 |  Function5  |  Function6   |  Function7   | Function8 | GPIO number |
        | :---------: | :---------: | :----------: | :----------: | :---------: | :-----------: | :---------: | :--------: | :-------: | :------------------------------: | :-----------------------------: | :--------: | :--------: | :--------: | :---------------------------------------: | :---------: | :----------: | :----------: | :-------: | :---------: |
        |             |             |              |              |             |               |             |            |   +3.3V   | <div className='yellow'>1</div>  |  <div className='red'>2</div>   |   +5.0V    |            |            |                                           |             |              |              |           |             |
        |     139     |             |              | I2S1_SDO2_M0 | I2C7_SDA_M3 | UART8_CTSN_M0 | PWM15_IR_M1 |            | GPIO4_B3  |  <div className='green'>3</div>  |  <div className='red'>4</div>   |   +5.0V    |            |            |                                           |             |              |              |           |             |
        |     138     |             |              | I2S1_SDO1_M0 | I2C7_SCL_M3 | UART8_RTSN_M0 |  PWM14_M1   |            | GPIO4_B2  |  <div className='green'>5</div>  | <div className='black'>6</div>  |    GND     |            |            |                                           |             |              |              |           |             |
        |     115     |             | SPI1_CS1_M1  |              | I2C8_SDA_M4 | UART7_CTSN_M1 | PWM15_IR_M0 |            | GPIO3_C3  |  <div className='green'>7</div>  | <div className='green'>8</div>  |  GPIO0_B5  |            |            | <div className='orange'>UART2_TX_M0</div> | I2C1_SCL_M0 | I2S1_MCLK_M1 |              |           |     13      |
        |             |             |              |              |             |               |             |            |    GND    |  <div className='black'>9</div>  | <div className='green'>10</div> |  GPIO0_B6  |            |            | <div className='orange'>UART2_RX_M0</div> | I2C1_SDA_M0 | I2S1_SCLK_M1 |              |           |     14      |
        |     113     |             | SPI1_CLK_M1  |              |             |  UART7_RX_M1  |             |            | GPIO3_C1  | <div className='green'>11</div>  | <div className='green'>12</div> |  GPIO3_B5  |            |  PWM12_M0  |                UART3_TX_M1                |             | I2S2_SCLK_M1 |              |           |     109     |
        |     111     |             | SPI1_MOSI_M1 |              | I2C3_SCL_M1 |               |             |            | GPIO3_B7  | <div className='green'>13</div>  | <div className='black'>14</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     112     |             | SPI1_MISO_M1 |              | I2C3_SDA_M1 |  UART7_TX_M1  |             |            | GPIO3_C0  | <div className='green'>15</div>  | <div className='green'>16</div> |  GPIO3_A4  |            |            |                                           |             |              |              |           |     100     |
        |             |             |              |              |             |               |             |            |   +3.3V   | <div className='yellow'>17</div> | <div className='green'>18</div> |  GPIO4_C4  |            |  PWM5_M2   |                                           |             |              | SPI3_MISO_M0 |           |     148     |
        |     42      |             | SPI0_MOSI_M2 |              |             |  UART4_RX_M2  |             |            | GPIO1_B2  | <div className='green'>19</div>  | <div className='black'>20</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     41      |             | SPI0_MISO_M2 |              |             |               |             |            | GPIO1_B1  | <div className='green'>21</div>  | <div className='green'>22</div> | SARADC_IN4 |            |            |                                           |             |              |              |           |             |
        |     43      |             | SPI0_CLK_M2  |              |             |  UART4_TX_M2  |             |            | GPIO1_B3  | <div className='green'>23</div>  | <div className='green'>24</div> |  GPIO1_B4  |            |            |                UART7_RX_M2                |             |              | SPI0_CS0_M2  |           |     44      |
        |             |             |              |              |             |               |             |            |    GND    | <div className='black'>25</div>  | <div className='green'>26</div> |  GPIO1_B5  |            |            |                UART7_TX_M2                |             |              | SPI0_CS1_M2  |           |     45      |
        |     150     |             | SPI3_CLK_M0  |              | I2C0_SDA_M1 |               | PWM7_IR_M3  |            | GPIO4_C6  |  <div className='blue'>27</div>  | <div className='blue'>28</div>  |  GPIO4_C5  |            |  PWM6_M2   |                                           | I2C0_SCL_M1 |              | SPI3_MOSI_M0 |           |     149     |
        |     35      |             |              |              | I2C4_SCL_M3 |               |  PWM1_M2    |            | GPIO1_A3  | <div className='green'>29</div>  | <div className='black'>30</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     34      |             |              |              | I2C4_SDA_M3 |               |  PWM0_M2    |            | GPIO1_A2  | <div className='green'>31</div>  | <div className='green'>32</div> |  GPIO3_C2  |            |  PWM14_M0  |               UART7_RTSN_M1               | I2C8_SCL_M4 |              | SPI1_CS0_M1  |           |     114     |
        |     103     |             |              |              |             |               |   PWM8_M0   |            | GPIO3_A7  | <div className='green'>33</div>  | <div className='black'>34</div> |    GND     |            |            |                                           |             |              |              |           |             |
        |     110     |             |              | I2S2_LRCK_M1 |             |  UART3_RX_M1  |  PWM13_M0   |            | GPIO3_B6  | <div className='green'>35</div>  | <div className='green'>36</div> |  GPIO3_B1  |            |  PWM2_M1   |                UART2_TX_M2                |             |              |              |           |     105     |
        |             |             |              |              |             |               |             |            | GPIO0_A0  | <div className='green'>37</div>  | <div className='green'>38</div> |  GPIO3_B2  |            | PWM3_IR_M1 |                UART2_RX_M2                |             | I2S2_SDI_M1  |              |           |     106     |
        |             |             |              |              |             |               |             |            |    GND    | <div className='black'>39</div>  | <div className='green'>40</div> |  GPIO3_B3  |            |            |                UART2_RTSN                 |             | I2S2_SDO_M1  |              |           |     107     |

        </div>
    </TabItem>

</Tabs>

### Gigabit Ethernet

### Maskrom Button

### MIPI CSI

<Tabs queryString="versions">
    <TabItem value="ROCK 5B">
        <div className='gpio_style' style={{ overflow :"auto"}} >

| Pin# | Name               | Pin# | Name               |
| :--: | :----------------- | :--: | :----------------- |
|  1   | GND                |  17  | MIPI_CSI0_RX_CLK0N |
|  2   | MIPI_CSI0_RX_D3N   |  18  | MIPI_CSI0_RX_CLK0P |
|  3   | MIPI_CSI0_RX_D3P   |  19  | GND                |
|  4   | GND                |  20  | MIPI_CAM3_CLKOUT   |
|  5   | MIPI_CSI0_RX_D2N   |  21  | GND                |
|  6   | MIPI_CSI0_RX_D2P   |  22  | MIPI_CAM1_CLKOUT   |
|  7   | GND                |  23  | MIPI_CSI0_PDN0_H   |
|  8   | MIPI_CSI0_RX_CLK1N |  24  | I2C3_SCL_M0_MIPI   |
|  9   | MIPI_CSI0_RX_CLK1P |  25  | I2C3_SDA_M0_MIPI   |
|  10  | GND                |  26  | MIPI_CSI0_PDN1_H   |
|  11  | MIPI_CSI0_RX_D1N   |  27  | CM_RST_L           |
|  12  | MIPI_CSI0_RX_D1P   |  28  | VCC_3V3_S3         |
|  13  | GND                |  29  | VCC_3V3_S3         |
|  14  | MIPI_CSI0_RX_D0N   |  30  | VCC5V0_SYS         |
|  15  | MIPI_CSI0_RX_D0P   |  31  | VCC5V0_SYS         |
|  16  | GND                |

        </div>
    </TabItem>

<TabItem value="ROCK 5B+">
        <div className='gpio_style' style={{ overflow :"auto"}} >
#### CAM0
| Pin# | Name                    | Pin# | Name                      |
| :--: | :---------------------- | :--: | :------------------------ |
|  1   | GND                     |  17  | MIPI_CSI0_RX_CLK0N        |
|  2   | MIPI_CSI0_RX_D3N        |  18  | MIPI_CSI0_RX_CLK0P        |  
|  3   | MIPI_CSI0_RX_D3P        |  19  | GND                       |
|  4   | GND                     |  20  | MIPI_CAM3_CLKOUT          |
|  5   | MIPI_CSI0_RX_D2N        |  21  | GND                       |
|  6   | MIPI_CSI0_RX_D2P        |  22  | MIPI_CAM1_CLKOUT          |
|  7   | GND                     |  23  | MIPI_CSI0_PDN0_H          |
|  8   | MIPI_CSI0_RX_CLK1N      |  24  | I2C3_SCL_M0_MIPI          |
|  9   | MIPI_CSI0_RX_CLK1P      |  25  | I2C3_SDA_M0_MIPI          |
|  10  | GND                     |  26  | MIPI_CSI0_PDN1_H          |
|  11  | MIPI_CSI0_RX_D1N        |  27  | CM_RST_L_1                |
|  12  | MIPI_CSI0_RX_D1P        |  28  | VCC_3V3_S3                |
|  13  | GND                     |  29  | VCC_3V3_S3                |
|  14  | MIPI_CSI0_RX_D0N        |  30  | VCC_5V                    |
|  15  | MIPI_CSI0_RX_D0P        |  31  | VCC_5V                    |
|  16  | GND                     |

#### CAM1

| Pin# | Name               | Pin# | Name               |
| :--: | :----------------- | :--: | :----------------- |
|  1   | GND                |  17  | MIPI_CSI1_RX_CLK0N |
|  2   | MIPI_CSI1_RX_D3N   |  18  | MIPI_CSI1_RX_CLK0P |
|  3   | MIPI_CSI1_RX_D3P   |  19  | GND                |
|  4   | GND                |  20  | MIPI_CAM4_CLKOUT   |
|  5   | MIPI_CSI1_RX_D2N   |  21  | GND                |
|  6   | MIPI_CSI1_RX_D2P   |  22  | MIPI_CAM2_CLKOUT   |
|  7   | GND                |  23  | MIPI_CSI1_PDN2_H   |
|  8   | MIPI_CSI1_RX_CLK1N |  24  | I2C4_SCL           |
|  9   | MIPI_CSI1_RX_CLK1P |  25  | I2C4_SDA           |
|  10  | GND                |  26  | MIPI_CSI1_PDN4_H   |
|  11  | MIPI_CSI1_RX_D1N   |  27  | CAM2_RST_L         |
|  12  | MIPI_CSI1_RX_D1P   |  28  | VCC_3V3_S3         |
|  13  | GND                |  29  | VCC_3V3_S3         |
|  14  | MIPI_CSI1_RX_D0N   |  30  | VCC_5V             |
|  15  | MIPI_CSI1_RX_D0P   |  31  | VCC_5V             |
|  16  | GND                |

        </div>
    </TabItem>

</Tabs>

### MIPI DSI

#### ROCK 5B/5B+

<div className='gpio_style' style={{ overflow :"auto"}} >

| Pin# | Name               | Pin# | Name        |
| :--: | :----------------- | :--: | :---------- |
|  1   | LCD_3V3            |  21  | GND         |
|  2   | VCC_1V8_S0         |  22  | GND         |
|  3   | GPIO0-A0           |  23  | TP_RST_L    |
|  4   | LCD_RESET          |  24  | LCD_3V3     |
|  5   | NC                 |  25  | TP_INT_L    |
|  6   | GND                |  26  | I2C6_SDA_M0 |
|  7   | MIPI_DPHY1_TX_D0N  |  27  | I2C6_SCL_M0 |
|  8   | MIPI_DPHY1_TX_D0P  |  28  | GND         |
|  9   | GND                |  29  | GND         |
|  10  | MIPI_DPHY1_TX_D1N  |  30  | LCD_3V3     |
|  11  | MIPI_DPHY1_TX_D1P  |  31  | LCD_3V3     |
|  12  | GND                |  32  | GND         |
|  13  | MIPI_DPHY1_TX_CLKN |  33  | GND         |
|  14  | MIPI_DPHY1_TX_CLKP |  34  | VCC_LEDK    |
|  15  | GND                |  35  | VCC_LEDK    |
|  16  | MIPI_DPHY1_TX_D2N  |  36  | NC          |
|  17  | MIPI_DPHY1_TX_D2P  |  37  | NC          |
|  18  | GND                |  38  | VCC_LEDA    |
|  19  | MIPI_DPHY1_TX_D3N  |  39  | VCC_LEDA    |
|  20  | MIPI_DPHY1_TX_D3P  |  40  | GND         |

 </div>

### PCIe

- PCIe E Key

<div className='gpio_style'>

| Pin# | Name                    | Pin# | Name                      | Pin# | Name              | Pin# | Name      |
| :--: | :---------------------- | :--: | :------------------------ | :--: | :---------------- | :--: | :-------- |
|  1   | GND                     |  21  | WIFI_WAKE_HOST_H_GPIO3_D5 |  49  | PCIE20_REFCLKN    |  69  | GND       |
|  2   | VCC3V3_WF               |  22  | UART1_RX_M0               |  50  | WIFIBT_32KIN_1T1R |  70  | BT_WAKE   |
|  3   | USB2_M2_DP              |  23  | WIFI_REG_ON               |  51  | GND               |  71  | NC        |
|  4   | VCC3V3_WF               |  32  | UART1_TX_M0               |  52  | PCIE_PERSTN       |  72  | VCC3V3_WF |
|  5   | USB2_M2_DM              |  33  | GND                       |  53  | PCIE_CLKREQN      |  73  | NC        |
|  6   | WIFI_LED                |  34  | UART1_CTS_M               |  54  | HOST_WAKE_BT_H    |  74  | VCC3V3_WF |
|  7   | GND                     |  35  | PCIE_TXP                  |  55  | PCIE_WAKEN        |  75  | GND       |
|  8   | PCM_CLK/I2S_SCK         |  36  | UART1_RTS_M               |  56  | BT_REG_ON_H       |  76  | GND       |
|  9   | SDIO_CLK                |  37  | PCIE_TXN                  |  57  | GND               |  77  | GND       |
|  10  | PCM_SYNC/I2S_WS         |  38  | NC                        |  58  | I2C4_SDA_M1       |  78  | NC        |
|  11  | SDMMC2_CMD_M0           |  39  | GND                       |  59  | NC                |  79  | NC        |
|  12  | PCM_OUT/I2S SD_OUT      |  40  | NC                        |  60  | I2C4_SCL_M1       |
|  13  | SDMMC2_D0_M0            |  41  | PCIE20_RXP                |  61  | NC                |
|  14  | PCM_IN/I2S SD_IN        |  42  | BT_REG_NO                 |  62  | NC                |
|  15  | SDMMC2_D1_M0            |  43  | PCIE20_RXN                |  63  | GND               |
|  16  | NC                      |  44  | NC                        |  64  | NC                |
|  17  | SDMMC2_D2_M0            |  45  | GND                       |  65  | NC                |
|  18  | GND                     |  46  | NC                        |  66  | NC                |
|  19  | SDMMC2_D3_M0            |  47  | PCIE20_REFC               |  67  | NC                |
|  20  | BT_WAKE_HOST_H_GPIO4_B4 |  48  | NC                        |  68  | NC                |

</div>

### POE

### TF Card Slot

| Pin# | Name         |
| :--: | :----------- |
|  1   | SDMMC0_D2    |
|  2   | SDMMC0_D3    |
|  3   | SDMMC0_CMD   |
|  4   | VCC3V3_SYS   |
|  5   | SDMMC0_CLK   |
|  6   | GND          |
|  7   | SDMMC0_D0    |
|  8   | SDMMC0_D1    |
|  9   | SDMMC0_DET_L |
|  10  | GND          |
|  11  | GND          |
|  12  | GND          |
|  13  | GND          |
