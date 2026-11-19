# StremCompat for Android TV

<p align="center">
  <img src="docs/assets/stremcompat-hero-en.png" alt="StremCompat home screen" width="1200">
</p>

<p align="center">
  <a href="https://github.com/StremCompat/android-tv/releases"><img alt="Latest release" src="https://img.shields.io/github/v/release/StremCompat/android-tv?display_name=tag&color=0F766E"></a>
  <a href="https://github.com/StremCompat/android-tv/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/StremCompat/android-tv/total?color=0F766E"></a>
  <img alt="Android TV 7.0 and newer" src="https://img.shields.io/badge/Android%20TV-7.0%20and%20newer-0F766E">
  <img alt="Test version" src="https://img.shields.io/badge/status-test%20version-ea345e">
  <a href="https://github.com/StremCompat/android-tv/stargazers"><img alt="Stars" src="https://img.shields.io/github/stars/StremCompat/android-tv?style=flat"></a>
  <a href="https://buymeacoffee.com/Alexesmm"><img alt="Buy me a coffee" src="https://img.shields.io/badge/support-Buy%20me%20a%20coffee-ffdd00?logo=buymeacoffee&logoColor=black"></a>
</p>

<p align="center"><b>English</b> · <a href="README.pt.md">Português</a></p>

StremCompat brings your **Stremio or Nuvio** account and addons to Android TV and Google TV boxes and TVs, with an interface made for the remote. It is an independent, unofficial project, not affiliated with or endorsed by Stremio, Nuvio or Google, and it plays only what your own addons provide.

> **Test versions.** Please report problems in [Discussions](https://github.com/StremCompat/android-tv/discussions).

## Two versions

| | **StremCompat** | **StremCompat Native** |
|---|---|---|
| Status | **Recommended** | **Beta**, not stable yet: faster, but expect rough edges |
| How it is made | The interface as a web page in a WebView | The native app in C, drawn with OpenGL ES (SDL2) |
| Video | Android's own player (ExoPlayer) | The same |
| Package | `io.github.alexesmm.stremcompat` | `io.github.alexesmm.stremcompat.native` |

Both can be installed together. On its first start the native version brings your account, library and settings from the web one.

There is also an **app for Android phones** (beta), with the same account and addons, published in this repository as `StremCompat-Phone-v…-beta-Android.apk`.

## Features

The same app as on LG ([full list](https://github.com/StremCompat/webos#features)):

- Stremio or Nuvio account with QR or email sign-in, Nuvio profiles with PINs, and Nuvio Collections as in Nuvio's apps.
- Home, Discover, Search, Library, Continue Watching, new episodes and, for Stremio accounts, a Calendar.
- Live channels from addons (such as NexoTV) and M3U lists, with what is on now and search.
- An addon store, adding addons and lists by address, typed or pasted from your phone, and organizing the rows of Home.
- Best source, source filters, subtitles and audio remembered per title, Skip intro and the next episode.
- **Video with ExoPlayer:** MKV, HEVC and surround sound play as in the official apps.
- **Torrents** play on the device itself, through a torrent engine inside the app. Debrid and direct links work too.
- What you are watching shows up in the "Continue watching" row of the Google TV home screen.
- Eleven languages.

## Screenshots

Captured from the real interface at 1920x1080, with a demo account, Stremio's official addons and a public channel list. The interface is the same on LG, Samsung and Android TV.

<table>
  <tr>
    <td width="50%" valign="top"><img src="docs/assets/screens/home.jpg" alt="Home" width="100%"><br><b>Home</b><br><sub>Your catalogs as rows, with the focused title large at the top.</sub></td>
    <td width="50%" valign="top"><img src="docs/assets/screens/profiles.jpg" alt="Who is watching" width="100%"><br><b>Who is watching</b><br><sub>Nuvio profiles, with PIN-protected ones marked.</sub></td>
  </tr>
  <tr>
    <td width="50%" valign="top"><img src="docs/assets/screens/series.jpg" alt="Series page" width="100%"><br><b>Series page</b><br><sub>Details, cast, seasons and episodes with their air dates.</sub></td>
    <td width="50%" valign="top"><img src="docs/assets/screens/sources.jpg" alt="Sources" width="100%"><br><b>Sources</b><br><sub>Every source your addons find, with quality and size; or Best source in one press.</sub></td>
  </tr>
  <tr>
    <td width="50%" valign="top"><img src="docs/assets/screens/discover.jpg" alt="Discover" width="100%"><br><b>Discover</b><br><sub>Browse any catalog by type, order and genre.</sub></td>
    <td width="50%" valign="top"><img src="docs/assets/screens/channels.jpg" alt="Live channels" width="100%"><br><b>Live channels</b><br><sub>Categories on the left, channels and what is on now on the right.</sub></td>
  </tr>
  <tr>
    <td width="50%" valign="top"><img src="docs/assets/screens/add-list.jpg" alt="Adding a list" width="100%"><br><b>Adding a list</b><br><sub>Type the address with the built-in keyboard, scan the QR to paste it from your phone, or pick a suggested list.</sub></td>
    <td width="50%" valign="top"><img src="docs/assets/screens/store.jpg" alt="Addon store" width="100%"><br><b>Addon store</b><br><sub>Community addons by popularity, with picture and description. The ones you have are hidden.</sub></td>
  </tr>
  <tr>
    <td width="50%" valign="top"><img src="docs/assets/screens/organize.jpg" alt="Organize catalogs" width="100%"><br><b>Organize catalogs</b><br><sub>Reorder or hide the rows of Home.</sub></td>
    <td width="50%" valign="top"><img src="docs/assets/screens/settings.jpg" alt="Settings" width="100%"><br><b>Settings</b><br><sub>Playback, subtitles, audio, interface, channels and account.</sub></td>
  </tr>
</table>

## Installation

1. Download the `.apk` of the version you want from [Releases](https://github.com/StremCompat/android-tv/releases):
   - `StremCompat-v…-AndroidTV.apk` (web version);
   - `StremCompat-Native-v…-AndroidTV.apk` (native version).
2. On the TV, install the **Downloader** app (by AFTVnews) from the Play Store, and allow it to install unknown apps (Settings > Device Preferences > Security & restrictions > Unknown sources).
3. In Downloader, type the address of the `.apk` from the release page and install it.

Or, from a computer: `adb install StremCompat-…-AndroidTV.apk`.

**Requirements:** Android TV or Google TV 7.0 or newer, on an ARM device (nearly every TV box and TV). The x86 emulator is not supported.

## Troubleshooting

- **The app shows "Starting…" for a long time on its first open:** it unpacks its local server once; later starts are quick.
- **A source does not play:** try another source; ExoPlayer plays most formats, but some addons' links expire quickly.
- **The QR code to paste an address from the phone does not open:** the phone must be on the same Wi-Fi; type the address with the app's keyboard instead.

## Other TVs and the project

StremCompat lives in the [StremCompat organization](https://github.com/StremCompat):

- **LG** (webOS 3 and newer): [StremCompat/webos](https://github.com/StremCompat/webos)
- **Samsung** (Tizen 4 and newer): [StremCompat/samsung](https://github.com/StremCompat/samsung)
- **Android TV / Google TV** (7.0 and newer): [StremCompat/android-tv](https://github.com/StremCompat/android-tv) (this page)
- Source code: [StremCompat/stremcompat](https://github.com/StremCompat/stremcompat) (web version and local server) and [StremCompat/native](https://github.com/StremCompat/native) (native version).

## Feedback and support

Questions in [Discussions](https://github.com/StremCompat/android-tv/discussions), reproducible bugs in [Issues](https://github.com/StremCompat/android-tv/issues). Source code: [StremCompat/stremcompat](https://github.com/StremCompat/stremcompat) and [StremCompat/native](https://github.com/StremCompat/native).

If StremCompat has been useful to you, you can [buy me a coffee ☕](https://buymeacoffee.com/Alexesmm), entirely optional.

StremCompat is licensed under [GPL-3.0](LICENSE). Stremio, Nuvio and Google are trademarks of their owners.
