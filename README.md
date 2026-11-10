# nintendo ds emulator

A lightweight browser-based Nintendo DS emulator built with HTML, JavaScript, and EmulatorJS. The project loads a local `.nds` or `.zip` ROM and runs it in the browser using the NDS core from the EmulatorJS CDN.

## overview

This repository is a minimal front-end emulator wrapper. The main entry point is `index.html`, which:

- accepts a ROM file from the user's machine
- creates an object URL for the selected game
- configures EmulatorJS runtime globals
- injects the EmulatorJS loader script
- renders the ROM inside the page.

  ## how to use
  just go to https://dsemu-silk.vercel.app/

## info

- `index.html` contains the UI, ROM upload logic, and emulator bootstrapping
- `EJS_player` is set to the target DOM element
- `EJS_core` is set to `nds`
- `EJS_gameUrl` points to the selected ROM file
- `EJS_pathtodata` points to the EmulatorJS runtime data bundle on the CDN
- `loader.js` is dynamically loaded from `https://cdn.emulatorjs.org/stable/data/loader.js`

## usage

1. Open `index.html` in a modern browser.
2. Select a Nintendo DS ROM (`.nds` or `.zip`).
3. Wait for the emulator to initialize.
4. Use the on-screen controls to play.

## requirements

- modern browser like edge or chrome  with JavaScript enabled
- internet access for EmulatorJS CDN assets
- local ROM file for gameplay

## limitations

- this is not a full standalone emulator build; it depends on the EmulatorJS runtime
- performance and compatibility vary by browser and hardware
- game loading requires a valid ROM and legal ownership/usage rights

## project structure

```text
.
├── index.html
├── README.md
├── LICENSE
```

## legal note

This project does not include copyrighted game files or BIOS images. Users are responsible for ensuring they only load ROMs they own or are legally permitted to use.
