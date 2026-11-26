<div align="center">
  <img src="assets/baryovpn-hero.png" alt="BaryoVPN — a clear, private and reliable Android VPN experience" width="820" />

  <h1>BaryoVPN for Android</h1>
  <p><strong>Connect with clarity. Manage profiles with confidence.</strong></p>
  <p>Organized server profiles · Live connection insight · Privacy-minded controls</p>

  <p>
    <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest"><img src="https://img.shields.io/github/v/release/BARYOPRO/BaryoVPN-Android?display_name=tag&style=for-the-badge&logo=android&logoColor=white&label=Latest%20release&color=2563EB" alt="Latest release" /></a>
    <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases"><img src="https://img.shields.io/github/downloads/BARYOPRO/BaryoVPN-Android/total?style=for-the-badge&logo=github&logoColor=white&label=Downloads&color=0F766E" alt="Total downloads" /></a>
    <a href="https://github.com/BARYOPRO/BaryoVPN-Android/issues/new?template=bug_report.md"><img src="https://img.shields.io/badge/Report%20a%20bug-DC2626?style=for-the-badge&logo=github&logoColor=white" alt="Report a bug" /></a>
  </p>
</div>

> [!IMPORTANT]
> This repository is the official **APK-only distribution hub** for BaryoVPN Android. It intentionally does not contain application source code, signing keys, private configuration, subscription URLs or server information.

## Start here

BaryoVPN is built for people who want a VPN app that explains what is happening instead of hiding it behind a single switch. Add a profile or subscription, choose a route, review the connection state and keep useful diagnostics close at hand.

**[Download the latest release](https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest)** · **[See all releases](https://github.com/BARYOPRO/BaryoVPN-Android/releases)** · **[Report a problem](https://github.com/BARYOPRO/BaryoVPN-Android/issues/new/choose)**

## Latest release: 2.43.9 · Build 396

The latest release focuses on a faster, lighter everyday experience:

- Smoother switching between tabs and settings sections.
- Fewer unnecessary screen updates while live traffic changes.
- Faster-feeling Servers, Proxy, Privacy, Hotspot and diagnostics screens.
- Live traffic and activity information remain available where they matter.
- The same signing certificate as previous releases.

### Choose your APK

If you are not sure which file to install, choose **Universal**. For the smallest download on a modern Android phone, choose **arm64-v8a**.

| Device | Recommended download |
| --- | --- |
| Most modern Android phones | [arm64-v8a](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.43.9/BaryoVPN-2.43.9-Build396-arm64-v8a.apk) |
| Older 32-bit ARM phones | [armeabi-v7a](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.43.9/BaryoVPN-2.43.9-Build396-armeabi-v7a.apk) |
| Intel 32-bit devices or emulators | [x86](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.43.9/BaryoVPN-2.43.9-Build396-x86.apk) |
| Intel 64-bit devices or emulators | [x86_64](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.43.9/BaryoVPN-2.43.9-Build396-x86_64.apk) |
| Unsure of your architecture | [Universal](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.43.9/BaryoVPN-2.43.9-Build396-universal.apk) |

> Android will show its normal installer confirmation. BaryoVPN never installs APKs silently.

## The BaryoVPN experience

| Area | Designed for |
| --- | --- |
| **Home dashboard** | See protection state, selected profile, latency, protocol, DNS mode and live traffic in one calm view. |
| **Server center** | Search, select, test and organize individual profiles or complete subscription groups. |
| **Privacy controls** | Tune DNS, IPv6 protection, app coverage, kill switch behavior and Ghost Mode. |
| **Subscriptions and QR** | Import supported links and subscription sources with validation and clear feedback. |
| **Local diagnostics** | Review connection events and sanitized runtime guidance directly on the device. |
| **Proxy and hotspot** | Use local proxy endpoints and inspect gateway activity when those modes are enabled. |
| **Responsive interface** | Enjoy a consistent layout across small phones, larger screens, light mode and dark mode. |

## Supported profile formats

Support depends on the fields supplied by a profile and the capabilities of the bundled core. Common formats include:

- VLESS, including common Reality and Vision fields
- VMess
- Trojan
- Hysteria2 (`hysteria2://` and `hy2://`)
- Shadowsocks and Outline dynamic access keys
- SOCKS5 and HTTP proxy profiles
- XHTTP transport profiles

Incomplete or invalid data is reported instead of being silently treated as a working connection.

## Privacy by design

BaryoVPN keeps profiles, credentials and subscription URLs in protected local storage paths on the device. Diagnostic views are designed to avoid exposing secrets, and the public repository does not contain private server data or signing material.

WebRTC Privacy Guard strengthens routing and blocks known STUN/TURN probe paths while the VPN is active. Android and browser behavior can vary by device and application, so no privacy feature should be treated as a guarantee against every environment.

For responsible security reports, read [SECURITY.md](SECURITY.md). Never publish credentials, subscription URLs, UUIDs or private server details in an issue.

## Compatibility

- Android 7.0 and newer (minimum API 24)
- Five architecture-aware APK variants in every release
- Android's standard VPN permission and installer flows
- Some manufacturers require battery-optimization exemptions for reliable background operation

## Help and feedback

- [Report a reproducible bug](https://github.com/BARYOPRO/BaryoVPN-Android/issues/new?template=bug_report.md)
- [Suggest an improvement](https://github.com/BARYOPRO/BaryoVPN-Android/issues/new?template=feature_request.md)
- [Browse open issues](https://github.com/BARYOPRO/BaryoVPN-Android/issues)
- [Read the security policy](SECURITY.md)
- [Browse release history](https://github.com/BARYOPRO/BaryoVPN-Android/releases)

When opening an issue, include the app version, Android version, device model, selected APK architecture and a short reproduction path. Remove private configuration data before posting.

<div align="center">
  <br />
  <strong>BaryoVPN</strong> · clear status · organized profiles · ready to connect
  <br />
  <sub>Official Android APK distribution · Source and signing material are intentionally kept private</sub>
</div>
