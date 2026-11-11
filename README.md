# Marquee

An [Evey](https://github.com/eveyproject/evey) plugin: a living cinema poster wall built from your own library on the home screen. Hover a poster, spin the roulette, pick tonight's watch.

## What it asks for

- `public`: titles and posters of the libraries the viewer can see, through the host bridge. No network, no stored data.
- Slot: `home.section`.

## Install

Each [release](../../releases) publishes `marquee-<version>.zip`, its cosign
signature (`.zip.sig`) and its sha256. In Evey, open **Admin > Plugins >
Install Plugin > From URL** and paste the URL given in the release notes; the
`#sha256:` it ends with makes Evey check the download, and Evey fetches the
signature next to it on its own. The preview shows **Signed by** the Evey
project key once you trust it.

The Evey project key has the fingerprint `sha256:c29eb603b19d99a50f3fa6c94b7e92c41710779261e73e0fa31d53a78902e09a`. Compare it with the one
the preview shows before you trust it.

## Build

```sh
./scripts/build-zip.sh      # -> out/marquee-<version>.zip
```

The same commit always gives the same zip, so a rebuild can be compared with
a published release byte for byte.

## Release

Bump `version` in `plugin.yaml`, then push a tag `v<version>`. The release
workflow builds, signs with the project key and publishes.

## License

MIT, see [LICENSE](LICENSE).
