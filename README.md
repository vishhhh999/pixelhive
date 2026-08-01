# Pixelhive — Landing Page

AI acquisition, conversion and retention systems for service businesses.
Single-file static site. No build step, no dependencies.

## Deploy on Vercel

1. Push this repo to GitHub
2. vercel.com → Add New Project → import the repo
3. Framework preset: **Other**. No build command, no output dir. Deploy.

## Before going live — 3 required edits

All in `index.html`:

1. **Booking link** — top of the `<script>` block:
   ```js
   const BOOKING_URL = "";   // paste Calendly link here
   const CONTACT_EMAIL = "hello@pixelhive.in";
   ```
   With a Calendly link, the form opens the booking page pre-filled.
   Without one, it composes a pre-filled email instead. Both work — Calendly converts better.

2. **Case card results** — the four orange `REPLACE BEFORE LIVE` lines on the
   TEV / Bombay Bar & Grill / Yogesh / IABA cards. One documented result each
   (metric, before/after, timeframe). Only claims you can defend on a call.

3. **Testimonials** — the three dashed orange slots. One real verbatim line each
   (Peter Patel, Yogesh, +1), or delete the third card. Never publish with the
   placeholders visible.

## Optional

- Swap the placeholder hex SVG in the header/footer for the real logo mark.
- The WebGL shader falls back to a static gradient if WebGL is unavailable.

## Hard rules baked into this page (don't undo them)

- Every CTA lands on the working form at `#book` — no anchor loops
- Counters have their final value in the HTML; animation layers on top. They can never show 0
- Leak math compounds: 100 × .62 × .73 × .81 × .84 ≈ 31 → 69% lost. The cascade shows it so a prospect can check
- Guarantee is capped at 90 additional days, not open-ended
- No invented team members, no fabricated quotes
