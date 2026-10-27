# Kite for Windows (test builds)

Kite is a private, no-nonsense web browser for Windows. Under the hood it is Firefox, set up the way Leeam wants it: no telemetry, no Firefox account, no sponsored anything, tracking protection on strict, and uBlock Origin and a cookie-banner blocker built in. It is an early test build, so expect rough edges. Thank you for trying it.

## Install

1. Download **[Kite-Setup.exe](https://github.com/ElecTream/kite-pc-releases/releases/latest/download/Kite-Setup.exe)** from the latest release, and run it.
2. Windows will say it protected your PC because the app is not signed yet. Click **More info**, then **Run anyway**. You only do this once.
3. Kite Setup walks you through it: **Next**, then pick whether Kite starts when setup finishes and whether to open Windows' default-apps page to make Kite your browser, then **Install**. It installs for your account only (no admin needed) and takes a moment.
4. Press **Finish**. The first time Kite opens it shows "Getting Firefox ESR from Mozilla" with a progress bar for about a minute. After that the browser opens. Later, start it from the Start menu: **Kite**.

Already have Kite? Running Kite Setup again updates it to that release. (The release also holds `KitePC-win-Setup.exe`, the plain installer Kite Setup runs for you; Kite's own updates come from it.)

**If Windows won't let you run it at all:** Smart App Control blocks unsigned apps and has to be off. Check at Settings > Privacy & security > Windows Security > App & browser control > Smart App Control. (Turning it off can't be undone without reinstalling Windows, so only do it if you are happy with that.) A work PC may also refuse unsigned apps; that one is up to your IT.

Kite updates itself. A new version downloads quietly and starts the next time you open Kite. When one is waiting, an **Update ready** card appears in the sidebar above the dock: **Restart** installs it now and keeps your tabs, **Later** hides the card until a newer version is ready (the gear keeps a small dot, and Preferences > About still has **Restart to update**).

## What to expect

- It looks like Kite (indigo, square corners), but Firefox's own inner pages, such as settings and the private new tab, still look like Firefox.
- The default search is Brave Search.
- Proton Pass is installed. It opens its own welcome page once. You can turn it off in Add-ons.
- Sites that need DRM (Netflix, Spotify and the like) don't play yet.
- Pages on a bare tailnet or home-network address (like 192.168.x.x) may ask whether the page can reach your local network.

## What Kite never sends

No telemetry, no crash reports, no Firefox or Mozilla accounts, no sync, no studies, no sponsored content, no search suggestions, no Safe Browsing lookups, no captive-portal checks. DNS-over-HTTPS is off, so your DNS stays with Windows. Kite itself only talks to Mozilla (to get and update the browser engine, once a day at most) and to this GitHub repo (to update Kite). Extensions you install yourself make their own connections, and Proton Pass talks to Proton.

## Something broke?

1. Open **Preferences** (the gear at the bottom of Kite's sidebar), scroll to **About** and press **Copy diagnostics**.
2. Open a new issue in this repo and paste it in, with a sentence about what you did and what happened.

The diagnostics are versions, a check of Kite's settings and the last update events. They never contain the addresses, titles or searches of pages you visited.

Kite writes no logs and sends nothing: there is no log file on your PC and nothing to upload. Copy diagnostics only puts text on your clipboard, and you paste it where you choose.

## Uninstall

Settings > Apps > Installed apps > Kite > Uninstall. Your browsing data stays in `%LOCALAPPDATA%\com.electream.kitepc`; delete that folder too if you want it gone.
