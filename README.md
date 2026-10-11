# Remote for Apple TV

Support page for **Remote for Apple TV**, a Stream Deck plugin that turns Stream Deck keys into Apple TV remote buttons. Get it on the [Elgato Marketplace](https://marketplace.elgato.com/).

## Get help

- **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](../../issues/new?template=feature_request.yml).

Please search [existing issues](../../issues) first.

## Requirements

- A Mac with Apple Silicon (M1 or later). Intel Macs are not supported.
- macOS 12 or later and Stream Deck 7.1 or later.
- An Apple TV on the same network as the Mac.

## Setup

1. Drag **Remote for Apple TV → Remote Button** onto a key.
2. In its settings, click **Scan**, choose your Apple TV, and click **Pair**. If nothing is found, type the Apple TV's IP address (Apple TV **Settings → Network**) and click **Scan** again.
3. Enter the PIN shown on the TV. A second PIN follows for AirPlay.
4. Choose what the key does under **Button**. Add more keys for other buttons; they all share the pairing.

Arrow and volume keys repeat while held.

## Troubleshooting

- **Scan finds nothing:** enter the Apple TV's IP address and scan again. Some routers and mesh Wi-Fi systems block automatic discovery.
- **Pairing failed:** the PIN was wrong or expired. Click **Pair** again for a new PIN.
- **A key shows a warning triangle:** the Apple TV may be off the network or its IP address changed. Reserve a fixed IP for it in your router, then pair again with **Change Apple TV**.
- **"This plugin requires a Mac with Apple Silicon":** the plugin doesn't run on Intel Macs.

When reporting a bug, attach the latest log from:

```
~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.appletvremote.sdPlugin/logs/
```

## Open-source software

The plugin is built on [pyatv](https://github.com/postlund/pyatv) and other open-source software; see `THIRD_PARTY_NOTICES.txt` inside the plugin. To request the build scripts used to rebuild the bundled helper (for example with a modified LGPL library), open an issue.

---

Apple TV is a trademark of Apple Inc. This plugin is not affiliated with, sponsored by, or endorsed by Apple Inc.
