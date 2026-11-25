# Remote for Apple TV

Support page for **Remote for Apple TV**, a Stream Deck plugin that turns Stream Deck keys into Apple TV remote buttons. Get it on the [Elgato Marketplace](https://marketplace.elgato.com/product/remote-for-apple-tv-f4c80b88-7b2c-46f3-a1c5-78cfe9dd0130).

## Get help

- **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](../../issues/new?template=feature_request.yml).

Please search [existing issues](../../issues) first.

## Requirements

- Windows 10 or later, or a Mac with Apple Silicon (M1 or later) running macOS 12 or later. Intel Macs are not supported.
- Stream Deck 7.1 or later.
- An Apple TV on the same network as the computer.

## Setup

1. Drag **Remote for Apple TV → Remote Button** onto a key.
2. In its settings, click **Scan**, choose your Apple TV, and click **Pair**. If nothing is found, type the Apple TV's IP address (Apple TV **Settings → Network**) and click **Scan** again.
3. Enter the PIN shown on the TV. A second PIN follows for AirPlay.
4. Choose what the key does under **Button**. Add more keys for other buttons; they all share the pairing.

Arrow and volume keys repeat while held.

**Disconnect key:** an open connection to the Apple TV can wake a sleeping computer. Add a key set to **Disconnect** and press it before you leave your computer; the next press of any other key reconnects automatically.

## What a key can do

Besides the remote buttons (arrows, Select, Back, Home, Control Center, Play/Pause, Skip, Previous/Next, Volume, Power), a key can be set to:

- **Open App:** opens the app you choose under **App** (the list comes from your Apple TV). The key shows the app's name.
- **Now Playing:** plays or pauses, then shows the artwork and title of what's playing.
- **Type Text:** types the text under **Text** into the field open on the Apple TV, for example Search. It replaces what's already there.
- **Play URL:** plays a direct link to a video or audio file on the Apple TV over AirPlay.
- **Power On** and **Power Off** (besides the Power toggle), **App Switcher**, and **Select (hold)** for context menus.

**Hold and Double press:** any key can also have a second command when held and a third when pressed twice, for example Home, with App Switcher on a double press and Control Center on hold. These can be remote commands only. When either is set, the key's own command runs when you let go (after the double-press window if there is one), and arrows don't repeat.

## Several Apple TVs

Click **Add Apple TV** in any key's or dial's settings to pair another one. The first one you paired is the default. Once two or more are paired, each key and dial has a **Control** menu for choosing which Apple TV it controls. Each Apple TV has its own **Forget** button.

## Stream Deck + dials

Drag **Remote for Apple TV → Remote Dial** onto a dial and choose what it does under **Dial**. It uses the same pairing as the keys.

- **Volume:** turn to change the volume, press to play or pause, touch the strip to show the level. The level only shows when the Apple TV knows it (for example with HomePod speakers). "Not available" means the Apple TV can't change the volume; turn on HDMI-CEC under **Settings → Remotes and Devices → Volume Control** on the Apple TV.
- **Navigate:** turn to move left and right (or up and down, under **Direction**), press to select, touch for Back, touch and hold for Home.
- **Scrub:** turn to jump back or forward by the **Step** (5 seconds to 1 minute), press to play or pause.
- **Seek:** like Scrub, but each click moves by a share of the length (1–10 %), for long videos.
- **Music:** turn for the previous or next track, press to play or pause, touch to turn shuffle on or off, touch and hold to change repeat (off, all, one).
- **Apps:** turn to choose one of your Apple TV's apps, press to open it, touch to reload the list.

The touch strip is updated after you use the dial, not continuously.

## Troubleshooting

- **Scan finds nothing:** enter the Apple TV's IP address and scan again. Some routers and mesh Wi-Fi systems block automatic discovery.
- **Pairing failed:** the PIN was wrong or expired. Click **Pair** again for a new PIN.
- **Pairing fails with an "SRPClientSession" error:** this was a bug in version 1.0.2. Update the plugin to 1.0.3 or later, then pair again.
- **A key shows a warning triangle:** the Apple TV may be off the network or its IP address changed. Reserve a fixed IP for it in your router, then click **Forget** next to that Apple TV and pair it again.
- **Your computer wakes from sleep by itself:** press a **Disconnect** key before the computer sleeps. The plugin also closes the connection on its own after the first wake.
- **Play URL doesn't play:** the link must go straight to a video or audio file (for example ending in .mp4 or .mp3) that the Apple TV can reach. Web pages and most streaming-service links don't work.
- **"This plugin requires a Mac with Apple Silicon":** the plugin doesn't run on Intel Macs.
- **Windows asks whether to allow network access:** choose **Allow** so the plugin can find and control your Apple TV on your local network.

When reporting a bug, attach the latest log from:

- **macOS:** `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.appletvremote.sdPlugin/logs/`
- **Windows:** `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.appletvremote.sdPlugin\logs\`

## Privacy

The plugin collects no personal data and connects only to your Apple TV on your local network. See the [Privacy Policy](PRIVACY.md).

## Open-source software

The plugin is built on [pyatv](https://github.com/postlund/pyatv) and other open-source software; see `THIRD_PARTY_NOTICES.txt` inside the plugin. To request the build scripts used to rebuild the bundled helper (for example with a modified LGPL library), open an issue.

---

Apple TV is a trademark of Apple Inc. This plugin is not affiliated with, sponsored by, or endorsed by Apple Inc.
