<img width="1892" height="1053" alt="palaOne" src="https://github.com/user-attachments/assets/0fdef5ba-eabd-4b71-9a0c-4c1dc78a4bee" />

# pala-one-firmware
Pala One — A tiny E-Ink reader project by Paul Lagier

The goal of the project was to create a simple, distraction-free reading device that feels minimal, portable and easy to build while still looking and behaving more like a real product than a typical DIY electronics project.

## Contributing

If you improve the firmware, add features or fix bugs, feel free to open a pull request.
Please clearly mention:
- which board version(s) you tested on (V1.1, V1.2, or both)
- what was changed
- how it was tested

## Board Versions

There are currently two supported Heltec Wireless Paper versions:
- `Heltec V1.1`
- `Heltec V1.2`

The board version is usually printed on the back of the PCB.

Both versions are built from the same source file (`Pala_One_2_1/Pala_One_2_1.ino`). Open it in Arduino IDE and uncomment the `#define` at the top that matches your hardware before compiling.


#### Display

| Function | Description |
|---|---|
| `clearScreen()` | Clear the display buffer and prepare a new frame |
| `drawHeader(title)` | Draw the standard section header bar |
| `drawTextAt(x, y, text, bold)` | Draw text at a pixel position |
| `drawCenteredLarge(text)` | Draw text centred on screen in a large font |
| `refreshDisplay()` | Push the frame buffer to the e-ink panel |

#### Input

| Function | Description |
|---|---|
| `waitForEvent()` | Block until a button gesture; returns `PALA_CLICK` / `PALA_DOUBLE` / `PALA_TRIPLE` / `PALA_LONG` |
| `pollEvent()` | Non-blocking variant; returns 0 if no event is ready |
| `buttonPressed()` | Returns 1 if the button is currently held, 0 otherwise |
| `pendingPresses()` | Count of individual short press-release events since last call; bypasses multi-click grouping |


#### Storage

| Function | Description |
|---|---|
| `storageRead(key, buf, maxlen)` | Read from `/apps/{key}.dat`; returns bytes read, -1 on error |
| `storageWrite(key, buf, len)` | Write to `/apps/{key}.dat`; returns bytes written, -1 on error |


## Features

- TXT book support
- Adjustable font size
- Adjustable line spacing
- Deep sleep mode
- Reading progress saving
- USB-C charging
- Lightweight portable design
- Open-source firmware

## Hardware

Pala One is based on:
- Heltec Wireless Paper
- 3D printed housing
- LiPo battery

## Downloads

This repository contains the firmware source code for the project.

Additional files such as:
- STL files
- STEP files
- assembly guides
- printable files
- project downloads

are available separately via Ko-fi:

https://ko-fi.com/s/e14ed892ea

## Community & Modifications

Community improvements, forks and firmware modifications are welcome.  
If you build your own version or improve the project, feel free to share it with the community.

## License & Copyright

The firmware in this repository is provided for personal and educational use.

Please do not:
- reupload paid project files
- redistribute complete download packages
- resell the project files
- commercially redistribute modified versions of paid assets

The design, branding, documentation and paid project assets remain copyright © Paul Lagier.

---

Created by Paul Lagier
