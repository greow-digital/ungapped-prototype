# Boka demo / Book a Demo — Paste-ready Prompt for Claude Code

Build a high-conversion demo booking page modeled after Funnel.io's `Schedule a personalized free consultation`-page. Two-column layout with 2-step form flow that captures emails on step 1 even if step 2 is abandoned.

---

## Prompt to paste

```
Build a demo booking page for Ungapped at /boka-demo (Swedish) and /book-a-demo (English). Reference: Funnel.io's demo page — left column with headline + description + 3 checkmark bullets, right column with a white card containing the form. Trust ratings + logo carousel below.

Output: boka-demo.sv.html and boka-demo.en.html (or one boka-demo.html with language toggle). Reuse all brand-guidelines.md tokens.

LAYOUT:

Section 1 (top, the booking section):
- Light gray background (#F4F4F4 or similar)
- Two-column grid on desktop (left ~45%, right ~55%)
- On mobile: stack vertically (left content first, form second)
- Section padding: 96px vertical desktop, 64px mobile

Section 2 (below booking section):
- White background
- Logo carousel headline: "1000+ svenska organisationer väljer Ungapped" / "1000+ European organizations choose Ungapped"
- Logo carousel (reuse same logos from homepage Section 2)

LEFT COLUMN — content:

1. Trust badges row at top (small, inline):
   - Capterra 4.5★
   - G2 4.3★
   - Style: brand logo + score + small star row, separated by spacing

2. H1 (large, bold, dark):
   - Swedish: "Boka en personlig demo"
   - English: "Book a personalized demo"

3. Description paragraph (body, mid-gray, ~3 lines):
   - Swedish: "Prata med någon i vårt team i ett oförpliktande 1:1-samtal. På 30 minuter går vi igenom:"
   - English: "Talk to a member of our team in a no-obligation, 1-to-1 call. In 30 minutes we will:"

4. Three checkmark bullets (icon + text):
   - Swedish:
     - ✓ Samla nyhetsbrev, SMS, events, enkäter och automation i en plattform
     - ✓ Hur ni kan anpassa segmentering och automation efter er data
     - ✓ Visa hur svenska organisationer använder plattformen i praktiken
   - English:
     - ✓ Bring email, SMS, events, surveys, and automation into one platform
     - ✓ Tailor segmentation and automation to your data
     - ✓ See how European organizations use the platform in practice

   Bullet styling: circular checkmark icon (teal stroke), text mid-gray, ~16-18px. 16-20px vertical spacing between bullets.

RIGHT COLUMN — form card:

White card, ~32px padding, soft drop shadow, rounded 12px corners.

THIS IS A 2-STEP FORM. Both steps live inside the same card and swap via JavaScript.

STEP 1 (initial state — minimal friction email capture):

1. Card heading (small, bold):
   - Swedish: "Boka din kostnadsfria demo"
   - English: "Schedule your free demo"

2. Sub-text (body, mid-gray):
   - Swedish: "Skriv din e-post så bokar vi en demo som passar dig."
   - English: "Share your email and we'll schedule a demo that suits you."

3. Email field:
   - Label/placeholder: "Jobb-e-post*" / "Work Email*"
   - type=email, required
   - Full-width
   - Height ~48px, rounded 6px, border #E5E5E5, focus coral border

4. CTA button below email field:
   - Swedish: "Boka demo"
   - English: "Get a demo"
   - Coral solid bg, white text, full-width or right-aligned next to email field
   - Height matches email field

5. Tiny privacy microcopy below CTA (10-12px gray):
   - Swedish: "Vi använder din e-post enbart för att kontakta dig om demon. Läs mer i vår Integritetspolicy."
   - English: "We use your email only to contact you about the demo. See our Privacy Policy."

STEP 2 (transitions in after Step 1 submit — same card, swapped content):

After Step 2 submit, transition to STEP 3 (calendar embed). The flow is 3-step: email → details → instant booking.

1. Card heading update (small, bold):
   - Swedish: "Berätta lite mer så bokar vi rätt expert till dig"
   - English: "Tell us a bit more so we can match you with the right expert"

2. Sub-text:
   - Swedish: "Vi anpassar demon efter dina verktyg och behov. Tar 30 sekunder."
   - English: "We tailor the demo to your tools and needs. Takes 30 seconds."

3. Form fields (in this order, ~16px vertical spacing):

   - Förnamn / First name (required)
   - Efternamn / Last name (required)
   - Företag / Company name (required)
   - Mobilnummer / Phone number (OPTIONAL — clearly marked "(valfritt)" / "(optional)")
   
   - Vilka verktyg är ni intresserade av? / Which tools are you interested in? (multi-select checkbox group, at least one required):
     □ Nyhetsbrev / Newsletters
     □ E-postkampanjer / Email campaigns
     □ SMS-marknadsföring / SMS marketing
     □ Enkäter & undersökningar / Surveys
     □ Eventhantering / Event management
     □ Marketing Automation
   
   - Hur många unika mottagare har ni? / How many unique recipients do you have? (dropdown, required):
     - Färre än 1 000 / Fewer than 1,000
     - 1 000–5 000 / 1,000–5,000
     - 5 000–10 000 / 5,000–10,000
     - 10 000–20 000 / 10,000–20,000
     - 20 000+ / 20,000+
     - Vet inte än / Not sure yet

4. Final CTA button:
   - Swedish: "Fortsätt till bokning"
   - English: "Continue to booking"
   - Coral solid, full-width

5. Show "Tillbaka" / "Back"-link top of step 2 (small) so user can correct email if needed.

STEP 3 (transitions in after Step 2 submit — same card, swapped content):

This step is the highest-conversion innovation: embed a calendar widget INSIDE the booking flow so qualified leads can book a time IN THE SAME SESSION instead of waiting for "we'll be in touch."

1. Card heading update:
   - Swedish: "Välj en tid som passar dig"
   - English: "Pick a time that works for you"

2. Sub-text:
   - Swedish: "Vi tar 30 minuter och anpassar demon efter [verktyg + mottagar-antal från Steg 2]."
   - English: "30 minutes, tailored to [tools + recipient-count from Step 2]."
   - Dynamic — pull values from Step 2 to show personalization

3. Embedded calendar widget:
   - Use Calendly OR Cal.com (Cal.com preferred — open source, free)
   - Implementation: `<iframe>` or vendor embed-script
   - Pre-filled with email + name from previous steps (no re-entry)
   - 30-min slots, business hours, allow next 14 days
   - On booking confirmation: show success message + send confirmation email automatically (handled by Calendly/Cal.com)

4. Mini-routing logic (advanced — implement only if backend supports):
   - If Step 2 indicated public sector + 5000+ recipients → route to procurement-expert calendar
   - If Step 2 indicated SMB / <1000 recipients → route to standard demo calendar
   - Otherwise → general team round-robin
   - For MVP build: single calendar OK, routing comes later via Chili Piper or similar

5. Show "Tillbaka" / "Back"-link top of step 3 so user can correct Step 2 details if needed

JS BEHAVIOR — Multi-step transitions (1 → 2 → 3):

- On Step 1 submit (HTML5 validation passes):
  - Capture email value
  - Send email to backend (or console.log "Email captured: x@y.com" for now — Erik will wire backend)
  - Animate transition: fade out Step 1 fields, fade in Step 2 fields (~200ms)
  - Pre-fill a hidden field with email so it's submitted with Step 2
  - URL: optional update with #step-2 anchor for analytics tracking

- On Step 2 submit:
  - HTML5 validation
  - Send full form to backend (or console.log full payload for now)
  - Show success message: "Tack! Vi kontaktar dig inom 24 timmar." / "Thanks! We'll be in touch within 24 hours."
  - Optional: redirect to thank-you page or show calendar embed

WHY THIS MATTERS (don't include in HTML, just for your understanding):

The 2-step flow is a conversion best practice for B2B demo pages:
- Step 1's low-friction email capture means abandoned forms still leave Erik with a marketable email address
- Step 2 looks less daunting because the user has already committed
- "Foot-in-the-door" psychology — users who completed step 1 are more likely to complete step 2
- Marketing-attribution-wise, you can re-engage Step 1 abandoners with retargeting

LOGO CAROUSEL (Section 2 below):

Reuse the same horizontal scrolling logo strip from the homepage. Same 12 logos, same animation. Caption above:
- Swedish: "1000+ svenska organisationer väljer Ungapped"
- English: "1000+ European organizations choose Ungapped"

ACCESSIBILITY:

- All form labels properly associated
- Required fields marked with both * AND aria-required
- Error states use aria-invalid + helper text
- Focus management on step transition: move focus to first Step 2 field
- Keyboard nav works through all fields
- Mobile: ensure form fields are at least 44x44px tap targets

DELIVERABLE:

Updated boka-demo.html (or .sv/.en variants). Verify at 375px / 768px / 1024px / 1280px. Test that:
1. Step 1 submit advances to Step 2
2. Email is captured even if user abandons Step 2
3. Step 2 submit fires (currently console.log)
4. Form is keyboard-navigable
5. Layout is clean on mobile (stack form below content)

Output a checklist of:
- What's complete (Step 1 form, Step 2 form, transition animation, validation)
- What's a placeholder (backend submission, success state behavior)
- Any decisions made not in the spec
```

---

## How to use this prompt

1. After homepage + signup are built, paste this prompt as a follow-up.
2. Claude Code generates `boka-demo.sv.html` + `boka-demo.en.html`.
3. Test the 2-step flow in browser.
4. Verify mobile layout.

## Why 2-step beats single-form for demo pages

Standard B2B SaaS demo forms ask for 6-8 fields upfront. Conversion typically 3-7%. Two-step flows:

- **Step 1 (email only):** 25-40% conversion typical. Even abandoners leave a marketable email.
- **Step 2 (full details):** 60-80% completion of those who got there.
- **Net conversion:** 15-30% on full lead, plus 10-20% of "email-only" leads that can be nurtured back.

For Ungapped specifically:
- Step 2's tool-checkbox + recipient-count question lets sales **route the lead** (offentlig sektor → procurement-rep, large company → enterprise-rep, SMB → standard demo).
- Recipient-count question doubles as **pricing-tier qualification** before the call.
- Multi-select tools indicates platform breadth interest — primer for cross-sell discussion in demo.

## Tracking events (for marketing attribution)

Mark with `data-track-event` attributes:
- `data-track-event="demo-step-1-submit"` → email captured
- `data-track-event="demo-step-2-submit"` → full lead captured
- `data-track-event="demo-step-2-abandon"` → step 1 done but step 2 abandoned (fire on page unload after step transition)
