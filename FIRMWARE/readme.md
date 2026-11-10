# Meridian 87

An 85-key TKL with a Tsangan-style bottom row (1.5u / 1u / 1.5u / 7u / 1.5u / 1u / 1.5u) and an EC11 rotary encoder in the Pause position, built on a Raspberry Pi Pico (RP2040).

* Keyboard Maintainer: [Ayaskant Sahoo](https://github.com/ayaskant007)
* Hardware Supported: Meridian 87 PCB (2-layer, 388.12 × 138.90 mm), Raspberry Pi Pico, EC11 encoder with push switch
* Hardware Availability: Custom PCB, see the project repository

Matrix: 6 rows × 17 columns, COL2ROW (1N4148 cathode toward the row).
Columns `GP0–GP16`, rows `GP17–GP22`, encoder A/B on `GP27`/`GP26`, encoder push in the matrix at row 0 / column 16.

Make example for this keyboard (after setting up your build environment):

    qmk compile -kb meridian87 -km default
    qmk compile -kb meridian87 -km via

Flashing example for this keyboard:

    qmk flash -kb meridian87 -km via

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Bootloader

Enter the bootloader in 3 ways:

* **Bootmagic reset**: Hold down Esc (top-left key) and plug in the keyboard
* **Physical reset button**: Hold the BOOTSEL button on the Pico while plugging in the USB cable
* **Keycode in layout**: Press `Fn` + `Esc` (`QK_BOOT`)

The Pico then appears as a USB drive called `RPI-RP2`; drag the `.uf2` file onto it.
