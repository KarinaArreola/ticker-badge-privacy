---
title: Ticker Badge Privacy Policy
---

# Ticker Badge Privacy Policy

**Effective date:** October 23, 2026

Ticker Badge is a Chrome extension that shows the stock ticker and price of the publicly traded company behind the website you're visiting. This policy explains what information the extension handles. In short: **Ticker Badge does not collect, sell or share your personal data. It has no accounts, no analytics and no tracking.**

## What the extension reads

- **The address of the site you're on (hostname only, e.g. `nike.com`).** Used on your device to check whether the site belongs to a listed company in the extension's built-in list. It is not stored and is not sent anywhere.
- **The visible text of fund-company websites only** (for example capitalgroup.com). Used on your device to work out which of that company's own ETFs the page is about. It is not stored and is not sent anywhere. Page text is not read on any other website.

The extension does not read your browsing history, form inputs, passwords, cookies or the full addresses (paths or query strings) of the pages you visit.

## What the extension stores

Everything is stored **only in your browser**, using Chrome's extension storage:

| Data | Where | How long |
|---|---|---|
| Your Finnhub and (optional) Twelve Data API keys | `chrome.storage.local` | Until you remove them in the extension's settings or uninstall the extension |
| Your settings: on/off for all sites, sites you've turned it off for | `chrome.storage.local` | Until you change them or uninstall |
| The badge's position and size | `chrome.storage.local` | Until you change them or uninstall |
| Recently fetched prices, market status and charts (a cache, to stay within the providers' rate limits) | `chrome.storage.session` (memory only) | Cleared when Chrome closes |

Ticker Badge does not use Chrome sync, so none of this is copied to your Google account or other devices.

## What the extension sends, and to whom

To show prices, the extension's background service contacts two market-data providers using **your own API keys**:

| Provider | What is sent | Why |
|---|---|---|
| [Finnhub](https://finnhub.io) (`finnhub.io`) | A ticker symbol (e.g. `NKE`) and your Finnhub API key | Price, market status and market cap |
| [Twelve Data](https://twelvedata.com) (`api.twelvedata.com`), only if you added a key | A ticker symbol and your Twelve Data API key | The intraday chart |

Only ticker symbols from the extension's built-in list are ever requested. **Page addresses, page text and your browsing history are never sent.** Requests are made without cookies and without a referrer. Like any web request, they reveal your IP address to the provider. Their handling of that is covered by their own privacy policies: [Finnhub](https://finnhub.io/privacy) and [Twelve Data](https://twelvedata.com/privacy).

If you click **Full quote on Google Finance**, that page opens in a new tab like any other link you choose to follow, and Google's [privacy policy](https://policies.google.com/privacy) applies there. Nothing is sent to Google unless you click it.

## What the extension does not do

- No analytics, telemetry, crash reporting or advertising
- No selling, renting or sharing of any data
- No remote code: everything the extension runs is included in the published package
- No use of data for creditworthiness, lending or any purpose other than showing stock information

## Chrome Web Store User Data Policy

The use of information received by Ticker Badge adheres to the [Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq), including the Limited Use requirements.

## Your choices

- Turn the badge off for one site or for all sites from the extension's toolbar popup.
- Remove your API keys in the extension's settings (Extension options).
- Uninstall the extension from `chrome://extensions`. This deletes everything it stored.

## Children

Ticker Badge is not directed at children under 13 and does not knowingly collect information from anyone.

## Changes

If this policy changes, the updated version will be posted at this address with a new effective date. Material changes will also be noted in the extension's release notes.

## Contact

Questions or concerns about this policy: please [open an issue](https://github.com/KarinaArreola/ticker-badge-privacy/issues) on this policy's GitHub page. Don't include API keys or other personal information in issues; they are public.
