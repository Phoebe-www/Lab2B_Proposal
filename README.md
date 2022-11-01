# Lab2b_Proposal

Siyun Wang

wsiyun@seas.upenn.edu

test on: Tested on: DELL Inspiron 5505, Windows 10


In this part, we used LED, 1kΩ resistance, breadboard and STEMMA QT. And we used STEMMA QT as input with GPIO 22.

## code

        #include "pico/stdlib.h"

        int main() {
        #ifndef PICO_DEFAULT_LED_PIN
        #warning blink example requires a board with a regular LED
        #else
        const uint LED_PIN = 22;
        gpio_init(LED_PIN);
        gpio_set_dir(LED_PIN, GPIO_OUT);
        while (true) {
                gpio_put(LED_PIN, 1);
                sleep_ms(250);
                gpio_put(LED_PIN, 0);
                sleep_ms(250);
                }
        #endif
        }


## result

![20221020193759](https://user-images.githubusercontent.com/113930091/197079025-95d31051-3212-4fe9-844b-67191d2d5f10.gif)


## outline

Since there are several GPIO pins on the QT-PY 2040, they can be used as I/O ports. I plan to use several GPIO pins to drive several different color LEDs. My idea is that I can design a traffic light that can change red, green and yellow colors. Red and green light color 10s, yellow light 5s. And the reason that I think my design is cool is that it can be used in real life and has strong practicality.

## component

 LED, 1kΩ resistance, STEMMA QT
 
## question

1. How to control the LED brightness change, or how to control the LED brightness slowdown proces？


# Update on Oct.31st

## component

RP2040, APDS9960, 510 Ohm resistor, LED, Protoboard, Wires

## peripheral 

GPIO, I2C1

## outline

Our work is an alarm that detects distance.

