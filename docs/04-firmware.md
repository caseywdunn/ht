# 4. Updating the firmware

**Why:** The factory firmware can't send Morse code. The **NR7Y CW firmware** adds a real CW transmitter, an iambic keyer, an on-screen Morse decoder, a code practice mode, and more. It's built on **F4HWN "Fusion"**, a popular community firmware for this radio, so you also get a better spectrum display, more menu options, and finer power control.

> ⚠️ **Read first.** Custom firmware is "at your own risk". The worst case is a bricked radio, which on a $30 radio is a lesson rather than a disaster. Follow the steps exactly, **back up your calibration**, and **use only the V3/K1 firmware** on a V3/K1 radio.

## 4.1 What you need

- The radio, **fully charged**
- The USB programming cable (K-plug)
- A computer running **Chrome** or **Edge**

## 4.2 Download the files

Go to the **[NR7Y firmware releases page](https://github.com/briand/uv-k1-k5v3-firmware-custom/releases)** and, under the **latest** release (v1.4 as of October 2026), download:

1. The firmware **`.bin`** file, e.g. `nr7y.k1-k5v3.v1.4.bin`
2. The CHIRP module **`.py`** file, e.g. `nr7y.k1-k5v3.chirp.v1.4a.py` (needed in [section 5](05-programming.md))

Always use the CHIRP module **from the same release** as the firmware.

> These are for the UV-K5 **V3 and UV-K1 only**. The original V1 radio has [a different repository](https://github.com/briand/uv-k5-firmware-custom-cw).

## 4.3 Connect the cable

1. **Turn the radio off.**
2. Open the rubber flap on the radio's right side and push the cable's 2-pin plug **all the way in**. It's stiff, and you may feel two clicks. A half-inserted plug is the #1 reason flashing fails.
3. Plug the USB end into your computer.

> **Mac users:** recent macOS has the CH340 driver built in. The cable shows up as something like `cu.usbserial-XXXX` or `cu.wchusbserial-XXXX`. **Windows users:** if no COM port appears in Device Manager, install the driver for the cable's chip (CH340 or FTDI).

## 4.4 Back up the calibration data (do not skip)

Every radio has factory calibration data (power levels, frequency accuracy) stored on it. Flashing *shouldn't* touch it, but a backup costs you one minute.

1. Turn the radio **on normally**, cable attached.
2. In Chrome, open **[UVTools2](https://armel.github.io/uvtools2/)**.
3. Click **Dump Calibration Data** and pick the serial port for your cable.
4. Save the `calibration.dat` file and **rename it with your radio's serial number** (on the label behind the battery), e.g. `calibration-K5V3-SN12345.dat`. Keep it somewhere safe.

## 4.5 Flash the firmware

1. **Turn the radio off.**
2. **Press and hold PTT first** (the big button at the top of the left side, *not* the two small buttons below it). *While still holding PTT*, turn the knob to switch the radio on. Keep holding for 2–3 seconds, then let go. The **flashlight LED comes on** and the screen stays **blank and dark**. That's correct: this is bootloader ("flashing") mode.
   - **If the screen shows the normal display (frequency, battery, etc.), the radio started normally. Don't flash.** Turn it off, wait a few seconds, and try again, making sure PTT is fully pressed *before* the knob clicks on. The flashlight alone doesn't prove you're in flash mode; the **dark screen** does.
   - **Don't hold Side 2.** PTT + Side 2 at power-on starts **AIR COPY (RDY)**, a wireless channel-cloning mode, not flash mode. If you see AIR COPY, **don't press any keys** (pressing MENU there transmits on 410 MHz, outside the ham bands). Just turn the radio off with no buttons held, and turn it back on.
3. In UVTools2, under **Firmware File (.bin)**, choose the `.bin` you downloaded.
4. Click **Flash firmware** and select the cable's serial port.
5. The LED blinks while it writes ("flashing the firmware", get it?). Wait for 100%. **Don't unplug anything until it finishes.**
6. The radio restarts with the new firmware. Unplug the cable and **turn the radio off and on once**.

If you see **"CW KEY STUCK"** after flashing, that's normal when the cable is still plugged in. Unplug it and power-cycle.

## 4.6 After flashing

- Run **Dump Calibration Data** again (radio on normally) and save that copy too.
- Press **M** to open the menu. You should see a **CW** category at the top. That means it worked.

> **Alternative tools:** [UV Studio](https://armel.github.io/uvstudio) (same author as UVTools2) and the [BKG programmer](https://programmer.bkg.club) also flash and configure these radios in the browser.

---

[← Guide home](../README.md) · [← 3. Shopping list](03-shopping-list.md) · [5. Programming frequencies with a cable →](05-programming.md)
