# Petit public website

This repository hosts the public GitHub Pages website for [Petit](https://github.com/petit-app/petit), an open-source Android app for managing pet health and care records.

## Public pages

- Website: <https://petit.woliveiras.com/>
- Privacy policy: <https://petit.woliveiras.com/privacy-policy/>

## Repository structure

- `index.html`: product landing page.
- `privacy-policy/index.html`: bilingual English and Brazilian Portuguese privacy policy.
- `assets/brand/`: website brand assets.
- `assets/screenshots/`: product screenshots used by the website.
- `LICENSE`: GNU AGPL-3.0 terms for the website source.

## Product and privacy boundaries

Petit is local-first. Pet profiles, health records, tasks, reminders, preferences, and app-owned media are stored on the user's Android device. Supported sharing flows transfer data directly between devices through Nearby Connections or an authorized local-network connection; Petit does not operate a hosted synchronization backend for those flows.

Google Drive backup is optional and uses storage owned by the user. Petit requests only the `https://www.googleapis.com/auth/drive.appdata` scope and stores its backup archives in that user's hidden Google Drive `appDataFolder`. This flow does not use Firebase or a Petit-operated backend. Disconnecting Google Drive or revoking authorization stops Petit from accessing Drive but does not automatically delete backups already stored there.

See the [privacy policy](https://petit.woliveiras.com/privacy-policy/) for the complete user-facing description.

## Local preview

From the repository root, run:

```bash
python3 -m http.server 8080
```

Then open:

- <http://localhost:8080/>
- <http://localhost:8080/privacy-policy/>

## Updating the site

1. Edit the relevant HTML or asset files.
2. Preview the affected pages locally at mobile and desktop widths.
3. Check links, language content, and accessibility before publishing.
4. Commit and push through the project's normal review workflow; GitHub Pages deploys from the configured branch.

## Open source and trademarks

This website and the Petit Android source code are available under the GNU Affero General Public License v3.0. The app source is maintained at [github.com/petit-app/petit](https://github.com/petit-app/petit). The Petit name, logo, and visual identity are governed separately by the trademark policy in the Android repository. Public forks must follow both the software license and the trademark rules.
