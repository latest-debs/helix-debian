![helix for Debian](.github/readme-header.png)

# helix for Debian

[![Release](https://img.shields.io/github/v/release/latest-debs/helix-debian)](https://github.com/latest-debs/helix-debian/releases)
[![Build](https://github.com/latest-debs/helix-debian/actions/workflows/release.yml/badge.svg)](../../actions)

[helix-editor/helix](https://github.com/helix-editor/helix) — A post-modern modal text editor. —
packaged for Debian as part of [latest-debs](https://github.com/latest-debs).

Want your own project packaged and maintained this way? See the
[latest-debs packaging service](https://github.com/latest-debs/apt-repo/blob/main/SERVICE.md).

## Install

Via the latest-debs apt repository:

```sh
sudo apt install extrepo  # if not already installed
sudo extrepo enable latest-debs
sudo apt update
sudo apt install helix
```

Or download a `.deb` from the [Releases](https://github.com/latest-debs/helix-debian/releases) page:

```sh
sudo apt install ./helix_*.deb
```

## Verify

```sh
apt-cache policy helix
helix --version
```

## Supported distributions & architectures

- Debian Bullseye (11), Bookworm (12), Trixie (13), Forky (14/testing), Sid (unstable)
- amd64, arm64, armhf, i386, armel, loong64, ppc64el, riscv64, s390x —
  whichever architectures helix-editor/helix actually publishes a Linux
  binary for

## Building

Run the [Build helix for Debian](../../actions) workflow on GitHub with the
desired upstream version. Packaging is driven by
[debian-multiarch-builder](https://github.com/ranjithrajv/debian-multiarch-builder).

## Collaborate with us

latest-debs is a community effort. If you rely on this package and want to
help keep it fresh, watching for a new upstream release or fixing a build
hiccup, we'd love your help. Open an issue on this repo, or email
**latest-debs@users.noreply.github.com** to get involved.

## Disclaimer

Unofficial, volunteer-run packaging — **best-effort, no SLA**.

- **Update cadence:** publishing a release normally triggers an immediate
  apt-repo rebuild via webhook; the ~6h scheduled run is the fallback. GitHub
  outages, a missing trigger token, rate limits, or upstream archive changes
  can delay or skip an update; there is no freshness guarantee.
- **Draft releases:** every build is published as a *draft* that a maintainer
  reviews before promoting, so a new version can lag its build.

For issues with helix itself, see
[helix-editor/helix](https://github.com/helix-editor/helix).

## License

Packaging scripts in this repo are MIT-licensed. The packaged binaries
remain under their upstream license (`MPL-2.0` — see
[helix-editor/helix](https://github.com/helix-editor/helix)).
