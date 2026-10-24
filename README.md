# Kite for Windows (test builds)

Kite is a private, no-nonsense web browser for Windows. Under the hood it is Firefox, set up the way Leeam wants it: no telemetry, no Firefox account, no sponsored anything, tracking protection on strict, and uBlock Origin and a cookie-banner blocker built in. It is an early test build, so expect rough edges. Thank you for trying it.

## Install

1. Download **[KitePC-win-Setup.exe](https://github.com/ElecTream/kite-pc-releases/releases/latest/download/KitePC-win-Setup.exe)**.
2. Run it. Windows will say it protected your PC because the app is not signed yet. Click **More info**, then **Run anyway**. You only do this once.
3. Kite installs for your account (no admin needed). The first time it opens it shows "Getting Firefox ESR from Mozilla" with a progress bar for about a minute. After that the browser opens.

**If Windows won't let you run it at all:** Smart App Control blocks unsigned apps and has to be off. Check at Settings > Privacy & security > Windows Security > App & browser control > Smart App Control. (Turning it off can't be undone without reinstalling Windows, so only do it if you are happy with that.) A work PC may also refuse unsigned apps; that one is up to your IT.

Kite updates itself. A new version downloads quietly and starts the next time you open Kite. The Kite page (Firefox menu > Kite) says "Restart to update" when one is waiting.

## What to expect

- It looks like Kite (indigo, square corners), but Firefox's own inner pages, such as settings and the private new tab, still look like Firefox.
- The default search is Brave Search.
- Proton Pass is installed. It opens its own welcome page once. You can turn it off in Add-ons.
- Sites that need DRM (Netflix, Spotify and the like) don't play yet.
- Pages on a bare tailnet or home-network address (like 192.168.x.x) may ask whether the page can reach your local network.

## What Kite never sends

No telemetry, no crash reports, no Firefox or Mozilla accounts, no sync, no studies, no sponsored content, no search suggestions, no Safe Browsing lookups, no captive-portal checks. DNS-over-HTTPS is off, so your DNS stays with Windows. Kite itself only talks to Mozilla (to get and update the browser engine, once a day at most) and to this GitHub repo (to update Kite). Extensions you install yourself make their own connections, and Proton Pass talks to Proton.

## Something broke?

1. Open the Kite page (Firefox menu > Kite) and press **Copy diagnostics**.
2. Open a new issue in this repo and paste it in, with a sentence about what you did and what happened.

The diagnostics are versions, a check of Kite's settings and the last update events. They never contain the addresses, titles or searches of pages you visited.

## Send log (optional)

The Kite page also has **Send log**. It only does anything when you press it, and first shows you exactly what will be sent. The log is scrubbed of web addresses, page titles and searches. It goes to a small server Leeam runs at home, reached over HTTPS, and is kept until Leeam deletes it. You get an upload id to quote in your issue.

## Uninstall

Settings > Apps > Installed apps > Kite > Uninstall. Your browsing data stays in `%LOCALAPPDATA%\com.electream.kitepc`; delete that folder too if you want it gone.
