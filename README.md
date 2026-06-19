# Zytra – Legal Pages (Privacy Policy & Terms of Use)

Source copies of the public legal pages for the **Zytra** Android app. These files are mirrored
into the separate GitHub Pages repo **`dev-deng/zytra-privacy`**, which serves the live site.

## Live URLs

| Document | Live URL | Source in this repo |
|---|---|---|
| Privacy Policy | https://dev-deng.github.io/zytra-privacy/ | `docs/privacy/index.html` |
| Terms of Use | https://dev-deng.github.io/zytra-privacy/terms.html | `docs/legal/terms.html` |

Both pages are DE + EN and link to each other. The Terms URL must match the `terms_url` string
(`app/src/main/res/values/strings.xml`, `translatable="false"`).

## Deployment

Manual sync (no CI in this repo): copy the source files into the `zytra-privacy` repo root as
`index.html` (privacy) and `terms.html` (terms), then verify both URLs load and the cross-links work.
When the data model changes, update `index.html` (and the date); for legally relevant Terms changes,
update `terms.html`, bump the date/version, and raise `UserPreferences.CURRENT_TERMS_VERSION` to force
renewed in-app consent.

The Play Console **Privacy Policy** field points to the privacy URL only; the Terms page is linked
from it but is not a separate mandatory field.

---

Zytra is a local-only cycle tracking app. No data leaves the device.
