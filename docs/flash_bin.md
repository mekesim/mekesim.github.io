---
comments: true
---

# How to flash a bin file to ESP32

## Method 1: Use the flash tool GUI application

1. Download and install the latest version of the ESP32 Flash Download Tool.
2. Connect the ESP32 to your computer using a USB cable.
3. Open the ESP32 Flash Download Tool and select the "ESP32 Download Tool" option.
4. Click the "Choose" button and navigate to the bin file you want to flash to the ESP32.
5. Select the bin file and click "Open."
6. In the "Flash Download Tool" window, select the "ESP32" option in the "Board" dropdown menu.
7. In the "Address" field, enter the starting address where the bin file will be written to the ESP32. This is usually 0x0000.
8. Click the "Download" button to begin flashing the bin file to the ESP32.
9. Wait for the flashing process to complete, and then disconnect the ESP32 from the computer.
10. Your ESP32 should now be running the new firmware from the bin file.

Wait for the flashing process to complete. This may take a few minutes.

Once the flashing is complete, you should see a "Success" message in the Flash Download Tool.

You can now disconnect your ESP32 from your computer and use it with the new firmware. Keep in mind that flashing the firmware will erase any existing data on the ESP32, so make sure to backup any important data before proceeding.

or you can flash it with command

## Method 2: Use the flash python file

1. Download the latest version of esptool.py from the official GitHub page ([https://github.com/espressif/esptool](https://github.com/espressif/esptool))

2. Connect your ESP32 board to your computer using a micro USB cable

3. Open a command prompt or terminal window and navigate to the directory where you saved the esptool.py file

4. Run the following command to flash the bin file to the ESP32:

    ```
    esptool.py --chip esp32 --port /dev/ttyUSB0 --baud 115200 write\_flash -z 0x1000 <path to bin file>
    ```

    !!! Note

        Replace `/dev/ttyUSB0` with the correct port for your ESP32 board and `<path to bin file>` with the actual path to the bin file on your computer.

5. Wait for the process to complete and the ESP32 to reboot. You should now be able to access the firmware on your ESP32.
