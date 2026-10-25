# 10. Programming frequencies with a cable

You *can* type frequencies in on the keypad, but with a cable you can load all the New Haven channels in this repo at once.

We use **[CHIRP](https://chirpmyradio.com)**, the free, standard radio programming app, with the **NR7Y module** you downloaded in step 4.2. (CHIRP's built-in Quansheng drivers don't know about the CW settings, so don't use them.)

## 10.1 Install CHIRP (one time)

1. Download **CHIRP-next** from [chirpmyradio.com](https://chirpmyradio.com/projects/chirp/wiki/Download) (Mac, Windows, or Linux).
2. Open CHIRP and turn on **Help → Developer Mode**. CHIRP restarts. You only do this once.

## 10.2 Every time you program

1. Make sure the radio is **not in CW mode with a "USB Port" key input**. In that state the radio turns off its serial port and CHIRP can't connect. To be safe, put the radio in **FM** (long-press **0** until the screen shows FM).
2. Connect the programming cable (K-plug) and turn the radio **on normally**.
3. In CHIRP: **File → Load Module** and pick the `nr7y...chirp...py` file. Accept the warning. **This has to be repeated every time you open CHIRP.**
4. **Radio → Download from radio.**
   - Vendor: **Quansheng**
   - Model: **UV-K1 & UV-K5 V3 (F4HWN Fusion)**, **NR7Y** variant
   - Port: your cable
5. **File → Save As** and save the image, e.g. `my-radio-backup-2026-10-24.img`. This is your backup of everything on the radio.

## 10.3 Load the W1YU channel list

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

1. **Make sure you have a radio tab.** If you don't, do **Radio → Download from radio** first ([10.2](#102-every-time-you-program)).
2. **Open the CSV.** Use **File → Import** (or **File → Open**) and choose [`w1yu-chirp.csv`](../w1yu-chirp.csv) from this repo. It opens in a **new tab** of its own. That's expected.
3. **Copy everything from the CSV tab.** Click any channel row in the CSV tab, press **⌘A** (Mac) or **Ctrl+A** (Windows) to select all, then **⌘C** / **Ctrl+C** to copy.
4. **Paste into the radio tab's Memories.** Click the **radio tab**, then its **Memories** sub-tab. Click the row for **channel 1** and press **⌘V** / **Ctrl+V**. Each channel lands at its own number from the file.
   - **The empty rows between groups are on purpose.** Each group starts at a round number (1 W1YU, 10 repeaters, 30 CW, 40 satellites, 60 weather, 70 aircraft, 80 marine, 90 trains), leaving room to add channels later.
   - Look through the list. CHIRP highlights any channel it doesn't like.
   - You can now close the CSV tab (don't save changes to it).
5. **Assign scan lists** so the radio's scan feature works ([how to scan](quick-reference.md#scanning)). The CSV can't carry this setting, so every pasted channel starts with its scan list **OFF**, and the radio skips OFF channels when scanning. In the radio tab's **Memories** sub-tab:
   1. Select channels **1–3**, then hold **⌘** (Mac) or **Ctrl** (Windows) and also select **7–22**. These are the voice channels: W1YU, calling and repeaters.
   2. **Right-click → Properties**, open the **Extra** tab, set **Scanlists (SList)** to **List [1]**, and click **OK**.
   3. Select channels **70–96** (aircraft, marine, trains) and set them to **List [2]** the same way.
   4. Leave the rest **OFF**. CW channels (4–6, 30) would stop the scan constantly, because the radio keeps the squelch open in Morse code mode. Weather (60–62) never goes quiet, and satellites are only overhead a few minutes at a time.

   (**View → Show extra fields** shows the scan list as a column, so you can check your work.)
6. **⚠️ Lock transmit to the ham bands.** Still in the radio tab:
   1. Click the **Settings** sub-tab.
   2. In the list on the left, click **Unlock Settings**.
   3. Set **TX Frequency Lock (F Lock)** to **`FCC HAM (144-148, 420-450)`**.
   4. Leave the checkbox below it, **Unlock 350-400 MHz RX (350 En)**, as it is. It only lets the radio *receive* 350–400 MHz and has no effect on transmitting. None of our channels use that range.

   The firmware default (`DEFAULT+ (137-174, 400-470)`) lets the radio transmit on non-ham frequencies, including the weather, marine and railroad channels in our list. **Every radio must have this set.**
7. **Show channel names on the screen.** Still in **Settings**, open **Basic Settings** and set **Channel Display Mode (ChDisp)** to **Name + Frequency (NAME + FREQ)**. Otherwise the radio may show only a frequency or channel number in memory mode. If you'd like the screen to show only one line instead of two (A and B), also set **RX Mode (RX MODE)** to **MAIN ONLY**. While you're there, set **Auto Lock Keypad After Delay (KeyLck)** to **OFF**, or to a longer delay like `02m:00s`, so the keys don't lock seconds after you stop pressing them.
8. **Radio → Upload to radio**, with the **radio tab** selected. Wait for it to finish, then turn the radio off and on.
9. **File → Save As** a new image (e.g. `my-radio-w1yu-2026-10-24.img`), so you have a copy of the finished setup.

> The CSV was checked against the NR7Y v1.4a CHIRP module: all 57 channels import cleanly. Channel names are limited to 10 characters. CW channels import in **CW** mode and aircraft channels in **AM**, so the radio switches mode automatically when you select them.

## 10.4 Saving, and setting up more than one radio

**Your edits aren't saved to your computer automatically.** Changes in CHIRP live only in the open tab until you choose **File → Save** (⌘S / Ctrl+S). Uploading to the radio does *not* save a copy on your computer, so save the image too.

**Yes, you can use one image for several radios**, if they're all UV-K5 V3s (or K1s) on the **same firmware version**:

1. Set up one radio completely (channels, scan lists, F Lock, ChDisp) and **File → Save As** e.g. `w1yu-setup.img`.
2. For each other radio: connect it, first do **Radio → Download from radio** and save that as a backup (e.g. `backup-SN12345.img`).
3. Open `w1yu-setup.img` (**File → Open**), select its tab, and **Radio → Upload to radio**.

What gets copied and what doesn't:

- **Copied:** channels, scan lists, and every setting, including F Lock and ChDisp.
  - It also copies **personal settings**: the call sign on the start-up screen and the CW messages from [10.7](#107-put-your-call-sign-on-the-radio). Change those per person before uploading, or just leave them blank in the shared image.
- **Not copied:** each radio's factory **calibration** (power and frequency accuracy). It's stored separately and is only uploaded if you tick **Settings → Calibration → upload calibration**. **Never tick that** when sharing an image between radios.
- **Firmware version must match.** Every radio should run the same firmware release. The NR7Y CHIRP module refuses to upload to a radio running older firmware, so flash it first.

## 10.5 Switching between channels and typing frequencies

- **Memory (channel) mode** shows channel names like `W1YU V1`. **Frequency (VFO) mode** shows a frequency you can type in directly. Toggle between them with the **VFO/MR** key (long-press **3**).
- In VFO mode, just type digits: `1 4 6 5 2 0` → 146.520 MHz.
- **Up/Down arrows** step through channels or frequencies.
- See the [Quick reference](quick-reference.md) for a one-page cheat sheet.

## 10.6 What the channel settings mean

| CHIRP column | Meaning |
|---|---|
| **Frequency** | What you listen on |
| **Duplex / Offset** | For repeaters: the radio transmits on a slightly different frequency. `-` 0.6 MHz is standard on 2 m below 147 MHz, `+` 0.6 above 147 MHz, and ±5 MHz on 70 cm. Satellite channels use a huge offset (~290 MHz) to transmit on one band and receive on the other. |
| **Tone / rToneFreq** | A sub-audible "key" tone (CTCSS or PL) the repeater requires before it will retransmit you. Wrong tone means nobody hears you. |
| **Mode** | `FM` for voice, `CW` for Morse |
| **Power** | Use the **lowest power that works**. On simplex across campus, low power is plenty. |

## 10.7 Put your call sign on the radio

The radio doesn't need your call sign to work. On voice you identify yourself by saying it. But putting it in makes the radio easy to identify and saves a lot of keying on CW. All of this is in the radio tab's **Settings** sub-tab in CHIRP. Upload when done.

**On the start-up screen** (*Settings → Basic Settings*):

| Setting | Set to |
|---|---|
| **Power On Display Message (POnMsg)** | `User message line 1 and line 2 (MESSAGE)` |
| **Message Line 1** (12 characters max) | Your call sign, e.g. `KC1ABC` |
| **Message Line 2** (12 characters max) | Your name, or `W1YU` |

Now your call sign shows every time the radio turns on, which also makes it easy to tell whose radio is whose.

**As CW messages** (*Settings → CW Macros*). It's much easier to type these here than to key them in on the radio:

| Setting | Example | Use |
|---|---|---|
| **CW Message 1** | `CQ CQ DE KC1ABC KC1ABC K` | Calling CQ. Plays with a **long-press of Side 1** (the default). |
| **CW Message 2** | `KC1ABC` | Your call sign, for identifying at the end of a contact |
| **CW Message 3** | `QRL?` | Asking if the frequency is in use |

Messages can be up to 46 characters. Prosigns can be typed as `<SK>`, `<BK>`, `<KA>`, `<SN>`, `<UR>` or `<SOS>`. The radio must be in CW mode with break-in on (**BKIN**) for a message to transmit; otherwise it only plays the sidetone. See [CW §4.4](04-cw.md#44-set-up-cw-mode).

---

[← Guide home](../README.md) · [← 9. Updating the firmware](09-firmware.md)
