# ESP32 Headless Marauder

The **ESP32 Headless Marauder** is a firmware build of [ESP32 Marauder](https://github.com/justcallmekoko/ESP32Marauder) designed to run **headlessly** with CLI (Command-Line Interface) access via a Chrome browser terminal.
It allows Wi-Fi penetration testing and security research directly from an ESP32 device — no onboard screen required.

---

## 🚀 Requirements

* Any ESP32 device with **4MB Flash** (Recommended: **ESP32-U**)
* Laptop with **Google Chrome** browser
* Internet connection
* Pre-compiled firmware files

---

## 🔧 Flashing Instructions

1. Read the [ESP32Marauder Wiki](https://github.com/justcallmekoko/ESP32Marauder/wiki) for detailed flashing steps.

2. Download the following firmware components:

   * **ESP32Marauder** → `0000` [ESP32Marauder](https://github.com/justcallmekoko/ESP32Marauder/releases/download/v1.8.4/esp32_marauder_v1_8_4_20250806_v6.bin)
   * **Bootloader** → `0x1000` [bootloader](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/MarauderV4/esp32_marauder.ino.bootloader.bin)
   * **Partitions** → `0x8000` [Partitions](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/MarauderV4/esp32_marauder.ino.partitions.bin)
   * **Boot App** → `0xE000` [Boot App](https://github.com/justcallmekoko/ESP32Marauder/raw/master/FlashFiles/FlipperZeroMultiBoardS3/boot_app0.bin)

3. Open [ESP Web Flasher](https://espressif.github.io/esptool-js/) in **Chrome**.

4. Connect your ESP32 and flash the above binaries at their respective offsets.

<img width="843" height="749" alt="Screenshot 2025-08-16 181543" src="https://github.com/user-attachments/assets/ee89a69b-3773-418e-a193-4b9bb3829291" />

---

## 🖥️ Usage

1. Once flashed, open the [ESP32 Web](https://pranav-v-20.github.io/ESP32-Headless-Marauder/) in your Chrome browser.
2. Interact with the ESP32 Marauder using available CLI commands.
3. Preloaded Wi-Fi penetration commands are available.

<img width="1155" height="828" alt="Screenshot 2025-08-16 174922" src="https://github.com/user-attachments/assets/77b136b4-61fd-4170-892a-a2ff4fe32772" />

---

## 📖 Documentation

* ESP32 Marauder Wiki → [Read Here](https://github.com/justcallmekoko/ESP32Marauder/wiki)
* CLI command list → Refer to wiki and built-in help.

---

## ⚠️ Disclaimer

This project is intended for **educational and research purposes only**.
Do not use it on networks or devices without **explicit permission**. The authors are not responsible for misuse.


Would you like me to also create a **step-by-step screenshot section** (with Chrome Web Flasher and CLI terminal examples) so the README looks more visual and beginner-friendly?
