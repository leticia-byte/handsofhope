# Hands of Hope Animal Hospital — Session Notes

**Project:** Hands of Hope Animal Hospital website (handsofhopeanimalhospital.com)
**Designer:** Leticia (Letty)
**Started:** 2026-08-07
**Status:** First build — homepage direction (Milestone 1, in progress)
**Salesforce onboarding project:** https://digitalempathy.lightning.force.com/lightning/r/a00PX00000w9WlfYAE/view

## Client summary
Family-owned, privately operated general practice in Byron, GA. Owners **Dr. John Hutchens** (DVM; dermatology focus, Zoetis speaker, endoscopy incoming) and **Lauren Hutchens** (practice leadership). Explicitly *not* corporate — a core differentiator in a market where ~half of nearby practices are corporate-owned. Fear Free. "Best medicine first" ("Ritz-Carlton of vet care"), but relationship-driven and warm.

**The heart of the brand:** The practice is named for the owners' daughter, **Hope**, who has Down syndrome. The logo is her handprint (palmar crease intentionally preserved) alongside their late pets. Each of the four exam rooms is named for one of their four children. A local artist hand-painted **park-scene murals** (soft blue + pastel, Sherwin Williams palette) throughout — a signature clients love and photograph. Handle the Hope story with dignity and warmth.

## Key facts (verbatim from onboarding call 2026-06-02)
- **Address:** 6009 Watson Blvd, Suite 430, Byron, GA 31008 _(corrected by Leticia 2026-08-24; onboarding transcript had auto-garbled it as "69 Watson")_
- **Phone:** (478) 336-1999
- **Text:** (844) 786-1354 (client-to-practice, via practice mgmt software — promote it)
- **Email:** info@handsofhopeanimalhospital.com
- **Hours:** Mon–Fri 8:00am–5:30pm
- **After-hours/emergency referral:** Middle Georgia Emergency Veterinary Center
- **Mission:** "Privately owned and operated, focused on individualized best-medicine care in a Fear Free environment."
- **Awards:** Best of Middle Georgia — Best Veterinarian, 2023, 2024, 2025
- **Services:** Wellness/preventive, Dermatology (John), Dental, Surgery, Diagnostics + Ultrasound (a doctor recently certified), Fear Free/Integrative (acupuncture/chiro visiting), Endoscopy (coming), in-house pharmacy.
- **Market:** Byron/Perry/Warner Robins, near Robins AFB — heavy military + teacher, middle class. ~25% cats.
- **Domain:** on Squarespace; emails originally Google, now via Squarespace. DE given delegated domain access.
- **Request-appointment button:** currently routes to info@ email (no direct software integration) — use generic form to info@.

## Decisions this session
- **Workflow:** vet-website-designer skill (per Leticia).
- **Scope:** Homepage only for this first build (Leticia's choice).
- **Copy mode:** GENERATED — no homepage copy doc found in Drive (Alie's copy not yet written; Home Copy was due ~6/30). Copy is DE-written placeholder grounded in the onboarding call, SEO/AEO-aware, correct heading hierarchy. **All copy is provisional — swap in Alie's final homepage copy when ready.** Draft-flagged spots: reviews (placeholder), associate doctor names/bios.
- **Direction:** Mural-inspired warmth. Per client design notes, the FOUNDATION is the practice's custom interior-art palette — park blues + pastels, warm and home-like (park blue #2A6079, mural sky #CFE3EC, pastel sage #D7E3D1, warm blush #EAD3C1, warm cream #F6F2EA, slate-blue ink #213A4C). The **logo's gold (#C9A25A / accent text #8A6024) is used as the accent** to tie the site to the badge — award chips, the star, reviews eyebrow, and the logo itself. Fonts: Fraunces (headings) + Nunito Sans (body). No gradients (per skill).
- **Logo:** Real logo integrated (client-provided `handsofhope-logo.avif`, converted to `assets/handsofhope-logo.png`) in the header and footer. It's a monochrome gold circular badge — Hope's handprint with a pet's paw print inside, "Hands of Hope Animal Hospital · EST. 2022." Leticia asked to match site colors to the logo; reconciled with the client's blues-and-pastels brief by using blues/pastels as the base and the logo gold as the accent (rather than an all-gold site, which would have contradicted the brief).
- **Design-notes captured (client):** outdoorsy/park-like, blues + pastels from the interior art; warm/personal/family/home (not clinical/corporate); showcase the murals (backgrounds/design elements) — pending real mural photos; feature the artwork story incl. local artist (Christy) and her annual custom ornament tradition (added to the murals section, artist details flagged to confirm); logo's personal meaning (handprint + pet paw print + palmar crease, Down syndrome) — supported via the Story section; prefer real photography/video over stock (placeholders in use until assets arrive).

## Homepage sections built
Top utility bar (award + contact) · sticky nav (transparent→solid) · hero (split, arched frame, proof chips) · Story ("Named for Hope") · Services (6 cards) · Murals/Our Space differentiator · The Hands of Hope Difference (3 up) · Team teaser (initial avatars) · Reviews (placeholder) · FAQ (accordion) · Contact + request form · footer w/ Designed by Digital Empathy.

## Open items / TODO before this can progress or launch
1. **Homepage copy:** replace all draft copy with Alie's final homepage copy once written/approved. Never alter provided copy once received.
2. **Real assets:** logo files, team headshots, mural photos, real pet/client photos, videos — all Drive subfolders (logo, Images/Videos, Bios) are currently EMPTY. Swap placehold.co images as assets arrive.
3. **Logo:** DONE — real logo integrated in header + footer (`assets/handsofhope-logo.png`, converted from the client's .avif). If a horizontal/wordmark or higher-res vector (SVG/PDF) version exists, swap it in for crisper rendering.
   - **Murals as backgrounds:** client wants mural imagery used in backgrounds/design elements — waiting on real mural photos before adding (placeholders reference mural scenes for now).
4. **GMB link (FLAGGED):** address links currently point to a Google Maps *search* placeholder. Per DE standard, replace with the practice's real Google Business Profile place URL sitewide before launch. Could not confirm the GMB listing in this session.
5. **GTM (FLAGGED):** container ID is placeholder `GTM-XXXXXXX` in one config spot (head + noscript). Pull the real ID from Salesforce `Project__c.GTM_Code__c` (DE Brain was not authorized this session) and replace before launch.
6. **Appointment form:** prototype only — wire through JotForm per DE standard (notification to info@ with PDF attach; autoresponder from full business name to submitter). Does not submit yet.
7. **Reviews:** replace placeholder testimonials with real, attributed Google/Facebook reviews.
8. **Associate doctors:** get names, titles, headshots, bios (Dr. Kristen, Dr. Julia mentioned; one is ultrasound-certified).
9. **Emergency link:** point "Middle Georgia Emergency Veterinary Center" to their real site/GMB.
10. **When more pages are added:** extract nav + footer into shared `includes/` partials with a `load-partials.js` loader (currently inline for the single homepage), and bake the GTM snippet into the page starter so new pages inherit it.

## Environment note
Built in Cowork outputs folder (not on the Windows Claude Projects machine). Step 0 git/GitHub/Vercel scaffolding (repo `digital-brees/handsofhope`, Vercel import, robots swap at launch) still needs to be done by Leticia on the build machine. `robots.txt` (block-all) and `robots.production.txt` (allow-all) are included here to carry the convention over.

## Files
- `index.html` — homepage
- `robots.txt` / `robots.production.txt`
- `README.md`
- `session-notes.md`
