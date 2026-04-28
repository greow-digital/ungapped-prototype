# Stand-out elements (Appendix B, C, D)

Tre self-contained HTML-filer som mappar mot casets "Extra — Optional but Powerful"-krav. Visuella, presenterbara, kan deployas till Vercel parallellt med prototypen.

## Filerna

| Fil | Vad | Slide-plats |
|---|---|---|
| `index.html` | **Group Marketing Dashboard** — funnel + sourced/influenced + per-brand + trend + decisions-panel | Appendix B |
| `bloodhound-campaign.html` | **Bloodhound Campaign** — 4-stegs flow-chart + cross-brand routing + KPI-band | Appendix C |
| `ai-workflow.html` | **AI Workflow** — Customer case production 6-stegs pipeline + output-explosion + principer | Appendix D |

## Hur de används

1. **För slide-decken:** Öppna varje fil i browsern, ta screenshot (helst Retina), klistra in i pitch-decken. Använd full-screen-läge (F11/Cmd+Ctrl+F) för rena bilder utan webbläsar-chrome.

2. **För live-demo i Q&A:** Hosta på Vercel under separat path från huvudprototypen, t.ex.:
   - `prototype.vercel.app/dashboard`
   - `prototype.vercel.app/bloodhound`
   - `prototype.vercel.app/ai-workflow`
   
   Eller lägg dem i samma folder och länka från Appendix-slidet.

3. **För follow-up-mail efter intervjun:** Inkludera live-länkar tillsammans med prototyp-länken.

## Deploy till Vercel (snabbinstruktion)

```bash
cd dashboard-mockup
vercel --prod
```

Eller via Vercel-dashboarden: dra-och-släpp foldern.

Kommer ge URL som `https://group-marketing-dashboard-xxxx.vercel.app`.

## Anpassningar du kan göra innan presentation

### Dashboard (`index.html`)
- Justera siffrorna i KPI-cards och funnel om du har riktiga eller mer-troliga estimat
- Byt brand-namn-ordning om du föredrar (idag: Ungapped / Profinder / Liana)
- Justera channel-attribution-confidence om du har avvikande hypotes

### Bloodhound (`bloodhound-campaign.html`)
- Justera volym-hypotesen (80–120/mån) baserat på Profinder-databas-storlek-uppskattning
- Justera conversion-multiplier-hypotesen (5–10×) om du vill vara mer/mindre konservativ
- Lägg till annan brand-routing-logik om du vill

### AI Workflow (`ai-workflow.html`)
- Lägg till specifika company-anchors där du nämner *"tested at Funnel, Refapp, Leadfeeder/Dealfront"*
- Justera tidsstämpel per steg om du har annorlunda erfarenhet
- Lägg till alternativa derivativa pieces om du vill

## Pitch-anchor (sägs när du visar respektive slide)

**Dashboard:**
> *"Det här är inte en mockup för pitchens skull — det är hur en group-CMO-dashboard borde se ut Day 30. Sex KPIs, sourced + influenced, decisions-panel överst. Det är vad ni får varje måndag morgon."*

**Bloodhound:**
> *"Det här är vad jag menar med 'Powered by Profinder'. Inget enskilt brand kan bygga den här loopen. Den kräver Profinder-data, tre brands' CRMs, och en gemensam routing-logik. När den fungerar blir varje champion som byter jobb en multiplikator."*

**AI Workflow:**
> *"Show you have done this before — det här är från min stack på Funnel och Leadfeeder. Tre dagar istället för tre veckor. Människan på rätt plats, AI på rätt plats. Inte AI som ersätter omdöme — AI som amplifierar det."*
