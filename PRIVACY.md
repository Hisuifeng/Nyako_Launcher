# Privacy

Nyako Launcher runs entirely on the user's machine. There is no launcher account system, no
backend service and no telemetry.

## What is stored locally

| Data | Where |
| --- | --- |
| Microsoft / Xbox refresh token | Windows Credential Manager, current Windows user only |
| Access tokens (Microsoft, Xbox, Minecraft) | process memory, discarded on exit |
| Launcher settings, instances, Java runtimes | `.nyako/launcher.db` (SQLite) in the working directory |
| Game files, libraries, assets, logs | `.minecraft` in the working directory |
| Offline account profiles | `.nyako/launcher.db` (name, UUID, no credentials) |

Offline accounts and "external" account entries are local placeholders; they are marked as
unverified in the UI and cannot sign in to online-mode servers.

## What is sent over the network

- Microsoft identity platform (`login.microsoftonline.com`, `www.microsoft.com/link`) — OAuth
  device-code sign-in, scopes `XboxLive.signin` and `XboxLive.offline_access` only.
- Xbox Live / XSTS (`user.auth.xboxlive.com`, `xsts.auth.xboxlive.com`) — token exchange with
  relying party `rp://api.minecraftservices.com/`.
- Minecraft Services (`api.minecraftservices.com`) — Minecraft token, player profile and skin.
- Mojang content delivery (`piston-meta.mojang.com`, `resources.download.minecraft.net`,
  `libraries.minecraft.net`) — version manifests, libraries, assets and client jars.
- Modrinth (`api.modrinth.com`) — only when the user searches for or downloads a mod or modpack.

No request contains an advertising identifier, and no data is sold, shared or uploaded to the
project's own infrastructure (the project has none).

## Revoking access

Removing the account inside the launcher deletes the refresh token from Windows Credential
Manager. The Microsoft account can also revoke the application's access from
<https://account.live.com/consent/Manage>.
