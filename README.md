# esp8266-sigma-delta
ESP8266_RTOS_SDK sigma-delta module driver

For unknown reasons sigma-delta module driver is not present in ESP8266_RTOS_SDK.

It can be used as Infrared carrier signal generator on any pin, or as cheap
audio output

To use this module:

1. move to `components` directory of your ESP8266_RTOS_SDK project
2. run `git clone https://github.com/QB4-dev/esp8266-sigma-delta`
3. add driver header in your code and start the module:
```
#include "driver/sigma_delta.h"
...
#define IR_TX_IO_NUM 2
...
//generate 38kHz carrier
sigma_delta_init(100,12);
//set IR_TX_IO_NUM GPIO as signal output
sigma_delta_set_output(IR_TX_IO_NUM);
```
