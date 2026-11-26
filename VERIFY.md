# Verifying a download

Every file on the release (installers, update feeds and the SBOM) has signed build provenance (SLSA v1). It's a Sigstore-signed statement, made by this repository's GitHub Actions workflow, of the file's SHA-256 and the workflow run that built it. That run's public page names the source version it was built from (its `ref` input, e.g. `v0.21.5`).

## Any platform: build provenance
With the GitHub CLI (`gh` 2.49 or later, signed in):
```
gh attestation verify TerminallyLLM-<version>-arm64.dmg -R JeremiePineau/terminallyllm-releases
```
It checks three things:
- the signature;
- that the file's hash matches;
- that the signer was `.github/workflows/build.yml` in this repository.

Add `--format json` to see the workflow run (`runDetails.metadata.invocationId`).

The signed bundles are also on the release (`TerminallyLLM-provenance-<windows|macos|linux>.sigstore.json`). To verify against the downloaded bundle instead of GitHub's attestation store, add `--bundle TerminallyLLM-provenance-macos.sigstore.json`.

## macOS: Developer ID and notarization
After installing:
```
codesign --verify --deep --strict --verbose=2 /Applications/TerminallyLLM.app
spctl --assess --type execute --verbose /Applications/TerminallyLLM.app
xcrun stapler validate /Applications/TerminallyLLM.app
```
- **`codesign`:** must say the app is valid on disk.
- **`spctl`:** must say `accepted` with `source=Notarized Developer ID`.
- **`codesign -dvv`:** the authority must be `Developer ID Application: … (LHK3JD23WG)`.

## Updates inside the app
The app downloads an update only after you click, and checks it against the SHA-512 in the update feed (`latest.yml`, `latest-mac.yml`, `latest-linux.yml`). It never installs an older version or a pre-release. On macOS, the update must also be signed by the same Developer ID.

## Windows
The Windows installer isn't code-signed. Verify it with the build provenance above. The SHA-512 in `latest.yml` is the one the in-app updater checks.
