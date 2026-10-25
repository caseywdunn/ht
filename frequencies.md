# New Haven Area Frequencies (W1YU)

Frequencies for VHF/UHF handhelds in and around New Haven, CT. All of these are already in [`w1yu-chirp.csv`](w1yu-chirp.csv) (the "Ch" column), except the listen-only frequencies marked "VFO" and the "not in the CSV" tables.

*Last checked: **October 2026**, against RepeaterBook, the Connecticut Spectrum Management Association (CSMA) coordination database, and club websites. Repeaters change tones, move, and go off the air. If something doesn't work, check [RepeaterBook](https://www.repeaterbook.com) and update this file.*

**How to read the tables**

- **Output:** the frequency you listen on (what goes in the radio's main frequency).
- **Offset:** how far your transmit frequency is from the output. `−0.6` means you transmit 600 kHz lower.
- **Tone:** the CTCSS/PL tone your radio must send to open the repeater.
- ✅ = confirmed by two or more sources. ⚠️ = verify before relying on it.

---

## 1. W1YU club frequencies (suggested)

These are **proposals** for the club to adopt. They were picked to fit the [ARRL band plan](https://www.arrl.org/band-plan) and to stay clear of busy local frequencies (see "Why these" below). Before adopting them, listen for a couple of weeks, and if possible check with the [CT Spectrum Management Association](https://efile.ctspectrum.com/search.html) (the CT frequency coordinator).

### Voice (FM simplex)

| Ch | Name | Frequency | Use |
|---|---|---|---|
| 1 | W1YU V1 | **147.555** | Primary club 2 m simplex: campus ops, events, meeting up |
| 2 | W1YU V2 | **147.435** | Alternate 2 m simplex, if V1 is busy |
| 3 | W1YU U1 | **446.050** | Primary club 70 cm simplex. Often works better than 2 m inside buildings. |

**Naming:** `W1YU` + mode (blank = FM voice, `CW` = Morse) + band (`V` = VHF/2 m, `U` = UHF/70 cm) + number.

**Why these:**
- They're in the 2 m FM-simplex segments (146.40–146.58 and 147.42–147.57 MHz).
- **Avoided:** 146.520 (national calling, shouldn't be used for long chats), 146.535 (CT ARES statewide simplex), 146.55/146.58 (popular local simplex; 146.58 is reported busy in the New Haven–Bridgeport area), 146.445–146.490 (NY-metro repeaters with 1 MHz splits use these), 146.505 and 147.495–147.52 (the W1SPC 147.505 repeater and its input), 145.505 (SPARC's simplex net), and 145.8–146.0 (satellites only).
- 446.050 is next to the 70 cm national calling frequency (446.000) in the FM simplex area. Stay away from 70 cm repeater pairs (442–445 and 447–450).

### Morse code (CW)

> Remember: CW channels only work with **another CW/SSB-capable radio** ([CW §4.2](docs/04-cw.md#42-important-cw-is-not-fm)). Leave CW mode before using any FM frequency.

| Ch | Name | Frequency | Mode | Use |
|---|---|---|---|---|
| 4 | W1YU CW V1 | **144.070** | CW | Primary club 2 m CW: practice and contacts |
| 5 | W1YU CW V2 | **144.090** | CW | Alternate 2 m CW, or a second group at the same time |
| 6 | W1YU CW U1 | **432.075** | CW | Primary club 70 cm CW |
| 30 | BKG CALL | **144.025** | CW | [Brass Knuckle Gang](https://bkg.club/clubs.html) 2 m CW calling frequency. Call CQ here, then move up after you make contact. |
| VFO | — | 144.200 | USB | **Listen only.** The national 2 m SSB calling frequency. Use cross-mode (long-press 8) to work SSB stations in CW. **Never transmit here in USB mode**: the radio actually sends FM. |

**Why these:** The ARRL plan puts 144.000–144.050 for EME (moonbounce, mostly CW) and **144.050–144.100 for general CW and weak signals**. BKG uses 144.025, at the top of the EME segment, so listen first and send `QRL?`. The W1YU frequencies sit in the general CW segment. On 70 cm, 432.070–432.100 is the weak-signal CW area, just below the 432.100 calling frequency.

### Suggested regular activities

| What | When (suggested) | Where |
|---|---|---|
| **Student simplex check-in** | A regular evening, e.g. after a club meeting | W1YU V1 147.555, to see who can reach whom across campus |
| **CW practice session**, slow (5–10 WPM) | A weekly evening, e.g. Thursday 9 pm | Start on 144.025 (BKG), move to W1YU CW V1 (144.070) |
| **Satellite pass party** | Whenever a high ISS or SO-50 pass happens in the evening | Cross Campus or another open sky. See [§5](#5-satellites). |
| **Fox hunt** (hidden-transmitter hunt) | Once a semester | 146.565 is the traditional fox-hunting frequency. Coordinate first. |

---

## 2. National and statewide simplex

| Ch | Name | Frequency | Use |
|---|---|---|---|
| 7 | CALL 2M | **146.520** | National 2 m FM simplex calling frequency. Make contact, then move to another frequency. |
| 8 | CALL 70CM | **446.000** | National 70 cm FM simplex calling frequency |
| 9 | CT ARES | **146.535** | CT ARES statewide simplex. Monitor during emergencies. |

---

## 3. Repeaters

Use **Tone** mode (send the tone; don't require it on receive) so you hear everything on the output. All of these are analog FM unless noted.

### 2 meters

| Ch | Name | Output | Offset | Tone | Call / Club | Location | Nets | |
|---|---|---|---|---|---|---|---|---|
| 10 | W1SPC 147 | **147.505** | **−1.0 MHz** (TX 146.505) | 77.0 | W1SPC / [Shore Point ARC](https://sparc.us) | Woodbridge | Region 2 ARES Mon 7:45 pm; SPARC Wed 8 pm; ARES sub-net Sun 8 pm | ✅ Non-standard split, already set in the CSV. EchoLink/IRLP connected. |
| 11 | W1GB WH | **146.610** | −0.6 | 110.9 | W1GB / [SCARA](https://www.scara.us) | West Haven | — | ✅ Mixed FM/P25. Wide coverage. |
| 12 | AA1VE EH | **147.255** | +0.6 | 110.9 | AA1VE / SCARA | East Haven | — | ✅ |
| 13 | W1NRG WAL | **147.360** | +0.6 | 162.2 | W1NRG / [Meriden ARC](https://w1nrg.com) | Wallingford | Tue 7 pm; Wed 7 pm; Sat 9 am | ✅ Mixed FM/Fusion. Emergency power. |
| 14 | KB1CBD MIL | **146.925** | −0.6 | 67.0 | KB1CBD / Milford ARRA | Milford | Mon 8 pm | ✅ Mixed FM/Fusion |
| 15 | KA1FAI MIL | **147.225** | +0.6 | 77.0 | KA1FAI / Coastline ARA | Milford | — | ✅ |
| 16 | W1VAR SHL | **146.985** | −0.6 | 141.3 | W1VAR / [Valley ARA](http://www.ctvara.org/) | Shelton | Tue 8 pm (verify) | ⚠️ Listed by CSMA, missing from the RepeaterBook search |

### 70 centimeters

| Ch | Name | Output | Offset | Tone | Call / Club | Location | Nets | |
|---|---|---|---|---|---|---|---|---|
| 20 | W1WPD 442 | **442.500** | +5 | **DCS 073** | W1WPD / Shore Point ARC | Woodbridge | **New Haven/Middlesex SKYWARN weather net Thu 7 pm**; SPARC Wed 8 pm | ⚠️ Sources disagree on the tone: most say DCS 073, CSMA also lists PL 77.0. If DCS doesn't open it, try PL 77.0. Linked to the New England network and EchoLink. |
| 21 | N1GTL HAM | **444.450** | +5 | 100.0 | N1GTL | Hamden | — | ✅ Emergency power |
| 22 | KB1AEV MER | **444.200** | +5 | 151.4 | KB1AEV | Meriden | — | ✅ Part of a linked system (EchoLink/IRLP) |

### Not in the CSV (unverified; check before using)

| Output | Offset | Tone | Call | Location | Issue |
|---|---|---|---|---|---|
| 145.290 | −0.6 | 110.9 | W1BCG (Shoreline ARC) | Killingworth | RepeaterBook shows off-air; the club still lists it |
| 146.835 | −0.6 | 100.0 | W1LAS (Waterbury ARC) | Prospect | Listing not updated since 2018 |
| 147.180 | +0.6 | 141.3 | W1HDN | Waterbury | Reported off-air in 2025 |
| 446.600 | −5 | 136.5 | KA1FAI | Milford | Only one source |
| 443.550 | +5 | 77.0 | N1LUF | Milford | Sources disagree on whether it's on the air |
| 444.825 / 449.825 | ±5 | 110.9 | SCARA | East Haven | Conflicting analog vs. digital listings |

> Several other local repeaters are **digital only** (DMR, D-STAR, Fusion) and won't work with this radio. They're left out on purpose.

---

## 4. Weather

**Receive only.** Make sure **F Lock** is set to **FCC HAM** ([Programming §10.3](docs/10-programming.md#103-load-the-w1yu-channel-list)) so the radio can't transmit on these.

| Ch | Name | Frequency | Station | Notes |
|---|---|---|---|---|
| 60 | WX WXJ42 | **162.400** | WXJ42, Meriden (West Peak) | Main NOAA Weather Radio station for New Haven County. Back in service July 2026 after a long outage. |
| 61 | WX 162.475 | 162.475 | WXM80 Riverhead NY / WXJ41 Hartford | Backups |
| 62 | WX KHB47 | 162.550 | KHB47, New London | Mainly southeastern CT |

**SKYWARN** (storm spotter) nets for New Haven County run on the **442.500** W1WPD repeater (Thursday 7 pm weekly net, plus activations during severe weather). Free spotter training: [NWS Upton/New York](https://www.weather.gov/okx/skywarn).

---

## 5. Satellites

Check **[AMSAT status](https://www.amsat.org/status/)** before a pass. Satellites fail, get turned off, or change schedules. Frequencies are from the [AMSAT FM satellite list](https://www.amsat.org/live-fm-satellites/) and [ARISS](https://www.ariss.org/contact-the-iss.html), as of October 2026.

### FM satellites (talk through them with a handheld)

| Satellite | Uplink (you TX) | Tone | Downlink (you RX) | Notes |
|---|---|---|---|---|
| **SO-50** | 145.850 | 67.0 | 436.795 ±10 kHz Doppler | The classic beginner satellite. **Must be armed:** transmit 2 seconds with a **74.4 Hz** tone (channel `SO50 ARM`) to start its 10-minute timer, then use 67.0. |
| **ISS** cross-band repeater | 145.990 | 67.0 | 437.800 ±10 kHz | Only on some of the time. Check [ARISS status](https://www.ariss.org). |
| **AO-123** (ASRTU-1) | 145.850 | 67.0 | 435.400 ±10 kHz | |
| **AO-91** (Fox-1B) | 435.250 ±10 kHz | 67.0 | 145.960 | Daylight passes only (weak battery). Doppler is on the **uplink**, so the channels change TX, not RX. |
| PO-101 | 437.500 | 141.3 | 145.900 | Reportedly failing; scheduled operation only. Not in the CSV. |
| IO-86 | 145.880 | 88.5 | 435.880 | Equatorial orbit, **not visible from Connecticut**. |

### Doppler channels in the CSV

On a pass the satellite's downlink frequency moves by about ±10 kHz on 70 cm. Step through these channels as it goes by:

| When | SO-50 RX | ISS RX | AO-123 RX | Channel suffix |
|---|---|---|---|---|
| Rising (AOS) | 436.805 | 437.810 | 435.410 | `+10` |
| | 436.800 | 437.805 | — | `+5` |
| Overhead | 436.795 | 437.800 | 435.400 | `0` |
| | 436.790 | 437.795 | — | `-5` |
| Setting (LOS) | 436.785 | 437.790 | 435.390 | `-10` |

Channels 40–58 in the CSV. Each one already has the correct uplink set as a cross-band offset, so just pick the channel and talk.

### ISS: listen-only frequencies (use VFO mode; **do not transmit**)

| Frequency | What |
|---|---|
| **145.800** | ISS voice downlink. Astronauts talking to schools during scheduled ARISS contacts. SSTV picture events have also used this frequency. |
| 437.550 | SSTV (slow-scan TV images) downlink, per ARISS. Check the announcement for each SSTV event. |
| 145.825 | APRS packet digipeater (sounds like buzzing data bursts) |
| 144.490 | ISS voice uplink. **Reserved for scheduled contacts. Don't transmit.** |

Decode ISS SSTV pictures by holding a phone running **Robot36** (Android) or **SSTV Slow Scan TV** (iOS) next to the radio's speaker.

### When and where

- **Pass predictions:** [Heavens-Above](https://www.heavens-above.com), [AMSAT pass predictor](https://www.amsat.org/track/), [N2YO](https://www.n2yo.com). New Haven is about **41.31° N, 72.92° W**, grid square **FN31**.
- **Etiquette:** listen first, keep transmissions short (call sign + grid), one contact per pass per station, and **don't transmit if you can't hear the satellite**.

---

## 6. Fun things to listen to (scanner channels)

The radio receives far outside the ham bands, so it doubles as a scanner. These are channels 70–96 in the CSV.

> ⚠️ **Receive only.** Never transmit on these. It's illegal and could interfere with real aircraft, ships and trains. With **F Lock set to FCC HAM** ([Programming §10.3](docs/10-programming.md#103-load-the-w1yu-channel-list)) the radio refuses to transmit here. **Listening is legal, but don't record, repost or share what you hear** from these services (federal law, 47 U.S.C. § 605).

**Tip:** to scan a group, use the radio's scan list feature (see the F4HWN docs) or just step through with the arrows. Activity comes in bursts, so be patient.

### Aircraft: Tweed-New Haven Airport (HVN)

Airband uses **AM**, and these channels are already set to AM. Tweed is right next to campus, so the tower is easy to hear, especially the airliners and the pilots reading back their clearances.

| Ch | Name | Frequency | What you'll hear |
|---|---|---|---|
| 70 | HVN TWR | **124.800** | **New Haven Tower**: takeoff and landing clearances (tower open 6 am–10 pm; outside those hours it's the pilot-to-pilot frequency) |
| 71 | HVN GND | 121.700 | Ground control (taxi instructions) and clearance delivery |
| 72 | HVN ATIS | 133.650 | Recorded airport weather and runway info, on a loop. Good test that airband works. |
| 73 | NY APP | 124.075 | New York Approach/Departure, handling arrivals and departures around HVN |
| 74 | AIR GUARD | 121.500 | Aviation emergency frequency. Usually silent. |

Learn the lingo: "Tweed tower, Breeze 123, 5 miles south, inbound for landing, with information Bravo." Live comparison: [LiveATC](https://www.liveatc.net). Source: [AirNav KHVN](https://www.airnav.com/airport/KHVN).

### Marine: New Haven Harbor and Long Island Sound

Marine VHF uses **FM**. Reception is best near the water (East Rock, Lighthouse Point, Long Wharf). Coast Guard Sector Long Island Sound is headquartered in New Haven.

| Ch | Name | Frequency | Marine Ch | What you'll hear |
|---|---|---|---|---|
| 80 | MAR CH16 | **156.800** | 16 | Distress, safety and calling. The Coast Guard monitors it 24/7. |
| 81 | MAR CH13 | 156.650 | 13 | Bridge-to-bridge: big ships and tugs coordinating passing |
| 82 | MAR CH22A | 157.100 | 22A | Coast Guard broadcasts (hazards, safety notices) |
| 83 | MAR CH09 | 156.450 | 9 | Recreational boater calling (busy on summer weekends) |
| 84 | MAR CH19A | 156.950 | 19A | Where New Haven harbor tugs and launches do their work |

Sources: [USCG VHF channels](https://navcen.uscg.gov/us-vhf-channel-information), [NOAA Coast Pilot 2, Ch. 8](https://nauticalcharts.noaa.gov/publications/coast-pilot/files/cp2/CPB2_C08_WEB.pdf).

### Trains: Union Station and the Northeast Corridor

Railroad radio is **narrow FM (NFM)**. New Haven is a big rail hub: Metro-North, Amtrak, Shore Line East and CTrail meet at Union Station, and CSX's Cedar Hill Yard is just north of town. You'll hear dispatchers giving signals and permissions, plus crews calling out signals ("Clear, 72"). Listen near Union Station or along the tracks.

| Ch | Name | Frequency | What you'll hear |
|---|---|---|---|
| 90 | MNR EAST | **160.335** | Metro-North dispatcher, east end (New Haven, Waterbury branch) |
| 91 | MNR WEST | **160.545** | Metro-North dispatcher, west end. Amtrak uses it on the New Haven Line too. |
| 92 | MNR TALK | 160.770 | Metro-North train-to-train talkaround |
| 93 | MNR YARDS | 161.040 | Metro-North yards (New Haven yard moves) |
| 94 | AMTK 54 | **160.920** | Amtrak road channel east of New Haven (to Boston, and to Springfield/Hartford Line) |
| 95 | AMTK NHYD | 160.455 | Amtrak New Haven yard |
| 96 | CSX CEDAR | 161.070 | CSX freight, Cedar Hill Yard |

⚠️ Railroads change channels without notice, and these come from hobbyist lists. Some have been moving to digital radio, which this radio can't decode. Source: [RadioReference: Connecticut railroads](https://www.radioreference.com/db/aid/1533).

### Also worth trying (not in the CSV)

| What | Frequency | Notes |
|---|---|---|
| ISS voice, SSTV and APRS | 145.800 / 437.550 / 145.825 | See [§5](#5-satellites) |
| APRS | 144.390 | Ham radio position reports (data bursts). Watch it live at [aprs.fi](https://aprs.fi). |
| FRS/GMRS walkie-talkies | 462.5625–462.725 | Families, hikers, events. Listening only. |
| FM broadcast | 88–108 MHz | Supported by the NR7Y firmware's broadcast FM receiver (v1.4+) |

**Police, fire and EMS:** most Connecticut public safety agencies use digital trunked radio (P25), which this radio **can't** decode. Use [Broadcastify](https://www.broadcastify.com) instead.

---

## 7. Band plans (quick reference)

### 2 meters (144–148 MHz), [ARRL band plan](https://www.arrl.org/band-plan)

| Frequency (MHz) | Use |
|---|---|
| 144.000–144.050 | EME (moonbounce), CW. **BKG calls on 144.025.** |
| 144.050–144.100 | **General CW and weak signals** (W1YU CW V1, CW V2) |
| 144.100–144.275 | SSB/CW weak signal. 144.200 = SSB calling. |
| 144.275–144.300 | Beacons |
| 144.300–144.500 | New OSCAR subband, simplex. 144.390 = APRS. 144.490 = ISS uplink. |
| 144.600–144.900 | Repeater inputs |
| 144.900–145.100 | Weak signal and FM simplex, packet |
| 145.100–145.500 | Repeater outputs |
| 145.500–145.800 | Misc. and experimental modes |
| **145.800–146.000** | **Satellites only. Never use for terrestrial contacts.** |
| 146.010–146.370 | Repeater inputs |
| **146.400–146.580** | **FM simplex.** 146.520 = national calling. |
| 146.610–147.390 | Repeater outputs (and 147.6–148.0 inputs) |
| **147.420–147.570** | **FM simplex** (W1YU V1, V2) |

### 70 centimeters (420–450 MHz), highlights

| Frequency (MHz) | Use |
|---|---|
| 420–432 | ATV, control links (avoid) |
| 432.000–432.070 | EME |
| **432.070–432.100** | **Weak-signal CW** (W1YU CW U1) |
| 432.100 | 70 cm SSB/CW calling |
| **435–438** | **Satellites only** |
| 442–445 | Repeater outputs |
| **446.000** | **National FM simplex calling** |
| 447–450 | Repeater inputs |

---

## Sources

- [RepeaterBook: New Haven County](https://www.repeaterbook.com/repeaters/location_search.php?state_id=09&loc=New+Haven&type=county)
- [CT Spectrum Management Association coordination search](https://efile.ctspectrum.com/search.html)
- [SCARA](https://www.scara.us/) · [Shore Point ARC nets](https://sparc.us/nets) · [Meriden ARC activities](https://w1nrg.com/activities/) · [Valley ARA](http://www.ctvara.org/) · [Shoreline ARC](https://shorelinearc.org/repeaters)
- [W1YU: On the Air](https://w1yu.sites.yale.edu/air)
- [CT ARES nets](https://ctares.org/nets/) · [CT ARES SKYWARN](https://ctares.org/Skywarn_Radio.php)
- [NWS Upton: Meriden transmitter](https://www.weather.gov/okx/meridentransmitterwebpage)
- [ARRL band plan](https://www.arrl.org/band-plan) · [Brass Knuckle Gang for clubs](https://bkg.club/clubs.html)
- [AMSAT FM satellites](https://www.amsat.org/live-fm-satellites/) · [ARISS frequencies](https://www.ariss.org/contact-the-iss.html)
