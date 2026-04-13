## **Lab 2 Reflection: WiFi Connectivity & OLED Integration**

### **1. WiFi Verification: AirLift FeatherWing**
To verify the WiFi capabilities of the AirLift FeatherWing, I used the ESP32 SPI webclient test. This script initializes the SPI bus, connects to the ESP32 coprocessor, and performs a GET request to a test URL.

**Key Technical Details:**
* **Pins Used:** `D13` (CS), `D11` (Ready), and `D12` (Reset).
* **Result:** Successful connection via mobile hotspot, verified by a successful IP lookup for `adafruit.com` and a ping to `google.com`.

<img src="Screenshot_from_2025-10-27_13-42-54.png" alt="Test success" style="width: 25%; height: auto; display: block; margin-top: 10px;" />

### **2. OLED Display Setup**
I utilized the `adafruit_displayio_sh1107` library to initialize the OLED display. The SH1107 is a vertically oriented **128x64** display. Using `displayio`, I was able to create a "splash" group to render shapes and text.

**Visual Layout:**
* A white background with a black inner border.
* Geometric primitives (squares of varying sizes).
* Dynamic text labels using `terminalio.FONT`.

---

## **Hardware Profile: Adafruit Fruit Jam (Mini RP2350)**

During the "Passive Reconnaissance" phase, I analyzed the **Fruit Jam**, a specialized RP2350 development board designed for multimedia and retro-computing.

### **Core Specifications**
| Feature | Details |
| :--- | :--- |
| **Microcontroller** | Raspberry Pi **RP2350** (Dual ARM Cortex-M33) |
| **Video Output** | **DVI Port** via HSTX interface (Supports up to 720p) |
| **Audio** | **TLV320DAC3100** I2S DAC; 3.5mm Jack & JST Speaker Header |
| **USB Connectivity** | 1x USB-C (Power/Data); 2x USB-A (Host mode for HID) |
| **Storage** | MicroSD card slot for assets and data logging |

### **On-Board Interface**
* **User Input:** 3x Programmable buttons, 1x Reset button.
* **Visuals:** 5x On-board NeoPixels for status and flair.
* **Infrared:** IR Receiver for remote control integration.
* **Expansion:** 16-pin GPIO header providing 3.3V/5V power and analog/digital I/O.

