# 🐼 PandaWorks — Elegoo Printer Profiles & HueForge Filament Data

**Independent tuning presets for the Elegoo Centauri Carbon (ECC) and Centauri Carbon 2 Combo (ECC2C), plus ready-to-use Elegoo PLA color and transmission-distance data for HueForge.**

These are configurations and measurements from my own equipment. I calibrate, test, inspect, and revise them—not just copy numbers out of the slicer's default profiles. The repo is both my working backup and a resource for other makers.

> **Pick the right files:** ECC and ECC2C printer/filament/process presets are machine-specific. HueForge filament data is a separate resource; you do **not** need either printer or a TD-1S to use the supplied filament entries in HueForge.

## 📦 What's here

| Collection | Contents currently published | Go to files |
|---|---|---|
| **Centauri Carbon (ECC)** | 1 printer, 9 filament, 3 process presets | [ECC profiles](./Elegoo%20Centauri%20Carbon/) |
| **Centauri Carbon 2 Combo (ECC2C)** | 1 printer, 9 filament, 4 process presets | [ECC2C profiles](./Elegoo%20Centauri%20Carbon%202%20Combo/) |
| **HueForge — Elegoo PLA** | 15 filament color / transmission-distance entries | [HueForge data](./HueForge/) |

Counts reflect the files currently published—not every filament I own or intend to calibrate. **All published printer/process presets are for 0.4 mm nozzles.**

---

## 🖨️ Centauri Carbon (ECC)

- [Printer preset](./Elegoo%20Centauri%20Carbon/Printer%20Profile/.4mm%20Hotend/)
- [Filament presets](./Elegoo%20Centauri%20Carbon/Filament%20Profiles/.4mm%20Hotend/PLA/)
- [Process presets](./Elegoo%20Centauri%20Carbon/Process%20Profiles/.4mm%20Hotend/)

**Processes:** 0.12 mm Fine · 0.16 mm Optimal · 0.20 mm Standard.

**Available filament presets:** Black, Bronze Filled, Dark Blue, Grey, Marble Filled, Red, Space Grey, White, and Wood Filled.

## 🖨️ Centauri Carbon 2 Combo (ECC2C)

- [Printer preset](./Elegoo%20Centauri%20Carbon%202%20Combo/Printer%20presets/)
- [Filament presets](./Elegoo%20Centauri%20Carbon%202%20Combo/Filament%20presets/)
- [Process presets](./Elegoo%20Centauri%20Carbon%202%20Combo/Process%20presets/)

**Processes:** 0.08 mm Fine · 0.12 mm Fine · 0.16 mm Optimal · 0.20 mm Standard.

**Available filament presets:** Black, Bronze Filled, Dark Blue, Grey, Marble Filled, Red, Space Grey, White, and Wood Filled.

**About filenames ending in `- Copy`:** These are deliberately named copies of Elegoo's default printer/process presets that I have modified. They're not accidental duplicates or unfinished filenames. They retain the familiar base naming because they are edited copies of those profiles.

### Compatibility and calibration notes

- The filament presets are made for **Elegoo-branded filament**, on the named printer. Do not assume another brand—or the other Centauri Carbon model—will behave identically.
- Pigments, fillers, batches, cooling, and printer hardware can all affect results. Verify critical settings and run a small test print before relying on someone else's configuration.
- Some JSON presets **inherit** settings from an existing Elegoo slicer profile. Keep the appropriate stock printer and base presets available when importing them.
- Filament presets contain individually calibrated values. There is no single universal flow ratio, pressure advance value, or maximum volumetric speed for everything in this repository.

---

## 🎨 HueForge — Elegoo PLA filament data

**[Download / view `Elegoo PLA TD-1s Results.json`](./HueForge/Elegoo%20PLA%20TD-1s%20Results.json)**

This is a **15-filament HueForge library** for anyone who wants to work with these Elegoo PLA colors without buying a BIQU TD-1S or spending hours measuring each spool.

### Where the numbers come from

- **Color / HEX:** Sourced from Elegoo's RFID filament-tag color data, rather than trusting the TD-1S to measure the filament's RGB color accurately.
- **Transmission distance (TD):** Measured from the physical filaments using my **BIQU TD-1S**.
- **Saved library:** I combined those values into HueForge filament profiles and shared the resulting JSON. I also corrected the colors in my own saved TD-1S profiles.

The HEX color and TD value are **different types of data from different sources**. The TD-1S provided the transmission-distance measurements, **not** the published HEX measurements.

### Currently included

| Elegoo PLA | HEX | TD |
|---|---|---:|
| Beige | `#FFEEC5` | 2.3 |
| Black | `#000000` | 0.1 |
| Brown | `#9B6A4D` | 2.4 |
| Dark Blue | `#2323F7` | 2.8 |
| Grey | `#747C7E` | 2.5 |
| Neon Green | `#29D464` | 4.6 |
| Orange | `#E97B47` | 5.7 |
| Pink | `#FBAFBC` | 5.3 |
| Purple | `#9E69E8` | 2.1 |
| Red | `#FF0000` | 4.7 |
| Sea Green | `#09C299` | 1.9 |
| Sky Blue | `#24A2CC` | 3.1 |
| Space Grey | `#979797` | 0.1 |
| White | `#FFFFFF` | 4.9 |
| Yellow | `#FFC800` | 6.0 |

*These are the values in the published JSON, not a claim that every future Elegoo production batch will have identical optical behavior. Specialty blends and other filament measurements will be added as they're ready.*

### Using the HueForge library

1. Download [`Elegoo PLA TD-1s Results.json`](./HueForge/Elegoo%20PLA%20TD-1s%20Results.json) using GitHub's raw-file download option.
2. Use HueForge's filament-library import feature to load the JSON, following the import workflow for your installed HueForge version.
3. Verify the imported filament names, HEX colors, and transmission-distance values before building a project.

This **HueForge JSON is not a slicer preset**. Import it into HueForge, not through your slicer's printer/process/filament preset importer.

---

## 🔬 How I develop and evaluate printer profiles

My process includes temperature tests, maximum volumetric flow testing, flow calibration, pressure advance at different speeds and accelerations, retraction, cooling, bridging, overhangs, and real-world print evaluation. I also inspect printed surfaces under magnification and use AI-assisted analysis to help find subtle patterns and artifacts.

**The actual printed results determine whether a setting is accepted.** This is independent experimentation on my specific equipment, not an official Elegoo certification or a promise that every printer will produce the same results.

---

## 📥 Downloading and importing printer presets

### Download

- **Individual file:** Open its folder on GitHub and choose **Download raw file**.
- **Whole repository:** Select **Code → Download ZIP** on the [repository home page](https://github.com/Ganja-Panda/Elegoo-CC1), then extract it.

### Import into Elegoo Slicer / OrcaSlicer

1. Open your compatible slicer and choose **File → Import → Import Configs** (menu wording may vary with version).
2. Select the relevant JSON presets for your **specific printer**. Some slicer versions also support importing configuration ZIPs.
3. Confirm any required inherited/base profiles are available.
4. Select the right printer, nozzle, filament, and process before printing.
5. Inspect temperatures, G-code, speeds, and other machine-specific settings and make a small verification print.

**Do not import the HueForge data through this slicer workflow.** It belongs in HueForge.

---

## 🚧 Ongoing work

More Elegoo filament colors, specialty blends, calibration refinements, and possibly other nozzle configurations may be published as I finish and verify them. An omitted color means there's no published profile for it yet—not that the filament is unsupported by the printer.

This repository exists to back up my work, share repeatable starting points, and let other people spend less time calibrating and more time **printing weird shit**.

## 📜 License

Distributed under the [MIT License](./LICENSE). Copyright © 2025 Ganja Panda as stated in the repository license.

Use it, modify it, sacrifice it to the filament gods. Just check your machine before firing it up.

*If the repository saves you some calibration time, a GitHub star is always appreciated.* 🐼
