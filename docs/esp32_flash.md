# Flash Code to ESP32 by Arduino IDE

To flash an ESP32, it need to install the ESP32 board support package in the Arduino IDE.

Here are the steps to follow:

- Connect the ESP32 devolop board to your computer using the USB cable.

- Open the Arduino IDE and go to `File > Preferences`. In the `Additional Board Manager URLs` field, enter the URL for the ESP32 board support package

```
https://dl.espressif.com/dl/package_esp32_index.json
```

- Go to `Tools > Board > Boards Manager` and search for "ESP32". Install the ESP32 board support package.

- Go to `Tools > Board` and select the ESP32 board you are using (e.g. "ESP32 Dev Module").

![Installing ESP32 in Arduino IDE (Windows, Mac OS X, Linux) | Random Nerd  Tutorials](https://i0.wp.com/randomnerdtutorials.com/wp-content/uploads/2016/12/windows-select-board.png?resize=614%2C520&quality=100&strip=all&ssl=1)

select the port that the ESP32 is connected to.

- Open the example sketch "Blink" by going to File > Examples > 01.Basics > Blink.

- Upload the sketch to the ESP32 by clicking the upload button (the right-facing arrow in the top left of the Arduino IDE).

If the upload is successful, the ESP32 should start blinking an LED (if it has one) at a 1-second interval.

!!! Bug

    For some kinds of ESP32 development board it's hardware design may not support auto download, while start flashing, it need pressing the ESP32's reset button before uploading the sketch.

If you are not sure which development board has such feature, you can be the suggested board from [this link](https://), I have verify the auto download feature.

If you have interesting about this "bug", can further read this article.