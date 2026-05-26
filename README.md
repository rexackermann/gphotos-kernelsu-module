# Google Photos Autobuild Magisk & KernelSU Module
[![CI Badge](https://github.com/rexackermann/gphotos-kernelsu-module/actions/workflows/ci.yml/badge.svg?event=schedule)](https://github.com/rexackermann/gphotos-kernelsu-module/actions/workflows/ci.yml)
[![CI Release](https://img.shields.io/github/v/release/rexackermann/gphotos-kernelsu-module?style=flat-square&color=blue)](https://github.com/rexackermann/gphotos-kernelsu-module/releases)

Automated daily builder for **Google Photos** using [**RookieEnough/De-Vanced**](https://github.com/RookieEnough/De-Vanced) patches.

This repository compiles both non-root APKs and flashable Magisk/KernelSU modules to spoof Pixel-exclusive features (such as **unlimited original-quality photo & video storage**) on any Android device.

---

## Features

- **Unlimited Storage Spoofing**: Automatically includes the `Spoof features` patch to spoof a Google Pixel XL device.
- **Account Persistence Fix**: Includes the `Fix selected account persistence` patch to keep you signed in on non-rooted configurations running microG/GmsCore.
- **Dual Formats**: Builds both:
  - **Flashable Magisk / KernelSU Modules** (for rooted devices)
  - **Patched APKs** (for non-rooted devices)
- **Automated Updates**: Scheduled via GitHub Actions to run every day. It checks for new De-Vanced patches releases, compiles if there is an update, and publishes a new release automatically.
- **Size Optimization**: Optimizes resources, strip-libs, and compiles classes for speed and size.

---

## Downloads

Grab the latest compiled modules and APKs from the [**Releases**](https://github.com/rexackermann/gphotos-kernelsu-module/releases) section.

---

## Local Building

### Prerequisites
Make sure you have `java` (OpenJDK 17 or newer), `jq`, and `zip` installed.

### Build Command
1. Clone the repository:
   ```bash
   git clone https://github.com/rexackermann/gphotos-kernelsu-module.git
   cd gphotos-kernelsu-module
   ```
2. Run the build script:
   ```bash
   ./build.sh config.toml
   ```
The compiled modules and APKs will be saved in the `build/` directory.

---

## Credits

- [RookieEnough/De-Vanced](https://github.com/RookieEnough/De-Vanced) - For the amazing Google Photos spoofing and compatibility patches.
- [kmdtaufik/morphe-magisk-module](https://github.com/kmdtaufik/morphe-magisk-module) - The original automated builder base.
- [MorpheApp](https://github.com/MorpheApp) - For the underlying patching framework and CLI engine.
