# Redactives — One Page Site

Κύριο αρχείο: `index.html` (πρώην `Redactives.dc.html` — μετονομάστηκε σε index.html για να γίνεται serve ως root page). Standalone για share: `Redactives-share.html` (re-bundle με super_inline_html μετά από αλλαγές).

## Brand
- **Γλώσσα:** Ελληνικά (τα ονόματα actives/grades/labels μένουν Αγγλικά).
- **Κόκκινο:** `#d91638` (το ΜΟΝΟ accent — όχι το παλιό #BF3331).
- **Παλέτα:** λευκό #FFFFFF, μαύρο #010101, γκρι #999A98.
- **Fonts:** Manrope (headings/body), IBM Plex Mono (δεδομένα/labels/codes).
- **Τόνος:** full clinical / pharmaceutical ledger. Tagline: "Stripped back. Built strong. Less… but better."
- **Logos:** `logo.svg` (μαύρο), `logo-white.svg` (λευκό), `logo-red.svg` (κόκκινο). Το χρώμα είναι `fill` attribute σε κάθε shape (ΟΧΙ `<style>` — δεν εφαρμόζεται σε `<img>`). Header: λευκό πάνω από βίντεο → κόκκινο στο scroll. Footer: λευκό.

## Δομή (σειρά scroll)
1. Full-width video hero (`redactives-hero.mp4`, woman video, κανονική ταχύτητα, curtain reveal, PLAY AGAIN button στο κέντρο όταν τελειώνει — όχι loop).
2. THE REDACTED TRUTH (hero copy + image slot + strikethrough animations)
3. THE NOISE (redacted INCI list)
4. THE METHOD (glossary)
5. THE GRADE SYSTEM (Dermo Activity Scale, 4 επίπεδα: LIGHT/MODERATE/ACTIVE/ULTRA ACTIVE, default LIGHT, επιλεγμένο = κόκκινο, μπάρα /4)
6. THE ACTIVES (10 προϊόντα: 5 serums + 5 creams, grid cards + filter tabs ΟΛΑ/SERUMS/CREAMS, 2 actives ανά κάρτα)
7. Delivery System, Trust strip
8. THE MANIFESTO (μαύρο section, animated strikethrough που μένει σταθερό)
9. Network / waitlist signup
10. Footer

## Interactions
- Strikethrough/redaction: `.js-strike` reveal on scroll (IntersectionObserver), μένει σταθερό.
- Header: transparent→white via IntersectionObserver sentinel.
- Tweaks (props): showGrid, animateRedactions, gradeDefault.

## Σημείωση
Το βίντεο δεν παίζει στο preview του agent (headless, χωρίς H.264 codec) — παίζει κανονικά στον browser του χρήστη.
