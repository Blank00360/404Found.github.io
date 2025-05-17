---
title: "Beginner's Guide: Blink the Onboard LED on Raspberry Pi Pico W with MicroPython"
layout: default
---

# 💡 Getting Started with Raspberry Pi Pico W: Blink the Onboard LED!

Welcome! 👋  
This beginner-friendly guide will show you how to blink the **onboard LED** on your **Raspberry Pi Pico W** using **MicroPython** — your very first step into the world of electronics and coding.

No prior experience required. Let’s get started!

---

## 🧰 What You’ll Need

✅ Raspberry Pi Pico W  
✅ Micro USB cable  
✅ Computer with internet access  
✅ Free software: [Thonny IDE](https://thonny.org)

---

## 🔌 Step 1: Install MicroPython on Pico W

1. **Download MicroPython firmware (.uf2)**  
   👉 [Get it here](https://www.raspberrypi.com/documentation/microcontrollers/micropython.html)

2. **Put Pico W in boot mode**
   - Unplug it from your computer.
   - Hold the **BOOTSEL** button.
   - While holding it, plug the Pico W into your computer using the USB cable.

3. **Copy the MicroPython file**
   - A new drive named `RPI-RP2` will appear.
   - Drag and drop the `.uf2` file into this drive.
   - Your Pico W will reboot and is now ready for MicroPython!

---

## 🖥️ Step 2: Install and Set Up Thonny

1. **Download Thonny**  
   👉 [thonny.org](https://thonny.org)

2. **Open Thonny**
   - Go to **Run → Select interpreter**
   - Choose: `MicroPython (Raspberry Pi Pico)`
   - Set the correct port if needed (usually auto-detects)

That’s it! You’re now connected to your Pico W.

---

## 🚨 Step 3: Blink the Onboard LED

Here’s your first MicroPython code. It will blink the onboard LED every half second.

### 🧾 Paste this into Thonny:

```python
import machine
import time

led = machine.Pin("LED", machine.Pin.OUT)

while True:
    led.toggle()
    time.sleep(0.5)
