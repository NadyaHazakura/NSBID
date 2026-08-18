# NS Browser

Open-source Chromium/AOSP browser build scaffold for GitHub Actions.

Package IDs:
- `io.github.nsbrowser` — standalone Chromium browser APK
- `io.github.nsbrowser.webview` — WebView-provider APK scaffold

Build goals:
- ARM64 (`arm64-v8a`) APK
- hardware GPU acceleration
- no Google Play Services dependency
- privacy/ad-block filtering
- custom filters and regional filter profiles
- translation integration hook
- conservative script injection hook
- crash/background/tab stability testing
- GitHub Releases containing APKs

Chromium source is fetched by CI instead of being stored in this small ZIP.
Set `CHROMIUM_REF` in the workflow to a verified Chromium branch/tag/commit.
The default uses a placeholder ref intentionally; replace it with a real verified
Chromium ref before running a release build.

Important: a real Android WebView provider is platform-integrated and normally
requires an AOSP/system-image build and privileged/provider configuration. The
second module is therefore a WebView-provider scaffold, not a claim that an
ordinary APK can replace the system WebView on every Android device.
