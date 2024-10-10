# Demo: Thermal Array-Based Detection and Ranging for Privacy-Preserving Human Sensing

This is the demo for our MobiHoc'24 paper: 

`TADAR: Thermal Array-Based Detection and Ranging for Privacy-Preserving Human Sensing`

- The paper can be found [here](https://arxiv.org/pdf/2409.17742).

- The complete open-source code can be found [here](https://github.com/aiot-lab/TADAR)


![hustlin_erd](Poster_TADAR.png)

If you are inerested in our work, and would like to build a system, here is the instruction to build the system:

## hardware
1. 1x ESP32-S3-DevKitM-1: see [here](https://docs.espressif.com/projects/esp-idf/en/stable/esp32s3/hw-reference/esp32s3/user-guide-devkitm-1.html)
2. 1x MLX90640BAA thermal array sensor: see [here](https://www.melexis.com/zh/product/MLX90640/MLX90640) (Can purchase sensor modules with breakout boards from Adafruit, Sparkfun, etc.)
    - 32x24 pixels, 
    - 110°x75° field of view;
3. 1x laptop with python installed (with annaconda is recommended)

## Connection
1. Connect the ESP32-S3-DevKitM-1 (using the UART port on the board rather than the USB port) to the laptop via USB-C cable
2. Connect the MLX90640BAA to the ESP32-S3-DevKitM-1 via I2C interface: 
    - SDA: GPIO 17
    - SCL: GPIO 18
    - VCC: 3.3V
    - GND: GND

## Firmware
- The firmware is developed using the platformio extension in VSCode.
- The firmware is in the `firmwar.zip` folder.
- Unzip the folder and open it in VSCode.
- Compile and upload the firmware to the ESP32-S3-DevKitM-1.

## Software
- The software is developed using python.
- Install the required python packages using the following command with requirements.txt:
```bash
pip install -r requirements.txt
```
- Run the python script `main.py` to start the system.
(You may need to change the serial port in the script to the port that the ESP32-S3-DevKitM-1 is connected to)
(If you encounter any issues, please rerun the script)

## Citation
If you find our work useful, please cite our paper:
```
@inproceedings{Zhang2024TADAR,
  title = {{{TADAR}}: {{Thermal}} Array-Based Detection and Ranging for Privacy-Preserving Human Sensing},
  booktitle = {Proceedings of the 25th International Symposium on Theory, Algorithmic Foundations, and Protocol Design for Mobile Networks and Mobile Computing ({{MOBIHOC}} '24)},
  author = {Zhang, Xie and Wu, Chenshu},
  year = {2024},
  pages = {1--10},
  publisher = {ACM},
  address = {Athens, Greece},
  doi = {10.1145/3641512.3686357}
}
```


