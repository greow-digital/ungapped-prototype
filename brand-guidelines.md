# Ungapped — Brand Guidelines

Extracted from current ungapped.se for visual continuity. Match feel, refine application.

## Colors

### Primary

| Role | Hex | Usage |
|---|---|---|
| Teal / Turquoise | `#1FB6B6` | Secondary CTA ("Boka demo"), accent dots, decorative elements, section pills |
| Coral / Red | `#E94B6E` | Primary CTA ("Testa gratis"), highlights |

### Neutrals

| Role | Hex |
|---|---|
| White | `#FFFFFF` |
| Off-white background | `#F8F8F8` |
| Light gray section bg | `#F4F4F4` |
| Mid gray text | `#6B6B6B` |
| Dark text | `#1A1A1A` |
| Border / divider | `#E5E5E5` |

### Accents

| Role | Hex | Usage |
|---|---|---|
| Yellow pill | `#F9D85A` | Section separator labels (rounded yellow pill with text) |
| Soft teal bg | `#E5F7F7` | Background for "Why Ungapped" cards or callouts |
| Soft coral bg | `#FCE5EA` | Optional accent backgrounds |

## Typography

- **Font family:** Open Sans, fallback to Inter, system-ui sans-serif. The current site uses a humanist sans-serif with friendly proportions.
- **Headings:** Bold (700)
- **Body:** Regular (400)
- **Buttons:** Semibold (600)

### Scale

| Element | Desktop | Mobile |
|---|---|---|
| H1 | 56px / line-height 1.1 | 36px |
| H2 | 40px / line-height 1.2 | 28px |
| H3 | 24px / line-height 1.3 | 20px |
| Body large | 18px / line-height 1.6 | 16px |
| Body | 16px / line-height 1.6 | 15px |
| Small | 14px | 13px |

## Spacing

- Section padding: 96px vertical desktop, 64px tablet, 48px mobile
- Container max-width: 1200px (centered, with horizontal padding 24-48px)
- Card padding: 32px desktop, 24px mobile
- Card gap: 24-32px in grids
- Generous whitespace is part of the brand. Don't crowd.

## Components

### Buttons

```css
/* Primary CTA */
background: #E94B6E;
color: white;
padding: 14px 28px;
border-radius: 6px;
font-weight: 600;
font-size: 16px;
border: none;
cursor: pointer;
transition: background 0.2s;
hover: background: #D43A5C;

/* Secondary CTA */
background: #1FB6B6;
color: white;
/* same shape as primary */
hover: background: #189A9A;

/* Tertiary / outline */
background: transparent;
color: #1A1A1A;
border: 2px solid #E5E5E5;
hover: border-color: #1A1A1A;
```

### Cards

```css
background: white;
border-radius: 12px;
padding: 32px;
box-shadow: 0 2px 12px rgba(0, 0, 0, 0.05);
transition: box-shadow 0.2s, transform 0.2s;
hover: box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08); transform: translateY(-2px);
```

### Section pills (yellow rounded labels)

```css
display: inline-block;
background: #F9D85A;
color: #1A1A1A;
padding: 8px 24px;
border-radius: 999px;
font-weight: 600;
font-size: 14px;
margin-bottom: 24px;
```

### Trust badges

Inline row, separated by middle-dots or vertical bars. Each badge: small icon + bolded score. Example: `Capterra 4.5★ · G2 4.3★ · Software Advice ★ · GDPR · Kollektivavtal`

### Logo carousel

- Horizontal infinite scroll, slow speed (~30s for full loop)
- Logos sized at ~40-60px height, grayscaled by default, color on hover (or always color if logos are clean)
- Pause on hover

### Step-by-step (Section 6)

- Numbered timeline (1, 2, 3, 4) with vertical line connecting (or horizontal on desktop)
- Each step: number badge (teal circle) + headline + body text + small screenshot or icon

## Voice

- **Clear, confident, Swedish-direct.** Inte poetisk, inte corporate-jargony.
- **Action-oriented.** Verb först där möjligt.
- **Honest about constraints.** "Inget kreditkort krävs" är värt mer än "frictionless onboarding".
- **Trust-signaling utan att skryta.** Visa, säg inte.
- **Som en kunnig kollega, inte en byrå.**

### Don't

- Em-dashes (`—`). Använd kolon eller punkt istället.
- "Världens bästa", "marknadsledande" utan specifik kvantifiering.
- Långa meningar. Korta är bättre.
- Anglicismer när svenska finns: använd "kommunikatör", inte "kommunikatör".

### Do

- "Sedan 2006." Konkret > vagt.
- "1000+ svenska organisationer." Kvantifierat > "many customers".
- "På svenska, från Stockholm." Geografisk konkretion = trust.

## Iconography

- Linje-stil ikoner, ~24-32px, teal eller dark gray
- Konsistent stroke-vikt
- Inte realistiska illustrationer i text-sektioner; reserverat för hero + AI-Assistent-sektion

## Imagery style

- Foton: ljusa, naturliga, svenska kontorsmiljöer eller studiomiljöer
- Inte stock-business-handshake-foton
- Produktscreenshots: faktiska UI-skärmar i deras visning
- Decorativa: teal dot patterns, soft gradient blobs (subtilt)
