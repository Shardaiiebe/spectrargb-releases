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
- **More keyboards, mice and mats**, as an experiment (switched on in Devices; tell us how it went):
  - **SteelSeries**: Apex keyboards (5, 7, 9, Pro, 3, the original Apex), Rival and Sensei mice;
  - **Corsair**: K55 RGB PRO, K57, K60, K65, K70, K95 RGB PLATINUM XT, K100 and Strafe RGB
    keyboards, Dark Core, Harpoon, Ironclaw, Katar, M55, M65 Ultra, M75 and Scimitar Elite mice (by
    cable), MM700 and MM800 mats, the ST100 stand;
  - **Logitech**: G813, G915 and G915 TKL keyboards (by cable or their own receiver), G502, G403,
    G703, G900, G903, G203 Prodigy, G303 and G Pro mice, G633, G635, G733 and G935 headsets;
  - **HyperX**: Alloy Origins (Core, 60, 65), Alloy Elite 2, Alloy FPS RGB, Origins 2 65 and Eve
    1800 keyboards, Pulsefire Surge, FPS Pro, Core, Raid, Haste and Dart mice;
  - **Wooting** keyboards (One, Two, 60HE, 80HE, UwU);
  - **Roccat**: Kone Aimo, Kone Pro (Air) and Burst mice, the Horde Aimo keyboard, the Elo 7.1
    headset.
  - Only their lighting: never their buttons', DPI or profile settings. Not on purpose: devices
    behind a Logitech Lightspeed receiver, Corsair's wireless receivers, some Corsair (K70 RGB MK.2,
    K95 RGB PLATINUM, older mice) and SteelSeries models (Rival 5, Aerox), Roccat's Vulcan
    keyboards, the HyperX Alloy Elite: their lighting can't be driven without changing how their
    keys work or writing to their memory. Some Corsair keyboards and mice may leave a knob, macro
    keys or DPI buttons to software while SpectraRGB lights them; tell us if one does.
- **Desktops**, as an experiment (switched on in Devices; tell us how it went):
  - the lighting of **ASUS** (Aura USB), **Gigabyte** (RGB Fusion 2) and **MSI** (Mystic Light)
    motherboards: their own LEDs, and the fans and strips on their RGB headers (you say what's
    plugged in, in Devices);
  - **coolers**: **NZXT Kraken** (X3, Z3, Elite RGB, X2), **Corsair Hydro** (Platinum, Pro XT,
    Elite RGB), Corsair's **Commander Core** coolers (Elite Capellix, Elite LCD) and the **ASUS ROG
    Strix LC III**, with the fans plugged into them: their lighting, and their liquid temperature
    and pump and fan speeds on the Cooling page. Their pump and fans keep running as they were set
    until you switch **Control cooling** on for one: then you set them, by curves on its liquid or
    any temperature SpectraRGB reads (never below the pump's safe minimum, full speed when it's
    too hot).
  - the lighting of hubs and fan controllers: **NZXT** HUE 2, Smart Device V2, RGB & Fan
    Controllers and RGB Controllers; **Corsair** Commander Pro and Lighting Node Pro and Core;
    **Lian Li** Uni Hubs (SL, AL, SL-Infinity, SL V2, AL V2); **Thermaltake** Riing Plus, Quad and
    Trio controllers; the **Cooler Master** ARGB controller A1 (and A1 Mini). You say what's
    plugged in (NZXT's own fans and strips are found by themselves). Never their fan speeds.
  - the lighting of **graphics cards**: NVIDIA's own Founders Editions and other GeForce cards
    whose driver offers lighting zones, and about 570 GeForce and Radeon cards by ASUS (ROG Strix,
    TUF, older Strix), MSI, Gigabyte/AORUS, EVGA (RTX 30) and Sapphire (Nitro+, Toxic, Pure),
    matched by their exact model. Only the lighting chip's color settings, nothing stored on the
    card.
  - **RGB RAM** (ENE-based modules; Corsair Vengeance RGB, RGB Pro, Dominator Platinum RGB and their
    DDR5 kin) and older ASUS Aura motherboards, lit over the motherboard's SMBus. That needs
    **PawnIO**, a signed driver SpectraRGB installs only when you ask (Devices); Windows then asks
    for administrator rights once: a copy of SpectraRGB's helper goes to Program Files and a
    Windows scheduled task, which only your account can start, runs it from then on (updates
    don't ask again; uninstalling removes both). Only modules recognized exactly are lit, and
    never their memory settings.
  - **Motherboard fan headers** (Cooling page, with PawnIO; Nuvoton and ITE chips): their speeds,
    and, once you switch it on, fixed speeds or curves on any temperature. Never below 30%; full
    speed when a temperature is critical or unknown; the BIOS's own settings back when SpectraRGB
    stops (after a crash within 5 seconds; if Windows ends SpectraRGB's helper by force, after a
    restart). Not while FanControl or LibreHardwareMonitor runs (they'd fight over the fans).
  - Not yet: MSI's newest X870 boards and older ones without per-LED lighting, most graphics cards
    by Palit, Gainward, PNY, Colorful and Galax, Gigabyte's RTX 50 series. A device report helps add
    them. Not at all, on purpose: ASRock motherboards' USB lighting, Cooler Master's older ARGB
    controllers, PowerColor Red Devil and most Zotac and Manli cards (they save every change into
    their memory, which wears it out), Gigabyte's and EVGA's older graphics cards (their protocols
    could store settings by accident), the first Lian Li Uni Hub.
- **Lights on your network**: WLED, Nanoleaf, Philips Hue (an Entertainment area, through the
  bridge), LIFX, Govee (with its LAN control on) and E1.31 (sACN) or Art-Net pixel controllers.
  Devices → "Lights on the network" finds them or takes an address. When SpectraRGB stops, they go
  back to what they showed.
- **OpenRGB**: devices only OpenRGB knows can be lit through it (Devices → "Use devices from
  OpenRGB", with OpenRGB's SDK server running), and programs that speak OpenRGB's SDK (games,
  Stream Deck plugins, sound visualizers) can light SpectraRGB's devices and wallpaper (Settings,
  off until you switch it on).
- Group devices that belong together (a PC case's insides) on the Layout page, and give them an
  effect of their own if you like.
- **Setups**: save a layout for each desk ("Home", "Office"), and SpectraRGB picks the one whose
  devices and screens are connected, by itself.
- **Sensors**: the CPU's (with PawnIO) and graphics cards' temperatures, coolers' and fans'
  readings, for effects (Temperature, effect code) and fan curves.
- **Automations**: the lights change by themselves and go back after, when the PC locks, a game
  fills the screen, at night, on battery, when you're away (start from a template on the
  Automations page). Switch them all off for a while from the tray.

Something not on the list? See [Help](#help): a device report helps add it.

## Install

1. Under [Releases](../../releases/latest), download `SpectraRGB_<version>_x64-setup.exe` and run it.
   It installs for you only (no admin rights needed).
2. Windows may warn that the app is from an unknown publisher (it isn't signed with a paid
   certificate): choose **More info**, then **Run anyway**.
3. **Quit other lighting software** first: Armoury Crate, G HUB, Razer Synapse, SteelSeries GG,
   HyperX NGENUITY, Wootility, SignalRGB, OpenRGB, your motherboard's, cooler's, fan hub's or
   graphics card's lighting app (MSI Center, Gigabyte Control Center, ASUS GPU Tweak, EVGA Precision
   X1, NZXT CAM, iCUE, L-Connect) and the like. They fight over the lights; SpectraRGB warns you
   about the ones it knows.
   Need your cooler's app for its fan settings? Keep it, and switch "Control this device" off for
   the cooler.
4. A short guide shows you around on the first start (it's in Settings if you want it again).

SpectraRGB keeps running in the tray (by the clock) when you close its window, and can start with
Windows (Settings).

## Updates

SpectraRGB looks for a new version once a day and offers to install it; you can also check by hand,
or switch the daily check off, in Settings → Updates. Updates are signed: only ones from SpectraRGB's
maker install.

## Control from anywhere

The lights switch, brightness, presets and the wallpaper also work without opening the window:
- **The tray icon's menu** (right-click): lights, brightness, presets, setups, wallpaper,
  automations.
- **Hotkeys** (Settings → Hotkeys): pick what a key combination does, press the combination. They
  work anywhere, also with the window closed. None are set until you add them.
- **The command line**, for shortcuts, scripts, AutoHotkey or a Stream Deck "Open" button:
  `"%LOCALAPPDATA%\SpectraRGB\SpectraRGB.exe" --lights off` (also `--brightness 40` or `up`/`down`,
  `--effect "Calm"`, `--next-effect`, `--previous-effect`, `--place "Office"`, `--wallpaper on`,
  `--automations off`, `--control "Device name" off`, `--show`, `--quit`; `--help` lists them).
- **The local API**, for scripts and tools that speak HTTP (Settings → Control from anywhere,
  off until you switch it on): `http://127.0.0.1:47320/api/v1`, with the token Settings shows as
  `Authorization: Bearer <token>`. Only programs on your PC can reach it; web pages can't.
  - Read: `GET /state` (lights, brightness, the preset showing, wallpaper, devices),
    `GET /devices`, `GET /effects`.
  - Do (`POST`): `/lights/on`, `/lights/off`, `/lights/toggle`; `/brightness/40`,
    `/brightness/up`, `/brightness/down`; `/effect/next`, `/effect/previous`,
    `/effect?name=Calm`; `/wallpaper/on`, `/off`, `/toggle`; `/devices/<name>/control/off`;
    `/window/show`; `/actions` with JSON like `{"type": "lights", "to": "off"}` or
    `{"type": "place", "name": "Office"}`.
  - Follow changes: the WebSocket `ws://127.0.0.1:47320/api/v1/events?token=<token>` sends
    `{"type": "state", ...}` on each change, and takes the same JSON actions.
  - PowerShell: `Invoke-RestMethod -Method Post http://127.0.0.1:47320/api/v1/lights/toggle
    -Headers @{ Authorization = "Bearer <token>" }`
- **Home Assistant** (or other home automation), through MQTT (Settings → Control from anywhere →
  MQTT, off until you set it up): fill in your broker (for Home Assistant's Mosquitto add-on: the
  Home Assistant machine, and a Home Assistant user). SpectraRGB then shows up in Home Assistant
  by itself, as a device with a light (on/off, brightness, your presets as its effects), a
  wallpaper switch and next/previous preset buttons, ready for automations. Other systems:
  publish to `spectrargb/<your PC's name>/light/set` (`{"state": "OFF"}`) or `.../action` (the
  API's JSON), follow `spectrargb/<your PC's name>/state`.

## Your privacy

Nothing leaves your PC, except the daily question to GitHub whether there's a new version, and
what you set up yourself: colors to the lights on your network, what the lights show to your own
MQTT broker, SpectraRGB's devices to programs using its OpenRGB server (this PC only, unless you
open it to your network).
- Effects that react to **key presses** only learn where on the keyboard and when, never which key.
- Effects that react to **sound** listen to what the PC plays (never the microphone), only while
  such an effect is on.
- Effects that take colors from the **screens** look at tiny images of them, never stored.
- Effects that react to **how busy your PC is** (a meter, a layer for when the processor is busy or
  the battery low) read only numbers, about once a second and only while such an effect is on: the
  processor's, memory's and graphics card's load, how fast data moves over the network and the
  disks, the battery. Never which programs, sites or files.
- Effects that follow **the time of day** use the PC's clock; for the real sunrise and sunset you
  can enter your location in Settings. It's worked out on your PC, nothing is looked up, and the
  location stays out of the settings files and problem reports you save.
- Effects that follow **what plays** (album colors, a flash on a new track) read what players tell
  Windows (the player in the volume flyout), only while such an effect is on: playing or paused,
  where in the track, and the cover's main colors. The track's title is only used to notice that
  a new one started, never kept or shown.
- The **Game** effect follows the match you play, only while it's on: Counter-Strike 2 and Dota 2
  send it to SpectraRGB on your PC once you set them up (Lighting → Game → Games: it writes one
  file into the game's config folder, after asking; Remove takes it away), League of Legends is
  asked on your PC while a match runs. Only health, armor, ammo, mana, the team, the bomb, kills,
  deaths and rounds are used; player names only to find your own player, never kept.
- **Automations** about the program in front only look at its file name (`game.exe`), on your PC:
  never logged or kept, except in the rules you make (problem reports leave them out). Ones about
  idle time only learn when the keyboard or mouse was last used, never what was typed.
- **Network lights**: the search asks your local network which lights are there (mDNS, the
  lights' own broadcasts); keys a light gives when paired (Nanoleaf, Hue) stay in your settings.
- **Sensors and fans** are read on your PC only; nothing about them is sent anywhere.
- Reports (below) are files you save and send yourself.
- **Hotkeys** only receive the combinations you set, nothing else you type. The **local API**
  answers programs on this PC only, with its token. **MQTT**, if you set it up, talks to your own
  broker only. Reports and exported settings never include the token or the MQTT password.

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
