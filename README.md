# Lab2b_Proposal

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


## gif

![20221020193759](https://user-images.githubusercontent.com/113930091/197079025-95d31051-3212-4fe9-844b-67191d2d5f10.gif)
