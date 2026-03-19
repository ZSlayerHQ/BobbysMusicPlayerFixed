# Bobby's Music Player — SPT 4.0.13 Fix

**A custom music player for Escape from Tarkov (SPT).** Adds configurable in-raid soundtrack, combat music, spawn music, and menu music with support for custom audio files.

Originally created by [BobbyRenzobbi](https://hub.sp-tarkov.com/user/26220-bobbyrenzobbi/). This fork updates the mod for SPT 4.0.13 compatibility.

## Features

### In-Raid Soundtrack
- Ambient background music during raids
- Map-specific playlists or combined playlist mode
- Configurable track length and volume
- Skip, restart, previous track, and pause hotkeys

### Combat Music
- Dynamic combat music triggered by:
  - Being attacked
  - Danger detection
  - Nearby grenades
  - Gunfire
  - Getting hit
- Configurable fade in/out timing
- Indoor and headset volume multipliers
- Adjustable detection ranges for shots and grenades

### Menu Music
- Custom menu music replacement
- Configurable track length

### Spawn Music
- Music that plays on raid start
- Separate volume control

### Audio Format Support
WAV, OGG, MP3, AIFF, S3M, IT, MOD, XM, XMA, VAG

## Installation

1. Download `BobbysMusicPlayer.dll` from the [Releases](https://github.com/ZSlayerHQ/BobbysMusicPlayerFixed/releases) page
2. Copy `BobbysMusicPlayer.dll` to `SPT/BepInEx/plugins/`
3. Launch the game once to generate the config file
4. Add your music files to `SPT/BepInEx/plugins/BobbysMusicPlayer/` (create the folder if needed):
   - `soundtrack/` — ambient raid music
   - `soundtrack/{mapname}/` — map-specific tracks (e.g. `soundtrack/bigmap/`, `soundtrack/factory4_day/`)
   - `combat/` — combat music
   - `spawn/` — spawn music
   - `menu/` — menu music

## Configuration

All settings are in `BepInEx/config/BobbyRenzobbi.MusicPlayer.cfg` or via the BepInEx Configuration Manager (F12).

### Soundtrack Settings

| Setting | Default | Description |
|---------|---------|-------------|
| Soundtrack Volume | 0.5 | Volume of ambient raid music (0-1) |
| Soundtrack Length | 180 | Seconds per track |
| Soundtrack Playlist | MapSpecificPlaylistOnly | `MapSpecificPlaylistOnly`, `CombinedPlaylists`, or `DefaultPlaylistOnly` |

### Combat Music Settings

| Setting | Default | Description |
|---------|---------|-------------|
| Combat Music Volume | 0.5 | Volume of combat music (0-1) |
| Combat In Fader | 1.0 | Seconds to fade in combat music |
| Combat Out Fader | 3.0 | Seconds to fade out combat music |
| Ambient Combat Multiplier | 1.0 | Multiplier for ambient volume during combat |
| Shot Near Cutoff | 30 | Distance in meters for nearby gunfire detection |
| Grenade Near Cutoff | 50 | Distance in meters for nearby grenade detection |
| Indoor Multiplier | 0.7 | Volume multiplier when indoors |
| Headset Multiplier | 0.8 | Volume multiplier when wearing headset |

### Combat Trigger Timers

| Setting | Default | Description |
|---------|---------|-------------|
| Combat Attacked Entry Time | 10 | Seconds of combat music after being attacked |
| Combat Danger Entry Time | 5 | Seconds after danger detected |
| Combat Grenade Entry Time | 8 | Seconds after nearby grenade |
| Combat Fire Entry Time | 5 | Seconds after nearby gunfire |
| Combat Hit Entry Time | 15 | Seconds after being hit |

### Hotkeys

| Setting | Default | Description |
|---------|---------|-------------|
| Skip Track | None | Skip to next track |
| Previous Track | None | Go to previous track |
| Restart Track | None | Restart current track |
| Pause Track | None | Pause/resume playback |

## Folder Structure

```
BepInEx/
├── plugins/
│   ├── BobbysMusicPlayer.dll
│   └── BobbysMusicPlayer/
│       ├── soundtrack/
│       │   ├── track1.ogg
│       │   ├── track2.mp3
│       │   ├── bigmap/           ← Customs-specific tracks
│       │   ├── factory4_day/     ← Factory day tracks
│       │   ├── interchange/      ← Interchange tracks
│       │   └── ...
│       ├── combat/
│       │   ├── combat1.ogg
│       │   └── combat2.mp3
│       ├── spawn/
│       │   └── spawn_theme.ogg
│       └── menu/
│           └── menu_music.ogg
└── config/
    └── BobbyRenzobbi.MusicPlayer.cfg
```

## Compatibility

| Requirement | Version |
|-------------|---------|
| **SPT** | 4.0.13 |
| **BepInEx** | 5.x |

## Credits

- **BobbyRenzobbi** — original mod author
- **ZSlayerHQ** — SPT 4.0.13 compatibility update

## Version

1.2.5

## License

All credit to the original author. This is an unofficial compatibility update.
