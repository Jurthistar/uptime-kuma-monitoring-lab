# Screenshot Guide

Take these only after the corresponding feature works. Use PNG images and place them in `docs/screenshots/` with the exact filenames below.

## Before every capture

- Blur or crop usernames, email addresses, webhook URLs, browser bookmarks, IP addresses, and local hostnames.
- Do not show passwords, API tokens, QR codes, or the Uptime Kuma administrator settings page.
- Use your browser's zoom controls if needed so the relevant part is legible.
- Capture only the application/window needed; avoid a full desktop image.

## Required screenshots

### `01-dashboard-overview.png`

**Capture:** Uptime Kuma's main dashboard showing two or three healthy public monitors and their response-time graph or status.

**Purpose:** Demonstrates the finished monitoring dashboard. It should be the first image visitors see in the README.

### `02-monitor-configuration.png`

**Capture:** The configuration screen for one safe public HTTP(S) monitor, such as `https://github.com`.

**Purpose:** Proves your configuration work. Crop out notification credentials, description fields with personal details, and private URLs.

### `03-alert-test.png`

**Capture:** A combined image showing the monitor in a Down state plus the failure/recovery notification. You may combine two cropped images side-by-side using any image editor.

**Purpose:** Shows that alerting was tested end to end.

### `04-status-page.png`

**Capture:** The finished public status page with only safe public monitors.

**Purpose:** Demonstrates stakeholder-facing operational communication.

### `05-pm2-status.png`

**Capture:** A PowerShell window after running `pm2 status`, with `uptime-kuma` shown as online.

**Purpose:** Demonstrates that the monitoring service is managed as a persistent background process.

## Add images to the README

The README already references the first and third images. To include another image, use this format:

```markdown
![Public status page](docs/screenshots/04-status-page.png)
```

Keep each image near the section it supports rather than placing all images at the end.

