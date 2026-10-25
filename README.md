# W1YU Handheld Radio (HT) Guide

A guide from the **Yale University Amateur Radio Club (W1YU)** for getting on the air with a handheld radio ("HT"), starting from zero: no license, no radio, no experience.

---

## Getting started

### 1. Get your license

You need an FCC amateur radio license to transmit. Anyone can listen. The entry-level license is **Technician**, and it covers everything in this guide.

1. **Study.** Every exam question comes from a public question pool, so you can practice on the real questions. **[HamStudy.org](https://hamstudy.org)** is free and excellent. Most people are ready after one to three weeks of casual study. No Morse code is required.
2. **Get an FCC Registration Number (FRN)**, free, in the FCC's [CORES system](https://apps.fcc.gov/cores/). You'll need it at the exam.
3. **Sign up for an exam session.** Sessions are run by volunteer examiners, in person or online. Find one with the [ARRL exam search](https://www.arrl.org/find-an-amateur-radio-license-exam-session) or the [HamStudy session finder](https://hamstudy.org/sessions). Many are free; some charge about $15.
4. **Take the test.** It's **35 multiple-choice questions**, and you need **26 correct** to pass.
5. **Pay the FCC's $35 application fee** online when they email you after the exam. Your call sign appears in the FCC database about a week later, and then you can transmit. The license lasts 10 years.

More about the rules: [Rules and safety](docs/02-rules-and-safety.md).

### 2. Get a radio

We use the **Quansheng UV-K5 (V3)**, about **$30**: [Amazon ASIN B0D2QYWMNH](https://www.amazon.com/dp/B0D2QYWMNH). Make sure the listing says **V3**.

**That's all you need to get on the air.** Out of the box it works for voice on the two most popular local bands (2 meters and 70 centimeters).

If you'd like, you can also:

- **Install new software (firmware)** that adds features like Morse code (CW). It's free and takes about 15 minutes ([how](docs/04-firmware.md)).
- **Get a USB programming cable** (about $12) so you can install the firmware and load our channel list from a computer.
- **Get a better antenna** for more range, and an **external Morse code paddle** that's easier to use than the radio's buttons.

Part numbers and prices: [Shopping list](docs/03-shopping-list.md).

### 3. Get on the air!

- **Load our channel list.** We've put together [preprogrammed frequencies](frequencies.md) for the New Haven area: the W1YU club channels, local repeaters, and more. Load them all at once from your computer ([how](docs/05-programming.md#53-load-the-w1yu-channel-list)), or type in a few by hand.
- **Talk.** Voice works great: chat with other students across campus, reach the region through local repeaters, and join the **W1YU net on Tuesdays at 8 pm**. See [Voice](docs/06-voice.md).
- **Try other modes.** With the new firmware the radio sends real Morse code. See [Morse code (CW)](docs/07-cw.md).
- **Keep the [quick reference](docs/quick-reference.md) handy.** It's a one-page cheat sheet of buttons: changing channels, typing in a frequency, and fixing common problems.

---

## What else can I do?

The same radio can listen far beyond the ham bands. These are all in the channel list:

- 🌦️ **Get broadcast weather reports** from NOAA Weather Radio, around the clock. ([channels](frequencies.md#4-weather))
- ✈️ **Listen to pilots talking to the tower** at Tweed-New Haven Airport. ([channels](frequencies.md#aircraft-tweed-new-haven-airport-hvn))
- 🚆 **Listen in on railroad communications:** Metro-North, Amtrak and freight trains around Union Station. ([channels](frequencies.md#trains-union-station-and-the-northeast-corridor))
- ⚓ **Hear ships, tugs and the Coast Guard** on Long Island Sound. ([channels](frequencies.md#marine-new-haven-harbor-and-long-island-sound))
- 🛰️ **Talk through satellites as they fly over**, including the International Space Station's ham radio repeater, with the right antenna. ([how](docs/08-satellites.md))

---

## The full guide

The detailed pages. Work through them in order the first time you set up a radio.

| # | Page | What's in it |
|---|---|---|
| — | [Quick reference](docs/quick-reference.md) | One-page cheat sheet: buttons, channels, frequency mode, common fixes |
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
