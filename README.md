# pitru-privacy

This repository hosts the public-facing privacy policy for the
**Pitru Calendar** iOS app. It exists as a separate repo so the app's
source code can stay private while the privacy policy URL stays
public and stable — Apple's App Store Connect requires the URL to be
publicly accessible and to not change across submissions.

## Live URL

```
https://sadhasiva1984.github.io/pitru-privacy/
```

Pasted into App Store Connect → App Information → Privacy Policy URL.

## What's here

| File | Purpose |
|---|---|
| `index.md` | The privacy policy itself. Mirrors the `PrivacyInfo.xcprivacy` manifest shipped with the app. |
| `_config.yml` | Minimal Jekyll config so GitHub Pages renders the markdown at a pretty URL. |
| `README.md` | This file. |

## How to update

1. Edit `index.md` (bump the `Effective Date` if the change is material)
2. `git commit && git push`
3. GitHub Pages rebuilds in ~30 seconds
4. The live URL serves the new content; the URL itself doesn't change

## Source of truth

The bundled `PrivacyInfo.xcprivacy` inside the app is the legal source
of truth — it's what Apple's App Review machine pipeline reads. This
markdown is the human-readable mirror. Whenever the manifest changes,
this file must be updated to match.

The app source code is in a separate (private) repository.
