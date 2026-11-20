# MouseBridge

**One mouse, one keyboard and one clipboard for your Windows PC and your Mac — with every screen arranged at its
real physical size.**

Put the computers side by side, move the pointer off the edge of one screen and it appears on the other computer,
exactly where that screen sits on your desk. Typing follows the pointer, and text you copy on one computer can be
pasted on the other. It works in both directions: the PC's mouse can drive the Mac, and the Mac's trackpad can drive
the PC.

This repository publishes MouseBridge's releases: the installers, their checksums and the update information that
MouseBridge checks. **You don't need a GitHub account** to download anything here.

- [What you need](#what-you-need)
- [Download](#download)
- [Install on Windows](#install-on-windows)
- [Install on the Mac](#install-on-the-mac)
- [Pair your computers](#pair-your-computers)
- [Arrange your screens](#arrange-your-screens)
- [Updating](#updating)
- [Checking a download](#checking-a-download)
- [Support MouseBridge](#support-mousebridge)
- [Privacy](#privacy)
- [Help](#help)

## What you need

- **Windows 10 (version 1809 or newer) or Windows 11**, 64-bit.
- **macOS 12 Monterey or newer**, on a Mac with Apple Silicon (M1 or newer) or an Intel processor.
- Both computers on **the same local network** (the same Wi-Fi or wired network at home or in the office). Guest
  Wi-Fi networks that isolate devices from each other do not work.
- MouseBridge running on every computer that shares the mouse.

## Download

Open the latest release, <https://github.com/Audacity01/mousebridge-releases/releases/latest>, and download the file
for your computer from the list under *Assets*:

| Computer | File |
|---|---|
| Windows PC | `MouseBridge-Setup-<version>-win-x64.exe` |
| Mac with Apple Silicon (M1, M2, M3, M4…) | `MouseBridge-<version>-macos-arm64.zip` (or the `.dmg`) |
| Mac with an Intel processor | `MouseBridge-<version>-macos-x64.zip` (or the `.dmg`) |

Not sure which Mac you have? Choose **Apple menu > About This Mac**. "Chip: Apple M…" means Apple Silicon;
"Processor: … Intel …" means Intel.

Do not use the *Source code* links under *Assets* or the green *Code* button of this page: they contain only this
README, not the app, and cannot be installed. `mousebridge-update.json` and `mousebridge-update.json.sig` are the
signed update information that MouseBridge reads; you don't need to download them. Releases marked *Pre-release*
(versions such as 1.2.0-beta.1) are for testing: they have no update information, and installed MouseBridge versions
never update to them.

## Install on Windows

1. **Run `MouseBridge-Setup-<version>-win-x64.exe`.**
2. **SmartScreen.** Windows may show *"Windows protected your PC"*, because this free installer is not signed with a
   paid certificate. Click **More info**, then **Run anyway**.

   **Smart App Control (Windows 11).** If Windows says *"Smart App Control blocked an app that may be unsafe"*
   instead, there is no *Run anyway*: with Smart App Control **On**, Windows blocks every program that is not signed
   with a trusted certificate — Setup, and MouseBridge itself each time it starts. Check it in *Windows Security > App
   & browser control > Smart App Control settings*; *Evaluation* and *Off* do not block MouseBridge.
3. **Choose who it is for.** **Install for all users (recommended)** needs an administrator password: MouseBridge goes
   into *Program Files*, Setup can open the Windows Firewall for it, and it can start with administrator rights when
   you sign in, so it keeps working while an administrator window (Task Manager, an installer) is in front. **Install
   for me only** needs no administrator password; Windows may then ask to allow MouseBridge through the firewall the
   first time it runs.
4. **Finish** with *Launch MouseBridge* ticked. MouseBridge lives in the notification area at the right end of the
   taskbar; click the **^** arrow if you do not see its icon.

## Install on the Mac

1. **Unzip the download.** Double-click the zip in your Downloads folder (Safari may already have done it). You get a
   folder with three items: `MouseBridge.app`, `Install MouseBridge.command` and `README-mac.txt`. (With the `.dmg`,
   double-click it instead; the same three items appear.)
2. **Double-click `Install MouseBridge.command`.** The first time, macOS refuses to open it, because this free build
   is not notarized by Apple:
   - **macOS 15 Sequoia and newer:** click **Done** (not *Move to Trash*). Open **System Settings > Privacy &
     Security**, scroll down to **Security** and click **Open Anyway** next to *"Install MouseBridge.command" was
     blocked*. Confirm with **Open Anyway** and your password.
   - **macOS 14 and older:** Control-click (or right-click) the file, choose **Open**, then **Open**.

   A Terminal window shows the installer's progress. It quits an older MouseBridge, copies the new one to
   **Applications**, signs it for your Mac, starts it and opens the Accessibility settings.
3. **Accessibility — required.** In *System Settings > Privacy & Security > Accessibility*, switch **MouseBridge** on.
   If it is not in the list, click **+**, choose **Applications > MouseBridge** and switch it on. Without this
   permission MouseBridge can neither follow nor move the pointer.
4. **Local Network — required on macOS 15 and newer.** When macOS asks *"Allow MouseBridge to find devices on local
   networks?"*, click **Allow**.

Always install and update with `Install MouseBridge.command`. Do not drag `MouseBridge.app` into Applications yourself:
the app has to be signed on your Mac, and macOS may otherwise call it "damaged".

## Pair your computers

Every MouseBridge installation shows a **security key**: 16 letters and digits in four groups, made up at random. All of
your computers must use **the same key**: it is what lets them trust each other. Use the key one of them shows:
MouseBridge refuses a key that is easy to guess.

1. Open MouseBridge's window on both computers and go to **Computers**. On Windows, click the MouseBridge icon in the
   notification area. On the Mac, click the menu bar icon and choose **Open MouseBridge**, or open MouseBridge from
   *Applications* or Spotlight.
2. On one computer, note its key (there is a copy button).
3. On the other computer, type that key into **Enter the key shown on your other computer**. Upper or lower case,
   spaces and dashes don't matter.
4. Within a few seconds both computers show each other as **Connected**.

If the computers don't find each other (some networks block discovery), type the other computer's address under
**Add a computer by address** on the *Computers* page and click **Add**. The address is shown at the top of the other
computer's *Computers* page; adding the Mac's address on the PC usually works best.

Keep the key private: anyone on your network who knows it could control your computer. **New key…** on the
*Computers* page makes a new one; then enter it on your other computers.

## Arrange your screens

The **Arrangement** page shows every screen of every connected computer at its real physical size. Drag the screens
until the picture matches your desk: the pointer crosses where two screens touch (the highlighted line), at the
physically matching point. If a screen shows an *estimated size*, select it and type its diagonal in inches.

| Windows keyboard | Mac keyboard | What it does |
|---|---|---|
| **Ctrl+Alt+Shift+Esc** | **Control+Option+Shift+Esc** | Brings the pointer back to the computer whose keyboard you are using. |
| **Ctrl+Alt+Shift+L** | **Control+Option+Shift+L** | Locks the pointer to the computer it is on, or unlocks it. |

## Updating

**MouseBridge 1.1 and newer update themselves.** About once a day MouseBridge asks this repository whether there is a
newer version; you can switch that off, or check at any time, in **Settings > Updates**. When there is one, MouseBridge
says so in its window and adds **Update to *version*…** to its tray / menu bar menu. Nothing is downloaded or installed
until you choose **Update now** (or that menu item). MouseBridge then downloads the update, checks its signature and
checksum, closes for a moment, installs it and starts again. Your settings and paired computers are kept.

- **On the Mac,** macOS ties the Accessibility permission to the exact app version. After an update, switch
  **MouseBridge** on again in *System Settings > Privacy & Security > Accessibility*. Until then MouseBridge can't
  control that Mac, so do it with the Mac's own keyboard and mouse or trackpad.
- **Update all your computers.** Keep MouseBridge at the same version on the PC and the Mac: after updating one, update
  the other too.
- **MouseBridge 1.0** does not update itself: download the new version and install it over the old one as described
  above. Your settings are kept.

## Checking a download

Every release has `SHA256SUMS.txt` with the SHA-256 checksum of each file. To check a download, compare its checksum
with the line for that file:

- Windows (PowerShell): `Get-FileHash .\MouseBridge-Setup-<version>-win-x64.exe -Algorithm SHA256`
- Mac (Terminal): `shasum -a 256 ~/Downloads/MouseBridge-<version>-macos-arm64.zip`

The update information that MouseBridge reads, `mousebridge-update.json`, is signed with MouseBridge's update signing
key, and MouseBridge ignores update information whose signature doesn't match. To check it yourself, save the key
below as `update-signing-public.pem` (when more than one key is listed, a release is signed with one of them: try each),
download `mousebridge-update.json` and `mousebridge-update.json.sig` from the same release, and run:

```sh
openssl dgst -sha256 -verify update-signing-public.pem -signature mousebridge-update.json.sig mousebridge-update.json
```

It prints `Verified OK` for genuine update information. The `size` and `sha256` it lists for each package must match
the file you downloaded.

The key (SHA-256 fingerprint `bfedec71bca50cf15523c9852b1b85c1158bce298037c1aebcd7aba1d22958d0`):

```text
-----BEGIN PUBLIC KEY-----
MFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAEeMxRcZd4iXZmJnPZ5YXAeEUy7Tyc
pyjkKlzV6ry+AC47S3nbXhs/dDmv0qBJdQKH46bkpov/oJUB/CwEJcIrYg==
-----END PUBLIC KEY-----
```

## Support MouseBridge

MouseBridge is free, with nothing locked: no ads, no account and no tracking. It is made by one person. If it's useful
to you, you can support it on Ko-fi: **<https://ko-fi.com/mousebridge>** (a one-time payment in US dollars, through
PayPal, no Ko-fi account needed; suggested $5). Support pays for code signing first, so installing MouseBridge shows
fewer warnings and the Mac keeps its permissions after updates. Paying unlocks nothing, and not paying takes nothing
away. In MouseBridge the same button is at the end of *Help* and in the tray / menu bar menu.

## Privacy

- MouseBridge works on your local network. To be found by your other computers, it announces this computer on every
  network it joins, about every 2 seconds while *Find other computers automatically* is on: its name (*Computer name*
  in *Settings*) and a fixed MouseBridge id. Any device on the same network sees that, and gets the same answer when it
  sends such an announcement itself or connects to TCP port 24850, before the security key is checked: the key protects
  control of your computers, not their names. On a network you don't trust, use a neutral computer name, or turn
  discovery off and add your computers by address.
- Your computers prove to each other that they know the shared security key before they exchange any input, copied
  text or screen layout, and all of that is encrypted. Copies that their app marks as private, such as passwords from a
  password manager, are never sent to the other computer.
- The only thing MouseBridge fetches from the internet is the update information of this repository, about once a day
  (and when you choose **Check for updates** or **Update now**). It is a plain download from github.com that names only
  MouseBridge and its version (`User-Agent: MouseBridge/<version>`): no account, computer name or other identifier.
  As with any download, GitHub sees your IP address. It never signs in to a proxy server, so no proxy learns your
  Windows sign-in from it. Automatic checks can be switched off in **Settings > Updates**.
- There is no telemetry. The log files never contain typed keys or clipboard contents.
- The support page opens only when you choose **Support MouseBridge**; MouseBridge sends Ko-fi nothing, and the count
  behind its occasional support note never leaves your computer.

## Help

- **Pointer stuck on the other computer?** Press **Ctrl+Alt+Shift+Esc** (Windows keyboard) or
  **Control+Option+Shift+Esc** (Mac keyboard).
- **A key does something else on the other computer?** Choose what your keyboard's keys do there in
  *Settings > Keyboard*, on the computer whose keyboard you type on. It changes single keys, not whole shortcuts.
- **Computers do not see each other?** Both must use the same security key and the same network. Allow MouseBridge in
  the Windows Firewall and in the Mac's *Local Network* settings, or use **Add a computer by address** on the
  *Computers* page.
- **Mac says it needs Accessibility although it is on?** Remove MouseBridge from the list with **−** and add it again
  with **+**. If that does not help, quit MouseBridge and run `tccutil reset PostEvent com.mousebridge.app` and
  `tccutil reset Accessibility com.mousebridge.app` in Terminal, then open it again and switch it on.
- **An update failed?** The version you have keeps running. Choose **Try again**, or download the new version here and
  install it as described above. On Windows, choose **Yes** when Windows asks for permission to install an update for
  all users. On the Mac, *"MouseBridge can't replace itself"* means macOS's *App Management* protection refused: allow
  MouseBridge in *System Settings > Privacy & Security > App Management*, or install the update by hand.
- **Logs:** `%LOCALAPPDATA%\MouseBridge\mousebridge.log` on Windows,
  `~/Library/Application Support/MouseBridge/mousebridge.log` on the Mac. Lines about updates start with `Updates:`.
  When an update fails on the Mac, the installer's own log is kept in
  `~/Library/Application Support/MouseBridge/logs/update-<time>.log`, and the message names it.
  A log names your computers and their network addresses, your monitors and your Windows user folder, and it records
  when you switched computers or locked the screen: share it only privately, never on a public page.
