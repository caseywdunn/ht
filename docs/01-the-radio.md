# 1. What is this radio?

We use the **Quansheng UV-K5 (Version 3)**, a cheap handheld radio that transmits and receives on two amateur ("ham") bands:

| Band | Frequencies | Nickname | Good for |
|---|---|---|---|
| VHF | 144–148 MHz | "2 meters" | Most local activity: repeaters, simplex, CW, satellite uplinks |
| UHF | 420–450 MHz | "70 centimeters" | Repeaters, simplex, satellite downlinks |

It puts out about 5 watts, roughly 1,000× the power of a cell phone's Bluetooth. With the stock antenna you can talk **a few miles** directly to another radio ("simplex"), **tens of miles** through a repeater, and **hundreds of miles** through a satellite passing overhead.

**Why this radio?** Its firmware is open source. Volunteers have written replacement firmware that adds features the factory never shipped. The one we use, **NR7Y CW firmware**, turns this $30 voice radio into a real Morse code transmitter. That's the point of the video this guide follows:

> 📺 **[NO MOD NEEDED! $30 Morse Code Radio](https://www.youtube.com/watch?v=qwPvv8Vp9-Q)**, by Forrest KI7QCF
>
> Watch it once all the way through before you start. The [Firmware](09-firmware.md), [Programming](10-programming.md) and [Morse code](04-cw.md) pages are the same steps, written out.

## Parts of the radio

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
- **Keypad lock:** **long-press F** to lock or unlock the keys. If buttons stop responding, this is almost always why.

## Is my radio a Version 3?

**This matters.** The firmware for the original UV-K5 (V1) and the V3 are different. Flashing the wrong one can brick the radio.

1. Take the battery off (slide the latch on the back).
2. Read the label inside. **If it says "V3", you're good.**
3. If it says nothing about a version, you probably have a V1. Stop: the firmware in this guide is for the V3 only.

Brightly colored or clear cases are all V1. The V3 is black with a grey frame around the display. (The **Quansheng UV-K1** uses the same firmware as the V3 and works too.)

---

[← Guide home](../README.md) · [2. Before you transmit: licensing and rules →](02-rules-and-safety.md)
