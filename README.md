# EasyBPM — updates

This repository is the update channel for **EasyBPM** by
[EasyOneAudio](https://easyoneaudio.com). It holds no source code: only the
signed installer packages attached to each release, and a `latest.json`
manifest that the app reads to learn whether a newer version exists.

There is nothing here to install by hand. EasyBPM checks this channel itself and
offers the update inside the app.

## Verifying a download

Every package is signed with our Developer ID Installer certificate
(Team ID `2VKTV5VPVB`) and notarized by Apple. To check a `.pkg` yourself:

```
pkgutil --check-signature EasyBPM.pkg
```

The output must name `Developer ID Installer: Dmytro Berezhnyi (2VKTV5VPVB)` and
report `Notarization: trusted by the Apple notary service`. EasyBPM performs this
same check before it will install anything, so a package that fails it is
rejected whether you run the command or not.

The `sha256` field in `latest.json` proves only that a download arrived intact.
The signature is what proves it came from us.

---

No releases published yet.
