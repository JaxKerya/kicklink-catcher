# Privacy Policy — KickLink Catcher

**Last updated:** February 12, 2026

## Overview

KickLink Catcher is a browser extension designed for Kick streamers and moderators. It collects and organizes links shared in the Kick Dashboard live chat. This privacy policy explains what data the extension accesses, how it is used, and how it is stored.

## Data Collection

KickLink Catcher does **not** collect, transmit, or share any personal data with external servers. All data processed by the extension remains entirely on your device.

### Data the extension accesses:

- **Chat messages on Kick Dashboard** — The extension reads chat messages on dashboard.kick.com to detect and extract URLs shared by viewers. Only the URL, the username of the sender, and the timestamp are extracted. Message content beyond URLs is not stored.

- **Page titles from linked URLs** — When you hover over a collected link, the extension may fetch the HTML page title from that URL to display a preview tooltip. This is a standard read-only HTTP request made directly from your browser. No data is sent to any intermediary server.

### Data the extension stores locally:

All of the following data is stored using `chrome.storage.local` on your device only:

| Data | Purpose | Retention |
|------|---------|-----------|
| Collected links (URL, username, timestamp) | Display in the Chat Links panel | Current session (cleared manually or on page reload) |
| Link history archives | Optional daily archive of collected links | Up to 1 year (auto-cleaned), or until manually cleared |
| Trusted domain list (whitelist) | Security classification of links | Until modified by user |
| Unsafe domain list (blacklist) | Security classification of links | Until modified by user |
| Language preference | UI language selection | Until modified by user |
| Link history toggle | Enable/disable link history feature | Until modified by user |
| Page title cache | Avoid re-fetching titles for previously seen URLs | Managed automatically (max 200 entries) |
| Update check timestamp | Track when the last version check occurred | Overwritten on each check |
| Latest version info | Notify user of available updates | Overwritten on each check |

## Data Sharing

KickLink Catcher does **not** share any data with third parties. No analytics, tracking, telemetry, or advertising services are used.

## Network Requests

The extension makes the following network requests:

1. **Page title fetching** — When a user hovers over a collected link, a GET request is made to the linked URL to retrieve the page title. This request goes directly from the user's browser to the destination website.

2. **Update check** — Once every 24 hours, the extension checks a public GitHub repository (https://raw.githubusercontent.com/JaxKerya/kicklink-catcher/refs/heads/main/version.json) to compare the installed version with the latest available version. Only the version number is read. No user data is sent in this request.

No other network requests are made by the extension.

## Permissions

| Permission | Reason |
|------------|--------|
| `storage` | Store user preferences, collected links, link history, and cache locally |
| `alarms` | Schedule periodic update checks (every 24 hours) |
| `activeTab` | Detect if the current tab is the Kick Dashboard to show status in the popup |
| `host_permissions (<all_urls>)` | Fetch page titles from arbitrary URLs shared in chat for link preview tooltips |

## Data Security

All data is stored locally using Chrome's built-in `chrome.storage.local` API. The extension does not use any external databases, cloud storage, or remote servers. Data never leaves your device except for the two network requests described above.

## User Control

- You can clear all collected links at any time using the "Clear Links" option.
- You can enable or disable the link history feature from the settings page.
- You can clear all link history at any time using the "Clear History" button.
- You can modify trusted and unsafe domain lists from the settings page.
- Uninstalling the extension removes all stored data.

## Children's Privacy

KickLink Catcher does not knowingly collect any data from children under the age of 13.

## Changes to This Policy

If this privacy policy is updated, the changes will be reflected in this document with an updated date. Continued use of the extension after changes constitutes acceptance of the updated policy.

## Contact

If you have any questions about this privacy policy, you can reach the developer at:

- GitHub: [github.com/JaxKerya](https://github.com/JaxKerya)
