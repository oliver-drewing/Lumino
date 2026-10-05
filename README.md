# Lumino

**A minimal night-light app for Android** (iOS prepared). Turns your screen into a soft, adjustable light source — quick to start, easy on the eyes in the dark.

Status: **first Play Store release in preparation**

> **Showcase repository.** The source code is private. This page describes what the app does and how it is built.

<!-- SCREENSHOTS: add images to /screenshots and uncomment
<p align="center">
  <img src="screenshots/presets.png" width="220" alt="Preset grid">
  <img src="screenshots/color-picker.png" width="220" alt="Color picker">
  <img src="screenshots/fullscreen-clock.png" width="220" alt="Fullscreen light with clock">
</p>
-->

## Features

- **Presets** for different moods, with optional auto-start of a favourite preset
- **Custom colors** via a dedicated color picker (hue, saturation, numeric input)
- **Screen brightness control** through the platform APIs, with a clear permission flow on Android
- **Fullscreen mode** with an optional clock overlay that keeps contrast readable on any color
- **Backup:** export and import presets as JSON

## Architecture

- **Kotlin Multiplatform** — UI, components, repositories and models live in `commonMain`
- Platform features (brightness, fullscreen, keep-screen-on, file sharing) via `expect`/`actual`
- **Compose Multiplatform** UI, **Decompose** for navigation, **Koin** for dependency injection
- **kotlinx.serialization** for persistence and backups
- Versioning derived from Git tags (SemVer)

## Tech stack

Kotlin · Kotlin Multiplatform · Compose Multiplatform · Decompose · Koin · Coroutines/StateFlow · kotlinx.serialization · kotlinx-datetime

## Quality

Unit tests for components, repositories, navigation, persistence and backup import/export.

---

Built by [Oliver Drewing](https://drewing.dev) · Android & Product Engineer
