# Navigation Restructure — Paste-ready Prompt for Claude Code

This is a focused follow-up prompt you can give Claude Code if the main build didn't capture the nav changes precisely, or if you want to validate / refactor the navigation independently.

---

## Prompt to paste

```
Refactor the navigation on the Ungapped homepage build (ungapped-homepage-build/index.html, both .sv.html and .en.html if applicable) according to the spec below. The current ungapped.se has a busy nav with parallel hamburger menu — we're consolidating that.

GOAL: Eliminate the hamburger menu on desktop. All primary navigation visible in the main nav bar. Less B2B-internal items (Karriär, GDPR) competing with buyer-relevant items (Use cases, Resurscenter).

DESKTOP NAVIGATION (left to right):

[Logo]   Plattform ▾ | Tjänster ▾ | Use cases | Priser | Blogg | Resurscenter ▾   🔍 🌐 Logga in   [Testa gratis] [Boka demo]

Changes from current ungapped.se:
- ADD: "Use cases" link between Tjänster and Priser. Links to /use-cases (Swedish: /anvandningsfall) where industry case studies live.
- ADD: "Resurscenter" replacing the current "Inspiration". Dropdown menu containing: Blogg, Kunskapsbank (manualer), Inspiration & mallar, Partners.
- ADD: 🔍 search icon as standalone interactive element. Click should open a search overlay (placeholder OK — just a modal that says "Search coming soon" if no real search backend).
- ADD: 🌐 language switcher icon as standalone interactive element. Click opens a small dropdown listing: Svenska / English / Norsk / Dansk / Français.
- REMOVE: "Karriär" from main nav. Place it in the footer under "Företag" column.
- REMOVE: "GDPR" from main nav. Place it in the footer under "Resurser" column.
- REMOVE: "Inspiration" as standalone item. Now lives inside "Resurscenter" dropdown.
- REMOVE: The desktop hamburger menu completely. All items now in main nav.

DROPDOWNS — content for each:

Plattform ▾
- E-postmarknadsföring
- SMS-marknadsföring
- Enkäter & undersökningar
- Eventhantering
- Marketing Automation

Tjänster ▾
- Rådgivning
- Utbildning
- Integrationer & API
- Uppstartspaket
- Tilläggstjänster

Resurscenter ▾
- Blogg
- Kunskapsbank
- Inspiration & mallar
- Partners

MOBILE NAVIGATION:

On viewports below 1024px, collapse the entire main nav into ONE hamburger menu (right side). The hamburger drawer should contain:
- The full nav stack (Plattform, Tjänster, Use cases, Priser, Blogg, Resurscenter all expanded as accordion)
- Search box at top (replaces icon)
- Language switcher at bottom (replaces icon)
- Logga in + Testa gratis + Boka demo buttons at bottom

LANGUAGE SWITCHER BEHAVIOR:

The 🌐 icon click opens a small dropdown anchored to the icon. Options:
- Svenska → /sv/ or ungapped.se
- English → /en/ or ungapped.com
- Norsk → /no/ or ungapped.no
- Dansk → /da/ or ungapped.dk
- Français → /fr/ or appropriate path

For now, all entries can link to # placeholders. Erik will wire real URLs later.

FOOTER STRUCTURE (5 columns):

Column 1 — Plattform
- E-postmarknadsföring / Email marketing
- SMS-marknadsföring / SMS marketing
- Enkäter & undersökningar / Surveys
- Eventhantering / Event management
- Marketing Automation

Column 2 — Användningsområden / Use cases
- Nyhetsbrev / Newsletters
- Transaktionella mejl / Transactional email
- Kundundersökningar / Customer surveys
- Webbformulär / Web forms
- SMS-kampanjer / SMS campaigns
- Inbjudningar / Invitations

Column 3 — Tjänster / Services
- Rådgivning / Advisory
- Utbildning / Training
- Integrationer / Integrations
- Uppstartspaket / Onboarding package

Column 4 — Företag / Company
- Om oss / About
- Karriär / Careers   ← MOVED HERE FROM MAIN NAV
- Partners
- Kontakt / Contact

Column 5 — Resurser / Resources
- Blogg / Blog
- Kunskapsbank / Knowledge hub
- Inspiration & mallar / Inspiration & templates
- GDPR   ← MOVED HERE FROM MAIN NAV
- Cookies
- Sitemap

Bottom bar (full width below columns):
- Logo + tagline
- Social icons (LinkedIn, Facebook, Instagram, YouTube)
- Copyright + Liana / Ilkka Group attribution
- Newsletter signup (email field + Subscribe button)

ACCESSIBILITY:

- Search icon: aria-label="Sök" / "Search"
- Language icon: aria-label="Byt språk" / "Change language"
- Dropdowns: keyboard-navigable (Tab + Enter + Escape)
- Mobile hamburger: aria-expanded toggle

DELIVERABLE:

Updated nav HTML + CSS in index.html. If using both index.sv.html and index.en.html, apply changes to both. Verify at 375px, 768px, 1024px, 1280px viewports.
```

---

## How to use this prompt

1. Open Claude Code in the `ungapped-homepage-build/` folder.
2. After the initial build is generated, paste the prompt above.
3. Claude Code will refactor the navigation per spec.
4. Verify in browser at the four breakpoints listed.

## Why this matters

The current ungapped.se has a parallel hamburger + main nav on desktop, which is unusual pattern-breaking that adds cognitive load. The above changes eliminate that, surface buyer-relevant items (Use cases, Resurscenter) higher, and demote internal items (Karriär, GDPR) to footer — where most B2B SaaS buyers expect them.

Effekt på CRO: bättre wayfinding, lägre bounce rate på homepage, fler clicks till case studies (Use cases) och resurser. IA är fundament — påverkar alla andra optimeringar.
