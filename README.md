# Aegis Browser — Flatpak

Aegis Browser is an experimental Linux web browser focused on privacy, security, and transparency. It is built with GTK and WebKitGTK. The browser prefers HTTPS connections, asks for confirmation before downloading files, and does not send telemetry.

This repository contains the Flatpak packaging files for Aegis Browser. The application source code is maintained separately in the [Aegis Browser repository](https://github.com/n8nfelipe/aegis-browser).

## Demo

[Watch the Aegis Browser video](aegis-browser.mp4).

## Packaging

The Flatpak manifest is `io.github.n8nfelipe.aegis-browser.yml`. It builds the `aegis-browser-webkit` Cargo package against the GNOME 50 runtime and SDK. Rust dependencies are vendored and pinned in `cargo-sources.json`, allowing Cargo to build offline inside the Flatpak build environment.

The package includes the desktop entry, application metadata, icons, and the Aegis privacy and tracker-blocking extensions.

## Permissions

The sandbox grants network access for browsing, Wayland and fallback X11 display access, GPU and audio access, desktop notifications, and access to the user's Downloads folder.

## Project details

- **Application ID:** `io.github.n8nfelipe.aegis-browser`
- **Current metadata version:** `0.1.0`
- **License:** Apache-2.0 OR MIT
- **Homepage:** [github.com/n8nfelipe/aegis-browser](https://github.com/n8nfelipe/aegis-browser)
