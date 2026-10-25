# W1YU Handheld Radio (HT) Guide

A beginner's guide for the **Yale University Amateur Radio Club (W1YU)** covering VHF/UHF handheld transceivers ("HTs"). It assumes **no radio experience at all**. You'll set up a ~$30 radio, load new firmware, program local frequencies, make voice contacts, and send Morse code (CW) over the air.

> **New here?** Read [What is this radio?](#1-what-is-this-radio) and [Before you transmit](#2-before-you-transmit-licensing-and-rules) first. Buy the parts in [Shopping list](#3-shopping-list), then work through sections 4 → 7 in order.

**Contents**

1. [What is this radio?](#1-what-is-this-radio)
2. [Before you transmit: licensing and rules](#2-before-you-transmit-licensing-and-rules)
3. [Shopping list (part numbers)](#3-shopping-list)
4. [Updating the firmware](#4-updating-the-firmware)
5. [Programming frequencies with a cable](#5-programming-frequencies-with-a-cable)
6. [Voice (FM)](#6-voice-fm)
7. [Morse code (CW)](#7-morse-code-cw)
8. [Satellites](#8-satellites)
9. [Troubleshooting](#9-troubleshooting)
10. [Glossary](#10-glossary)
11. [Learning resources and links](#11-learning-resources-and-links)

Files in this repo:

| File | What it is |
|---|---|
| [`README.md`](README.md) | This guide |
| [`frequencies.md`](frequencies.md) | New Haven area repeaters, simplex, W1YU club channels, CW, satellites, weather, and listen-only aircraft, marine and railroad channels. Readable on a phone. |
| [`w1yu-chirp.csv`](w1yu-chirp.csv) | The same channels as a CHIRP file you can load straight into the radio (see [section 5](#5-programming-frequencies-with-a-cable)) |

---

## 1. What is this radio?

We use the **Quansheng UV-K5 (Version 3)**, a cheap handheld radio that transmits and receives on two amateur ("ham") bands:

| Band | Frequencies | Nickname | Good for |
|---|---|---|---|
| VHF | 144–148 MHz | "2 meters" | Most local activity: repeaters, simplex, CW, satellite uplinks |
| UHF | 420–450 MHz | "70 centimeters" | Repeaters, simplex, satellite downlinks |

It puts out about 5 watts, roughly 1,000× the power of a cell phone's Bluetooth. With the stock antenna that's enough to reach a hilltop repeater 20–30 miles away, or another handheld a few miles away directly ("simplex").

**Why this radio?** Its firmware is open source. Volunteers have written replacement firmware that adds features the factory never shipped. The one we use, **NR7Y CW firmware**, turns this $30 voice radio into a real Morse code transmitter. That's the point of the video this guide follows:

> 📺 **[NO MOD NEEDED! $30 Morse Code Radio](https://www.youtube.com/watch?v=qwPvv8Vp9-Q)**, by Forrest KI7QCF
>
> Watch it once all the way through before you start. Sections 4, 5 and 7 below are the same steps, written out.

### Parts of the radio

```
          Antenna (SMA)   On/off + volume knob   Flashlight
                 │              │                 │
            ┌────┴──────────────┴─────────────────┴──┐
            │            ┌───────────────┐           │
     PTT ───┤            │    DISPLAY    │           │
            │            └───────────────┘           │
   SIDE 1 ──┤      [ M ]  [ ▲ ]  [ ▼ ]  [EXIT]       │
   SIDE 2 ──┤      [ 1 ]  [ 2 ]  [ 3 ]               │
            │      [ 4 ]  [ 5 ]  [ 6 ]               │
            │      [ 7 ]  [ 8 ]  [ 9 ]               │
            │      [ * ]  [ 0 ]  [ F ]               │
            └────────────────────────────────────────┘
   Under the rubber flap on the side: 2-pin speaker/mic ("K-plug") jack,
   used for the programming cable. USB-C port: charging, and the CW key adapter.
```

- **PTT** (push-to-talk): the big button on the left side. Hold it to transmit; release it to listen.
- **SIDE1 / SIDE2**: the two small buttons below PTT. In CW mode they can act as a Morse paddle.
- **M**: menu / confirm. **EXIT**: back out. **F**: "function" (shift) key.
- **Long-press** means hold a key about 1 second.

### Is my radio a Version 3?

**This matters.** The firmware for the original UV-K5 (V1) and the V3 are different. Flashing the wrong one can brick the radio.

1. Take the battery off (slide the latch on the back).
2. Read the label inside. **If it says "V3", you're good.**
3. If it says nothing about a version, you probably have a V1. Stop and ask an officer.

Brightly colored or clear cases are all V1. The V3 is black with a grey frame around the display. (The **Quansheng UV-K1** uses the same firmware as the V3 and works too.)

---

## 2. Before you transmit: licensing and rules

**Listening is legal for everyone.** You can program the radio, listen to repeaters and satellites, and practice Morse with the radio's built-in practice mode ([section 7.5](#75-practice-without-transmitting)) with no license.

**Transmitting requires an FCC amateur license.** The entry-level license is **Technician**: a 35-question multiple-choice exam with no Morse code requirement. It gives you every privilege this radio can use, CW on 2 m included.

- Study free at **[HamStudy.org](https://hamstudy.org)** (flashcards and practice exams). Most people pass after 1–3 weeks of casual study.
- Find an exam session: **[ARRL exam search](https://www.arrl.org/find-an-amateur-radio-license-exam-session)**. Many are free or cost about $15; there are online sessions too. The FCC also charges a $35 application fee.
- **Not licensed yet?** You can still talk on the air if a licensed **control operator** is standing next to you and the club station call sign (or theirs) is used. Ask an officer.

### The rules that matter day one

1. **Identify.** Say (or send in Morse) your call sign at least every **10 minutes** and at the end of every contact.
2. **Stay inside the ham bands.** This radio can be set up to transmit almost anywhere, including police, fire, aviation, marine, FRS/GMRS walkie-talkie, and business frequencies. **Never do this.** It's illegal, it can interfere with emergency services, and the FCC does fine people. After flashing, set **F Lock to FCC HAM** ([section 5.3](#53-load-the-w1yu-channel-list)) so the radio can only transmit on 144–148 and 420–450 MHz.
3. **No music, no profanity, no business, no encryption.**
4. **Listen before you transmit.** Make sure the frequency isn't in use.
5. **Emergency traffic always has priority.** If you hear someone say "break" or "emergency", stop and stand by.

### Safety

- **RF exposure:** hold the radio so the antenna is a few inches from your face, and never transmit with the antenna touching your body. At 5 W on a handheld, normal use is well within FCC exposure limits.
- **Battery:** it's lithium-ion. Charge it with a standard USB-C charger, don't leave it in a hot car, and don't use a swollen battery.
- **Never transmit without an antenna attached.** It can damage the radio.

---

## 3. Shopping list

Prices are approximate, as of fall 2026. Amazon ASINs are given so you can find the exact item.

### Required

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| **Quansheng UV-K5 V3** handheld | Amazon **ASIN B0D2QYWMNH** ([link](https://www.amazon.com/dp/B0D2QYWMNH)) | $30 | The radio from the video. **Make sure the listing says V3**, and check the label behind the battery when it arrives. Comes with battery, antenna, USB-C charging cable and belt clip. |
| **USB programming cable**, Baofeng/Kenwood style 2-pin "K-plug" | Amazon **ASIN B0B9S7N2LQ** ([link](https://www.amazon.com/dp/B0B9S7N2LQ)), "BAOFENG USB Programming Cable" | $10–15 | Used to flash firmware and program channels. The club only needs **one or two** to share. Any Baofeng UV-5R programming cable should work; ones with a **CH340** or **FTDI** chip have fewer driver problems than "Prolific" ones. |
| Computer with **Chrome** or **Edge** | — | — | Flashing happens in a web page that uses Web Serial. **Safari won't work.** (Firefox 151+ also works.) |

### For Morse code (CW)

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| **KI6CR Labs "USB-C to 3.5mm – Quansheng CW Adapter (UV-K5 Ver 3)"** | [ki6cr-labs.com/shop/quansheng-usb-adapter](https://www.ki6cr-labs.com/shop/quansheng-usb-adapter/) | $10–12.50 | Plugs into the radio's USB-C port and gives you a 3.5 mm jack for a Morse key. **No soldering or opening the radio.** Comes as **3.5mm Female (5-pack)** or **3.5mm Male (single)**. For a club, get the **female 5-pack**: one per radio, and any paddle with a normal 3.5 mm plug cable connects to it. |
| **Morse paddle or straight key** with a 3.5 mm stereo (TRS) plug | Any. Budget options: [KM4CFT paddles at HamGadgets](https://hamgadgets.com/); many $20–40 options on Amazon or eBay. Nicer: [CW Morse outdoor paddles](https://cwmorse.us/collections/outdoor-paddles), very nice portable paddles, but more expensive. | $20–60+ | Optional to start. **The radio's own PTT and side buttons can be used as a key** ([section 7.3](#73-three-ways-to-key-the-radio)), so you can begin with no extra hardware. Use a **short, shielded** cable. |

> ⚠️ The KI6CR adapter is **not** the same as a "USB-C to 3.5 mm headphone adapter". Those contain audio electronics and **will not work**. You need the passive adapter made for this firmware. ([Why](https://briand.github.io/cw-firmware-docs/hardware/usb-trs-cable/): the firmware reads the key directly off the USB-C data pins: Tip = dit on D+, Ring = dah on D−, Sleeve = ground.)

### Strongly recommended upgrades

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| Better antenna (**SMA-Female** connector) | [Signal Stuff "Signal Stick"](https://signalstuff.com/radio-models/quansheng-uvk5/) for the UV-K5, or a **genuine** Nagoya **NA-771** in **SMA-Female** | $15–30 | Probably the single biggest improvement you can make. The radio's jack is SMA-**male**, so the antenna must be SMA-**female** (the Baofeng type). Many Nagoyas on Amazon are counterfeit. |
| Spare battery | Quansheng UV-K5 battery (1600–2500 mAh) | $10–15 | |

### For satellites (optional)

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| Handheld dual-band Yagi | **Arrow II 146/437-10WBP** ([arrowantennas.com](https://www.arrowantennas.com/)) or **Elk 2M/440L5** | $90–150 | Lets you hear satellites clearly as they pass overhead. |
| **SMA-Female to BNC-Female** adapter | Any | $5 | Connects the radio to the Arrow/Elk antenna's BNC cable. |

> 💡 The [Brass Knuckle Gang club page](https://bkg.club/clubs.html) suggests starting with "three radios and a spare" and one flashing night. The **Quansheng UV-K1** also runs this firmware. BKG recommends it to clubs because every unit is identical. The KI6CR adapter calls K1 support "experimental", though, so this guide sticks with the K5 V3 from the video.

---

## 4. Updating the firmware

**Why:** The factory firmware can't send Morse code. The **NR7Y CW firmware** adds a real CW transmitter, an iambic keyer, an on-screen Morse decoder, a code practice mode, and more. It's built on **F4HWN "Fusion"**, a popular community firmware for this radio, so you also get a better spectrum display, more menu options, and finer power control.

> ⚠️ **Read first.** Custom firmware is "at your own risk". The worst case is a bricked radio, which on a $30 radio is a lesson rather than a disaster. Follow the steps exactly, **back up your calibration**, and **use only the V3/K1 firmware** on a V3/K1 radio.

### 4.1 What you need

- The radio, **fully charged**
- The USB programming cable (K-plug)
- A computer running **Chrome** or **Edge**

### 4.2 Download the files

Go to the **[NR7Y firmware releases page](https://github.com/briand/uv-k1-k5v3-firmware-custom/releases)** and, under the **latest** release (v1.4 as of October 2026), download:

1. The firmware **`.bin`** file, e.g. `nr7y.k1-k5v3.v1.4.bin`
2. The CHIRP module **`.py`** file, e.g. `nr7y.k1-k5v3.chirp.v1.4a.py` (needed in [section 5](#5-programming-frequencies-with-a-cable))

Always use the CHIRP module **from the same release** as the firmware.

> These are for the UV-K5 **V3 and UV-K1 only**. The original V1 radio has [a different repository](https://github.com/briand/uv-k5-firmware-custom-cw).

### 4.3 Connect the cable

1. **Turn the radio off.**
2. Open the rubber flap on the radio's right side and push the cable's 2-pin plug **all the way in**. It's stiff, and you may feel two clicks. A half-inserted plug is the #1 reason flashing fails.
3. Plug the USB end into your computer.

> **Mac users:** recent macOS has the CH340 driver built in. The cable shows up as something like `cu.usbserial-XXXX` or `cu.wchusbserial-XXXX`. **Windows users:** if no COM port appears in Device Manager, install the driver for the cable's chip (CH340 or FTDI).

### 4.4 Back up the calibration data (do not skip)

Every radio has factory calibration data (power levels, frequency accuracy) stored on it. Flashing *shouldn't* touch it, but a backup costs you one minute.

1. Turn the radio **on normally**, cable attached.
2. In Chrome, open **[UVTools2](https://armel.github.io/uvtools2/)**.
3. Click **Dump Calibration Data** and pick the serial port for your cable.
4. Save the `calibration.dat` file and **rename it with your radio's serial number** (on the label behind the battery), e.g. `calibration-K5V3-SN12345.dat`. Keep it somewhere safe.

### 4.5 Flash the firmware

1. **Turn the radio off.**
2. **Press and hold PTT first** (the big button at the top of the left side, *not* the two small buttons below it). *While still holding PTT*, turn the knob to switch the radio on. Keep holding for 2–3 seconds, then let go. The **flashlight LED comes on** and the screen stays **blank and dark**. That's correct: this is bootloader ("flashing") mode.
   - **If the screen shows the normal display (frequency, battery, etc.), the radio started normally. Don't flash.** Turn it off, wait a few seconds, and try again, making sure PTT is fully pressed *before* the knob clicks on. The flashlight alone doesn't prove you're in flash mode; the **dark screen** does.
   - **Don't hold Side 2.** PTT + Side 2 at power-on starts **AIR COPY (RDY)**, a wireless channel-cloning mode, not flash mode. If you see AIR COPY, **don't press any keys** (pressing MENU there transmits on 410 MHz, outside the ham bands). Just turn the radio off with no buttons held, and turn it back on.
3. In UVTools2, under **Firmware File (.bin)**, choose the `.bin` you downloaded.
4. Click **Flash firmware** and select the cable's serial port.
5. The LED blinks while it writes ("flashing the firmware", get it?). Wait for 100%. **Don't unplug anything until it finishes.**
6. The radio restarts with the new firmware. Unplug the cable and **turn the radio off and on once**.

If you see **"CW KEY STUCK"** after flashing, that's normal when the cable is still plugged in. Unplug it and power-cycle.

### 4.6 After flashing

- Run **Dump Calibration Data** again (radio on normally) and save that copy too.
- Press **M** to open the menu. You should see a **CW** category at the top. That means it worked.

> **Alternative tools:** [UV Studio](https://armel.github.io/uvstudio) (same author as UVTools2) and the [BKG programmer](https://programmer.bkg.club) also flash and configure these radios in the browser.

---

## 5. Programming frequencies with a cable

You *can* type frequencies in on the keypad, but with a cable you can load all the New Haven channels in this repo at once.

We use **[CHIRP](https://chirpmyradio.com)**, the free, standard radio programming app, with the **NR7Y module** you downloaded in step 4.2. (CHIRP's built-in Quansheng drivers don't know about the CW settings, so don't use them.)

### 5.1 Install CHIRP (one time)

1. Download **CHIRP-next** from [chirpmyradio.com](https://chirpmyradio.com/projects/chirp/wiki/Download) (Mac, Windows, or Linux).
2. Open CHIRP and turn on **Help → Developer Mode**. CHIRP restarts. You only do this once.

### 5.2 Every time you program

1. Make sure the radio is **not in CW mode with a "USB Port" key input**. In that state the radio turns off its serial port and CHIRP can't connect. To be safe, put the radio in **FM** (long-press **0** until the screen shows FM).
2. Connect the programming cable (K-plug) and turn the radio **on normally**.
3. In CHIRP: **File → Load Module** and pick the `nr7y...chirp...py` file. Accept the warning. **This has to be repeated every time you open CHIRP.**
4. **Radio → Download from radio.**
   - Vendor: **Quansheng**
   - Model: **UV-K1 & UV-K5 V3 (F4HWN Fusion)**, **NR7Y** variant
   - Port: your cable
5. **File → Save As** and save the image, e.g. `my-radio-backup-2026-10-24.img`. This is your backup of everything on the radio.

### 5.3 Load the W1YU channel list

**First, understand CHIRP's tabs.** Every file or radio you open in CHIRP gets its own tab across the top of the window. Each tab has **sub-tabs** just underneath it:

```
┌──────────────────────────────┬──────────────────┐
│ Quansheng UV-K1 & UV-K5 V3 ▼ │ w1yu-chirp.csv   │   ← main tabs (one per radio/file)
├──────────────────────────────┴──────────────────┤
│ [Memories] [Settings] [Browser] [Info]          │   ← sub-tabs of the RADIO tab
├─────────────────────────────────────────────────┤
│  1  W1YU V1   147.555000 ...                    │
│  2  W1YU V2   147.435000 ...                    │
```

- The **radio tab** is the one created by *Radio → Download from radio*. It has **Memories** and **Settings** sub-tabs (plus Browser and Info in developer mode). **This is what gets uploaded to the radio.**
- A **CSV tab** appears if you *open* the CSV file. It only has a **Memories** sub-tab, no Settings. **Nothing in a CSV tab goes to the radio** until you copy it into the radio tab.

**Steps**

Getting the channels in is two moves: **open the CSV in its own tab**, then **copy and paste** its rows into the radio tab. Importing the CSV alone does **not** put anything on the radio.

1. **Make sure you have a radio tab.** If you don't, do **Radio → Download from radio** first ([5.2](#52-every-time-you-program)).
2. **Open the CSV.** Use **File → Import** (or **File → Open**) and choose [`w1yu-chirp.csv`](w1yu-chirp.csv) from this repo. It opens in a **new tab** of its own. That's expected.
3. **Copy everything from the CSV tab.** Click any channel row in the CSV tab, press **⌘A** (Mac) or **Ctrl+A** (Windows) to select all, then **⌘C** / **Ctrl+C** to copy.
4. **Paste into the radio tab's Memories.** Click the **radio tab**, then its **Memories** sub-tab. Click the row for **channel 1** and press **⌘V** / **Ctrl+V**. Each channel lands at its own number from the file.
   - **The empty rows between groups are on purpose.** Each group starts at a round number (1 W1YU, 10 repeaters, 30 CW, 40 satellites, 60 weather, 70 aircraft, 80 marine, 90 trains), leaving room to add channels later.
   - Look through the list. CHIRP highlights any channel it doesn't like.
   - You can now close the CSV tab (don't save changes to it).
5. **⚠️ Lock transmit to the ham bands.** Still in the radio tab:
   1. Click the **Settings** sub-tab.
   2. In the list on the left, click **Unlock Settings**.
   3. Set **TX Frequency Lock (F Lock)** to **`FCC HAM (144-148, 420-450)`**.
   4. Leave the checkbox below it, **Unlock 350-400 MHz RX (350 En)**, as it is. It only lets the radio *receive* 350–400 MHz and has no effect on transmitting. None of our channels use that range.

   The firmware default (`DEFAULT+ (137-174, 400-470)`) lets the radio transmit on non-ham frequencies, including the weather, marine and railroad channels in our list. **Every radio must have this set.**
6. **Radio → Upload to radio**, with the **radio tab** selected. Wait for it to finish, then turn the radio off and on.
7. **File → Save As** a new image (e.g. `my-radio-w1yu-2026-10-24.img`), so you have a copy of the finished setup.

> The CSV was checked against the NR7Y v1.4a CHIRP module: all 57 channels import cleanly. Channel names are limited to 10 characters. CW channels import in **CW** mode and aircraft channels in **AM**, so the radio switches mode automatically when you select them.

### 5.4 Switching between channels and typing frequencies

- **Memory (channel) mode** shows channel names like `W1YU V1`. **Frequency (VFO) mode** shows a frequency you can type in directly. Toggle between them with the **VFO/MR** key (long-press **3**).
- In VFO mode, just type digits: `1 4 6 5 2 0` → 146.520 MHz.
- **Up/Down arrows** step through channels or frequencies.

### 5.5 What the channel settings mean

| CHIRP column | Meaning |
|---|---|
| **Frequency** | What you listen on |
| **Duplex / Offset** | For repeaters: the radio transmits on a slightly different frequency. `-` 0.6 MHz is standard on 2 m below 147 MHz, `+` 0.6 above 147 MHz, and ±5 MHz on 70 cm. Satellite channels use a huge offset (~290 MHz) to transmit on one band and receive on the other. |
| **Tone / rToneFreq** | A sub-audible "key" tone (CTCSS or PL) the repeater requires before it will retransmit you. Wrong tone means nobody hears you. |
| **Mode** | `FM` for voice, `CW` for Morse |
| **Power** | Use the **lowest power that works**. On simplex across campus, low power is plenty. |

---

## 6. Voice (FM)

### 6.1 Simplex vs. repeaters

- **Simplex:** radio to radio on one frequency. Range with handhelds is roughly 1–5 miles, more from a hilltop or high floor. Great for campus and events.
- **Repeater:** a radio on a tall tower or hilltop that listens on one frequency and retransmits you on another, much more powerfully. Handhelds can talk across the region. Most repeaters need the right **offset** and **tone**. These are already set in the CHIRP file.

See [`frequencies.md`](frequencies.md) for local repeaters and the W1YU simplex channels.

### 6.2 How to talk on the radio

1. **Listen first.** Wait a few seconds to make sure nobody is mid-conversation.
2. **Press and hold PTT, wait half a second, *then* speak.** People often clip their first word.
3. Hold the mic **2–4 inches** from your mouth, slightly to the side, and talk in a normal voice. Don't shout.
4. **Release PTT** when you're done. Repeaters have a timeout (often 3 minutes), so keep transmissions short.
5. **Pause 1–2 seconds** between transmissions on a repeater so others (especially emergencies) can break in.

### 6.3 Example contacts

**Announcing yourself on a repeater or simplex:**
> "KC1ABC listening."   *(or "KC1ABC monitoring")*

Plain "CQ" calls are rare on FM. Just say your call sign.

**Calling someone specific:**
> "KC1XYZ, this is KC1ABC."

**A complete short contact:**
> **You:** "KC1ABC listening on the W1YU simplex channel."
> **Them:** "KC1ABC, this is KC1XYZ. Hi, I'm Sam, I'm over in the engineering library. How are you hearing me?"
> **You:** "KC1XYZ from KC1ABC. Hi Sam, I'm Alex, I'm at Payne Whitney. You're loud and clear. This is my first contact on the new radio!"
> **Them:** "Congratulations! … 73, KC1XYZ."
> **You:** "73, thanks Sam. KC1ABC clear."

("73" means "best regards". Say your call sign at the end.)

### 6.4 Checking into a net

A **net** is a scheduled on-air meeting run by a **net control** station. They're friendly and a great first contact. When net control asks for check-ins, say your call sign **phonetically**, and only your call sign:

> "Kilo Charlie One Alpha Bravo Charlie."

Then wait to be acknowledged. Local nets are listed in [`frequencies.md`](frequencies.md). **Suggestion:** W1YU should run its own weekly student net (see the suggestions there).

### 6.5 Phonetic alphabet

| | | | | | |
|---|---|---|---|---|---|
| A Alpha | B Bravo | C Charlie | D Delta | E Echo | F Foxtrot |
| G Golf | H Hotel | I India | J Juliet | K Kilo | L Lima |
| M Mike | N November | O Oscar | P Papa | Q Quebec | R Romeo |
| S Sierra | T Tango | U Uniform | V Victor | W Whiskey | X X-ray |
| Y Yankee | Z Zulu | | | | |

### 6.6 Voice tips

- If you hear nothing, or voices sound garbled, check that the radio is in **FM** mode (long-press **0** cycles FM → AM → USB → CW).
- If a repeater "kerchunks" (a short burst of noise or a beep) when you un-key, you're getting in. If nothing happens, check the tone and offset.
- **Squelch** silences static when nobody's talking. If you hear constant hiss, raise the squelch in the menu. Too high and you'll miss weak stations.
- Move around: a few feet or a window can make a big difference on UHF/VHF. Indoors, especially in stone and steel buildings, is tough.

---

## 7. Morse code (CW)

> 📺 **Follow along: [NO MOD NEEDED! $30 Morse Code Radio](https://www.youtube.com/watch?v=qwPvv8Vp9-Q)** (Forrest KI7QCF)
> 📖 **Full reference: [NR7Y CW Firmware Docs](https://briand.github.io/cw-firmware-docs/)**

### 7.1 Why CW on 2 meters?

**CW** ("continuous wave") is Morse code sent by switching a radio signal on and off. It's the oldest digital mode, gets through when voice won't, and is a lot of fun. On VHF almost nobody does it, because normal handhelds can't. With this firmware a $30 radio can, so a club full of students with these radios can fill an empty corner of the band.

There's a growing community doing exactly this: the **[Brass Knuckle Gang (BKG)](https://bkg.club)**, a 2 m CW club started by the video's creator. They call on **144.025 MHz**. Make a 2 m CW contact with a member and you're in. (See their [page for clubs](https://bkg.club/clubs.html).)

### 7.2 Important: CW is not FM

The radio sends a real on/off **carrier** in CW mode, not a beep sent over FM. That means:

- **The other station must also be in CW (or USB/SSB) mode** to hear you as tones. A normal FM radio only hears silence and clicks.
- Two club members with flashed radios, both in CW mode on the same frequency, can talk to each other. So can anyone with an SSB-capable 2 m radio.
- Use the **CW / weak-signal part of the band** (144.025–144.100 MHz). Never use repeater or FM simplex frequencies for CW. See [`frequencies.md`](frequencies.md).

### 7.3 Three ways to key the radio

| Method | Hardware needed | Menu `CWkin` setting | Good for |
|---|---|---|---|
| **PTT as a straight key** | Nothing | `PTT HandKey` (the default) | Trying it out in 30 seconds |
| **Side buttons as a paddle** | Nothing | `Side Btn Iambic` (PTT = dah, Side 1 = dit) | Practicing with the iambic keyer on the go |
| **External paddle or key** via the KI6CR adapter | KI6CR USB-C adapter + paddle | `USB Port Iambic` (paddle) or `USB Port Handkey` (straight key) | Real operating |

If dits and dahs come out backwards on a paddle, choose the **Reversed** version of the setting.

### 7.4 Set up CW mode

1. **Put the radio in CW mode:** on the main screen, **long-press 0** to cycle modulation FM → AM → USB → **CW**. The screen shows **CW**.
   - In CW mode the squelch is held open, so you'll hear background hiss. That's normal: you're listening for weak tones. **Long-press M** (monitor) to toggle squelch if you need quiet.
2. **Open the menu:** press **M**. The **CW** category is at the top. Press **M** again to see the items:

| Menu item | What it does | Range (default) | Suggested |
|---|---|---|---|
| `CWkin` | Key input: which buttons or port act as the key ([7.3](#73-three-ways-to-key-the-radio)) | (PTT HandKey) | `Side Btn Iambic` to start; `USB Port Iambic` with a paddle |
| `CWkmod` | Keyer mode: Iambic A, Iambic B, Ultimatic, Bug | (Mode B) | Leave at **B**, or **A** if your paddle timing feels off |
| `CWwpm` | Speed in words per minute | 10–45 (18) | **12–15** while learning |
| `CWfreq` | Pitch of your sidetone and TX tone | 450–800 Hz (600) | 600 |
| `CWvol` | Sidetone volume (what *you* hear) | OFF, 1–15 (7) | To taste |
| `CWbkin` | Break-in: keying the paddle automatically transmits. **OFF = sidetone only, no RF.** | ON/OFF (ON) | **OFF while practicing, ON to transmit** |
| `CWhang` | How long TX stays on after you stop keying | 10–2000 ms (300) | 300–600 ms |
| `CWmsg1`–`CWmsg4` | Recorded messages (e.g. your CQ) | up to 46 characters | `CQ CQ DE <call> K` |
| `CWmrpt` | Delay between message repeats | 0–127 s (4) | |
| `CWrgr` | Length of the dah in a "proper roger" | 3–20 dits (9) | 9 (BKG tradition!) |

3. **Long-press 7** toggles break-in quickly. A **BKIN** icon appears when it's on (i.e. keying will transmit).

**Default side-key shortcuts** (on a freshly flashed radio):

| Key | Action |
|---|---|
| Side 1 short press | PROPER ROGER (di-*daaaaah*-dit) |
| Side 1 long press | Play CW message 1 |
| Side 2 short press | CW SPEED (use arrows to change) |
| Side 2 long press | CW KEY INPUT (step with arrows, **M** to apply) |
| M long press | Monitor |

> If you set `CWkin` to `Side Btn Iambic`, Side 1 becomes your dit paddle. You can reassign the side keys in the menu (`F1Shrt`, `F1Long`, `F2Shrt`, `F2Long`, `M Long`) or in CHIRP.

### 7.5 Practice without transmitting

The **Code Practice Oscillator (CPO)** turns the radio into a practice buzzer with an on-screen decoder. It **doesn't transmit, so no license is needed.**

- **Enter:** press **F**, then **long-press 5**. (Works from any mode.)
- **UP/DOWN:** change speed. **5:** clear the screen. **4:** flash the flashlight with your keying (fun!). **EXIT:** leave.
- **Drills:** press **F** inside CPO to cycle **Send Callsigns** (key the call shown) → **Copy Callsigns** (listen and key back what you heard) → Off. Copy Callsigns supports **Farnsworth spacing** (**2/8** keys): characters at full speed with longer gaps, the recommended way to learn.

The radio's **on-screen decoder** also works on the air. It shows what you send and what it hears, so you can check yourself.

### 7.6 Plug in an external paddle (KI6CR adapter)

1. Plug the KI6CR adapter into the radio's **USB-C port**, and your paddle into the adapter.
2. Put the radio in **CW** mode.
3. Set `CWkin` to **`USB Port Iambic`** (or `USB Port Handkey` for a straight key). Press **M** to apply.
   - If it says **"key err"** or **"CW KEY STUCK"**, the firmware thinks a paddle contact is closed. Turn the radio off, check the connection, and turn it back on.
4. Test in CPO or with break-in **OFF** first, then turn break-in ON.

**Known quirks with the USB-C adapter (from the [firmware docs](https://briand.github.io/cw-firmware-docs/hardware/usb-trs-cable/)):**

- **RF can get into the key line** and cause a stuck transmitter or random dits. If the radio keeps transmitting: **hold EXIT** to stop. To prevent it:
  - Keep the paddle cable **short and shielded**.
  - Use **Medium power, not High.**
  - Move the antenna away from the radio (a short coax to an external antenna), or add a "rat-tail" counterpoise wire to the antenna.
- There's a **7-second transmit timeout**: hold the key down 7 s without a gap and it drops TX ("TX TIMEOUT / RELEASE KEY").
- **CHIRP and USB serial don't work** while the radio is in CW mode with a USB Port input. Switch to FM to program.

### 7.7 Making a 2 m CW contact

1. Go to a CW frequency (e.g. **144.025** BKG calling, or **W1YU CW V1** on 144.070: see [`frequencies.md`](frequencies.md)) in **CW mode** with break-in ON.
2. Listen. Then send **`QRL?`** ("is this frequency in use?"). If nobody answers, call CQ.
3. Typical slow exchange:

```
You:   CQ CQ DE KC1ABC KC1ABC K
Them:  KC1ABC DE KC1XYZ K
You:   KC1XYZ DE KC1ABC  R  TNX CALL  UR 599  NAME ALEX  QTH NEW HAVEN  BK
Them:  R R  UR 559  NAME SAM  QTH HAMDEN  BK
You:   R  TNX SAM  73  KC1XYZ DE KC1ABC SK
Them:  73 SK  (dit dit)
```

| Abbrev. | Meaning | | Abbrev. | Meaning |
|---|---|---|---|---|
| CQ | Calling anyone | | UR | Your |
| DE | From ("this is") | | RST 599 | Signal report: readable 5, strength 9, tone 9 |
| K | Over, go ahead | | QTH | Location |
| BK | Back to you | | 73 | Best regards |
| R | Roger, received | | SK | End of contact |
| TNX / TU | Thanks / thank you | | QRS | Please send slower |

- **Send slowly.** It's always polite to go at the other station's speed. "QRS is a feature, not an apology."
- **Proper roger:** BKG custom is a long-dah `R` (di-*daaaah*-dit) at least once per contact. It's on **Side 1** by default.
- **Tuning:** if the other station's tone sounds much higher or lower than yours, they're slightly off frequency. In CW mode, press **\*** for **RIT** and adjust in 10 Hz steps.
- **Working SSB stations:** **long-press 8** turns on **cross-mode**, which shifts your transmit so an SSB operator hears your tone.

### 7.8 Learn Morse code

- **Learn by sound, not by sight.** Don't memorize dot/dash charts. Learn each letter's *rhythm* at full speed (Koch method + Farnsworth spacing).
- **[LCWO.net](https://lcwo.net)**: free online Koch-method course
- **[Morse Code Ninja](https://morsecode.ninja)**: free practice audio and YouTube/podcast drills
- **[Long Island CW Club](https://longislandcwclub.org)**: live online classes for beginners, close to home
- **[CWops CW Academy](https://cwops.org/cw-academy/)**: free structured online classes
- The radio's CPO **Copy Callsigns** drill ([7.5](#75-practice-without-transmitting))

---

## 8. Satellites

Yes, you can talk through a satellite with this radio. Several amateur satellites carry **FM repeaters**. When one passes overhead (about 10 minutes at a time), you can hear stations hundreds of miles away and talk to them with a handheld.

**Easiest first step: just listen.** Program the satellite channels from [`frequencies.md`](frequencies.md), look up a pass, go outside with a clear view of the sky, and listen on the downlink. The ISS and SO-50 are the most popular.

1. **Find a pass:** [Heavens-Above](https://www.heavens-above.com) (set your location to New Haven), [AMSAT Pass Predictions](https://www.amsat.org/track/), or a phone app (GoSatWatch on iOS, Look4Sat on Android). Passes with a maximum elevation above 30° are easiest.
2. **Check status:** [AMSAT live satellite status](https://www.amsat.org/status/) shows recent reports for each satellite.
3. **Doppler:** the satellite moves fast, so its frequency shifts during the pass. The channel list includes 5 channels per satellite. Start at the "+10" (AOS) channel when it rises, step down as it passes overhead, and finish on "−10" (LOS).
4. **Antenna:** a stock rubber-duck antenna can hear the ISS on a good pass. For transmitting, use a handheld Yagi like the Arrow II ([section 3](#for-satellites-optional)).

> **Limitation:** this radio is **half-duplex**. It can't listen while it transmits, so you won't hear yourself through the satellite. That's fine to start. Keep transmissions very short (call sign plus grid square, e.g. `KC1ABC FN31`), and don't transmit if you can't hear the satellite.
>
> New Haven's grid square is **FN31**.

---

## 9. Troubleshooting

| Problem | Fix |
|---|---|
| Computer doesn't see the radio / no serial port | Push the K-plug in **harder**. Try another USB port. Install the CH340/FTDI driver. Use Chrome or Edge, not Safari. |
| UVTools2 flashing fails | Make sure you're in bootloader mode: hold PTT *before* switching on; flashlight on **and screen dark**. A normal display means it didn't work, so try again. Have the cable connected and UVTools2 open first. Reseat the cable. Charge the battery. |
| CHIRP can't connect | Take the radio out of CW/USB Port mode (switch to FM). Re-do **File → Load Module**. Turn the radio on normally (not bootloader mode). |
| CHIRP says *"This is a radio-independent file and cannot be uploaded directly to a radio"* | You're on the CSV tab, not the radio tab. Do **Radio → Download from radio** to get a radio tab, then copy all rows from the CSV tab and paste them into the radio tab's Memories at channel 1 ([5.3](#53-load-the-w1yu-channel-list)). Upload from the radio tab. |
| NR7Y model is missing in CHIRP | You forgot **File → Load Module** this session. Developer Mode must be on. |
| Screen says **AIR COPY (RDY)** | You held PTT + Side 2 at power-on. Don't press MENU. Turn off, release all buttons, turn on. If it keeps coming back, make sure PTT and Side 2 aren't stuck pressed (the belt clip or a case can press them), or take the battery off for 10 seconds. |
| "CW KEY STUCK" at power-on | Unplug the programming cable or paddle, turn the radio off, then back on. |
| Radio won't stop transmitting in CW | **Hold EXIT.** Then: shorter key cable, lower power, move the antenna away from the radio. |
| Can hear the repeater but it doesn't respond | Wrong tone or offset. Check the channel in CHIRP against [`frequencies.md`](frequencies.md) and RepeaterBook. |
| Everything sounds distorted or silent | Wrong mode. Long-press **0** until you're in **FM** for voice. |
| Other person can't hear my CW | They must be in CW/USB mode too. Make sure **BKIN** is showing (break-in on). |

---

## 10. Glossary

| Term | Meaning |
|---|---|
| **HT** | "Handie-talkie", a handheld transceiver |
| **VHF / UHF** | Very / Ultra High Frequency. Here, the 2 m (144 MHz) and 70 cm (440 MHz) bands. |
| **Simplex** | Direct radio-to-radio on one frequency |
| **Repeater** | A relay station that retransmits you on another frequency |
| **Offset** | The difference between a repeater's listen and transmit frequencies |
| **CTCSS / PL tone** | A sub-audible tone a repeater requires before it will retransmit you |
| **VFO / MR** | Frequency mode (type any frequency) vs. memory channel mode |
| **Squelch** | Mutes the speaker when no signal is present |
| **CW** | Morse code sent by turning a carrier on and off |
| **Paddle / straight key** | A paddle has two levers (dit, dah) and an electronic **keyer** makes the timing. A straight key is one up/down lever where you make the timing. |
| **Iambic** | Squeezing both paddle levers sends alternating dit-dah-dit-dah |
| **Sidetone** | The beep you hear while sending, so you can hear your own Morse |
| **Break-in (BKIN)** | Keying automatically switches the radio to transmit |
| **RIT** | Receive Incremental Tuning. Fine-tunes what you hear without moving your transmit frequency. |
| **Firmware** | The software running inside the radio |
| **Bootloader mode** | A special start-up mode for installing firmware (hold PTT at power-on) |
| **CHIRP** | Free software for programming radio channels from a computer |
| **Net** | A scheduled on-air meeting run by a net control station |
| **AOS / LOS** | Acquisition / Loss of Signal: when a satellite rises and sets |
| **Doppler** | The frequency shift caused by a satellite's motion |
| **73** | Best regards |
| **QRL? / QRS / QTH** | "Is this frequency busy?" / "Send slower" / "My location" |

---

## 11. Learning resources and links

**This project's sources**
- 📺 [NO MOD NEEDED! $30 Morse Code Radio](https://www.youtube.com/watch?v=qwPvv8Vp9-Q) (KI7QCF). The video's description has the creator's affiliate links for the radio and cable if you'd like to support them.
- 📺 [How to do the internal paddle rework](https://youtu.be/hzdnNWqUeL0) (KI7QCF). An optional soldering mod for people who'd rather not use the USB-C adapter.
- 📖 [NR7Y CW Firmware Docs](https://briand.github.io/cw-firmware-docs/)
- 💾 [NR7Y firmware source and releases (UV-K5 V3 / UV-K1)](https://github.com/briand/uv-k1-k5v3-firmware-custom)
- 🔧 [UVTools2 flasher](https://armel.github.io/uvtools2/) · [UV Studio](https://armel.github.io/uvstudio) · [BKG programmer](https://programmer.bkg.club)
- 🤜 [Brass Knuckle Gang: 2 m CW club](https://bkg.club) (Discord linked from their site)
- 🔌 [KI6CR Labs CW adapter](https://www.ki6cr-labs.com/shop/quansheng-usb-adapter/)

**General**
- [ARRL: getting licensed](https://www.arrl.org/getting-licensed) · [HamStudy.org](https://hamstudy.org)
- [ARRL band plan](https://www.arrl.org/band-plan)
- [RepeaterBook](https://www.repeaterbook.com) (repeater directory; also an app)
- [CHIRP](https://chirpmyradio.com)
- [AMSAT](https://www.amsat.org) (amateur satellites) · [ARISS](https://www.ariss.org) (ham radio on the ISS)

---

*Maintained by W1YU. Corrections and additions welcome: open an issue or pull request, or tell an officer. Repeater tones and satellite status change, so if something in [`frequencies.md`](frequencies.md) is wrong, please fix it.*
