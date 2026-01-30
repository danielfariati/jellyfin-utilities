Jellyfin Manifest Generator
===
This script can be used to manage a Jellyfin manifest file that describes a plugin repository. See [Blog Post](https://jellyfin.org/posts/plugin-updates/) for more details from the Jellyfin team.

Usage
---
Add a new application to the manifest
```bash
python manifest.py -f /tmp/manifest.json -app Last.fm -desc "Scrobble Last.fm plays with Jellyfin" -ov "A plugin that scrobbles your Jellyfin music to LastFM" -owner "danielfariati" -cat "music" -guid "ASDFSDF"
```

Note: that for a first time manifest file creation, pass the `-create` option.

Adding a new version to the application is done via
```bash
python manifest.py -f /tmp/manifest.json -app Last.fm -ver "1.0.0" -cl "This is my changelog text." -abi "10.11.0.0" -url "https://github.com/danielfariati" -ts "2020-07-24"
```
