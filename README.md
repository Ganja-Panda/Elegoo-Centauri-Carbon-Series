# 🐼 PandaWorks — Elegoo Centauri Carbon & Centauri Carbon 2 Combo Profiles

**Printer, filament, and process presets for the Elegoo Centauri Carbon (ECC) and Centauri Carbon 2 Combo (ECC2C).**

These are my personal, machine-specific tuning profiles, built through repeated calibration, test prints, and close inspection—not generic settings copied from a manufacturer chart. The repository is a growing reference and backup for my Elegoo printer configurations.

> **Start here:** Choose the folder for **your printer**. ECC and ECC2C settings are separate; **do not treat their filament, process, or printer profiles as interchangeable**.

## 📦 Choose your printer

| Printer | Package | Current contents | Nozzle |
|---|---|---|---|
| **Centauri Carbon (ECC)** | [Open ECC profiles](./Elegoo%20Centauri%20Carbon/) | 1 printer preset · 9 filament presets · 3 process presets | 0.4 mm |
| **Centauri Carbon 2 Combo (ECC2C)** | [Open ECC2C profiles](./Elegoo%20Centauri%20Carbon%202%20Combo/) | 1 printer preset · 9 filament presets · 4 process presets | 0.4 mm |

**These counts describe the files currently in the repository, not every material I own or intend to calibrate.** More profiles will be added as testing is completed.

### 🖨️ Elegoo Centauri Carbon (ECC)

- [Printer preset](./Elegoo%20Centauri%20Carbon/Printer%20Profile/.4mm%20Hotend/)
- [Filament presets](./Elegoo%20Centauri%20Carbon/Filament%20Profiles/.4mm%20Hotend/PLA/)
- [Process presets](./Elegoo%20Centauri%20Carbon/Process%20Profiles/.4mm%20Hotend/)

**Process layer heights:** 0.12 mm Fine, 0.16 mm Optimal, and 0.20 mm Standard.

**Included filament profiles:** Black, Bronze Filled, Dark Blue, Grey, Marble Filled, Red, Space Grey, White, and Wood Filled.

### 🎨 Elegoo Centauri Carbon 2 Combo (ECC2C)

- [Printer preset](./Elegoo%20Centauri%20Carbon%202%20Combo/Printer%20presets/)
- [Filament presets](./Elegoo%20Centauri%20Carbon%202%20Combo/Filament%20presets/)
- [Process presets](./Elegoo%20Centauri%20Carbon%202%20Combo/Process%20presets/)

**Process layer heights:** 0.08 mm Fine, 0.12 mm Fine, 0.16 mm Optimal, and 0.20 mm Standard.

**Included filament profiles:** Black, Bronze Filled, Dark Blue, Grey, Marble Filled, Red, Space Grey, White, and Wood Filled.

> **ECC2C package note:** Some currently published printer/process filenames include `- Copy`. These are the names of the uploaded JSON files. Check the preset names and inherited base presets inside your slicer after import.

---

## ⚠️ Compatibility and scope

- Profiles are tuned for **Elegoo-branded filament** on the **specific printer** identified by their folder and preset names.
- The currently published presets target **0.4 mm nozzles**. Additional nozzle sizes are not presented here as tested packages.
- Different pigment loads, fillers, melt behavior, cooling characteristics, and printer hardware can change the ideal settings, even for filaments sold under the same material family.
- **Do not assume** a profile tuned on my printer is perfect on yours. Start with a small test print and verify extrusion, first layers, temperatures, and cooling.
- Some JSON presets **inherit** settings from an existing Elegoo/OrcaSlicer base profile. If an import reports a missing parent preset, install/select the matching printer and baseline presets first; don't assume each file is completely standalone.

## 🔬 What I tune and inspect

My calibration process considers:

- Temperature response and material-specific extrusion behavior
- Maximum volumetric flow
- Flow ratio and extrusion consistency
- Pressure advance across different motion conditions
- Retraction and stringing
- Cooling, bridges, overhangs, and surface quality
- Layer consistency and fine surface artifacts under magnification

I use physical calibration prints, high-magnification inspection, and AI-assisted analysis as tools to identify defects and compare results. **The printed results—not an AI prediction—are the basis for accepting a profile.**

Filament tuning is ongoing. These files are practical configurations from my own equipment, not universal material specifications or guarantees of identical results across machines.

---

## 📥 Download

**A single preset:** Open the printer folder above, select the JSON file, then use GitHub's **Download raw file** action.

**Everything:** From the [repository home page](https://github.com/Ganja-Panda/Elegoo-CC1), select **Code → Download ZIP**, then extract the archive and choose your printer's folder.

You do not need Git installed to download the files.

## 🧩 Import into your slicer

1. Open your compatible Elegoo Slicer or OrcaSlicer installation.
2. Select **File → Import → Import Configs** (wording may vary by slicer version).
3. Select the appropriate JSON preset files for **your printer**. If your slicer supports importing a config ZIP directly, you can use that route as well.
4. Check that the printer, filament, and process presets appeared correctly, and resolve any inherited-base-profile warnings.
5. Confirm the **printer model, nozzle diameter, filament selection, and process settings** before starting a test print.

**Importing is not the same as validating.** Check all settings that affect safe machine operation—especially temperatures, speeds, G-code, and machine selection—before printing. A slicer update may also change import behavior or preset compatibility.

---

## 🚧 Work in progress

This is a living repository. Additional Elegoo filament colors, specialized blends, refinements, and other nozzle sizes may appear after I finish calibrating and verifying them. A folder or planned item is **not** a promise that its settings have already been tested.

For updates, inspect the repository's file history and newly added presets.

## 🛠 Why this repository exists

I use this space to back up my tuned settings, keep ECC and ECC2C configurations organized, and share useful starting points with other Elegoo owners who would rather spend less time fighting calibration and more time printing weird shit.

## 📜 License

Distributed under the [MIT License](./LICENSE). Copyright © 2025 Ganja Panda, as stated in the repository license.

Use it, modify it, sacrifice it to the filament gods. Just verify your setup before firing up the machine.

*If this repository helps, a GitHub star is appreciated.* 🐼
