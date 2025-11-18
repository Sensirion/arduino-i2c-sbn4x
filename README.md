# Sensirion I²C SBN4X Arduino Library

This is the Sensirion SBN4X library for Arduino allowing you to
communicate with a SBN4x sensor
over I²C.

<img src="images/product_image.jpg" width="300px">

Click [here](https://sensirion.com/products/product-categories/) to learn more about the Sensirion SBN4x sensor.



The default I²C address of [SBN4x](https://sensirion.com/products/catalog) is ****.



## Installation of the library

This library can be installed using the Arduino Library manager:
Start the [Arduino IDE](http://www.arduino.cc/en/main/software) and open
the Library Manager via

`Sketch` ➔ `Include Library` ➔ `Manage Libraries...`

Search for the `Sensirion I2C SBN4X` library in the `Filter
your search...` field and install it by clicking the `install` button.

If you cannot find it in the library manager, download the latest release as .zip file
and add it to your [Arduino IDE](http://www.arduino.cc/en/main/software) via

`Sketch` ➔ `Include Library` ➔ `Add .ZIP Library...`

Don't forget to **install the dependencies** listed below the same way via library
manager or `Add .ZIP Library`

#### Dependencies
* [Sensirion Core](https://github.com/Sensirion/arduino-core)

## Connect the sensor

Use the following pin description to connect your SBN4X to the standard I²C bus of your Arduino board:

<img src="images/product_pinout.jpg" width="300px">

| *Pin* | *Cable Color* | *Name* | *Description*  | *Comments* |
|-------|---------------|:------:|----------------|------------|
| 1 | green | SDA | I2C: Serial data input / output |
| 2 | black | GND | Ground |
| 3 | yellow | SCL | I2C: Serial clock input |
| 4 | red | VDD | Supply Voltage | 4.9V to 5.5V




The recommended voltage is 5.0V.

### Board specific wiring
You will find pinout schematics for recommended board models below:



<details><summary>Arduino Uno</summary>
<p>

| *SBN4X* | *SBN4X Pin* | *Cable Color* | *Board Pin* |
| :---: | --- | --- | --- |
| SDA | 1 | green | D18/SDA |
| GND | 2 | black | GND |
| SCL | 3 | yellow | D19/SCL |
| VDD | 4 | red | 5V |



<img src="images/Arduino-Uno-Rev3-i2c-pinout.png" width="600px">
</p>
</details>




<details><summary>Arduino Nano</summary>
<p>

| *SBN4X* | *SBN4X Pin* | *Cable Color* | *Board Pin* |
| :---: | --- | --- | --- |
| SDA | 1 | green | A4 |
| GND | 2 | black | GND |
| SCL | 3 | yellow | A5 |
| VDD | 4 | red | 5V |



<img src="images/Arduino-Nano-i2c-pinout.png" width="600px">
</p>
</details>




<details><summary>Arduino Micro</summary>
<p>

| *SBN4X* | *SBN4X Pin* | *Cable Color* | *Board Pin* |
| :---: | --- | --- | --- |
| SDA | 1 | green | D2/SDA |
| GND | 2 | black | GND |
| SCL | 3 | yellow | ~D3/SCL |
| VDD | 4 | red | 5V |



<img src="images/Arduino-Micro-i2c-pinout.png" width="600px">
</p>
</details>




<details><summary>Arduino Mega 2560</summary>
<p>

| *SBN4X* | *SBN4X Pin* | *Cable Color* | *Board Pin* |
| :---: | --- | --- | --- |
| SDA | 1 | green | D20/SDA |
| GND | 2 | black | GND |
| SCL | 3 | yellow | D21/SCL |
| VDD | 4 | red | 5V |



<img src="images/Arduino-Mega-2560-Rev3-i2c-pinout.png" width="600px">
</p>
</details>




<details><summary>ESP32 DevKitC</summary>
<p>

| *SBN4X* | *SBN4X Pin* | *Cable Color* | *Board Pin* |
| :---: | --- | --- | --- |
| SDA | 1 | green | GPIO 21 |
| GND | 2 | black | GND |
| SCL | 3 | yellow | GPIO 22 |
| VDD | 4 | red | 5V |



<img src="images/esp32-devkitc-i2c-pinout.png" width="600px">
</p>
</details>



## Quick Start

1. Install the libraries and dependencies according to [Installation of the library](#installation-of-the-library)

2. Connect the SBN4X sensor to your Arduino as explained in [Connect the sensor](#connect-the-sensor)

3. Open the `exampleUsage` sample project within the Arduino IDE:

   `File` ➔ `Examples` ➔ `Sensirion I2C SBN4X` ➔ `exampleUsage`



4. Click the `Upload` button in the Arduino IDE or `Sketch` ➔ `Upload`

5. When the upload process has finished, open the `Serial Monitor` or `Serial
   Plotter` via the `Tools` menu to observe the measurement values. Note that
   the `Baud Rate` in the used tool has to be set to `115200 baud`.

## Contributing

**Contributions are welcome!**

This Sensirion library uses
[`clang-format`](https://releases.llvm.org/download.html) to standardize the
formatting of all our `.cpp` and `.h` files. Make sure your contributions are
formatted accordingly:

The `-i` flag will apply the format changes to the files listed.

```bash
clang-format -i src/*.cpp src/*.h
```

Note that differences from this formatting will result in a failed build until
they are fixed.
:

## License

See [LICENSE](LICENSE).