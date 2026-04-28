# Signup Page — Paste-ready Prompt for Claude Code

Build a high-conversion signup page modeled after Rule.io's `Skapa konto`-page. Minimal friction left pane (form), product-focused right pane (proof of value).

---

## Prompt to paste

```
Build a signup page for Ungapped at /signup (Swedish: /skapa-konto, English: /sign-up). Reference: Rule.io's Skapa konto-page — split-pane layout with form left, product visual + proof right.

Output: signup.sv.html and signup.en.html (or one signup.html with language toggle). Reuse the brand-guidelines.md tokens.

LAYOUT:

Two-column full-viewport layout on desktop:
- LEFT PANE: ~40-45% width, white background, the form
- RIGHT PANE: ~55-60% width, soft gradient background (Ungapped coral/teal mix at low opacity), product visual + headline + proof points

On mobile: stack vertically. Form first, product visual below (or hide/simplify product visual on small screens to keep above-fold form-first).

LEFT PANE (form) — top to bottom:

1. Ungapped logo top-left (~32-40px height, link to homepage)
2. H1: "Skapa konto" / "Create account" (28-32px, bold, dark)
3. Login link below H1: "Har du redan ett konto? Logga in" / "Already have an account? Log in"
4. Google SSO button: "Fortsätt med Google" / "Continue with Google"
   - White background, gray border, Google logo on left, full-width
5. (Optional) Microsoft SSO button: "Fortsätt med Microsoft" / "Continue with Microsoft"
   - Same shape. Important for public sector buyers (Microsoft 365 is dominant)
6. "ELLER" / "OR" divider — horizontal line with text in middle
7. Email field
   - Label: "E-post" / "Email"
   - Input: type=email, required
8. Password field
   - Label: "Lösenord" / "Password"
   - Input: type=password, required
   - Show/hide toggle (eye icon)
   - Hint text below: "Minst 8 tecken" / "Minimum 8 characters"
9. Primary CTA: "Skapa konto" / "Create account"
   - Coral solid background, white text, full-width, ~48px tall, rounded 6px
10. Terms microcopy below CTA, small gray text:
    - Swedish: "Genom att skapa ett konto godkänner du våra Användarvillkor och Integritetspolicy."
    - English: "By creating an account you agree to our Terms of Service and Privacy Policy."

Form spacing: generous (16-20px between fields). Field height ~48px. Border-radius 6px. Border #E5E5E5. Focus state with coral border.

RIGHT PANE (product visual + proof) — top to bottom:

1. H2 headline (centered horizontally, top of pane):
   - Swedish: "Boosta din digitala kommunikation med Ungapped."
   - English: "Boost your digital communication with Ungapped."
2. Subheadline (centered, below headline, body-large size):
   - Swedish: "Vår intuitiva plattform gör det enkelt att skapa träffsäkra kampanjer, med eller utan avancerad kunskap."
   - English: "Our intuitive platform makes it easy to create on-target campaigns, with or without advanced expertise."

3. Large product visual (centered below subheadline):
   Show Ungapped's analytics dashboard with floating stat cards. Should signal "results you'll get from day one."
   
   Key elements to mock:
   - Tablet/laptop frame containing analytics dashboard
   - Floating card top-left: "Nya aktiva prenumeranter" / "New active subscribers" with donut chart (e.g. 135 total, split: 45% Manuell import, 20% Integration, 35% Anmälningsformulär)
   - Floating card top-right: "Öppningar / Opens 2,512 ↑+23" with trend +33.34%
   - Center: list of campaigns with metrics (Weekly news, Weekly campaigns) showing send-times, recipient counts, clicks
   - Floating card bottom-right: "Total clicks 1,707 ↑+65% from last week" with mini bar chart (Mon-Sun)
   - Floating card bottom-left: "Total skickade / Total sent 7 321 ↑+23, 100%" with progress bar
   
   All stat numbers should look real but generic enough to not be misleading. Use Ungapped brand colors for accents.

4. Decorative gradient orbs on edges of right pane (CSS only):
   - Top-left small blob: coral at 30% opacity, blurred
   - Right side: teal blob at 30% opacity, blurred
   - Bottom small blob: subtle pink/coral

5. Trust microcopy at bottom of right pane:
   - Swedish: "1000+ svenska organisationer · Capterra 4.5★ · G2 4.3★ · GDPR by default"
   - English: "1000+ European organizations · Capterra 4.5★ · G2 4.3★ · GDPR by default"

IMPLEMENTATION NOTES:

- Form validation: HTML5 native (required, type=email, minlength=8 on password). No JS validation needed for MVP — can be added later.
- Submission: form action="#" or "javascript:void(0)" for now, with a console.log("Form submitted") on submit. Erik wires real backend later.
- Google SSO button is non-functional for now (link to # or alert "Google SSO coming soon"). Same for Microsoft.
- Mobile-friendly: when viewport < 768px, hide right pane entirely (or show only headline + 2 stat cards as compressed proof). Form takes full width.
- Accessibility:
  - Form labels properly associated with inputs (`<label for="email">`)
  - SSO buttons aria-labeled
  - Password show/hide toggle aria-pressed
  - Keyboard navigation works through all fields

REUSE FROM HOMEPAGE BUILD:

- Same color tokens (coral #E94B6E, teal #1FB6B6, dark #1A1A1A, mid-gray #6B6B6B)
- Same typography (Open Sans, weights 400/600/700)
- Same button styles
- Same logo SVG
- Same trust badges (Capterra, G2)

DELIVERABLE:

Standalone signup.html (or .sv/.en variants) that opens directly. Verify at 375px (mobile, form-first), 768px (tablet, possibly side-by-side), 1024px (desktop, full split-pane), 1280px+ (large).
```

---

## How to use this prompt

1. After the homepage build is done, paste this prompt as a follow-up.
2. Claude Code will generate the signup page with the same brand tokens.
3. Validate at the four breakpoints listed.

## Why this matters (signup page conversion)

The current Ungapped flow ("Testa gratis" → ?) likely leads to a longer form with multiple fields. That's friction. Rule's split-pane approach:
- **Reduces form friction** (only email + password, plus SSO shortcuts)
- **Reinforces value at moment of decision** (right pane shows "what you get": analytics, growth, results)
- **Visual confirmation that the product is real and modern**

For Ungapped's offentlig-sektor + member-orgs ICP, **Microsoft SSO matters specifically** — Microsoft 365 is dominant in those orgs. Adding it removes a real signup blocker.

## Stretch goals (post-MVP)

- BankID as third SSO option (relevant for Swedish enterprise + offentlig sektor)
- Animated stat counters on right pane (numbers count up on load)
- Subtle background pattern animation
- Show different testimonial quote based on referrer (kommun visitors see kommun quote)
