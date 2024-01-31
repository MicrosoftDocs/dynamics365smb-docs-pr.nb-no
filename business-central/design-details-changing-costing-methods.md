---
title: Utformingsdetaljer – Endre lagermetode for varer
description: Finn ut hvordan du tilordner en annen lagermetode til en vare selv om du allerede har brukt varen i transaksjoner.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'costing methods, costing, item cost'
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Utformingsdetaljer: Endre lagermetode for varer

I [!INCLUDE[prod_short](includes/prod_short.md)] kan du ikke endre lagermetode for en vare etter at du har tatt med varen i en transaksjon. Etter at du for eksempel har kjøpt eller solgt varen. Hvis en feil lagermetode ble tilordnet varen eller varene, kan det være at du ikke oppdager problemet før du har gjort finansrapporteringen.

Dette emnet beskriver hvordan du løser dette problemet. Den anbefalte fremgangsmåten er å erstatte varen med den uriktige lagermetoden med en ny vare og bruke en monteringsordre til å overføre lageret fra den gamle varen til den nye.

> [!NOTE]
> Ved hjelp av monteringsordrer kan kostnadene fremdeles flyte selv om det finnes utestående kjøpsfakturaer eller leveringsgebyrer som skal bokføres. I tillegg kan du angre konverteringen og få antallet av de opprinnelige varene tilbake om nødvendig.

> [!TIP]
> Vi anbefaler at du starter konverteringsprosessen med én enkelt vare eller et lite sett med varer for å bli kjent med prosessen.

## Om lagermetoder

Lagermetoder styrer kostnadsberegninger når varer kjøpes, mottas på lager og selges. Lagermetoder påvirker tidsberegningen av beløp som er registrert i vareforbruk og som påvirker bruttofortjenesten. Dette er flyten som beregner vareforbruk. Solgte varers kost (vareforbruk) og inntekt brukes til å fastsette bruttofortjenesten på følgende måte:

*bruttofortjeneste* = *omsetning - vareforbruk*

Når du definerer lagervarer, må du tilordne en lagermetode. Metoden kan variere mellom ulike virksomheter og varer, så det er viktig å velge den riktige. [!INCLUDE[prod_short](includes/prod_short.md)] støtter følgende lagermetoder:

* Gjennomsnitt
* FIFO
* LIFO
* Standard
* Serienummer

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostmetoder](design-details-costing-methods.md).

## Bruk monteringsordrer til å endre tilordninger for lagermetode

Denne delen beskriver følgende fremgangsmåte for å endre lagermetoden som er tilordnet en vare:

1. Definer standard lagermetode.
2. Identifiser varene lagermetoden skal endres for, og nummerer dem på nytt.
3. Opprett nye varer med den gamle nummereringsplanen, og kopier hoveddata i en bunke.
4. Kopier relaterte hoveddata manuelt fra den eksisterende varen til den nye varen.
5. Fastsett lagerantallet som skal konverteres fra den opprinnelige varen til den nye varen.
6. Overfør lageret til den nye varen.
7. Håndter lagerantall som er tildelt behov.
8. Sperre den opprinnelige varen for ytterligere bruk.  

### Definere standard lagermetode

For å unngå fremtidige feil kan du angi en standard lagermetode for nye varer. Når noen oppretter en ny vare, foreslår [!INCLUDE[prod_short](includes/prod_short.md)] denne standard lagermetoden. Du angir standardmetoden i feltet **Standard lagermetode** på **Lageroppsett**-siden. 

### Identifisere varene lagermetoden skal endres for, og nummerere dem på nytt

Du vil kanskje gi de nye varene de samme numrene som de erstatter. Dette gjør du ved å endre numrene på de eksisterende varene. Hvis det eksisterende varenummeret for eksempel er "P1000", kan det du endrer det til "X-P1000". Dette er en manuell endring du må foreta for hver vare.

### Opprette nye varer med den gamle nummereringsplanen, og kopiere hoveddata i en bunke

Opprett de nye varene med gjeldende nummeroppsett. Med unntak av **Lagermetode**-feltet, skal de nye varene inneholde de samme hoveddataene som de eksisterende varene. Hvis du vil overføre hoveddata for varen og relaterte data fra andre funksjoner, bruker du **Kopier vare**-handlingen på **Varekort**-siden. Hvis du vil ha mer informasjon, se [Kopiere eksisterende varer for å opprette nye varer](inventory-how-copy-items.md).

Når du har opprettet de nye varene og overført hoveddata, tilordner du den riktige lagermetoden.

### Kopiere relaterte hoveddata manuelt fra den opprinnelige varen til den nye varen

Hvis du vil gjøre slik at de nye varene kan brukes, må du kopiere noen hoveddata manuelt fra andre områder, som beskrevet i tabellen nedenfor.

|Distrikt  |Hva som skal kopieres  |Hvordan du kopierer  |
|---------|---------|---------|
|Lager |Lagerføringsenheter (LFE-er) |Kontroller om det er angitt en LFE for den opprinnelige varen. Hvis det er angitt planleggingsparametere for hvert LFE-kort, må du opprette en LFE manuelt for den nye varen. Hvis parameterne ikke er angitt, kan du bruke kjørselen **Opprett lagerføringsenhet** fra **Varekort**-siden til å opprette dataene.|
| |Vareerstatninger |Kontroller om det er definert vareerstatninger for den opprinnelige varen. Hvis det finnes, overfører du disse dataene til den nye varen. Hvis du vil vise erstatningsvarer, bruker du handlingen **Erstatninger** på **Varekort**-siden. |
| |Analyserapporter |Se gjennom rapportene for vareanalyse, salgsanalyse og kjøpsanalyse. For de som refererer til de opprinnelige varene kan du opprette en ny analyserapport med en referanse til den nye varen (beholde den opprinnelige analyserapporten som historikk), eller justere rapportene slik at de refererer til den nye varen. |
| |Standardkladder |Kontroller om standardkladdene refererer til den opprinnelige varen, og overfør disse dataene til den nye varen når det er nødvendig. Denne informasjonen finnes i standardkladdene som er tilgjengelige i varekladden.  |
|Salg |Forskuddsprosenter for salg | Kontroller om forskuddsprosenter for salg er definert for den opprinnelige varen, og overfør disse dataene til den nye varen. Hvis du vil vise forskuddsprosenter, velger du **Salg** på **Varekort**-siden, og deretter **Forskuddsprosenter**.|
|Kjøp |Forskuddsprosenter for kjøp |Kontroller om forskuddsprosenter for kjøp er definert for den opprinnelige varen, og overfør disse dataene til den nye varen. Hvis du vil vise forskuddsprosenter, velger du **Kjøp** på **Varekort**-siden, og deretter **Forskuddsprosenter**. |
|Lager |Hylleinnhold |Se gjennom hylleinnholdet som er definert for den opprinnelige varen. Hvis kolonner som min. ant., maks. ant., standard og dedikert er definert enkeltvis, må du manuelt opprette hylleinnhold for den nye varen. Hvis ikke, kreves det ingen handling. [!INCLUDE[prod_short](includes/prod_short.md)] vedlikeholder postene når du registrerer lagerdokumenter og -journaler.|
|Jobb |Prosjektpriser |Kontroller om prosjektpriser er definert for den opprinnelige varen, og overfør disse dataene til den nye varen. Denne informasjonen er tilgjengelig på **Prosjektkort**-siden i delen **Prosjektdetaljer - antall priser** i **faktaboksruten**. |
|Tjeneste |Ressurskompetanse for service |Kontroller om ressurskompetanse for service er definert for den opprinnelige varen, og overfør disse dataene til den nye varen. Hvis du vil vise ressurskompetanse, bruker du handlingen **Ressurskompetanse** på **Varekort**-siden.  |
| |Servicevarekomponenter |Kontroller om komponenter er definert for den opprinnelige servicevaren, og overfør disse dataene til den nye varen. Hvis du vil vise servicevarekomponenter, bruker du **Servicevare**-handlingen på **Varekort**-sideb til å åpne listen over relaterte servicevarer, og deretter velger du **Komponenter**-handlingen.  |
|Produksjon |Prod.stykklister |Kontroller om eventuelle produksjonsstykklister inneholder den opprinnelige varen, og erstatte den med den nye varen. Hvis du vil erstatte den opprinnelige varen, velger du handlingen **Bytt ut produksjonsstykklistevare** på siden **Produksjonsstykklister**. |
|Montering |Monteringsstykklister |Kontroller om eventuelle monteringsstykklister inneholder den opprinnelige varen, og erstatte den manuelt med den nye varen. |

> [!IMPORTANT]
> Hvis den nye lagermetoden er standard, må du angi en verdi i feltet **Kostpris (standard)** på **Varekort**-siden. Du kan bruke siden **Standardkost - forslag** til å definere kostandeler i henhold til dette. Hvis du vil ha mer informasjon, kan du se [Oppdatere standardkost](finance-how-to-update-standard-costs.md).

### Fastsette lagerantallet som skal konverteres fra den opprinnelige varen til den nye varen

> [!NOTE]
> Dette trinnet tar ikke hensyn til antall som er inkludert i ikke-leverte ordrer. Hvis du vil ha mer informasjon, kan du se [Håndter lagerantall som er tildelt behov](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Bruk en vareopptellingskladd til å lage en liste over antallene på lageret. Avhengig av oppsett av lagerlokasjons bruker du ett av følgende:

* Vareopptellingskladder
* Lager opptellingskladder

Begge kladdene kan beregne lagerantallet for varen, inkludert lokasjon, variant, hylle og lagringslokasjon. Hvis du vil ha mer informasjon, se [Telle, justere og reklassifisere lagerbeholdning ved hjelp av kladder](inventory-how-count-adjust-reclassify.md)

### Overføre lageret til den nye varen

Opprett og bokfør monteringsordrer for å overføre kost og lagerantall fra den opprinnelige varen til den nye varen. Monteringsordrer kan konvertere én vare til en annen samtidig som kostnadene beholdes. Dette sikrer at nettosummene for lagerkontoen og vareforbruk ikke berøres (bortsett fra når den nye lagermetoden er standard, der kostnader distribueres til avvikskontoer). Hvis du vil ha mer informasjon, se [Monteringsstyring](assembly-assemble-items.md).

Når du oppretter monteringsordrer, bruker du opplysningene fra Vareopptellingskladder eller Lager opptellingskladd. Tabellene nedenfor beskriver informasjonen i rapportene som kan registreres i hodet og på linjene i monteringsordren.

#### Overskrift

|Felt  |Verdi å angi  |
|---------|---------|
|Varenr. |Nummeret på den nye varen. |
|Antall |Antallet i vareopptellingskladd.<br> **OBS!** Antallene som beregnes av vareopptellingskladdene, inkluderer ikke antallene i ordrer som ennå ikke er levert.  |
|Variantkode |Det samme som i vareopptellingskladd.  |
|Lokasjonskode |Det samme som i vareopptellingskladd. |
|Enhetskode |Det samme som i vareopptellingskladd. |
|Hyllekode |Det samme som i vareopptellingskladd. |

#### Linjer

|Felt  |Verdi å angi  |
|---------|---------|
|Type |Vare |
|Nr. |Nummeret på den opprinnelige varen. |
|Antall per |1 |
|Variantkode |Det samme som i vareopptellingskladd. |
|Lokasjonskode |Det samme som i vareopptellingskladd. |
|Enhetskode |Det samme som i vareopptellingskladd. |

> [!NOTE]
> En monteringsordre kan bare håndtere én LFE om gangen for en vare. Du må opprette en monteringsordre for hver LFE-kombinasjon som har et antall på lager.

> [!NOTE]
> For en lagerlokasjon må du kanskje opprette plukk før du kan bokføre monteringsordren. Du undersøker dette ved å gå gjennom oppsettet for plukking på **Lokasjonskort**-siden. Hvis du vil ha mer informasjon, kan du se [Definere varer og lokasjoner for lagerstyring](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### Håndtere lagerantall som er tildelt behov

Ideelt sett vil lageret for den opprinnelige varen gå til null etter at du har overført lagerantallene. Det kan imidlertid finnes åpne ordrer, forslag og kladder (se tabellen nedenfor) som fortsatt krever et antall av den opprinnelige varen. Antallet kan også sperres med en reservasjon eller varesporing.

**Eksempel**: Det finnes 1 000 stk. på lager, og 20 stk. er reservert for en salgsordre som ennå ikke er levert. I dette tilfellet kan du velge å beholde de 20 stk. i den gamle varen, slik at du kan oppfylle den åpne ordren.

> [!NOTE]
> Det finnes funksjonsområder som kan påvirke antallet, som vises i tabellen nedenfor, slik at det kan være vanskelig å finne riktig antall. Med utgangspunkt i eksemplet ovenfor kan du for å være på den sikre siden velge å holde 100 stk. og overføre de resterende 900 stk. i stedet. En annen måte å gjøre det på, er å behandle dokumenter og kladder slik at bare et lite håndterbart antall gjenstår. Enda et annet alternativ er å overføre hele antallet til den nye varen og deretter overføre noe av det tilbake til den opprinnelige varen ved hjelp av monteringsordren.

Tabellen nedenfor viser funksjonsområder der det kan være restantall.

|Distrikt  |Hvor det kan søkes etter restantall  |
|---------|---------|
|Salg |Salgsdokumenter, inkludert ordrer, ordrereturer, fakturaer, tilbud, rammebestillinger og kreditnotaer |
|Lager |Varekladder, reservasjoner, varesporing og standardkost – forslag |
|Kjøp |Kjøpsdokumenter, inkludert ordrer, ordrereturer, fakturaer, tilbud, rammebestillinger og kreditnotaer |
|Planlegging |Bestillingsforslag, planleggingsforslag og ordreplanlegging |
|Lager |Overføringsordrer, lagerleveringer, lagerjournaler og lagerplukkinger, plasseringer og flyttinger, interne plukkinger og plassering samt hylleopprettingsforslag |
|Montering |Monteringsdokumenter, inkludert ordrer, returordrer og rammebestillinger |
|Prosjekter |Prosjektplanleggingslinjer og prosjektkladdelinjer |
|Tjeneste |Servicedokumenter og servicekontrakter |
|Produksjon |Produksjonsordrer (planlagte, fast planlagte og frigitte) |

### Sperre den opprinnelige varen for ytterligere bruk

Når beholdningen for den opprinnelige varen er null, kan du sperre varen for å hindre at det blir brukt i nye transaksjoner. Du sperrer varen ved å aktivere **Sperret** på **Varekort**-siden. Hvis du vil ha mer informasjon, kan du se [Sperre varer fra salg eller kjøp](inventory-how-block-items.md).

## Sammendrag

Endring av lagermetoden for varer som er brukt i transaksjoner, er en prosess og ikke en standardhandling i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan bruke fremgangsmåtene som er beskrevet i dette emnet, som en mal for prosessen.

Prosessen kan ta tid fordi det er flere manuelle trinn. Når du tar deg td til å fullføre dett, vil det imidlertid redusere innvirkningen av feil i finans.

Vi anbefaler følgende:

1. Vurdere gjennomførbarheten for prosessen ved å ta én, eller kanskje noen få, representative varer gjennom hele prosessen.
2. Vurder å kontakte en erfaren partner som kan hjelpe deg med prosessen.

## Se også

[Designdetaljer: Kostmetoder](design-details-costing-methods.md)  
[Oversikt](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]