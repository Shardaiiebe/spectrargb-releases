# SpectraRGB

One lighting effect across your RGB devices, and a live wallpaper behind your desktop icons that
shows the same effect, without the vendors' software. For Windows 11 (Windows 10 is untested).

## What it works with

- **Devices with Windows Dynamic Lighting** (many recent keyboards, mice and laptops; Windows lists
  them in Settings → Personalization → Dynamic Lighting): no extra setup.
- **ASUS ROG Strix laptops**: keyboard and lightbar.
- **Logitech G815** keyboard.
- **HP ZBook Fury 16 G9** laptops with the per-key RGB keyboard, plus other laptops with the same
  keyboard controller (likely other HP ZBooks) as an experiment.
- **Razer**: the Basilisk V3 mouse, plus about 90 other Razer mice and keyboards as an experiment
  (Devices offers it when one is connected; tell us how it went).
- **Desktops**, as an experiment (switched on in Devices; tell us how it went):
  - the lighting of **ASUS** (Aura USB), **Gigabyte** (RGB Fusion 2) and **MSI** (Mystic Light)
    motherboards: their own LEDs, and the fans and strips on their RGB headers (you say what's
    plugged in, in Devices);
  - the lighting of **NZXT Kraken** (X3, Z3, Elite RGB, X2) and **Corsair Hydro** (Platinum, Pro
    XT, Elite RGB) coolers and the **ASUS ROG Strix LC III**, with the fans plugged into them.
    Only their lighting: never their pump or fan speeds, which keep running as they were set.
  - Not yet: Corsair coolers on a Commander Core (Elite Capellix, Elite LCD: lighting them would
    stop their own fan and pump curves), MSI's newest X870 boards and older ones without per-LED
    lighting, fan hubs (Corsair, NZXT, Lian Li). A device report helps add them.
- Group devices that belong together (a PC case's insides) on the Layout page, and give them an
  effect of their own if you like.

Something not on the list? See [Help](#help): a device report helps add it.

## Install

1. Under [Releases](../../releases/latest), download `SpectraRGB_<version>_x64-setup.exe` and run it.
   It installs for you only (no admin rights needed).
2. Windows may warn that the app is from an unknown publisher (it isn't signed with a paid
   certificate): choose **More info**, then **Run anyway**.
3. **Quit other lighting software** first: Armoury Crate, G HUB, Razer Synapse, SignalRGB, OpenRGB,
   your motherboard's or cooler's lighting app (MSI Center, Gigabyte Control Center, NZXT CAM,
   iCUE) and the like. They fight over the lights; SpectraRGB warns you about the ones it knows.
   Need your cooler's app for its fan settings? Keep it, and switch "Control this device" off for
   the cooler.
4. A short guide shows you around on the first start (it's in Settings if you want it again).

SpectraRGB keeps running in the tray (by the clock) when you close its window, and can start with
Windows (Settings).

## Updates

SpectraRGB looks for a new version once a day and offers to install it; you can also check by hand,
or switch the daily check off, in Settings → Updates. Updates are signed: only ones from SpectraRGB's
maker install.

## Your privacy

Nothing leaves your PC, except the daily question to GitHub whether there's a new version.
- Effects that react to **key presses** only learn where on the keyboard and when, never which key.
- Effects that react to **sound** listen to what the PC plays (never the microphone), only while
  such an effect is on.
- Effects that take colors from the **screens** look at tiny images of them, never stored.
- Reports (below) are files you save and send yourself.

## Help

Join **[SpectraRGB's Discord](https://discord.gg/JgBMpJe3fm)** for questions, ideas and reports.
- **A device that isn't supported**: Devices → "Device not supported yet?" → create a report, and
  send it there, saying which device you'd like supported. It only reads from the devices and
  leaves out serial numbers.
- **Something not working**: Settings → Problems → "Save a problem report", and send it there.
- **Asked for a recording** (a device nobody has described yet): Devices → "Record a lighting
  program"; it walks you through it, and keeps only that device's lighting messages.
- **Another program should light a device** (its maker's app, a game): switch "Control this
  device" off on its card in Devices.

## Uninstall

Windows Settings → Apps → Installed apps → SpectraRGB → Uninstall. Tick **Delete the application
data** there to remove your settings and wallpapers too (else they're kept for a reinstall).
