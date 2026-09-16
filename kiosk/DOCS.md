# casasmooth Kiosk Add-on Documentation

> **Note**: this file is the source of truth. The copy at
> `casasmooth-addon/kiosk/DOCS.md` is synchronised by the
> `build_addon.yml` GitHub Actions workflow on every release. Edit
> here, not there.

## Overview

This add-on turns a screen connected to your Home Assistant box into a
wall-mounted display: a Chromium browser, in kiosk mode, showing the
home screen of your casasmooth mobile app — with no login. It requires
the main **casasmooth** add-on to be installed and running.

## Installation

It is installed automatically by the main casasmooth add-on when it
detects a DRM/GPU device on the box (`cs_provision_kiosk.py`, part of
`cs_update`) — you do not need to install it by hand. It is a no-op,
near-zero-CPU wait when no screen is connected: it stays installed and
quietly polls for a display to appear.

## What it shows

The screen shows the box's own mobile app home, in a dedicated,
credential-less mode (`?context=kiosk`): live sensor readouts and
simple on/off controls, never account settings, energy, security, or
anything requiring a login.

## Requirements

- A screen connected via HDMI or a supported DSI panel.
- Nothing else to configure — the `kiosk_url` option defaults to the
  correct value and should be left alone.

## Support

- Repository: <https://github.com/teleia/casasmooth-addon>
- Issues: <https://github.com/teleia/casasmooth-addon/issues>
