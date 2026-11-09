# Campusly website

The public introduction page for Campusly, with a download link for the Android app.

- Website: hosted on Vercel
- Web app: <https://www.campusly.work>
- Android download: [latest release](https://github.com/Muzzammil-Azhar/campusly-website/releases/latest)

## Why this repository exists

Campusly's source code lives in a **private** repository. It holds the backend, database migrations and deployment setup, so it stays private.

A download link must work for anyone, so it cannot point into a private repository. This **public** repository holds only two things:

1. **This page.** Plain HTML and CSS with no build step, so there is nothing to break and anyone can read exactly what it does.
2. **The APK, as a GitHub Release.** Releases give each version a permanent download address, a version history and a public file anyone can check.

No app source code, keys or private data are in this repository.

## How the download link works

The button points to `releases/latest/download/campusly.apk`. GitHub always redirects that address to the newest release, so publishing a new version never needs a website change. Each release names its APK `campusly.apk` and states its version and SHA-256.

## Google Play and this APK

This APK is signed with the upload key. Google Play re-signs apps with its own key, so a phone with this APK installed cannot update to the Play Store version in place. Uninstall this one first. The page says this under the download button.

## Publishing a new version

1. Build and verify the APK in the private repository.
2. Create a release here tagged `vX.Y.Z` with the file renamed to `campusly.apk`.
3. Update the version, size and SHA-256 in `index.html`, then redeploy.
