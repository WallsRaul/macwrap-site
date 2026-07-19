<p align="center">
  <img src="macwrap-logo-512.png" alt="MacWrap" width="140">
</p>

<h1 align="center">MacWrap</h1>

<p align="center">
  <b>Run your Windows apps as native Mac apps.</b><br>
  Drag a Windows <code>.exe</code> onto MacWrap and get a real <code>.app</code> back — its own icon,<br>
  double-click to launch, no terminal, no setup. You'd never know there's Windows underneath.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/macOS-14%2B-000000?logo=apple&logoColor=white">
  <img src="https://img.shields.io/badge/Apple%20Silicon-M1–M4-22c55e">
  <img src="https://img.shields.io/github/v/release/WallsRaul/macwrap-site?label=version&color=5babec">
  <img src="https://img.shields.io/badge/engine-Wine%2011%20·%20LGPL-8b7fd9">
  <img src="https://img.shields.io/badge/beta-free%20until%20further%20notice-22c55e">
</p>

<p align="center">
  <a href="https://github.com/WallsRaul/macwrap-site/releases/latest/download/MacWrap.dmg"><b>⬇&nbsp; Download for Mac (.dmg)</b></a>
  &nbsp;·&nbsp; <a href="https://macwrap.app">Website</a>
  &nbsp;·&nbsp; <a href="https://macwrap.lemonsqueezy.com/checkout/buy/675b04d0-2520-4bc6-8df1-1e3cc1edc191">♥ Donate</a>
</p>

* * *

## ✨ What is MacWrap?

MacWrap turns any Windows program into a **native-feeling Mac app**. No virtual machine, no Windows
desktop, no per-app guesswork — each app becomes its own `.app` bundle with the real icon, and you
double-click to run it.

It runs on a **patched, hardware-accelerated build of Wine** (plus Apple's Game Porting Toolkit for
games) that we maintain ourselves — so things work that other layers can't.

## 🖼 Screenshots

<p align="center">
  <img src="docs/screenshot-wrap.png" width="420" alt="Drop a .exe, get a native .app">
  &nbsp;
  <img src="docs/screenshot-analysis.png" width="420" alt="Compatibility analysis before you commit">
</p>

<p align="center"><i>Left: drop a <code>.exe</code> or an installer.&nbsp;&nbsp;Right: MacWrap analyzes it and tells you what to expect <b>before</b> wrapping it.</i></p>

## 🚀 Features

- **Drag & drop** — drop any `.exe` or installer, get a native `.app`.
- **Honest compatibility** — MacWrap analyzes each app and tells you which tier it lands in, *before* you commit.
- **Games** — wrap DX11/DX12 titles via Apple's Game Porting Toolkit + D3DMetal.
- **Epic Games library** — connect your Epic account and bring your games (and the free weekly giveaways) to Mac.
- **Real native bundle** — original icon, double-click, no terminal.
- **Bilingual** — English & Spanish, auto by system language.

## 📊 Compatibility — honest by design

No compatibility layer runs *everything*, and anyone who says otherwise is lying. MacWrap tells you up front:

| Tier | What runs |
|------|-----------|
| 🟢 **Runs great** | Win32 / .NET Framework apps · GDI/GDI+ interfaces · most legacy professional software |
| 🔵 **Runs with a recipe** | Needs runtimes/tweaks we apply automatically — .NET, Access DB, Direct2D editors |
| 🟠 **Partial** | Heavy Direct2D/Direct3D edge cases; some features may be limited |
| 🔴 **Not yet** | Modern WinRT · kernel drivers · online anti-cheat (Fortnite, etc.) |

**Already running:** The Witcher 3 · legacy .NET/Access business suites · Sierra Chart · AmiBroker ·
Notepad++ · 7-Zip · VLC · IrfanView · EmEditor · WinMerge · MobaXterm · WinSCP · HeidiSQL ·
TallyPrime · Warframe · Resident Evil 4 · Need for Speed Most Wanted — and more.

## ⬇ Download & Install

1. [**Download MacWrap.dmg**](https://github.com/WallsRaul/macwrap-site/releases/latest/download/MacWrap.dmg) (Apple Silicon).
2. Open the `.dmg`, drag **MacWrap** to Applications.
3. First launch: **right-click → Open** (one-time macOS prompt for unsigned apps).
4. Drag a Windows `.exe` onto it. Done.

> [!TIP]
> MacWrap is **free during the beta, until further notice** — every feature unlocked, nothing to
> activate and nothing to pay.

> [!NOTE]
> MacWrap needs **Rosetta 2** (the engine is x86_64). The app detects and installs it automatically
> with one click on first run — nothing technical on your side.

## ❤️ Support the project

MacWrap is free and built by **one developer**. Every recipe — making a stubborn Windows app finally
run on Mac — is hours of deep work. If MacWrap saved you from buying a Windows PC or a pricey VM, a
small donation keeps it going:

- [**♥ Donate** (card / Apple Pay)](https://macwrap.lemonsqueezy.com/checkout/buy/675b04d0-2520-4bc6-8df1-1e3cc1edc191)
- [Donate with **PayPal**](https://www.paypal.me/WallsRaul)

100% optional — MacWrap stays free either way. 🙏

## 🛠 How it works

Swift orchestrates everything: it analyzes the `.exe`, picks the right recipe, sets up an isolated
Wine "bottle", injects the program, and packages it as a standard macOS `.app`. The graphics stack is
a self-patched Wine (wined3d / d2d1 on MoltenVK / Metal) plus Apple's Game Porting Toolkit + D3DMetal
for Direct3D games.

* * *

<sub>MacWrap runs on a modified build of <a href="https://www.winehq.org">Wine</a> (LGPL). Modified source:
<a href="https://github.com/WallsRaul/macwrap-wine">github.com/WallsRaul/macwrap-wine</a>.
Windows is a trademark of Microsoft. Apple, Mac and Apple Silicon are trademarks of Apple Inc.
MacWrap is not affiliated with Microsoft or Apple. It packages software you already own and are
licensed to use; it does not distribute third-party applications.</sub>
