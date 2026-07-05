# XConnect Client Updates

Static update manifests for XConnect VPN clients.

Base raw URL:

```text
https://raw.githubusercontent.com/svdkilla/XConnect_Client/main
```

Client flow:

1. Load `channels/stable.json`.
2. Pick the current platform manifest URL.
3. Compare `latest.version` and `latest.build` with the local app version.
4. If a newer build exists, download the matching artifact and verify `sha256`.

Current manifests are prepared for:

- `pc` (alias for the Windows desktop build)
- `windows`
- `linux`
- `macos`
- `android`
- `ios`
- `web`

Windows artifacts are currently stored in `artifacts/v0.1.3/`; older Windows and Android ARM artifacts remain in previous version folders.
All artifacts are served through GitHub raw URLs.
Future production releases can move large binaries to GitHub Releases without changing the manifest shape.
