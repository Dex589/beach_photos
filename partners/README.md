# Beach Report local partners

`partners.json` is the list of local businesses advertised on Beach Report beach
screens (app and website). The app and site read it straight from this repo via
jsDelivr, so editing it needs no app update or website rebuild. After a change,
purge the CDN cache so it shows within minutes:

    https://purge.jsdelivr.net/gh/Dex589/beach_photos@main/partners/partners.json

**Logos and images in this folder belong to the businesses and are used with
their permission. They are NOT covered by the open licenses of the beach photos
elsewhere in this repo.** Keep contracts and contact details out of this repo;
it's public.

## One partner

```json
{
  "id": "sunset-rentals",
  "name": "Sunset Beach Rentals",
  "category": "Rentals",
  "headline": "Chairs, umbrellas & boards right on the sand",
  "body": "Family-owned since 1998. Free delivery to Pass-a-Grille and St. Pete Beach.",
  "offer": { "text": "10% off any rental", "code": "BEACHREPORT" },
  "logo": "sunset-rentals/logo.png",
  "image": "sunset-rentals/photo.jpg",
  "url": "https://example.com",
  "phone": "+17275550123",
  "address": "123 Gulf Way, St. Pete Beach, FL",
  "lat": 27.7067,
  "lon": -82.7393,
  "beaches": ["pass-a-grille", "st-pete-beach"],
  "start": "2026-11-15",
  "end": "2027-05-15",
  "kind": "partner"
}
```

- `id`: lowercase-hyphen, unique, never reused (tap counts are kept by id).
- `beaches`: Beach Report beach ids (the slug in the beach page URL) the ad shows on.
- `start` / `end`: the ad shows from `start` through `end` (inclusive). Omit `end`
  for open-ended.
- `logo` / `image`: paths inside this `partners/` folder (square logo ~256px PNG;
  photo ~1200×600 JPG, landscape). Both optional.
- `offer`, `url`, `phone`, `address`/`lat`/`lon`: optional; buttons appear for
  what's filled in (Visit, Call, Directions).
- `kind`: `"partner"` (promotion swap, labeled "Local partner") or `"sponsor"`
  (paid, labeled "Sponsored").
- Set `"paused": true` to hide an ad without deleting it.
