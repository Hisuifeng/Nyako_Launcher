# Nyako Launcher 0.1.0

First public alpha build of Nyako Launcher — a third-party launcher for Minecraft: Java Edition
on Windows.

## Download

`NyakoLauncher-0.1.0-win-x64.zip` (portable, no installer)

1. Extract the archive.
2. Run `nyako-launcher.exe`.
3. Sign in with a Microsoft account under **Settings → Accounts → Microsoft sign-in**, or create
   an offline account for LAN testing.

## Highlights

- Multiple instances with independent game directory, version, loader (vanilla / Fabric / Forge /
  NeoForge / Quilt), memory and JVM arguments.
- Downloads version manifests, client jars, libraries and assets from Mojang's public services
  with SHA-1 verification.
- Microsoft account sign-in through the official OAuth device-code flow
  (scopes `XboxLive.signin`, `XboxLive.offline_access`), then Xbox Live / XSTS /
  Minecraft Services. Refresh token is kept in Windows Credential Manager; access tokens stay in
  memory.
- Offline and external (authlib-injector style) accounts, clearly marked as unverified.
- Plugin-first UI (Tauri 2 + Rust + Vue 3), light/dark theme, English and Chinese.

## Requirements

- Windows 10 / 11 x64
- Microsoft Edge WebView2 Runtime
- Java 21 runtime (or let the launcher download one)

## Known limitations

- Microsoft sign-in returns `403 Invalid app registration` until this application ID is
  reviewed and allow-listed by Mojang for Minecraft Services.
- Windows x64 only for now; no auto-update yet.

See [README.md](README.md) for details and [PRIVACY.md](PRIVACY.md) for data handling.
