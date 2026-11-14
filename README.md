# Freaq: FM synth for Eurorack

Freaq is an FM synth with a generative sequencer. It uses an Arduino Nano. The synth design and the code are by [Meebleeps](https://github.com/Meebleeps/MeeBleeps-Freaq-FM-Synth). I designed a PCB and a front panel, so that it fits in a Eurorack case. You can also use it as a standalone synth.

![Freaq](https://github.com/user-attachments/assets/d43b7279-5da6-433b-8786-0992f0a1a54e)

## Build guide and video

- Step-by-step build guide on Instructables: [Freaq FM Synth](https://www.instructables.com/Freaq-FM-Synth/)
- Video on YouTube: [Freaq](https://www.youtube.com/watch?v=fAgmykZD0DI)

## Features

- Two independent FM voices, each with 2 operators
- A generative sequencer with 2 tracks. The tracks can play in unison, or with different step counts (polymetric). For example, one voice can play bass and the other voice can play lead.
- Many waveforms, an attack and decay envelope, and an LFO for each voice
- Power: 12 V from a Eurorack power connector, or 9 V through a JST connector

## What you need

### Hardware

- All parts are in the [parts list](Parts%20List.pdf).
- The schematic is [Schematic.png](Schematic.png).
- The Gerber files for the PCB and the front panel are in [Gerber Files](Gerber%20Files/). You can send them to a PCB maker.

### Software

- Arduino IDE
- The **Mozzi** library. The version that you need depends on the sketch. See the next section.

## Select the sketch

There are two sketches in `Freaq_IDE_Code/`. They make the same sounds.

| Sketch | Mozzi version | Use it when |
|--------|---------------|-------------|
| `Freaq_Updated_Mozzi` | Mozzi 2 (the current version) | **Recommended.** Use this sketch. |
| `Freaq_Original_Code` | Mozzi 1.1.2 (old version) | Only if you already use Mozzi 1.1.2 |

## Upload the firmware

1. Download this repository. Click **Code → Download ZIP**, then extract the ZIP file.
2. In the Arduino IDE, open the **Library Manager**.
3. Search for **Mozzi** and install the newest version.
4. Open `Freaq_IDE_Code/Freaq_Updated_Mozzi/Freaq_Updated_Mozzi.ino`.
5. Connect the Arduino Nano to your computer with a USB cable.
6. In the **Tools** menu, set these values:
   - **Board:** Arduino Nano
   - **Processor:** ATmega328P
   - **Port:** the COM port of your Nano
7. Click **Upload**.
8. Wait for the message **Done uploading**.

> **Note:** If the upload fails, set **Processor** to **ATmega328P (Old Bootloader)**, then try again. Many clone Nano boards need this setting.

> **Note:** To use `Freaq_Original_Code`, install Mozzi version **1.1.2** in step 3. In the Library Manager, select **1.1.2** in the version list, then click **Install**.

## Start-up tip

When Freaq starts, the mutation and density settings are very low. You may hear only a few notes. To start the sequencer:

1. Turn the **mutation** knob fully to the left, then fully to the right.
2. Hold the **FUNC** button.
3. While you hold **FUNC**, turn the **mutation** knob fully to the left, then fully to the right.

## How to play

The buttons and knobs are described in the [Meebleeps Freaq README](https://github.com/Meebleeps/MeeBleeps-Freaq-FM-Synth#user-guide).

## Files in this repository

| Folder or file | Contents |
|----------------|----------|
| `Freaq_IDE_Code/` | Firmware: the updated sketch and the original sketch |
| `Eagle Files/` | Eagle files for the PCB |
| `KiCad - Front Panel/` | KiCad files for the front panel |
| `Front Panel - Inkscape.svg`, `Front Panel.png` | Front panel artwork |
| `Gerber Files/` | Gerber files for the PCB and the front panel, ready to order |
| `Parts List.pdf` | Parts list |
| `Schematic.png` | Schematic |

## Why I made it

I want to make my own modular synth that is simple to build. Each module has these aims:

- It operates from 9 V (and 12 V).
- It is easy to build, with a minimum of components.
- It uses an Arduino, to keep the parts count low and everything in tune.
- It fits in any Eurorack case, and it can use normal Eurorack power.
- It sounds good.

As a standalone synth, Freaq is as good as most small synths that you can buy.

![Freaq module](https://github.com/user-attachments/assets/2b71c2c9-46d3-4fc6-9805-e5f03454d055)

## Credits

- Synth design and code: [Meebleeps Freaq FM Synth](https://github.com/Meebleeps/MeeBleeps-Freaq-FM-Synth). Thank you, Meebleeps.
- Audio library: [Mozzi](https://sensorium.github.io/Mozzi/).
- PCB, front panel, Eurorack version and the Mozzi 2 update: Marcus ([lonesoulsurfer](https://github.com/lonesoulsurfer)).

## Support

Do you like this project? You can support my work on [GitHub Sponsors](https://github.com/sponsors/lonesoulsurfer).

## Licence

This project uses the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](LICENSE) (CC BY-NC-SA 4.0), the same licence as the Meebleeps original.

- You can build, share and change this project.
- You must name Meebleeps and lonesoulsurfer.
- You must not use it for commercial purposes. For example, do not sell kits or built synths.
- If you share a changed version, you must use the same licence.
