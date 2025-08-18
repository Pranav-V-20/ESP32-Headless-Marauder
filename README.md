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

3. Open [ESP Web Flasher](https://esptool.spacehuhn.com/) in **Chrome**.

4. Connect your ESP32 and flash the above binaries at their respective offsets.

<img width="843" height="749" alt="Screenshot 2025-08-16 181543" src="https://github.com/user-attachments/assets/ee89a69b-3773-418e-a193-4b9bb3829291" />

---

## 🖥️ Usage

1. Once flashed, open the [ESP32 Web](https://pranav-v-20.github.io/ESP32-Headless-Marauder/) in your Chrome browser.
2. Interact with the ESP32 Marauder using available CLI commands.
3. Preloaded Wi-Fi penetration commands are available.

<img width="1155" height="828" alt="Screenshot 2025-08-16 174922" src="https://github.com/user-attachments/assets/77b136b4-61fd-4170-892a-a2ff4fe32772" />

---

## 🔧 System & Utility Commands

* **`help`** – Displays all available commands with basic usage information.
* **`reboot`** – Restarts the device.
* **`update -s`** – Updates firmware from a server.
* **`update -w`** – Updates firmware from a web/USB source.
* **`ls <directory>`** – Lists files and directories at the specified path.
* **`led -s`** – Toggles status LED on/off.
* **`led -p`** – Puts LED in pulse mode.
* **`info`** – Shows device/system information.
* **`info -a`** – Shows extended device/system information.

---

## 📡 Wi-Fi Channel & Settings

* **`channel -s`** – Selects and sets the Wi-Fi channel.
* **`settings -s enable`** – Enables specific system settings.
* **`settings -s disable`** – Disables specific system settings.
* **`settings -r`** – Resets settings to default.

---

## 🧹 List & Data Management

* **`clearlist -a`** – Clears all stored lists.
* **`clearlist -c`** – Clears client list.
* **`clearlist -s`** – Clears SSID list.
* **`list -a`** – Displays all saved lists.
* **`list -s`** – Shows saved SSID list.
* **`list -c`** – Shows client list.
* **`list -t`** – Shows target list.
* **`list -i`** – Shows index list.
* **`list -p`** – Shows packet logs.
* **`select -a`** – Selects all items in a list.
* **`select -s`** – Selects SSID(s).
* **`select -c`** – Selects client(s).
* **`select -f`** – Selects by filter (`equals` or `contains`).
* **`save -a`** – Saves all configurations/lists.
* **`save -s`** – Saves SSID list only.
* **`load -a`** – Loads all saved configurations.
* **`load -s`** – Loads SSID list only.

---

## 🌍 GPS & Location

* **`gpsdata`** – Displays live GPS data.
* **`gps -g`** – Shows GPS fix information.
* **`gps ix`** – Index of GPS data.
* **`gps sat`** – Number of satellites detected.
* **`gps lon`** – Longitude.
* **`gps lat`** – Latitude.
* **`gps alt`** – Altitude.
* **`gps date`** – Date and timestamp.
* **`gps accuracy`** – Accuracy level of GPS fix.
* **`gps text`** – Textual GPS information.
* **`gps nmea`** – Raw NMEA data stream.
* **`gps -n gps/glonass/galileo/navic/qzss/beidou`** – Selects satellite system.
* **`gps -b`** – Switches Beidou usage between BD/GB.
* **`nmea`** – Outputs raw NMEA sentences directly.

---

## 🛰️ Scanning & Recon

* **`scanap`** – Scans for Wi-Fi access points.
* **`scansta`** – Scans for connected stations (clients).
* **`scanall`** – Scans both APs and clients.
* **`stopscan`** – Stops ongoing scan.
* **`stopscan -f`** – Forces scan stop.
* **`pingscan`** – Sends ICMP pings to discover devices.
* **`arpscan`** – Performs ARP-based discovery of devices.
* **`arpscan -f`** – Forces ARP scan.
* **`portscan -a -t <index>`** – Scans open ports of target.
* **`sigmon`** – Monitors signal strength of detected networks.
* **`packetcount`** – Shows number of captured packets.
* **`wardrive`** – Starts war driving mode (logs APs while moving).
* **`wardrive -s`** – War drive with GPS support.

---

## 🕵️ Packet Sniffing

* **`sniffraw`** – Captures raw 802.11 packets.
* **`sniffbeacon`** – Captures Wi-Fi beacon frames.
* **`sniffprobe`** – Captures probe request frames.
* **`sniffpwn`** – Captures and stores packets for replay/analysis.
* **`sniffpinescan`** – Detects PineAP/Karma activity.
* **`sniffmultissid`** – Detects multiple SSIDs in use.
* **`sniffesp`** – Captures ESP-related packets.
* **`sniffdeauth`** – Captures deauthentication frames.
* **`sniffpmkid`** – Captures PMKID handshake for cracking.
* **`sniffpmkid -c <channel>`** – Capture PMKID on a specific channel.
* **`sniffpmkid -d`** – Save PMKID dump to file.
* **`sniffpmkid -l`** – List captured PMKIDs.

---

## ⚔️ Attack Modes

* **`attack -t -l`** – Launch attack (loop mode).
* **`attack -t -r`** – Launch attack (random mode).
* **`attack -t -a`** – Launch attack (all targets).
* **`attack deauth`** – Sends deauthentication frames.
* **`attack deauth -c`** – Deauth a specific channel.
* **`attack deauth -s`** – Deauth a specific SSID.
* **`attack probe`** – Sends fake probe requests.
* **`attack rickroll`** – Starts Wi-Fi Rickroll prank.
* **`attack badmsg`** – Sends malformed messages.
* **`attack badmsg -c`** – Targeted bad message attack.
* **`attack sleep`** – Sends packets to put devices into sleep mode.
* **`attack sleep -c`** – Sleep attack on specific channel.

---

## 🎭 Evil Portal & Karma

* **`evilportal -c start`** – Starts captive portal.
* **`evilportal -c start -w <html.html>`** – Starts portal with custom HTML file.
* **`evilportal sethtml`** – Updates portal HTML.
* **`karma -p <example>`** – Karma attack (rogue AP mimicking real SSIDs).

---

## 📡 SSID Management

* **`ssid -a`** – Add new SSID to the list.
* **`ssid -a -g`** – Add SSID with group option.
* **`ssid -a -n`** – Add SSID with name option.
* **`ssid -r`** – Remove SSID.
* **`join -a -p <password> -s <SSID>`** – Joins a network with given SSID and password.

---

## 🔵 Bluetooth / BLE

* **`sniffbt`** – Sniffs nearby Bluetooth traffic.
* **`sniffbt -t <target>`** – Sniffs a specific target.
* **`blespam -t linux`** – Sends spam advertisements to Linux devices.
* **`blespam -t windows`** – Sends spam advertisements to Windows devices.
* **`blespam -t flipper`** – Sends spam ads to Flipper devices.
* **`blespam -t all`** – Sends spam ads to all devices.
* **`spoofat -t <target>`** – Spoofs Bluetooth address to impersonate target.
* **`btwardrive`** – Bluetooth war driving mode.
* **`btwardrive -c`** – War drive Bluetooth with GPS support.
* **`sniffskim`** – Sniffs Bluetooth-based skimming devices.

---

## 📖 Documentation

* ESP32 Marauder Wiki → [Read Here](https://github.com/justcallmekoko/ESP32Marauder/wiki)
* CLI command list → Refer to wiki and built-in help.

---

## ⚠️ Disclaimer

This project is intended for **educational and research purposes only**.
Do not use it on networks or devices without **explicit permission**. The authors are not responsible for misuse.


Would you like me to also create a **step-by-step screenshot section** (with Chrome Web Flasher and CLI terminal examples) so the README looks more visual and beginner-friendly?
