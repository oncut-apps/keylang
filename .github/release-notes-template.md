<!--
Release notes for a GitHub release of oncut KeyLang. Copy into the release
description and replace every {placeholder}. The files attached to the release
must be byte for byte the ones on downloads.oncut.gr (KEYLANG-LAUNCH.md, D1).
Title of the release: "oncut KeyLang {version}", tag "v{version}".
-->

{One or two sentences: what this version changes for the person using it.}

## Downloads

| File | For | SHA-256 |
| --- | --- | --- |
| `oncut_KeyLang-{version}-windows-x64-setup.exe` | Windows 10 and 11; 14-day trial, a license key unlocks it | `{sha256}` |
| `oncut_KeyLang-{version}-x86_64.AppImage` | Linux, X11 session; free | `{sha256}` |

`SHA256SUMS` and `SHA256SUMS.minisig` are attached too. The same files are at
<https://apps.oncut.gr/keylang>. Windows: run the installer (per user, no
administrator rights; installer and application signed by oncut). Linux: `chmod +x` the AppImage
and run it; Ubuntu 24.04 needs `sudo apt install libfuse2t64` once.

## Checking the files

```sh
minisign -Vm SHA256SUMS -P {public key from apps.oncut.gr/keys}
sha256sum -c --ignore-missing SHA256SUMS
```

The first command proves `SHA256SUMS` comes from oncut, the second that your
file matches it. Release key id: `3AA1B9E2CD1C2AE8`.

## Licenses

KeyLang is proprietary software under its
[End-User License Agreement](https://apps.oncut.gr/keylang/eula). It ships with
Qt {qt version} (LGPL-3.0) and FFmpeg {ffmpeg version} (LGPL-2.1-or-later),
dynamically linked and replaceable; the Linux AppImage also bundles LGPL
libraries from Ubuntu 24.04. License texts and the written offer of
corresponding source are inside every package; the list is at
<https://apps.oncut.gr/keylang/licenses>. {If attached: The corresponding
source archives of the LGPL components are attached to this release.}

Privacy: <https://apps.oncut.gr/privacy>. Refunds: <https://apps.oncut.gr/refunds>.
