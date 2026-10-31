# Contact Entry

A free, good-looking contact entry form that runs entirely in the browser. No server, no sign-up, no database to set up — open the page and start adding contacts.

**Fields:** Name, Mobile Number, Email, City, State, Pincode, Occupation

## Features

- Add, edit and remove contacts
- Validation for Indian mobile numbers (10 digits, saved as `+91…`), email and 6-digit pincode
- Duplicate mobile number check
- Live stats: total contacts, added today, last 7 days, top occupation
- Search, filter by occupation or city, sort by date / name / city
- Export to CSV (opens in Excel, Google Sheets, GridCraft, LibreOffice) and import a CSV backup
- Live date & time widget with a time-of-day greeting
- Smooth animations while filling the form (respects "reduce motion" settings)
- Light and dark mode, works on phones (contacts turn into cards)
- Quick links to YouTube live music streams

## Privacy

Everything is stored in your browser's local storage on your device. Nothing is sent anywhere.
That also means:

- Contacts saved on one device or browser don't appear on another.
- Clearing browser data deletes your contacts — use **Download CSV** regularly as a backup, and **Import** to restore.

## Use it

**Option 1 — GitHub Pages (free hosting):**
1. Fork this repository.
2. Go to **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Open the link GitHub gives you.

**Option 2 — on your computer:** download `index.html` and double-click it.

## Make it yours

Open `index.html` and edit the `CONFIG` block at the top of the script:

```js
const CONFIG = {
  brand: "Contact Entry",
  brandLine: "Your Business · Your City",
  timeZone: "Asia/Kolkata",
  cityLabel: "Panipat time",
  defaultState: "Haryana",
  cities: ["Panipat", "Karnal", "Sonipat", "Delhi"],
  storageKey: "contact-entry:v1"
};
```

The occupation quick-pick list is the `OCCS` array just below it.

## CSV format

Exports use these columns, and imports accept the same (only `name` and `mobile` are required):

```
name,mobile,email,city,state,pincode,occupation,createdAt,updatedAt
```

## License

MIT — free to use, change and share. See [LICENSE](LICENSE).
