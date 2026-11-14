<div align="center">
  <img src="assets/baryovpn-hero.png" alt="BaryoVPN" width="760" />

  <h1>BaryoVPN</h1>
  <p><strong>A clear, private and reliable Android VPN experience.</strong></p>
  <p>
    Organized profiles · Live connection insight · Privacy-first controls
  </p>

  <p>
    <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest"><img src="https://img.shields.io/badge/Download-latest%20APK-2563EB?style=for-the-badge&logo=android&logoColor=white" alt="Download latest APK" /></a>
    <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases"><img src="https://img.shields.io/github/downloads/BARYOPRO/BaryoVPN-Android/total?style=for-the-badge&color=0F766E" alt="Total downloads" /></a>
    <a href="https://github.com/BARYOPRO/BaryoVPN-Android/issues/new?template=bug_report.md"><img src="https://img.shields.io/badge/Report%20a%20bug-DC2626?style=for-the-badge" alt="Report a bug" /></a>
  </p>
</div>

> [!IMPORTANT]
> This is the official **APK-only distribution hub** for BaryoVPN Android. It intentionally does not contain application source code, signing keys, private configuration or server information.

## Why BaryoVPN?

BaryoVPN is designed to make Android VPN management feel understandable: the home screen explains what is happening, the server center keeps profiles organized, and the activity view provides useful local connection feedback without sending logs to a public service.

## Highlights

| Experience | What you get |
| --- | --- |
| **Clear home dashboard** | Protection state, selected server, latency, protocol, DNS mode and live traffic in one view. |
| **Organized server center** | Search, select, test and manage individual profiles or subscription groups. |
| **Privacy controls** | Ghost Mode, kill switch, DNS and IPv6 posture, app coverage and WebRTC Privacy Guard. |
| **Reliable updates** | Architecture-aware APK selection, download validation and Android’s standard installer confirmation. |
| **QR and subscription workflow** | Import supported profiles and subscriptions with validation and clear feedback. |
| **Local diagnostics** | Review connection events and sanitized runtime guidance on the device. |
| **Responsive interface** | Designed for narrow phones, large displays, light mode and dark mode. |

## Latest release

### BaryoVPN 2.40.27 · Build 347

- Fixed bottom navigation overlap on edge-to-edge and narrow Android screens.
- Added consistent safe spacing across Home, Servers, Activity, Controls and Settings.
- Focused startup stability fix: saved profiles now finish restoring before the dashboard is shown.
- Removed the premature startup completion timeout that caused a brief incorrect screen.
- Added WebRTC Privacy Guard and continued connection-stability improvements.
- Preserved the existing navigation order, connection behavior and update flow.

[**View the full release and all downloads →**](https://github.com/BARYOPRO/BaryoVPN-Android/releases/tag/v2.40.27)

## Download

Choose the APK that matches your device. If you are unsure, use **Universal**.

| Device architecture | Download |
| --- | --- |
| ARM 64-bit · most modern phones | [arm64-v8a](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.40.27/BaryoVPN-2.40.27-Build347-arm64-v8a.apk) |
| ARM 32-bit · older phones | [armeabi-v7a](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.40.27/BaryoVPN-2.40.27-Build347-armeabi-v7a.apk) |
| Intel 32-bit | [x86](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.40.27/BaryoVPN-2.40.27-Build347-x86.apk) |
| Intel 64-bit | [x86_64](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.40.27/BaryoVPN-2.40.27-Build347-x86_64.apk) |
| Any supported architecture | [Universal](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.40.27/BaryoVPN-2.40.27-Build347-universal.apk) |

> Android will show its normal installation confirmation. BaryoVPN never installs APKs silently.

## Supported profile formats

Support depends on the fields supplied by the profile and the capabilities of the bundled core. Common formats include:

- VLESS, including common Reality and Vision fields
- VMess
- Trojan
- Hysteria2 (`hysteria2://` and `hy2://`)
- Shadowsocks and Outline dynamic access keys
- SOCKS5 and HTTP proxy profiles
- XHTTP transport profiles

Unsupported or incomplete data is reported instead of being silently treated as a working connection.

## Privacy and security

BaryoVPN keeps profiles, credentials and subscription URLs on the device using the app’s protected local storage paths. Diagnostic views are designed to avoid exposing secrets. WebRTC Privacy Guard strengthens routing and blocks known STUN/TURN probe paths while the VPN is active; Android and browser-level behavior can still vary by device and application.

For responsible security reports, read [SECURITY.md](SECURITY.md). Do not publish credentials, subscription URLs, UUIDs or private server details in an issue.

## Compatibility

- Android 7.0 and newer · minimum API 24
- Five release APK variants are provided for every release
- The app uses Android’s standard VPN permission and installer flows
- Vendor battery policies may require the user to allow background operation

## Getting help

- [Open an issue](https://github.com/BARYOPRO/BaryoVPN-Android/issues/new/choose)
- [Browse existing issues](https://github.com/BARYOPRO/BaryoVPN-Android/issues)
- [Read security guidance](SECURITY.md)
- [View release history](https://github.com/BARYOPRO/BaryoVPN-Android/releases)

When reporting a problem, include the app version, Android version, device model, selected architecture and a short reproduction path. Never include private configuration data.

<div align="center">
  <br />
  <strong>BaryoVPN</strong> · clear status · organized profiles · ready to connect
</div>
