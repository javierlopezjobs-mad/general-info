# Twelve Testers app profile — Tasting Partner

Copy-paste source for the Twelve Testers listing at
<https://twelvetesters.com/dashboard/apps/new>.

- **Play package:** `com.jlopezlabs.tastingpartner`
- **Last updated:** 2026-11-12
- **Name check:** the landing page and privacy policy use **Tasting Partner**;
  older material in this repo still says *Tasting Party* / *Tasting Go*. Use the
  exact name shown in your Play Console listing and replace it everywhere below
  if it differs.

---

## 1. Profile fields

| Field | Value |
| --- | --- |
| App name | Tasting Partner |
| Category | Food & Drink |
| Platform | Android (fixed) |
| App language | English (the app also supports Spanish) |
| Target number of testers | 20 |
| Session length | 15 days (fixed by Twelve Testers) |
| Developer name | JL Horizon Labs |
| App icon | [`play-store-icon.png`](play-store-icon.png) (512×512 PNG) |
| Screenshots | [`screenshots/0_1_4_en/`](screenshots/0_1_4_en/) — choose up to 6 |

**About the target.** Google Play requires **12 testers opted in for 14
consecutive days**. Twelve Testers defaults the listing target to 20 to absorb
dropouts. If you do not want that many reciprocal swaps, set 12–15; the form
warns below 20 but lets you publish.

---

## 2. Description (paste into **Description**)

Tasting Partner is a personal tasting journal for food and drink products.
Create tastings, add products by scanning a barcode, searching a product
database, or entering them manually, then rate each product on your preferred
scale — 5 stars, 10 stars, or a 0–100 slider — and keep private tasting notes,
including voice notes transcribed on-device.

Browse every product across all your tastings, compare what you have tried, and
keep nutrition details such as ingredients, calories, sugars, saturated fat,
fibre, sodium, and alcohol in one place. Back up or export your data whenever
you want.

Everything is stored on your device: no account, no cloud, no tracking.
Available in English and Spanish. Currently looking for Android testers to find
bugs, improve usability, and share feedback before the Google Play release.

---

## 3. Testing instructions (paste into **Testing instructions**)

Please install Tasting Partner from the Play closed-testing link using the same
Google account that joined the test, then exercise the main flows:

1. Open the app and complete the notification permission prompt. The daily
   reminder is how the app helps you keep the 14-day testing window visible;
   it sends one local reminder per day and does not send anything to a server.
2. Create a tasting, for example "Weekend tasting".
3. Add at least three products: one by scanning a barcode, one with product
   search, and one with manual entry.
4. Rate the products using each scale (Settings → Rating scale: 5 stars,
   10 stars, 0–100 slider). Add a typed note to one product and try a voice note
   on another. The first voice note downloads a speech model once; later
   dictation works offline.
5. Open the Products tab and review the combined product list. Open a product
   to check the rating, notes, and nutrition fields.
6. Share a tasting (link or file) and, if you receive a shared tasting, open the
   preview. Ratings are intentionally never shared.
7. From Settings → Data, export a JSON backup and a CSV. Import the JSON backup
   once to confirm restore works. Importing replaces all current data, so do
   this before adding anything you want to keep.
8. Keep the app installed and stay opted in for the full 14 days. Please use the
   app regularly and send private feedback rather than a public review.

---

## 4. What feedback do you want? (paste into **What feedback do you want?**)

I would appreciate feedback about:

- Crashes, freezes, ANRs, or anything that breaks the add → rate → note flow.
- Barcode scanning and product search: missed scans, wrong matches, duplicates,
  or confusing empty states.
- Whether the three rating scales are clear, and whether unrated products are
  obvious everywhere.
- Voice notes: recording, transcription quality, and the one-time model
  download.
- Sharing a tasting by link and by file, and opening a shared tasting.
- JSON backup, JSON restore, and CSV export.
- Navigation, layout on your phone, dark mode, and the Spanish translation.
- Anything that feels unfinished or missing before production.

---

## 5. Known issues / don't report (paste into **Known issues**)

- The first voice note downloads a ~75 MB speech model. This is expected and
  only happens once per device.
- Share links and shared `.tasting.json` files open on Android only. iOS
  Universal Links and receiving shared tastings on web/iOS are not supported yet.
- Importing a full JSON backup replaces all current data by design. It is a
  restore flow, not a merge.
- The daily testing reminder is a local notification and does not verify app
  usage; only Play Console counts the opt-in streak.
- Some Android file pickers offer Tasting Partner for unrelated JSON files. The
  app rejects files it does not recognise without changing your data.

---

## 6. Closed-testing links (copy from Play Console)

Twelve Testers asks for the tester links from **Play Console → Closed testing →
Testers**. The values below are the expected URLs, but copy the exact ones from
the console before publishing.

| Field | Expected value |
| --- | --- |
| Google Group | `<your-group>@googlegroups.com` or `https://groups.google.com/g/<your-group>` |
| Join on the web (optional) | `https://play.google.com/apps/testing/com.jlopezlabs.tastingpartner` |
| Join on Android (required) | `https://play.google.com/store/apps/details?id=com.jlopezlabs.tastingpartner` |

Do not publish the `<your-group>` placeholder. If you do not use a Google Group
for testers, fill in the group you actually created in Play Console.

---

## 7. Screenshots

Twelve Testers accepts **up to 6 screenshots**, each **5 MB or smaller**. The
repository currently has 7 English captures and 6 Spanish captures.

English set ([`screenshots/0_1_4_en/`](screenshots/0_1_4_en/), 1080×2400 PNG):

1. `Screenshot_20260903-123706.png`
2. `Screenshot_20260903-123712.png`
3. `Screenshot_20260903-123742.png`
4. `Screenshot_20260903-123749.png`
5. `Screenshot_20260903-123759.png`
6. `Screenshot_20260903-123810.png`
7. `Screenshot_20260903-123821.png`

Review them and drop the least representative one. They were captured from
**v0.1.4**, before the rating-scale, sharing, nutrition, and daily-reminder
work, so they do not show the current UI. The icon above is current.

### If you want screenshots of the current build

I could not capture Android screenshots from this environment: no physical
device is connected and the available emulator cannot start without KVM. Take
them yourself on the Android phone you use for the closed test:

1. Install the current closed-test build and create sample data: 2–3 tastings
   and 5–6 products with ratings and notes.
2. Capture 6 screens with the phone's screenshot shortcut:
   - Tastings list
   - Tasting detail with rated products
   - Add product chooser (scan / search / manual)
   - Product details with rating, note, and nutrition
   - Settings → Rating scale
   - Products tab or the Share tasting dialog
3. Remove anything private from the status bar and notifications.
4. Keep each file under 5 MB (1080×2400 PNG is fine).

Spanish alternatives are in
[`screenshots/0_1_4_es/`](screenshots/0_1_4_es/) if you want a Spanish listing.

---

## 8. Publish checklist

- [ ] Create a Twelve Testers account and verify the email address.
- [ ] Post the app with the icon and 6 screenshots above.
- [ ] Paste the description, testing instructions, feedback goals, and known
      issues from this file.
- [ ] Copy the real Google Group, web-join, and Android-join links from Play
      Console → Closed testing → Testers.
- [ ] Publish the listing.
- [ ] Send testing requests to roughly 14 other apps you would genuinely test.
      Twelve Testers is reciprocal: your listing is what you offer in return.
- [ ] Accept requests, install each partner's app, and give private feedback.
- [ ] Keep at least 12 testers opted in for 14 consecutive days, then apply for
      production access in Play Console.
