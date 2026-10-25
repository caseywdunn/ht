# 8. Shopping list

Prices are approximate, as of fall 2026. Amazon ASINs are given so you can find the exact item.

## Required

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| **Quansheng UV-K5 V3** handheld | Amazon **ASIN B0D2QYWMNH** ([link](https://www.amazon.com/dp/B0D2QYWMNH)) | $30 | The radio from the video. **Make sure the listing says V3**, and check the label behind the battery when it arrives. Comes with battery, antenna, USB-C charging cable and belt clip. |
| **USB programming cable**, Baofeng/Kenwood style 2-pin "K-plug" | Amazon **ASIN B0B9S7N2LQ** ([link](https://www.amazon.com/dp/B0B9S7N2LQ)), "BAOFENG USB Programming Cable" | $10–15 | Used to flash firmware and program channels. One cable can be shared by several people. Any Baofeng UV-5R programming cable should work; ones with a **CH340** or **FTDI** chip have fewer driver problems than "Prolific" ones. |
| Computer with **Chrome** or **Edge** | — | — | Flashing happens in a web page that uses Web Serial. **Safari won't work.** (Firefox 151+ also works.) |

## For Morse code (CW)

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| **KI6CR Labs "USB-C to 3.5mm – Quansheng CW Adapter (UV-K5 Ver 3)"** | [ki6cr-labs.com/shop/quansheng-usb-adapter](https://www.ki6cr-labs.com/shop/quansheng-usb-adapter/) | $10–12.50 | Plugs into the radio's USB-C port and gives you a 3.5 mm jack for a Morse key. **No soldering or opening the radio.** Comes as **3.5mm Female (5-pack)** or **3.5mm Male (single)**. Get the **female** version: any paddle with a normal 3.5 mm plug cable connects to it. The 5-pack is a good deal if a few friends order together. |
| **Morse paddle or straight key** with a 3.5 mm stereo (TRS) plug | Any. Budget options: [KM4CFT paddles at HamGadgets](https://hamgadgets.com/); many $20–40 options on Amazon or eBay. Nicer: [CW Morse outdoor paddles](https://cwmorse.us/collections/outdoor-paddles), very nice portable paddles, but more expensive. | $20–60+ | Optional to start. **The radio's own PTT and side buttons can be used as a key** ([section 4.3](04-cw.md#43-practice-with-the-radios-buttons)), so you can begin with no extra hardware. Use a **short, shielded** cable. |

> ⚠️ The KI6CR adapter is **not** the same as a "USB-C to 3.5 mm headphone adapter". Those contain audio electronics and **will not work**. You need the passive adapter made for this firmware. ([Why](https://briand.github.io/cw-firmware-docs/hardware/usb-trs-cable/): the firmware reads the key directly off the USB-C data pins: Tip = dit on D+, Ring = dah on D−, Sleeve = ground.)

## Strongly recommended upgrades

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| Better antenna (**SMA-Female** connector) | [Signal Stuff "Signal Stick"](https://signalstuff.com/radio-models/quansheng-uvk5/) for the UV-K5, or a **genuine** Nagoya **NA-771** in **SMA-Female** | $15–30 | Probably the single biggest improvement you can make. The radio's jack is SMA-**male**, so the antenna must be SMA-**female** (the Baofeng type). Many Nagoyas on Amazon are counterfeit. |
| Spare battery | Quansheng UV-K5 battery (1600–2500 mAh) | $10–15 | |

## For satellites (optional)

| Item | Part / where | ~Price | Notes |
|---|---|---|---|
| Handheld dual-band Yagi | **Arrow II 146/437-10WBP** ([arrowantennas.com](https://www.arrowantennas.com/)) or **Elk 2M/440L5** | $90–150 | Lets you hear satellites clearly as they pass overhead. |
| **SMA-Female to BNC-Female** adapter | Any | $5 | Connects the radio to the Arrow/Elk antenna's BNC cable. |

> 💡 The **Quansheng UV-K1** also runs this firmware, and the [Brass Knuckle Gang](https://bkg.club/clubs.html) recommends it because every unit is identical. The KI6CR adapter calls K1 support "experimental", though, so this guide sticks with the K5 V3 from the video.

---

[← Guide home](../README.md) · [← 7. Glossary](07-glossary.md) · [9. Updating the firmware →](09-firmware.md)
