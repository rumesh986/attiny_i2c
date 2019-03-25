# attiny_i2c
i2c protocol for use on avr devices like attiny85

## Usage
Simply copy the files to your project directory
Add `#include "attiny_i2c.h` to your main .c file.
By default the `SDA pin` is set as `PB0` and `SCL pin` is set as `PB2`.
You can change the pins in `attiny_lcd.h`

### void init_i2c(void);
Setup the device for sending messages through i2c.

### uint8_t send_bytes(uint8_t address, uint8_t *bytes, size_t size);
Send messages through i2c using this command.
`address` is the address of the slave device.
`bytes` is a pointer to your message.
`size` is the number of bytes you wish to send.
