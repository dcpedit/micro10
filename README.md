# µ10 Keyboard

![µ10_keyboard](https://user-images.githubusercontent.com/800930/168409768-f59eebf5-3d8f-4886-aac2-d2045f0f248f.JPG)

Here you will find all the source files I used to build my µ10 (aka Micro10) keyboard.  Below is a list of features:

* 10u wide QAZ-ish layout
* Supports a 10u spacebar
* Designed to be wireless (via nice!nano + ZMK)
* Optional daughterboard for OLED and rotary encoder
* PCB uses Kailh hot swap sockets
* PCB supports a 1.25u modifier on each end if a split spacebar (2.25u + 2.75u) setup or 6.25u spacebar is utilized.  This will require modifications to the case design (mainly to add blockers).

[Keyboard Layout Editor (KLE)](http://www.keyboard-layout-editor.com/#/gists/2a9c0bfd3bc5586766325f682a7adc31)

<img width="551" alt="Micro10_default_keymap" src="https://user-images.githubusercontent.com/800930/168410217-aa84e700-590b-47c6-ab6a-d3187b8ccb65.png">

# ZMK Firmware

See my fork of ZMK under the `dcpedit` branch:
https://github.com/dcpedit/zmk/tree/dcpedit

The relevant files are in the `micro10` folder under shields:
https://github.com/dcpedit/zmk/tree/dcpedit/app/boards/shields/micro10

```
git clone -b dcpedit https://github.com/dcpedit/zmk.git
```

## Build
Follow the [ZMK environment setup](https://zmk.dev/docs/development/setup).  I highly recommend using VS Code & Docker.
```
cd app
west build -b nice_nano_v2 -- -DSHIELD=micro10
```
Binary will be located here.  Copy it into your nice!nano:
```
app/build/zephyr/zmk.uf2
```


# Image Gallery
https://imgur.com/a/AuKd2NT
