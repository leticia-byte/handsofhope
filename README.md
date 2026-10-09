# Hands of Hope Animal Hospital — Homepage Prototype

First-build homepage for Hands of Hope Animal Hospital (Byron, GA), created with the DE vet-website-designer skill.

## Aesthetic direction & rationale
**Mural-inspired warmth.** The practice's signature is the hand-painted, park-scene murals throughout the hospital (soft blue + pastel). The site borrows that palette and a warm, editorial voice to deliver the owners' stated goal: *"more home than hospital."* The design leads with the deeply personal story behind the name (their daughter, Hope) and keeps the tone warm, family-forward, and premium without feeling corporate.

## Color palette
| Token | Hex | Use |
|---|---|---|
| Ink (slate-blue) | `#22384A` | Headings, body text, dark sections |
| Park blue (primary) | `#2A5F7F` | Buttons, links (white text passes WCAG AA) |
| Primary deep | `#1E4A63` | Hover states |
| Soft sky | `#CFE2ED` | Section bands |
| Pastel sage | `#D9E4D2` | "Difference" band, icons |
| Warm blush | `#EAD0BF` | Decorative accents |
| Warm cream | `#F7F3EC` | Page background |
| Gold (award) | `#8A5A1E` text | Award accents |

No CSS gradients used (per DE skill standard).

## Typography
- **Headings:** Fraunces (warm, modern serif)
- **Body:** Nunito Sans (friendly humanist sans)
- Fluid `clamp()` scale, one H1, correct H2→H3 hierarchy.

## Copy mode
**Generated** (DE-written placeholder grounded in the 2026-06-02 onboarding call). Provisional — replace with Alie's final homepage copy when ready. Draft-flagged: reviews, associate-doctor names/bios.

## Sitemap
Homepage only for this first build. Nav links currently anchor to on-page sections; they become real page links (About, Services, Team, Reviews, Contact, Careers, Blog) as the site expands.

## Assumptions made
- Practice details taken verbatim from the onboarding transcript.
- Logo is a stand-in SVG (hand cradling a heart) until real files arrive.
- All imagery is `placehold.co` with descriptive alt text — no stock people/faces used as staff, per DE image rules.

## Sections needing real content / wiring
See `session-notes.md` "Open items / TODO." Highlights: real homepage copy, logo, team + mural + pet photos, GMB link, GTM container ID, JotForm on the appointment form, real reviews.

## Accessibility
Built to WCAG 2.1 AA: skip link, visible focus rings, keyboard-operable nav/menu/accordion (Escape closes menu), one H1 + ordered headings, labeled form fields, descriptive alt text, `prefers-reduced-motion` fallback, viewport meta without `user-scalable=no`.

## Notes
Single-file homepage for review speed. When additional pages are added, extract the nav + footer into shared `includes/` partials and bake GTM into the page starter so new pages inherit tracking automatically.
