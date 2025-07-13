# ODrive DFU

README.md em português: [README.pt-br.md](https://github.com/achavevirou/odrive_dfu)

The **ODrive DFU** application is a simple utility designed to **set the board into DFU MODE (STM32 BOOTLOADER)**.  
This application is free and **has no affiliation with ODrive Robotics**.

![odrive_dfu_interface_en-us](https://github.com/achavevirou/odrive_dfu/blob/main/img/odrive_dfu_interface_en-us.png)

---

## ✅ Requirements

To connect to **ODrive | XDrive | Odesc**, make sure that:

- The board is running the native firmware (**ODrive 3.6 CDC Interface**);
- The controller driver is **WinUSB**.

---

## 🛠 Installing the Driver with Zadig

1. Download Zadig: [https://zadig.akeo.ie](https://zadig.akeo.ie)  
2. Open Zadig and go to `Options > List All Devices`.  
3. From the device list, select `ODrive 3.6 CDC Interface (Interface 0)`.  
4. Under `Driver`, check if the current one is **WinUSB**.  
5. If not, select **WinUSB** and click **Install Driver** or **Reinstall Driver**.  
6. Repeat the process for `ODrive 3.6 Native Interface (Interface 2)`.

---

## ▶️ Using the Application

1. Download [ODrive DFU 1.0](https://github.com/achavevirou/odrive_dfu/releases) and run.  
2. Click the **Connect** button.  
3. Then click the **DFU Mode** button.  
4. If everything is correct, the board will disconnect and appear in Windows as **STM32 BOOTLOADER**, indicating it's ready for firmware flashing.

---

## 🧩 If the Board Is Not Detected as STM32 BOOTLOADER

- Open **Device Manager**.  
- Go to `View > Show hidden devices`.  
- Under `Universal Serial Bus devices`, check for any **disconnected STM32 BOOTLOADER** entries.  
- **If found, uninstall all of them**.  
- Disconnect and reconnect the board.  
- Try DFU mode again using the application.

---

## ⚠️ Conflict with Thrustmaster Drivers

If you have previously installed drivers for a **Thrustmaster device**, there may be a conflict.  
Follow the tutorial below to **uninstall Guillemot STM DFU drivers**:

👉 [Uninstall Guillemot STM DFU](https://support.pimax.com/en/support/solutions/articles/60000812307-failure-upgrade-blinking-led-)

---

## 💡 STM32 BOOTLOADER Driver Error?

Just reinstall **WinUSB** using Zadig as described above.

---

## 🔌 Last Resort: ST Link

If nothing else works, use an **ST Link** to flash the firmware to **ODrive | XDrive | Odesc**.

> ⚠️ Warning: not all ST Links sold online work properly.  
> Prefer those with an **original chip**.

### Wiring Diagram:

> The XDrive Mini board should be powered with a **DC power supply between 12V and 56V**. If the board is Odesc, pay attention to the limit voltage (**24V or 56V depending on the version**).

![ST Link and XDrive Diagram](https://github.com/achavevirou/odrive_dfu/blob/main/img/stlink_xdrive_odrive_odesc.jpg)

### Programming:

- Use **STM32 ST-LINK Utility** to flash `.bin` or `.hex` files.  
- Use **STM32CubeProgrammer** to flash `.elf`, `.bin`, or `.hex` files.

---

## 🙏 A Small Request

If the ODrive DFU application or any of the tips helped you, please consider **subscribing to the channel**:

🔗 [A Chave Virou YouTube Channel](https://www.youtube.com/@achavevirou)

---

## 🌐 Other Links

- 📸 [Instagram A Chave Virou](https://www.instagram.com/achavevirou)  
- 📘 [Facebook A Chave Virou](https://www.facebook.com/share/g/1ArMr9tooj/?mibextid=wwXIfr)  
- 🛍️ [Online Store A Chave Virou](https://www.achavevirou.com.br/)

---
