# W1YU Handheld Radio (HT) Guide

A beginner's guide for the **Yale University Amateur Radio Club (W1YU)** covering VHF/UHF handheld transceivers ("HTs"). It assumes **no radio experience at all**. You'll set up a ~$30 radio, load new firmware, program local frequencies, make voice contacts, and send Morse code (CW) over the air.

We use the **Quansheng UV-K5 (V3)** with the **NR7Y CW firmware**, following this video:

> 📺 **[NO MOD NEEDED! $30 Morse Code Radio](https://www.youtube.com/watch?v=qwPvv8Vp9-Q)**, by Forrest KI7QCF

---

## Quick start: using the radio

*For a radio that's already flashed and has the W1YU channels loaded. If yours isn't set up yet, start with [the full guide](#the-full-guide).*

> 🔑 **Not licensed yet?** Listening is fine. **Don't press PTT** unless a licensed operator is with you ([why](docs/02-rules-and-safety.md)).

### The basics

| To… | Do this |
|---|---|
| **Turn on / set volume** | Turn the knob on top |
| **Unlock the keys** (lock icon, keys don't respond) | **Long-press F** (bottom right) |
| **Talk** | Hold **PTT** (big button on the left side), wait half a second, speak, then **let go to listen** |
| **Say who you are** | Say your call sign at the end of a contact and every 10 minutes |

"Long-press" means hold the key about one second.

### Channels (memory mode)

In memory mode the screen shows a **channel name** like `W1YU V1`.

| To… | Do this |
|---|---|
| **Go to the next or previous channel** | Press **▲** or **▼** |
| **Get back to memory mode** from frequency mode | **Long-press 3** |

Useful channels (full list in [`frequencies.md`](frequencies.md)):

| Ch | Name | What |
|---|---|---|
| 1 | W1YU V1 | Club voice channel. Start here. |
| 4 | W1YU CW V1 | Club Morse code channel |
| 7 | CALL 2M | National calling frequency (146.520) |
| 10 | W1SPC 147 | Repeater: W1YU net, Tuesdays 8 pm |
| 60 | WX WXJ42 | NOAA weather (listen only) |
| 70 | HVN TWR | Tweed airport tower (listen only) |

### Frequencies (frequency / "VFO" mode)

In frequency mode the screen shows a **frequency** like `146.520`.

| To… | Do this |
|---|---|
| **Switch between channel and frequency mode** | **Long-press 3** (the key is labeled VFO MEM) |
| **Type a frequency** | Type 6 digits. `1 4 6 5 2 0` gives **146.520**. |
| **Nudge the frequency up or down** | Press **▲** or **▼** |
| **Switch between the top (A) and bottom (B) line** | **Long-press 2**. The radio talks on whichever line is selected. |

### If something seems wrong

| Problem | Fix |
|---|---|
| Voices sound garbled, or you hear hiss and tones | You're in the wrong mode. **Long-press 0** until the screen shows **FM**. |
| Hear nothing at all | Turn up the volume. **Long-press M** (monitor) to open the squelch and check that the radio is receiving. |
| Repeater doesn't answer | Use the channel from the list. It has the right tone and offset already set. |
| Anything else | See [Troubleshooting](docs/09-troubleshooting.md) |

### Morse code in 30 seconds

1. Select channel **4 (W1YU CW V1)**. The radio switches to CW automatically.
2. **Long-press 7** until **BKIN** shows at the top. Keying will now transmit.
3. Tap **PTT** as a Morse key. To practice without transmitting, use **F**, then **long-press 5** (practice mode, no license needed).

More in [Morse code (CW)](docs/07-cw.md).

---

## The full guide

Work through these in order the first time.

| # | Page | What's in it |
|---|---|---|
| 1 | [The radio](docs/01-the-radio.md) | What it is, buttons, checking you have a V3 |
| 2 | [Rules and safety](docs/02-rules-and-safety.md) | Licensing, the rules that matter day one, safety |
| 3 | [Shopping list](docs/03-shopping-list.md) | Parts with part numbers and prices |
| 4 | [Firmware](docs/04-firmware.md) | Installing the NR7Y CW firmware |
| 5 | [Programming](docs/05-programming.md) | CHIRP, loading the W1YU channels, putting your call sign on the radio |
| 6 | [Voice (FM)](docs/06-voice.md) | Simplex, repeaters, how to talk, nets, phonetics |
| 7 | [Morse code (CW)](docs/07-cw.md) | Keying options, CW settings, practice mode, paddles, on-air contacts |
| 8 | [Satellites](docs/08-satellites.md) | Hearing and working the ISS and FM satellites |
| 9 | [Troubleshooting](docs/09-troubleshooting.md) | Common problems and fixes |
| 10 | [Glossary](docs/10-glossary.md) | Jargon explained |

**Frequencies:** [`frequencies.md`](frequencies.md) lists New Haven repeaters, W1YU simplex and CW channels, satellites, weather, and listen-only aircraft, marine and railroad channels. The same channels are in [`w1yu-chirp.csv`](w1yu-chirp.csv), ready to load ([how](docs/05-programming.md#53-load-the-w1yu-channel-list)).

---

## Learning resources and links

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
