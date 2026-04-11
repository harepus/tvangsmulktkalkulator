# Tvangsmulktkalkulator.no — Prosjektplan

## Hva er dette?
Gratis kalkulator som beregner tvangsmulkt (daglig bot) fra Skatteetaten for sen levering av mva-melding, skattemelding, a-melding m.m. Ingen konkurrenter i SERPen — eneste dedikerte verktøy for dette.

## Markedsgrunnlag
- 73 789 vedtak om tvangsmulkt i 2017 (433 MNOK totalt)
- 28 000 bedrifter betalte tvangsmulkt i 2021
- 215 000 risikerte tvangsmulkt bare for skattemeldingen det året
- Null eksisterende kalkulatorer — kun Skatteetatens egne infosider i SERP
- Tryti.no har dagmulkt-kalkulator, men det er for byggekontrakter (helt annet juridisk begrep)

## Målgruppe
Småbedriftseiere med ENK eller AS som nettopp fikk varsel fra Skatteetaten. Typisk: frilansere, enkeltpersonforetak, små holdingselskaper. Googler i panikk og vil ha et tall.

## Satser (2026, rettsgebyr = 1 345 kr)
| Melding | Dagssats | Maks |
|---|---|---|
| Mva-melding | 672,50 kr/dag | 67 250 kr |
| Skattemelding | 672,50 kr/dag | 67 250 kr |
| A-melding | 134,50 kr/dag per ansatt | 1 345 000 kr/periode |
| Aksjonærregister | 672,50 kr/dag | 13 450 kr |
| Særavgift | 672,50 kr/dag | 67 250 kr |
| OTP (pensjon) | 250 kr/dag per ansatt | Ingen oppgitt maks |
| Bokføringspålegg | 1 345 kr/dag | 1 000 000 kr |
| Tredjepartsopplysninger | 672,50 kr/dag | 67 250 kr |

Kilde: https://www.skatteetaten.no/en/business-and-organisation/start-and-run/deadlines-certificates-and-accounting/enforcement-fines/

## Teknisk stack
- Én statisk HTML-fil, null avhengigheter (kun Google Fonts DM Sans)
- ~6KB total, laster på <100ms
- Deployes til Cloudflare Pages (gratis)
- Domene: tvangsmulktkalkulator.no (kjøpt via Domeneshop, NS pekes til Cloudflare)

## Sesong og trafikktopper
- **30. april** — frist skattemelding → vedtak tikker inn i mai
- **31. mai** — utvidet frist næringsdrivende
- **Annenhver måned** — mva-frister (10. i oddetallsmåneder)
- **5. hver måned** — a-meldingsfrist
- **31. juli** — årsregnskap til Brønnøysund
- Peak-måneder: mai, juni, januar/februar

## Monetisering
1. **Google AdSense / Ezoic** — annonse-inntekt per sidevisning. Norsk B2B-trafikk gir ~100–200 kr RPM (inntekt per 1 000 sidevisninger)
2. **Direkte outreach til Fiken/Tripletex/Visma** — "Jeg har X besøk/mnd fra bedriftseiere som nettopp fikk bot — vil dere ha sponset plassering?" Ingen av disse har åpne affiliate-programmer per april 2026
3. **Lead-gen til Sanna** — CTA: "Har du holdingselskap? Sanna fikser regnskapet for 3 990 kr/år" (kobler til Sanna-jobben)
4. **Sjekk Ageras.no** for regnskapsfører-affiliate

## Realistisk inntekt
Med 1 000–3 000 besøk/mnd i peak (mai/juni), AdSense gir ~100–600 kr/mnd i peak. Ikke livsendrende, men passiv med null drift. Stacker med andre kalkulatorsider over tid. Sponset plassering kan gi 1 000–3 000 kr/mnd om Fiken/Tripletex biter.

## Handlingsplan

### Uke 1 (nå)
- [x] Kalkulator bygget (index.html ferdig)
- [x] Domene kjøpt (tvangsmulktkalkulator.no)
- [ ] Pek NS fra Domeneshop til Cloudflare
- [ ] Opprett Cloudflare Pages-prosjekt, push index.html
- [ ] Verifiser at siden laster på tvangsmulktkalkulator.no
- [ ] Opprett Google Search Console, submit URL til indeksering
- [ ] Opprett sitemap.xml (enkel, én URL)

### Uke 2–3
- [ ] Skriv SEO-artikkel: "Hva er tvangsmulkt? Alt du trenger å vite"
- [ ] Skriv SEO-artikkel: "Alle frister for AS og ENK i 2026"
- [ ] Skriv SEO-artikkel: "Slik klager du på tvangsmulkt (steg for steg)"
- [ ] Skriv SEO-artikkel: "Forskjellen på tvangsmulkt og tilleggsskatt"
- [ ] Sett opp Google AdSense (krev minimum noe innhold, så gjør dette etter artiklene)

### Uke 3–4 — distribusjon
- [ ] Post i Facebook-grupper: Gründer Norge, Enkeltpersonforetak Norge, Regnskap Norge
- [ ] LinkedIn-post fra egen profil: "Bygde en gratis kalkulator for tvangsmulkt"
- [ ] Reddit r/norge — svar på relevante spørsmål med lenke
- [ ] Sett opp Google Alerts for "tvangsmulkt" → svar på nye diskusjoner med lenke

### Mai (gullvinduet)
- [ ] Skattemeldingsfristen 30. april har passert — vedtak starter i mai
- [ ] Boost LinkedIn-post eller skriv ny: "30. april er passert — sjekk hva forsinkelsen koster deg"
- [ ] Kontakt Fiken/Tripletex med trafikktall og tilby sponset plassering

### Løpende
- [ ] Oppdater rettsgebyr hvert år (endres 1. januar)
- [ ] Legg til nye artikler basert på longtail-søk fra Search Console
- [ ] Vurder utvidelse til relaterte kalkulatorer (forsinkelsesrente, tilleggsskatt)

## Søkeord å målrette
- tvangsmulkt
- tvangsmulkt kalkulator
- tvangsmulkt skatteetaten
- tvangsmulkt mva
- tvangsmulkt a-melding
- tvangsmulkt skattemelding
- klage tvangsmulkt
- tvangsmulkt satser 2026
- hva er tvangsmulkt
- tvangsmulkt ENK
- tvangsmulkt AS
- tvangsmulkt hvor mye

## Lenker
- Skatteetaten tvangsmulkt: https://www.skatteetaten.no/bedrift/starte-og-drive/frister-sertifikater-og-regnskap/tvangsmulkt/
- Klage via Altinn: https://info.altinn.no/skjemaoversikt/skatteetaten/klage-pa-vedtak-om-tvangsmulkt-og-overtredelsesgebyr-rapportert-med-organisasjonsnummer/
- Skatteforvaltningsloven §14-1: https://lovdata.no/lov/2016-05-27-14/§14-1
