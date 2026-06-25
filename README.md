# Morphe Patched Builds

Automated CI/CD pipeline for building Morphe-patched YouTube and YouTube Music applications using GitHub Actions.

## Overview
This repository utilizes GitHub Actions to automatically fetch, patch, and release the latest versions of YouTube and YouTube Music using [Morphe Patches](https://github.com/MorpheApp). It generates both standard APKs for non-root devices and Magisk modules for rooted environments.

## Features
- **Automated Nightly Builds**: Monitors upstream patches daily and triggers builds automatically.
- **Multi-Architecture Support**: Generates separate `arm64-v8a` and `armeabi-v7a` optimized APKs.
- **Magisk Integration**: Outputs direct flashable `.zip` modules for root users.
- **Dynamic Source Fetching**: Automatically extracts the latest untouched, `nodpi` APKs from secure archives.

## Workflow Setup
1. **Fork** this repository (Keeping the fork private is highly recommended).
2. Navigate to **Settings > Actions > General > Workflow permissions** and select `Read and write permissions`.
3. Go to the **Actions** tab, click on `Build Morphe APKs and Magisk Modules`, and manually trigger the workflow via **Run workflow**.
4. Retrieve your compiled assets from the **Releases** page upon completion.

## Output Artifacts
| Application | Architecture | Type | Target |
| :--- | :--- | :---: | :--- |
| **YouTube** | arm64-v8a / armeabi-v7a | APK | Non-Root |
| **YouTube** | Universal | ZIP | Root (Magisk) |
| **YT Music** | arm64-v8a / armeabi-v7a | APK | Non-Root |
| **YT Music** | Universal | ZIP | Root (Magisk) |

## Dependencies
- **Non-Root**: [MicroG-RE](https://github.com/WSTxda/MicroG-RE) is required for Google account authentication.
- **Root**: [Zygisk-Detach](https://github.com/j-hc/zygisk-detach) is recommended to prevent unintended Play Store updates.

## Credits & Acknowledgments
- [MorpheApp](https://github.com/MorpheApp) - Core CLI, Patches, and Integrations
- [j-hc](https://github.com/j-hc) - APK Archiving & Zygisk-Detach Module
- [WSTxda](https://github.com/WSTxda) - MicroG-RE
- [topjohnwu](https://github.com/topjohnwu) - Magisk Framework

---
*Disclaimer: This repository is intended for personal, educational, and automated testing purposes only. No proprietary or modified APKs are hosted directly in this repository.*
