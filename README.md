<div align="center">

# BaryoVPN

### A focused Android VPN experience built for clarity, control and calm

<p>
  <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest"><img src="https://img.shields.io/badge/Download-latest%20APK-635BFF?style=for-the-badge&logo=android&logoColor=white" alt="Download latest APK"></a>
  <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases"><img src="https://img.shields.io/github/downloads/BARYOPRO/BaryoVPN-Android/total?style=for-the-badge&color=0F766E" alt="Downloads"></a>
  <a href="https://github.com/BARYOPRO/BaryoVPN-Android/issues/new?template=bug_report.md"><img src="https://img.shields.io/badge/Report-a%20bug-E05D6F?style=for-the-badge" alt="Report a bug"></a>
</p>

<p>
  <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest">Get the latest release</a>
  · <a href="SECURITY.md">Security & privacy</a>
  · <a href="https://github.com/BARYOPRO/BaryoVPN-Android/issues">Community issues</a>
</p>

</div>

> [!CAUTION]
> **Attention: Update and install from the app**
>
> You can now check for updates, download the latest version, and start installation directly from BaryoVPN’s **Update Center**. Android will ask you to review and confirm the installation.

---

<div align="center">
  <img src="assets/baryovpn-hero.png" alt="BaryoVPN promotional product overview" width="720">
</div>

<p align="center"><sub>BaryoVPN product overview · clear status, privacy-minded design and live connection insights.</sub></p>

## The short version

BaryoVPN gives you a calmer way to work with Android VPN connections: a clear home dashboard, an organized server center, practical subscription tools and local connection activity in one focused app.

This repository is the **official public distribution hub** for BaryoVPN Android. It is intentionally separate from other projects and contains release materials for users—not application source code or private implementation details.

## What BaryoVPN includes

| Area | User-facing capability |
|---|---|
| **Home dashboard** | Protection state, selected server, latency, protocol, DNS mode and live download/upload traffic in one view. |
| **Server center** | Search, organize and select individual profiles or profiles imported from multiple subscription groups. |
| **Subscription tools** | Add, rename, copy, paste and refresh subscription links with clear update feedback. |
| **QR workflow** | Scan a supported subscription or configuration QR code and receive a green verification confirmation before continuing. |
| **Activity center** | Review connection state, session traffic and local diagnostic events without sending them to a public service. |
| **Large collections** | Designed to stay practical with substantial profile libraries through local organization and efficient updates. |
| **Battery-aware runtime** | Conservative background polling, traffic sampling and recovery behavior to reduce unnecessary CPU work while connected. |
| **Resilience options** | Connection profiles and safeguards designed for unstable or restrictive network conditions, while keeping certificate and leak-protection choices explicit. |

## Supported profile types

BaryoVPN can work with commonly used Xray-based profile formats, depending on the fields provided by the source and the capabilities of the bundled core:

- VLESS, including common Reality and Vision fields
- VMess
- Trojan
- Hysteria2 (`hysteria2://` and `hy2://`) with Xray v2 outbound mapping
- Shadowsocks
- Outline dynamic access keys (`ssconf://`), including prefix disguises
- SOCKS5 and HTTP proxy profiles
- XHTTP transport profiles

The app validates unsupported or incomplete data instead of silently treating it as a working connection. TUIC v5 is not included in the current bundled core; users should not expect a TUIC profile to connect in this release.

## Latest release · 2.38.6 / Build 306
[![Release](https://img.shields.io/github/v/release/BARYOPRO/BaryoVPN-Android?display_name=tag&sort=semver&style=flat-square&color=635BFF)](https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest)
> [!CAUTION]
> **IMPORTANT — PLEASE READ BEFORE INSTALLING:** Back up anything important before installing or updating BaryoVPN. Build 306 is a standalone Android **APK-only release**. No application source code or source archive is included.

### What’s new in 2.38.6
- **Predictable Adaptive Latency:** measures latency once when a VPN connection starts and does not repeat while that connection remains active.
- **No surprise checks:** returning to the app or changing the selected server no longer starts an automatic latency measurement.
- **Manual control retained:** users can still run a latency test from the server controls whenever they choose.
- **Distribution only:** this public repository publishes release APKs and documentation, not the app source.

### Previous 2.38.4 highlights
- **Responsive Start/Stop:** Native Start and Stop dispatch independently of the serialized latency-probe queue; Disconnecting remains visible until the native service confirms teardown.
- **Race-safe cleanup:** Stop closes the TUN descriptor immediately and performs blocking Xray/secure-store cleanup in the background. Lifecycle generation guards prevent stale recovery or scheduled callbacks from reconnecting after a manual Stop.
- **Start timeout recovery:** A timed-out native Start is invalidated and followed by a bounded cleanup request so a late completion cannot silently leave a tunnel active. DNA reconnect waits for native Stop completion.
- **Modern DNA quick actions:** The three-dot profile menu is now an in-app dialog that closes on outside tap, Android Back or the close control.

### Recent 2.37 updates
- **2.37.3 / Build 299:** Update Center refreshes device ABI information when checking for updates. If the ABI cannot be confirmed, automatic APK selection stops instead of falling back to Universal.
- **2.37.2 / Build 298:** Update Center reads the installed version and build from application metadata, uses cache-busting for GitHub release checks and improves the NEW badge lifecycle.
- **2.37.1 / Build 297:** Version-aware NEW badges help users discover newly introduced settings, including Adaptive Latency.
- **2.37.0 / Build 296:** Adaptive Latency can refresh latency after a successful connection, a connected server change or a return from the background, without a background timer.

See the [2.38.6 release notes](https://github.com/BARYOPRO/BaryoVPN-Android/releases/tag/v2.38.6) for this build and the [release history](https://github.com/BARYOPRO/BaryoVPN-Android/releases) for earlier versions. The public repository remains distribution-only and does not contain application source code.

### Included in 2.36.0 Build 295
- Removed the experimental Fastest Connect flow; the dashboard keeps manual server selection and connection.
- Reduced idle native status polling while preserving responsive updates during active VPN sessions.
- Optimized dashboard log processing and improved Update Center reliability.
- Preserved the existing manual Connect flow, secure profile storage, Xray v26.10.31 engine, QR scanner, Midnight Aurora theme and ABI-aware installer.

### Included in 2.31.6 Build 286
- Fixed the in-app APK update handoff.
- The downloaded APK is now opened with Android’s native Package Installer using the correct APK MIME type and secure read permission.
- The user still confirms the installation in Android; BaryoVPN never installs silently.
- Added a clear error when Android cannot find an APK installer for the downloaded file.
- Kept Midnight Aurora, exact ABI and size detection, QR scanning improvements and all existing VPN flows.
- Published one Universal APK plus four architecture-specific APKs.
- The public distribution repository remains source-free by design.

### Included from 2.30.3
- Removed the post-splash blank/white flash by rendering the first app screen underneath the startup overlay before the transition completes.
- Kept the professional three-second branded startup while making the handoff to the dashboard continuous and non-blocking.
- Reduced startup storage work by removing a duplicated subscription snapshot read during bootstrap.
- Matched the native Android startup window to the light and dark application palettes instead of a hard-coded white background.
- Added Android deep-link handling for `hysteria2://` and `hy2://`.

### Included from 2.30.2
- Added native Hysteria2 import support for single `hysteria2://` and `hy2://` links.
- Hysteria2 profiles are converted to the bundled Xray v2 outbound with TLS, SNI and authentication preserved.
- Added Hysteria2 support to subscription parsing, profile inspection and standard share export.
- Legacy Hysteria2 `insecure=1` metadata is migrated through the current certificate verification path; deprecated `allowInsecure` is not emitted in the final Xray configuration.
- Added regression tests for manual import, subscription import, Xray JSON conversion and round-trip export.
- Version metadata is synchronized at 2.30.2 / Android build 271.
- The public repository remains distribution-only and contains no application source code.

### Included from 2.30.1
- Advanced TLS verification settings in the profile editor: Strict, Verify by name (VCN), Certificate pinning (PCS) and Legacy compatibility.
- Legacy `allowInsecure` is migrated at runtime and is never passed to the current Xray schema.
- Certificate pins are validated as SHA-256 fingerprints before a profile can be saved.
- Added regression coverage for the new TLS modes; the full suite passes with 190 tests.
- Version metadata is synchronized at 2.30.1 / Android build 270.
- Reliable Stop action from the foreground notification across Android versions and vendor ROMs.
- Immediate removal of the foreground notification after stopping from inside the app.
- Xray and VPN TUN teardown no longer wait behind a blocked startup task.
- Immediate Connecting feedback while network, permission and configuration checks continue.
- Clear Error state when startup validation fails instead of leaving the app stuck on Connecting.
- Existing encrypted `.baryovpn` transfer, DNS, profile and subscription features are preserved.
### Download the latest release
<p align="center">
  <a href="https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest">
    <img src="https://img.shields.io/badge/Download%20BaryoVPN-latest%20release-635BFF?style=for-the-badge&logo=android&logoColor=white" alt="Download the latest BaryoVPN release" />
  </a>
</p>
Open the [latest release page](https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest) for current downloads. The links below point specifically to **2.38.6 / Build 306**:

- [Universal — all four supported architectures](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.38.6/BaryoVPN-2.38.6-universal-Build306.apk)
- [arm64-v8a — modern 64-bit ARM phones](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.38.6/BaryoVPN-2.38.6-arm64-v8a-Build306.apk)
- [armeabi-v7a — older 32-bit ARM phones](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.38.6/BaryoVPN-2.38.6-armeabi-v7a-Build306.apk)
- [x86 — 32-bit Intel devices/emulators](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.38.6/BaryoVPN-2.38.6-x86-Build306.apk)
- [x86_64 — 64-bit Intel devices/emulators](https://github.com/BARYOPRO/BaryoVPN-Android/releases/download/v2.38.6/BaryoVPN-2.38.6-x86_64-Build306.apk)

For a manual download, choose the Universal APK or the package matching your device architecture. The in-app updater uses ABI detection and selects the matching architecture-specific APK; if it cannot confirm the device ABI, it stops automatic selection. Download APKs only from the official release page and choose the package matching your device architecture.

## Install in a few steps

1. Open the [latest release](https://github.com/BARYOPRO/BaryoVPN-Android/releases/latest).
2. Download the Universal APK asset, or choose the matching architecture-specific APK above.
3. If Android asks, allow installation from your browser or file manager.
4. Install and open BaryoVPN.
5. Add a subscription or import a supported profile with the in-app tools.

> Download only from this repository or another source you explicitly trust. Android may show a standard warning for an APK installed outside Google Play.

## Why is the APK large?

The 2.38.5 Build 305 Universal APK is approximately **214.5 MiB** because it is a **standalone universal APK**, not a small development shell. It packages everything needed for a direct installation:

- the Android and React Native runtime;
- the complete user interface bundle and application resources;
- the bundled native connection engine;
- native binaries and compatibility data for multiple Android CPU architectures;
- the visual assets required for the complete app experience.

A universal APK is intentionally larger than architecture-specific split packages, but it is simpler for users: one download works across a wider range of Android devices and does not require Metro, a desktop computer or a separate runtime download.

The size is a distribution trade-off. It does **not** mean the app is silently bundling private subscriptions or uploading user data. GitHub Release assets are used because they support large APKs cleanly while keeping version history and download links organized.

## Ownership and permitted use

> [!CAUTION]
> **Ownership notice:** BaryoVPN is an original software product created and maintained by **Ehsan Farzian**.
>
> **Copyright © 2026 Ehsan Farzian. All rights reserved.**
>
> The BaryoVPN name, branding, visual design, user interface, product concept, application builds and related materials are protected intellectual property. Copying, reproducing, modifying, forking, repackaging, decompiling, redistributing, publishing, mirroring, sublicensing, selling or using any part of BaryoVPN for commercial or competing purposes without prior explicit written authorization is prohibited.
>
> Downloading or installing a public APK does not transfer ownership, grant a license to the application, or authorize redistribution. Any authorized use must preserve the original attribution and comply with written terms from the copyright holder.

## Privacy and public reporting

BaryoVPN's public distribution repository does not contain application source code, prebuilt application-source packages, private implementation reports or user subscription data. GitHub-generated repository snapshots contain only the public documentation and distribution assets, not the app implementation. Please do not post subscription URLs, access tokens, credentials, UUIDs, private keys, raw configuration files or personal data in public issues. Read [SECURITY.md](SECURITY.md) before reporting anything that may be private.

## Release timeline

| Version | Highlights |
|---|---|
| **2.38.6 Build 306** | Predictable connection-start Adaptive Latency with no repeated automatic checks
| **2.38.5 Build 305** | Responsive VPN lifecycle, refined DNA dialogs and modern dashboard with reduced-motion support |
| **2.38.4 Build 304** | Responsive Start/Stop, stale-reconnect fencing and modern DNA quick actions |
| **2.38.3 Build 303** | Modern, centered DNA dialogs and reliable outside-tap dismissal |
| **2.38.2 Build 302** | Responsive Disconnect; immediate TUN closure and non-blocking native teardown |
| **2.38.1 Build 301** | Baryo DNA / Mode Studio, encrypted local-profile transfer; supported settings only |
| **2.38.0 Build 300** | Virtualized App Routing list, no fixed app cutoff and precomputed search keys |
| **2.37.3 Build 299** | ABI refresh and safer automatic APK selection in Update Center |
| **2.37.2 Build 298** | Installed-version accuracy, release-check cache handling and NEW badge fixes |
| **2.37.1 Build 297** | Version-aware NEW badges and Adaptive Latency discovery |
| **2.37.0 Build 296** | Event-driven Adaptive Latency without a background timer |
| **2.36.0 Build 295** | Manual connection flow, reduced idle work and dashboard performance improvements |
| **2.35.0 Build 294** | Introduced experimental Fastest Connect, later removed in 2.36.0 |
| **2.34.0 Build 293** | About-page version accuracy and release-aware update information |
| **2.33.0 Build 292** | Distinct Midnight Aurora palette and Android update notifications |
| **2.32.1 Build 291** | Midnight Aurora refinement and live theme swatches |
| **2.32.0 Build 290** | Plain dark startup and improved APK installer handoff |
| **2.31.9 Build 289** | Animated native Baryo launch logo with AndroidX SplashScreen compatibility; removed in 2.32.0 |
| **2.31.6 Build 286** | Native Android APK installer handoff with correct MIME and secure read permission |
| **2.31.5 Build 285** | Midnight Aurora theme, invalid accent fallback protection and the verified ABI-aware Update Center |
| **2.31.4 Build 284** | Exact installed APK ABI and size detection, architecture-aware update selection and verified single-ABI packages |
| **2.31.3 Build 283** | Modern Update Center, release checking, APK security details, real download progress and user-controlled installation |
| **2.31.2 Build 282** | QR scanning reliability, zoom and torch controls, camera error feedback, standalone release APKs for Universal plus four Android architectures |
| **2.31.1 Build 281** | Connection recovery, Stop/close stability fixes, standalone release APKs for Universal plus four Android architectures |
| **2.31.0 Build 280** | Patched Xray-core v26.10.31, standalone release APKs for Universal plus four Android ABIs, updated About metadata and SHA-256 manifests |
| **2.30.4 Build 279** | Exact rollback to the known-good native APK packaging and Universal manifest baseline |
| **2.30.3** | Smooth startup handoff, no post-splash white flash, reduced bootstrap work and universal release build 272 |
| **2.30.2** | Hysteria2 import/export support, Xray v2 mapping and universal release build 271 |
| **2.30.1** | Advanced TLS verification UI, PCS/VCN migration and universal release build 270 |
| **2.30.0** | Reliable notification/app Stop handling, faster startup feedback and safer VPN lifecycle teardown |
| **2.29.1** | Optional `.baryovpn` passwords, immediate import refresh and responsive empty-state actions |
| **2.28.14** | Outline dynamic keys and prefix support, plus clearer connection diagnostics |
| **2.28.8** | Bug Fix release with stability and connection improvements |
| **2.28.7** | QR success confirmation with BaryoVPN logo and green verification check |
| **2.28.6** | Subscription Center redesign with copy, paste, QR, smart naming and HTTPS preview |
| **2.28.5** | Security hardening release and safer diagnostics |

<div align="center">

---

**BaryoVPN** · clear status · organized profiles · ready to connect

</div>
