# Tvangsmulktkalkulator.no — Full nettside-audit

**Dato:** 11. april 2026
**URL:** https://tvangsmulktkalkulator.no/
**Scope:** SEO, design, UX-copy, tilgjengelighet (WCAG 2.1 AA)

---

## 1. Sammendrag

Siden er teknisk rask, godt skrevet og løser et reelt problem ingen andre tar. On-page SEO-grunnlaget er solid med riktig title, meta description og heading-struktur. De tre største mulighetene er: **(1)** legge til structured data (FAQ + WebApplication schema) for å dominere SERPen, **(2)** fikse det visuelle gapet mellom kalkulator og innhold for å holde på brukeren, og **(3)** legge til en tydelig CTA som konverterer trafikk til verdi (lead-gen eller affiliate).

**Helhetskarakter:** Sterkt fundament — 7–8 fikser tar den fra "god MVP" til "SEO-maskin."

---

## 2. SEO-audit

### 2.1 On-page SEO

| Element | Status | Detaljer |
|---|---|---|
| **Title tag** | OK | "Tvangsmulkt-kalkulator 2026 \| Beregn boten fra Skatteetaten" — 55 tegn, inkl. primært søkeord + årstall. Solid. |
| **Meta description** | OK | "Beregn tvangsmulkt fra Skatteetaten for sen levering av mva-melding, skattemelding, a-melding og mer. Oppdatert med satser for 2026." — 131 tegn, tydelig og handlingsorientert. |
| **H1** | OK | "Tvangsmulkt-kalkulator" — én H1, primært søkeord. |
| **H2-struktur** | OK | Tre H2-er: "Hva er tvangsmulkt?", "Viktige frister", "Kan du klage?" — logisk hierarki, gode longtail-hooks. |
| **Canonical** | OK | `https://tvangsmulktkalkulator.no/` — riktig satt. |
| **lang-attributt** | OK | `nb` — riktig for norsk bokmål. |
| **robots** | OK | `index, follow` — riktig. |
| **Viewport** | OK | `width=device-width, initial-scale=1` |
| **OG:title** | OK | "Tvangsmulkt-kalkulator 2026" |
| **OG:description** | OK | "Beregn hva sen levering til Skatteetaten koster deg per dag." |
| **OG:image** | MANGLER | Ingen og:image. Deling på Facebook/LinkedIn viser generisk forhåndsvisning. |
| **Structured data** | MANGLER | Ingen JSON-LD. Stor missed opportunity for FAQ rich snippet og WebApplication. |
| **Sitemap.xml** | MANGLER | Nevnt i handlingsplanen men ikke implementert ennå. |
| **Internal links** | MANGLER | Null interne lenker. Kun 2 eksterne (Altinn og Skatteetaten). Når artiklene kommer er dette kritisk. |
| **Bilder** | N/A | Ingen bilder på siden — greit for en kalkulator, men en illustration eller ikon kunne brukes. |
| **Keyword i første 100 ord** | OK | "Tvangsmulkt" og "Skatteetaten" er begge i subtitle. |

### 2.2 Teknisk SEO

| Sjekk | Status | Detaljer |
|---|---|---|
| HTTPS | OK | Cloudflare Pages gir automatisk SSL. |
| Page speed | OK | ~6 KB statisk HTML, <100ms lastetid. Ekstremt raskt. |
| Mobile-vennlig | OK (men sjekk) | Viewport er satt, container har `max-width: 620px`. Bør verifisere at dropdown og input skalerer godt på iPhone SE-bredde. |
| Render-blocking | OK | Kun Google Fonts (DM Sans) som ekstern avhengighet. Vurder `font-display: swap` hvis ikke satt. |
| Crawlability | OK | Ingen JS-rendering nødvendig — alt innhold er i HTML. |
| Core Web Vitals | OK (estimert) | Ingen tunge bilder, scripts, eller layout shifts. Forventer grønne scorer. |
| Indexering | ADVARSEL | Siden dukker IKKE opp i Google-søk per 11. april 2026. Sannsynligvis ikke indeksert ennå — submit via Search Console umiddelbart. |

### 2.3 Keyword-muligheter

| Søkeord | Est. vanskelighet | Mulighet | Nåværende ranking | Intent | Anbefalt innhold |
|---|---|---|---|---|---|
| tvangsmulkt kalkulator | Lav | Hoy | Ikke indeksert | Transaksjonell | Nåværende side (+ schema) |
| tvangsmulkt | Moderat | Hoy | Ikke indeksert | Informasjon | Artikkel: "Hva er tvangsmulkt?" |
| tvangsmulkt skatteetaten | Lav | Hoy | Ikke indeksert | Navigasjon | Nåværende side, expand info |
| tvangsmulkt mva | Lav | Hoy | Ikke indeksert | Kommersiell | Nåværende side + artikkel |
| tvangsmulkt a-melding | Lav | Hoy | Ikke indeksert | Kommersiell | Nåværende side + artikkel |
| tvangsmulkt skattemelding | Lav | Hoy | Ikke indeksert | Kommersiell | Nåværende side + artikkel |
| klage tvangsmulkt | Lav | Hoy | Ikke indeksert | Informasjon | Artikkel: "Slik klager du" |
| tvangsmulkt satser 2026 | Lav | Hoy | Ikke indeksert | Informasjon | Nåværende side + tabell-artikkel |
| hva er tvangsmulkt | Lav | Hoy | Ikke indeksert | Informasjon | Pillar-artikkel |
| tvangsmulkt ENK | Lav | Medium | Ikke indeksert | Kommersiell | Artikkel: "Tvangsmulkt for ENK" |
| tvangsmulkt AS | Lav | Medium | Ikke indeksert | Kommersiell | Artikkel: "Tvangsmulkt for AS" |
| tvangsmulkt hvor mye | Lav | Hoy | Ikke indeksert | Transaksjonell | Nåværende side |
| forskjell tvangsmulkt tilleggsskatt | Lav | Medium | Ikke indeksert | Informasjon | Artikkel |
| frist mva-melding 2026 | Moderat | Medium | Ikke indeksert | Informasjon | Frister-artikkel |
| forsinkelsesrente skatt | Moderat | Medium | Ikke indeksert | Informasjon | Ny kalkulator |

**Konkurrenter i SERPen:** Skatteetaten.no (infoside, ikke kalkulator), Tripletex.no (bloggpost om satser), nexbal.com (guide). Ingen har en dedikert kalkulator — du eier denne nisjen.

### 2.4 Content gaps

| Gap | Hvorfor det er viktig | Format | Prioritet | Estimert innsats |
|---|---|---|---|---|
| FAQ-schema på kalkulatorsiden | Gir rich snippets i Google — mer synlig, høyere CTR | JSON-LD på eksisterende side | Hoy | 30 min |
| "Hva er tvangsmulkt?" pillar-artikkel | Dekker hoved-søkeordet, bygger topisk autoritet | Bloggpost (1500+ ord) | Hoy | 3–4 timer |
| "Slik klager du på tvangsmulkt" | Fangstnett for brukere som allerede har fått bot | Bloggpost med steg-for-steg | Hoy | 2–3 timer |
| "Alle frister for AS og ENK i 2026" | Sesongrelevant, høy søkeintensjon i mai | Bloggpost med tabell | Hoy | 2 timer |
| Sitemap.xml | Grunnleggende crawl-hygiene | XML-fil | Hoy | 15 min |
| OG-bilde | Bedre deling på sosiale medier | PNG 1200x630 | Medium | 1 time |
| "Forskjellen på tvangsmulkt og tilleggsskatt" | Forvirrende for mange — longtail-søkeord | Bloggpost | Medium | 2 timer |

### 2.5 Prioritert SEO-handlingsplan

**Gjor denne uken (quick wins):**

1. **Submit til Google Search Console** — Siden er ikke indeksert. Prioritet #1. (10 min)
2. **Lag sitemap.xml** — Én URL nå, utvides med artikler. Submit til GSC. (15 min)
3. **Legg til FAQ-schema (JSON-LD)** — Bruk H2-ene "Hva er tvangsmulkt?" og "Kan du klage?" som FAQ-items. Gir rich snippets. (30 min)
4. **Legg til WebApplication-schema** — Forteller Google at dette er et verktøy, ikke bare en infoside. (15 min)
5. **Lag og legg til OG-bilde** — Enkel grafikk: "Tvangsmulkt-kalkulator 2026" med Skatteetaten-referanse. (1 time)
6. **Legg til `font-display: swap`** — Forhindrer invisible text under font-lasting. (5 min)

**Strategiske investeringer (denne måneden):**

7. **Skriv pillar-artikkel "Hva er tvangsmulkt?"** — 1500+ ord, lenke tilbake til kalkulatoren. (4 timer)
8. **Skriv "Slik klager du"-artikkel** — Praktisk steg-for-steg, lenke til Altinn-skjema. (3 timer)
9. **Skriv frister-artikkel** — Treffer sesongtrafikk i mai. (2 timer)
10. **Bygg intern lenkestrategi** — Hver artikkel lenker til kalkulatoren, kalkulatorsiden lenker til artiklene. (Løpende)

---

## 3. Design-kritikk

### 3.1 Førsteinntrykk (2-sekunders test)

Øyet trekkes først til H1 "Tvangsmulkt-kalkulator", deretter dropdown-feltet. Formålet er umiddelbart tydelig — dette er en kalkulator. Den varme, dempede fargepaletten (off-white bakgrunn, mørk tekst, oransje accent) føles profesjonell uten å være kald. Godt gjort for en MVP.

### 3.2 Brukervennlighet

| Funn | Alvorlighet | Anbefaling |
|---|---|---|
| Kalkulatoren oppdaterer seg live uten "Beregn"-knapp | Positivt | Bra — reduserer friksjon. |
| Info-seksjonene under krever scrolling og har ingen visuell kobling til kalkulatoren | Moderat | Legg til subtile ankerpunkter eller en enkel innholdsfortegnelse under kalkulatoren. |
| Ingen tydelig neste-steg etter beregning | Moderat | Legg til en CTA: "Lever nå via Altinn" eller "Finn en regnskapsfører" etter resultatet. |
| Dropdown viser 8 alternativer uten gruppering | Minor | Vurder `<optgroup>` for å gruppere vanlige vs. sjeldne meldingstyper. |

### 3.3 Visuelt hierarki

- **Bra:** Kalkulatoren er tydelig avgrenset i hvit boks mot off-white bakgrunn. "Du må betale"-seksjonen med oransje farge skiller seg ut.
- **Problem:** Det grønne tip-boksen ("Slik unngår du tvangsmulkt") har veldig lav kontrast og føles visuelt fraværende. Teksten er grå på lysegrønn — den forsvinner.
- **Problem:** Info-seksjonene under (H2-ene) har ingen visuell differensiering — ren tekst uten kort, ikoner, eller annen visuell markering. De "flyter" og føles løsrevet fra kalkulatoren.
- **Problem:** Containerbredde er maks 620px, men sidebakgrunnen strekker seg over hele skjermen. På bred desktop (1440px+) ser siden tynn og ensom ut med >400px tomrom på hver side.

### 3.4 Konsistens

| Element | Funn | Anbefaling |
|---|---|---|
| Labels | UPPERCASE + 12.8px + letter-spacing — fungerer men er tungt å lese | Vurder sentence case + 14px for bedre lesbarhet |
| Fargebruk | Oransje brukes for "Du må betale" og maks-badge, men ingenting annet | OK, men legg til en liten fargeklatt i tip-boksen for å koble den visuelt |
| Typografi | DM Sans er et godt valg — moderne, lesbart | Bra |
| Spacing | Inkonsistent — mye plass mellom result og tip, lite mellom info-seksjonene | Jevn ut paddings |

### 3.5 Hva fungerer bra

- Ren, fokusert layout uten distraksjoner
- Live beregning uten knapp-klikk
- "Maks"-badge gir viktig kontekst
- Fargeskjemaet er behagelig og profesjonelt
- DM Sans er et utmerket typografivalg

### 3.6 Topp-prioriteringer design

1. **Stram inn spacing** mellom result-boks, tip-boks, og info-seksjonene. Fjern det visuelle gapet.
2. **Gjor tip-boksen visuelt sterkere** — den grønne bakgrunnen er for svak. Legg til ikon, sterkere bakgrunn, eller en tydelig ramme.
3. **Legg til CTA etter resultatet** — en tydelig knapp "Lever nå" eller "Finn regnskapsfører" mangler totalt.
4. **Vurder å gi info-seksjonene kort-stil** — lignende den hvite kalkulatorboksen, for å gi dem visuell vekt og konsistens.

---

## 4. UX-copy review

### 4.1 Overordnet tone

Tonen er nøktern, saklig og direkte — passende for en bruker som googler i panikk etter å ha fått varsel fra Skatteetaten. Språket er fritt for sjargong og byråkratisk stil. Godt gjort.

### 4.2 Element-for-element

| Element | Nåværende tekst | Vurdering | Forslag |
|---|---|---|---|
| **Subtitle** | "Beregn hva sen levering til Skatteetaten koster deg — oppdatert 2026" | Bra — setter kontekst og urgency. "Oppdatert 2026" bygger tillit. | OK som den er. |
| **Label 1** | "HVA HAR DU IKKE LEVERT?" | God — konversasjonell, direkte. MEN: uppercase gjør den vanskeligere å skanne. | Endre til "Hva har du ikke levert?" (sentence case). |
| **Label 2** | "ANTALL DAGER FORSINKET" | Tydelig men stiv. | "Hvor mange dager er du forsinket?" (mer naturlig) eller behold som er + sentence case. |
| **Label 3** | "ANTALL ANSATTE" | Kun synlig for a-melding/OTP — bra at den skjules dynamisk. Label-teksten endres til kontekstuelt riktig ("Ansatte med feil/mangler" / "Ansatte uten OTP"). | Smart implementasjon. |
| **Resultat: "Du må betale"** | "Du må betale" + beløp i oransje | Direkte og effektivt. Oransje farge forsterker urgency. | Perfekt. |
| **Maks-badge** | "Maks: 67 250 kr" | God — gir kontekst. Men "Maks" alene kan forvirre: maks av hva? | Vurder: "Øvre grense: 67 250 kr" eller "Maksbeløp: 67 250 kr". |
| **Tip-seksjon** | "Slik unngår du tvangsmulkt" + tekst om Fiken/Tripletex/Visma | Godt innhold, men det er en utmerket monetiserings-mulighet som nå bare er ren tekst uten lenker. | Legg til lenker til regnskapsprogram eller lead-gen CTA. |
| **"Hva er tvangsmulkt?"** | Forklarende avsnitt | Godt skrevet, kort og tydelig. Bruker "du" konsekvent. | OK. |
| **"Kan du klage?"** | "Ja. Du har rett til å klage..." | Starter med "Ja" — bra. Direkte og handlingsorientert. | Vurder å legge til en sterkere CTA: "Start klagen nå via Altinn" som knapp. |
| **Footer** | "Satser hentet fra Skatteetaten. Kalkulatoren gir et estimat..." | Bygger tillit med kilde-referanse og disclaimer. Bra. | OK. |

### 4.3 Manglende copy

| Hva mangler | Hvorfor det er viktig | Forslag |
|---|---|---|
| **CTA etter resultat** | Brukeren ser beløpet og tenker "hva nå?" — ingen veiledning. | "Lever oppgaven nå" (knapp til Altinn) + "Trenger du hjelp? Finn en regnskapsfører" |
| **Kontekst rundt "7 dager"** | Default-verdien er 7, men brukeren vet kanskje ikke hvor mange dager det har gått. | Legg til hint-tekst: "Antall dager siden fristen gikk ut" |
| **Bekreftelse / forklaring av beregningen** | Brukeren ser et tall men forstår kanskje ikke logikken. | En liten tekst: "672,50 kr/dag x 7 dager = 4 708 kr" er allerede der — bra. Men vurder en tooltip eller kort forklaring av hva "rettsgebyr" betyr. |
| **Empty state for 0 dager** | Hva skjer om brukeren skriver 0? | Vis en melding: "Ingen tvangsmulkt ennå — lever innen fristen!" |

### 4.4 Lokalisering

Siden er på norsk bokmål. `lang="nb"` er korrekt. Ingen engelske ord lekker inn. Tallformatet bruker norsk standard (mellomrom som tusenskilletegn, komma som desimalskilletegn). Alt riktig.

---

## 5. Tilgjengelighets-audit (WCAG 2.1 AA)

**Standard:** WCAG 2.1 AA | **Dato:** 11. april 2026
**Funn totalt:** 9 | **Kritisk:** 1 | **Alvorlig:** 4 | **Minor:** 4

### 5.1 Perceivable (oppfattbar)

| # | Funn | WCAG-krav | Alvorlighet | Anbefaling |
|---|---|---|---|---|
| 1 | Label-tekst (`#6b6b6b`, 12.8px) på bakgrunn (`#fafaf8`) gir ca. 4.9:1 kontrast — tangerer 4.5:1-kravet for liten tekst, men fontstørrelsen er under 14px | 1.4.3 Kontrast | Alvorlig | Øk label-farge til minst `#595959` (~6:1) eller øk font til 14px+ |
| 2 | Footer-tekst (12.8px, `#6b6b6b`) — samme kontrastproblem | 1.4.3 Kontrast | Alvorlig | Øk farge eller fontstørrelse |
| 3 | Tip-boksen: grå tekst (`#6b6b6b`) på lysegrønn bakgrunn — lav kontrast | 1.4.3 Kontrast | Alvorlig | Gjør teksten mørkere eller bakgrunnen sterkere |
| 4 | Ingen `<main>`-element — skjermlesere kan ikke identifisere hovedinnhold | 1.3.1 Semantikk | Minor | Wrap innholdet i `<main>` |

### 5.2 Operable (betjenbar)

| # | Funn | WCAG-krav | Alvorlighet | Anbefaling |
|---|---|---|---|---|
| 5 | `outline: none` på input og select — ingen synlig fokusindikator ved tastaturnavigasjon | 2.4.7 Synlig fokus | Kritisk | Legg til `:focus-visible { outline: 2px solid #c4420a; outline-offset: 2px; }` |
| 6 | Ingen skip-link ("Hopp til innhold") | 2.4.1 Skip-lenke | Minor | Legg til en skip-link som er synlig ved fokus |

### 5.3 Understandable (forståelig)

| # | Funn | WCAG-krav | Alvorlighet | Anbefaling |
|---|---|---|---|---|
| 7 | Ingen feilmelding ved ugyldig input (f.eks. negative tall, tekst i tallfeltet) | 3.3.1 Feilidentifisering | Alvorlig | Legg til validering og feilmeldinger |
| 8 | Lenken "Altinn (RF-1364)" har ingen `text-decoration` — kan forveksles med vanlig tekst | 3.2.4 Konsistens | Minor | Legg til understreking eller tydelig lenke-stil |

### 5.4 Robust

| # | Funn | WCAG-krav | Alvorlighet | Anbefaling |
|---|---|---|---|---|
| 9 | Mangler `role`-attributter og ARIA-labels for dynamiske resultat-oppdateringer | 4.1.2 Navn, rolle, verdi | Minor | Legg til `aria-live="polite"` på resultatfeltet slik at skjermlesere annonserer endringer |

### 5.5 Fargekontrast-sjekk

| Element | Forgrunn | Bakgrunn | Ratio (est.) | Krav | Bestått? |
|---|---|---|---|---|---|
| Brødtekst | `#1a1a1a` | `#fafaf8` | ~17:1 | 4.5:1 | Ja |
| H1 | `#1a1a1a` | `#fafaf8` | ~17:1 | 3:1 (stor) | Ja |
| Labels | `#6b6b6b` | `#fafaf8` | ~4.9:1 | 4.5:1 | Grenseverdi |
| "Du må betale" | `#c4420a` | `#ffeedd` (est.) | ~4.2:1 | 3:1 (stor tekst, 25.6px) | Ja |
| Footer | `#6b6b6b` | `#fafaf8` | ~4.9:1 | 4.5:1 | Grenseverdi |
| Tip-tekst | `#6b6b6b` | `#efffef` (est.) | ~4.5:1 | 4.5:1 | Grenseverdi |
| Lenker | `#1d5ba0` | `#fafaf8` | ~6.5:1 | 4.5:1 | Ja |

### 5.6 Prioriterte tilgjengelighets-fikser

1. **Legg til fokusindikator** — Kritisk. Tastaturbrukere kan ikke se hvor de er. En linje CSS fikser det.
2. **Øk label/footer-kontrast** — Tre elementer tangerer minstekravet. Gjør teksten litt mørkere.
3. **Legg til `aria-live` på resultater** — Skjermlesere annonserer ikke beregnings-endringer nå.
4. **Wrap i `<main>`** — Enkel semantisk forbedring.
5. **Legg til input-validering** — Forhindre negative tall og gi feilmeldinger.

---

## 6. Samlet prioriteringsliste (alle fire auditer)

### Gjor i dag (under 2 timer total):

| # | Hva | Kategori | Effekt | Tid |
|---|---|---|---|---|
| 1 | Submit til Google Search Console + sitemap.xml | SEO | Kritisk — ikke indeksert | 20 min |
| 2 | Legg til `:focus-visible` outline på inputs | Tilgjengelighet | Kritisk — WCAG-feil | 5 min |
| 3 | Legg til FAQ + WebApplication JSON-LD | SEO | Hoy — rich snippets | 30 min |
| 4 | Øk label/footer-farge fra `#6b6b6b` til `#595959` | Tilgjengelighet | Hoy — kontrast | 5 min |
| 5 | Wrap innhold i `<main>`, legg til `aria-live="polite"` | Tilgjengelighet | Medium | 10 min |
| 6 | Endre labels til sentence case | UX copy | Medium — lesbarhet | 5 min |
| 7 | Gjor tip-boksen visuelt sterkere | Design | Medium | 15 min |

### Gjor denne uken:

| # | Hva | Kategori | Effekt | Tid |
|---|---|---|---|---|
| 8 | Lag og legg til OG-bilde (1200x630) | SEO | Medium — social sharing | 1 time |
| 9 | Legg til CTA etter resultat ("Lever nå" / "Finn regnskapsfører") | UX/Monetisering | Hoy — konvertering | 1 time |
| 10 | Legg til input-validering + feilmeldinger | Tilgjengelighet/UX | Medium | 1 time |
| 11 | Legg til lenker i tip-boksen (Fiken/Tripletex/Visma) | Monetisering | Medium | 30 min |
| 12 | Stram inn spacing mellom seksjonene | Design | Medium | 30 min |

### Gjor denne måneden:

| # | Hva | Kategori | Effekt | Tid |
|---|---|---|---|---|
| 13 | Skriv "Hva er tvangsmulkt?" pillar-artikkel | SEO/Innhold | Hoy | 4 timer |
| 14 | Skriv "Slik klager du"-artikkel | SEO/Innhold | Hoy | 3 timer |
| 15 | Skriv "Frister for AS og ENK 2026"-artikkel | SEO/Innhold | Hoy — sesong | 2 timer |
| 16 | Bygg intern lenkestrategi mellom artikler og kalkulator | SEO | Hoy | Løpende |

---

## 7. Kode-snippets for raske fikser

### FAQ Schema (JSON-LD)
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Hva er tvangsmulkt?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Tvangsmulkt er en daglig bot Skatteetaten ilegger bedrifter som ikke leverer pliktige oppgaver innen fristen. Boten løper hver dag til du leverer, eller til du treffer maksgrensen."
      }
    },
    {
      "@type": "Question",
      "name": "Kan du klage på tvangsmulkt?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ja. Du har rett til å klage på vedtaket om tvangsmulkt. Klagefristen er seks uker. Klage sendes via Altinn (RF-1364)."
      }
    },
    {
      "@type": "Question",
      "name": "Hvor mye koster tvangsmulkt per dag i 2026?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "I 2026 er dagssatsen 672,50 kr for de fleste meldinger (mva, skattemelding, aksjonærregister). A-melding beregnes per ansatt (134,50 kr/dag). Bokføringspålegg har sats på 1 345 kr/dag."
      }
    }
  ]
}
</script>
```

### WebApplication Schema
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebApplication",
  "name": "Tvangsmulkt-kalkulator",
  "url": "https://tvangsmulktkalkulator.no",
  "applicationCategory": "FinanceApplication",
  "operatingSystem": "All",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "NOK"
  },
  "description": "Gratis kalkulator som beregner tvangsmulkt fra Skatteetaten for sen levering av mva-melding, skattemelding, a-melding og mer."
}
</script>
```

### Fokusindikator (CSS)
```css
:focus-visible {
  outline: 2px solid #c4420a;
  outline-offset: 2px;
}
```

### aria-live på resultat
```html
<div class="total-row" aria-live="polite" role="status">
  <span>Du må betale</span>
  <span id="o-total">4 708 kr</span>
</div>
```
