# Quick reference: using the radio

*A one-page cheat sheet for a radio that's already flashed and has the W1YU channels loaded. If yours isn't set up yet, start with [Firmware](09-firmware.md) and [Programming](10-programming.md).*

> 📘 **Manuals:** [Quansheng UV-K5 factory manual](https://en.qsfj.com/support/downloads/3268) (get the **V3 User Manual**; it describes the original software) · [NR7Y CW firmware docs](https://briand.github.io/cw-firmware-docs/) · [F4HWN Fusion firmware](https://github.com/armel/uv-k1-k5v3-firmware-custom#readme)

> 🔑 **Not licensed yet?** Listening is fine. **Don't press PTT** unless a licensed operator is with you ([why](02-rules-and-safety.md)).

## The basics

| To… | Do this |
|---|---|
| **Turn on / set volume** | Turn the knob on top |
| **Unlock the keys** (lock icon, keys don't respond) | **Long-press F** (bottom right) |
| **Stop the keys locking by themselves** | Menu → **Keys** → **KeyLck** → **OFF** (or a longer time). See [Using the menu](#using-the-menu). |
| **Talk** | Hold **PTT** (big button on the left side), wait half a second, speak, then **let go to listen** |
| **Say who you are** | Say your call sign at the end of a contact and every 10 minutes |

"Long-press" means hold the key about one second.

## Two ways to tune: memory mode and frequency mode

The radio works in one of two modes:

- **Memory mode:** you pick from **saved channels**, like presets on a car radio. The screen shows a **channel name** like `W1YU V1`. Use this most of the time.
  - **No name showing, just a frequency or a channel number?** Turn names on: Menu → **Display** → **ChDisp** → **NAME+FREQ** ([how](#using-the-menu)). (In CHIRP it's **Settings → Basic Settings → Channel Display Mode (ChDisp)**.)
- **Frequency mode** (hams call it **"VFO" mode**): you **type in any frequency** you like. The screen shows just a **frequency** like `146.520`, with no channel name.

**To switch between them, long-press the 3 key** (it's labeled **VFO MEM**). Each long-press flips to the other mode:

| You want… | And the screen shows… | Do this |
|---|---|---|
| **Memory mode** | A frequency with no channel name (you're in frequency mode) | **Long-press 3** once. A channel name appears. |
| **Frequency mode** | A channel name (you're in memory mode) | **Long-press 3** once. The channel name disappears and you can type a frequency. |

## One line or two (A and B)

The radio can show **two lines**, **A** (top) and **B** (bottom). Each has its own channel or frequency, like two radios in one. Each line can also be in its own mode, and long-press 3 changes only the **selected** line (the one with the arrow or highlight).

| To… | Do this |
|---|---|
| **Switch between line A and line B** | **Long-press 2** (labeled A/B). The radio talks and listens on the selected line. |
| **Show just one line** (simplest) | Menu → **Radio** → **RxMode** → **MAIN ONLY** ([how](#using-the-menu)). **MO** appears at the top of the screen. |
| **Show and listen to both lines** | Set **RxMode** to **DUAL RX RESPOND** (shown as **DWR**). The radio listens to both and answers on whichever one was last active. |

With **MAIN ONLY**, the radio listens only to the selected line, and long-press 2 still switches between A and B.

## Channels (memory mode)

| To… | Do this |
|---|---|
| **Get into memory mode** | **Long-press 3** until a channel name shows |
| **Go to the next or previous channel** | Press **▲** or **▼** |

Useful channels (full list in [`frequencies.md`](../frequencies.md)):

| Ch | Name | What |
|---|---|---|
| 1 | W1YU V1 | Club voice channel. Start here. |
| 4 | W1YU CW V1 | Club Morse code channel |
| 7 | CALL 2M | National calling frequency (146.520) |
| 10 | W1SPC 147 | Repeater in Woodbridge |
| 60 | WX WXJ42 | NOAA weather (listen only) |
| 70 | HVN TWR | Tweed airport tower (listen only) |

## Frequencies (frequency / "VFO" mode)

| To… | Do this |
|---|---|
| **Get into frequency mode** | **Long-press 3** until the channel name disappears and only a frequency shows |
| **Type a frequency** | Type 6 digits. `1 4 6 5 2 0` gives **146.520**. |
| **Nudge the frequency up or down** | Press **▲** or **▼** |

## Squelch (muting the static)

**Squelch** keeps the speaker silent when nobody is talking, so you don't hear constant static (a hissing noise). The level shows under each line on the screen as **SQL** plus a number from 0 to 9.

| To… | Do this |
|---|---|
| **Make it quieter** (cut out more static) | Press **F**, then **▲** |
| **Hear weaker stations** | Press **F**, then **▼** |
| **Set an exact level** | Menu → **Radio** → **Sql** |
| **Briefly hear everything**, static included | **Long-press M** (monitor). Long-press again to go back. |

- **Too low** and you'll hear static all the time, and scanning will stop on noise.
- **Too high** and you'll miss weak stations.
- Around **2–4** usually works. Set it just high enough that the static goes away.

In Morse code (CW) mode the radio holds the squelch open on purpose, so hearing static there is normal.

## Scanning

Scanning makes the radio step through channels or frequencies by itself and **stop when it hears someone**. It's a great way to find activity.

| To… | Do this |
|---|---|
| **Start scanning** | **Long-press \*** (the key is labeled SCAN). A small **S** appears at the top of the screen. |
| **Stop and stay on what it found** | Press **M** |
| **Stop and go back to where you started** | Press **EXIT** |

What it scans depends on the mode you're in:

- **In memory mode** it steps through your **saved channels**. If you followed [the setup steps](10-programming.md#103-load-the-w1yu-channel-list), there are two scan lists:
  - **List 1:** voice channels (W1YU, calling, repeaters)
  - **List 2:** listen-only channels (aircraft, marine, trains)

  **To switch lists, type two digits while it's scanning:**

  | Type | Scans |
  |---|---|
  | `0` `1` | List 1: voice channels |
  | `0` `2` | List 2: listen-only channels |
  | `0` `0` | **All** lists together |

  The radio switches right away and keeps scanning. You can also choose which list it starts with: Menu → **Scan** → **SList**.
- **In frequency mode** it steps **up through frequencies** from where you are, a little at a time. This is good for exploring a band and finding activity that isn't in your channel list.

When a transmission ends, the radio waits a few seconds, then keeps scanning.

### Skipping a channel

| To… | Do this |
|---|---|
| **Skip a channel that keeps stopping the scan** | When the scan stops on it, **long-press M**. The radio marks the channel to skip and keeps scanning. It stays skipped, even after you turn the radio off. |
| **Stop skipping it** | Go to that channel in memory mode and **long-press 5** once. |
| **Take a channel out of scanning for good** | In CHIRP, set its scan list to **OFF** ([how](10-programming.md#103-load-the-w1yu-channel-list)) and upload. |

Careful with **long-press 5** on a channel that *isn't* skipped: each long-press moves that channel to the next scan list (1 → 2 → 3 … → ALL → OFF). If you change one by accident, CHIRP is the easiest way to set it back.

> **Scan finds nothing at all in memory mode?** The channels probably have no scan list assigned. Fix it in CHIRP ([step 5 here](10-programming.md#103-load-the-w1yu-channel-list)).

## Using the menu

Settings are grouped into **categories**.

1. Press **M**. A list of categories appears (**CW**, **Channels**, **Scan**, **Keys**, **Display**, **Radio**…).
2. Use **▲ / ▼** to pick a category and press **M** to open it.
3. Use **▲ / ▼** to pick a setting and press **M** to change it.
4. Use **▲ / ▼** to choose a value and press **M** to save it.
5. Press **EXIT** to back out, one level per press.

| Setting | Category | What it does |
|---|---|---|
| **ChDisp** | Display | What memory mode shows (choose **NAME+FREQ**) |
| **POnMsg** | Display | The start-up message |
| **KeyLck** | Keys | Keypad auto-lock delay (**OFF** to disable) |
| **RxMode** | Radio | One line (**MAIN ONLY**) or listen to both |
| **Sql** | Radio | Squelch level |
| **SList** | Scan | Which scan list to use |
| **CWwpm**, **CWkin**, … | CW | Morse code settings ([details](04-cw.md#49-settings-reference)) |

**Can't find something?** The **All** category, at the bottom of the category list, has every setting in one long list.

## If something seems wrong

| Problem | Fix |
|---|---|
| Voices sound garbled, or you hear hiss and tones | You're in the wrong mode. **Long-press 0** until the screen shows **FM**. |
| Hear nothing at all | Turn up the volume. **Long-press M** (monitor) to open the squelch and check that the radio is receiving. |
| Repeater doesn't answer | Use the channel from the list. It has the right tone and offset already set. |
| Anything else | See [Troubleshooting](06-troubleshooting.md) |

## Morse code in 30 seconds

1. **Practice first** (no license needed): press **F**, then **long-press 5**. **Side 1** sends dits and **PTT** sends dahs; hold one to repeat. **EXIT** leaves.
2. **On the air:** select channel **4 (W1YU CW V1)**. The radio switches to CW automatically.
3. **Long-press 7** until **BKIN** shows at the top. Now Side 1 and PTT transmit Morse code.

More in [Morse code (CW)](04-cw.md).

---

[← Guide home](../README.md) · [1. What is this radio? →](01-the-radio.md)
