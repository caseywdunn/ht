# 9. Troubleshooting

| Problem | Fix |
|---|---|
| Computer doesn't see the radio / no serial port | Push the K-plug in **harder**. Try another USB port. Install the CH340/FTDI driver. Use Chrome or Edge, not Safari. |
| UVTools2 flashing fails | Make sure you're in bootloader mode: hold PTT *before* switching on; flashlight on **and screen dark**. A normal display means it didn't work, so try again. Have the cable connected and UVTools2 open first. Reseat the cable. Charge the battery. |
| Keys don't respond / lock icon on screen | The keypad is locked. **Long-press F** (the `F #` key, bottom right) to unlock. The firmware auto-locks after a short idle time by default. To turn that off, set **Menu → Keys → KeyLck** to **OFF**, or in CHIRP **Settings → Basic Settings → Auto Lock Keypad After Delay (KeyLck)**. |
| CHIRP can't connect | Take the radio out of CW/USB Port mode (switch to FM). Re-do **File → Load Module**. Turn the radio on normally (not bootloader mode). |
| CHIRP says *"This is a radio-independent file and cannot be uploaded directly to a radio"* | You're on the CSV tab, not the radio tab. Do **Radio → Download from radio** to get a radio tab, then copy all rows from the CSV tab and paste them into the radio tab's Memories at channel 1 ([5.3](05-programming.md#53-load-the-w1yu-channel-list)). Upload from the radio tab. |
| NR7Y model is missing in CHIRP | You forgot **File → Load Module** this session. Developer Mode must be on. |
| Screen says **AIR COPY (RDY)** | You held PTT + Side 2 at power-on. Don't press MENU. Turn off, release all buttons, turn on. If it keeps coming back, make sure PTT and Side 2 aren't stuck pressed (the belt clip or a case can press them), or take the battery off for 10 seconds. |
| "CW KEY STUCK" at power-on | Unplug the programming cable or paddle, turn the radio off, then back on. |
| Radio won't stop transmitting in CW | **Hold EXIT.** Then: shorter key cable, lower power, move the antenna away from the radio. |
| Can hear the repeater but it doesn't respond | Wrong tone or offset. Check the channel in CHIRP against [`frequencies.md`](../frequencies.md) and RepeaterBook. |
| Everything sounds distorted or silent | Wrong mode. Long-press **0** until you're in **FM** for voice. |
| Other person can't hear my CW | They must be in CW/USB mode too. Make sure **BKIN** is showing (break-in on). |

---

[← Guide home](../README.md) · [← 8. Satellites](08-satellites.md) · [10. Glossary →](10-glossary.md)
