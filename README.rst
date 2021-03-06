Fork of the now archived https://bitbucket.org/thesheep/micropython-ht16k33

Micropython Library for the HT16K33-based LED Matrices
******************************************************

This is a library for using the I²C-based LED matrices with the HT16K33 chip.
It supports both 16x8 and 8x8 matrices.

Example
=======

This is an example for the ESP8266 port of Micropython::

    from machine import I2C, Pin
    from ht16k33_matrix import Matrix8x8
    i2c = I2C(sda=Pin(4), scl=Pin(5))
    display = Matrix8x8(i2c)
    display.brightness(8)
    display.blink_rate(2)
    display.fill(True)
    display.pixel(0, 0, False)
    display.pixel(7, 0, False)
    display.pixel(0, 7, False)
    display.pixel(7, 7, False)
    display.show()
