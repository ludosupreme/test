# Ludo Supreme – website (GitHub Pages)

Static site: `index.html`, `privacy.html`, `terms.html`, `contact.html`, `404.html`. No external requests (no fonts, scripts or trackers).

## 1. Fill in the placeholders (required before publishing)
Replace these three tokens in all `.html` files:

| Token | Replace with |
|---|---|
| `{{DEVELOPER_NAME}}` | Your name or studio name (must match your Play developer profile) |
| `{{CONTACT_EMAIL}}` | A working support email (must match the Play listing) |
| (done) Play link already set to `com.ludosupreme.app`; change the link text to "Coming soon" until the app is live |

Linux/macOS one-liner:
```
sed -i 's/{{DEVELOPER_NAME}}/Your Name/g; s/{{CONTACT_EMAIL}}/you@example.com/g; s#{{PLAY_STORE_URL}}#https://play.google.com/store/apps/details?id=com.ludosupreme.app#g' *.html
grep -l '{{' *.html   # must print nothing
```

## 2. Publish on GitHub Pages
1. Create a repo (named exactly `test`) and push these files to the repo root.
2. Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`.
3. Your URL will be `https://ludosupreme.github.io/test/`.

## 3. Google Play Console
- **Privacy policy URL:** `https://ludosupreme.github.io/test/privacy.html` (App content → Privacy policy). It must be public, not a PDF, and load without login.
- **Data safety form:** "Does your app collect or share any of the required user data types?" → **No**. Data is processed on-device only; no ads, analytics or network transfer. Re-check this if you add any SDK.
- **Ads:** "Contains ads" → **No**.
- **Target audience:** choose 13+ (or 18+) unless you intend to join the Families programme; the *Kids* board layout name in Snakes & Ladders may look child-directed, so decide deliberately.
- **Store listing assets** are in `play-store-assets/`: 512×512 icon, 1024×500 feature graphic, six 1080×1920 phone screenshots (all real in-app captures).
- **Contact details** in the listing must match the email on the Contact page.

## 4. Keep it accurate
The privacy policy states: no account, no ads, no analytics, local-only storage, optional vibration and local reminder notifications, and a user-initiated Share button. If you add ads, analytics, crash reporting, accounts or online play, update `privacy.html` and the Data safety form first.
