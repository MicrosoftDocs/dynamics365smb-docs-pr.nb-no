---
title: Administrere aktiva (inneholder video)
description: 'Les om aktivafunksjonaliteten, og få en oversikt over hvordan du arbeider med aktiva og administrere aktiva.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Administrer aktiva

Aktivafunksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] gir en oversikt over hvilke aktiva du har, og sørger for at avskrivningen er korrekt. Det hjelper deg også med å spore vedlikeholdskostnader, administrere forsikringspoliser, bokføre aktivatransaksjoner og generere ulike rapporter og statistikker.

## Hva er et aktiva?

Aktiva er forskjellige fra andre varer på lageret. Et anleggsmiddel, også kjent som en kapitaleiendel, er et konkret stykke eiendom, anlegg eller utstyr (PP &E) som du eier eller administrerer med forventning om at det vil fortsette å bidra til å generere inntekt. Et aktiva er fast når det er en vare som bedriften din ikke vil bruke, selge eller konvertere til kontanter i løpet av neste kalenderår. Anleggsmidler er forskjellige fra omløpsmidler, som er i kontanter eller planlagt å bli konvertert til kontanter i løpet av de neste 12 månedene. Aktiva er også forskjellige fra lagerbeholdningen, fordi beholdningen vanligvis forbrukes i løpet av kort tid.

## Typer av anleggsmidler

Bedrifter investerer vanligvis i noen få typer anleggsmidler. Noen eksempler er:

- Bygninger og anlegg
- Datautstyr og programvare
- Møbler og inventar
- Maskin
- Kjøretøy

## Forstå aktivaregnskap

Anleggsregnskap betyr å holde presise økonomiske poster om kapitalen din. Disse postene inneholder detaljer om de fem stadiene i et aktivums livssyklus. Etter det første kjøpet omfatter livssyklusen til hvert aktiva minst tre av følgende faser:

- Anskaffelse: Du legger til et nytt innholdselement i bøkene dine.
- Avskrivning: Du registrerer det periodiske verdifallet for et aktiva, som du bruker en avskrivningsmetode til å beregne. Hvis du vil vite mer, kan du gå til [Beregning av aktivaavskrivning](LocalFunctionality/India/FA_Depreciation.md).
- Revaluering: Du registrerer en vurdering av den nåværende virkelige markedsverdien av en eiendel. Hvis du vil vite mer, kan du gå til [Revaluere aktiva](fa-how-revalue.md).
- Forringelse: Du registrerer en verdireduksjon på grunn av hendelser eller omstendigheter.
- Avhending: Du selger, vraker eller på annen måte avhender en eiendel ved slutten av levetiden.

Revisjoner er også inkludert i de detaljerte kontrollene av selskapets regnskapsmateriale etter at du har lukket bøkene for regnskapsåret. Enten internt eller eksternt, revisjoner er der du kan legge merke til inkonsekvenser eller forskjeller mellom notatene dine og den faktiske tilstanden til eiendelene dine. Revisjoner fremmer åpenhet i eiendeler og regnskap hvis du taper mer penger enn forventet.

## Videooversikt

Følgende video dekker det grunnleggende ved aktiva:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Første oppsett av aktiva

Før du kan administrere aktiva, må du fullføre følgende oppsett:

- Standardverdier
- Aktivaregnskap
- Bokføringsgrupper og -typer
- Fordelingsnøkler
- Aktivakladder

Hvis du vil finne ut mer, går du til [Definer aktiva](fa-setup.md).

## Analyse av aktiva

Denne delen beskriver analyseverktøyene du kan bruke til å få innsikt i data om aktivaene dine..

| Til ... | Se |
| --- | --- |
| Finn ut mer om muligheter for analyse av data om aktiva. | [Oversikt over analyse av aktiva](fa-analytics-overview.md) |
| Utfør ad hoc-analyse av aktivadata direkte på listesider og spørringer. | [Ad hoc-analyse av aktivadata](ad-hoc-analysis-fa.md) |
| Utforsk Innebygde rapporter for aktiva. | [Innebygde aktivarapporter](fa-reports.md) |
| Overvåk vedlikeholdskostnader. | [Overvåk vedlikeholdskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Overvåk forsikringsdekning. | [Overvåk forsikringsdekning](fa-how-insure.md#to-monitor-insurance-coverage) |
| Vise salgsposter. | [Vis avhendingsposter](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vis forventede salgsverdier. | [Vis forventede avhendingsverdier](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Registrere aktiva

For hvert enkelt aktiva må du definere et kort som inneholder opplysninger om dem. Du kan for eksempel definere bygninger eller produksjonsutstyr som hovedaktivaer i en komponentoversikt. Du kan gruppere aktiva på forskjellige måter, for eksempel etter klasse, avdeling eller lokasjon. Deretter kan du kjøpe, vedlikeholde og selge aktiva. Du kan også definere budsjetterte aktiva. Med budsjettering kan du ta med forventede anskaffelser og salg i rapporter.

| Til  | Se |
| --- | --- |
| Administrere aktivabudsjetter, og budsjettere anskaffelseskostnader, salg av aktiva og avskrivninger. |[Administrer budsjetter for aktiva](fa-how-manage-budgets.md) |
| Opprette aktiva, tilordne avskrivningsmetoder, bokføre anskaffelser, skrapverdier og skrive ut aktivaoversikter. |[Anskaff aktiva](fa-how-acquire.md) |

## Konfigurer avskrivninger for aktivaene

Hvis du vil spore aktivaavskrivninger og andre finansielle transaksjoner for aktiva, definerer du et eller flere avskrivningstablåer for hver. Det er noen trinn for å avskrive aktivaer:

1. Kjør en rapport som beregner periodiske avskrivninger.
1. Fyll ut en kladd med de resulterende postene.
1. Bokfør kladden.

[!INCLUDE[prod_short](includes/prod_short.md)] støtter flere ulike avskrivningsmetoder. Hvis du vil ha mer informasjon, kan du gå til [Avskrivningsmetoder](fa-depreciation-methods.md). Du kan definere flere avskrivningstablåer for hver aktiva for ulike formål, for eksempel ett for mva-rapportering og et annet for intern rapportering.

| Til  | Se |
| --- | --- |
| Lær mer om ulike avskrivningsmetoder for aktiva. |[Avskrivningsmetoder](fa-depreciation-methods.md) |
| Beregne avskrivning, bokføre avskrivning og analysere avskrivning i aktivarapporter. |[Avskriv eller amortiser aktiva](fa-how-depreciate-amortize.md) |
| Vis endrede avskrivningstablåverdier. | [Vis endrede avskrivningstablåverdier](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Registrer aktivatransaksjoner manuelt på siden **Aktivafinanskladd** eller **Aktivakladd**, avhengig av om transaksjonene er for finansiell rapportering eller intern håndtering. | [Konfigurer aktivumavskrivninger](fa-how-setup-depreciation.md) |

## Vedlikehold og forsikring av anleggsmidler

Du kan registrere vedlikeholdskostnader og dato for neste service for hver aktiva. Sporing av vedlikeholdsutgifter kan være viktig for budsjettering og avgjørelser om utskiftning av aktiva. Du kan knytte hvert aktiva til en eller flere forsikringspoliser og kontrollere at polisepremiene samsvarer med verdien av aktivaene.

| Til  | Se |
| --- | --- |
| Registrere servicebesøk, bokføre vedlikeholdskostnader og overvåke vedlikeholdskostnader. |[Vedlikehold aktiva](fa-how-maintain.md) |
| Overvåk vedlikeholdskostnader. | [Overvåk vedlikeholdskostnader](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Oppdatere forsikringsopplysninger, bokføre anskaffelseskostnader til forsikringspoliser, endre forsikringsdekningen, vise forsikringsstatistikk og vise forsikringspoliser. |[Forsikre aktiva](fa-how-insure.md) |
| Overvåk forsikringsdekning. | [Overvåk forsikringsdekning](fa-how-insure.md#to-monitor-insurance-coverage) |

## Reklassifisere, overføre, dele opp / kombinere, justere verdi, nedskrive og avhende aktiva

| Til  | Se |
| --- | --- |
| Klassifisere aktiva på nytt, overføre aktiva til ulike lokasjoner, og dele opp eller knytte sammen aktiva. |[Overføre, dele opp eller kombinere aktiva](fa-how-trans-split-combine.md) |
| Justere verdier for aktiva og bokføre oppskrivnings- og nedskrivningstransaksjoner. |[Revaluer aktiva](fa-how-revalue.md) |
| Bokføre salgstransaksjoner, vise salgsposter og bokføre delvise salg. |[Avhend eller tilbaketrekk aktiva](fa-how-dispose-retire.md) |
| Vis salgsposter. | [Vis avhendingsposter](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Vis forventede salgsverdier. | [Vis forventede avhendingsverdier](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## Tips for å forbedre aktivaregnskapet

Det er et par ting du kan implementere i regnskapsstrategien for aktiva som kan bidra til å sikre at du maksimerer inntektene.

- Opprett en terskel for store bokstaver. Når du kjøper en vare, må du fastsette et fast beløp for store og små bokstaver. Beløpet bidrar til å sikre at regnskapsbøkene dine er konsistente, og gjør det lettere for deg og teamet ditt å oppdage regnskapsfeil.
- Evaluer utstyrets livssyklus på nytt. Det er viktig å beregne hvor lenge du kan bruke aktivaene til det opprinnelige formålet. Siden regnskap og avskrivning er avhengig av nøyaktige livssyklusestimater, bør du evaluere på nytt når det er nødvendig, fordi det kan endres over tid.
- Merk ressursene dine. Det er viktig å spore og merke eiendelene dine gjennom hele livssyklusen fordi mange faktorer kan påvirke verdien. Merking bidrar til å spore varene gjennom fasene av livssyklusen, og bidrar til å forhindre tyveri, eliminere feilplassering og støtte økonomisk statistikk.
- Automatiser innsikt med programvare for aktivaregnskap. Automatisering av manuelle aktiviteter for å spore dataene dine med programvare for aktivaregnskap gjør det enklere å fullføre prosesser. Passordbeskyttelse kan bare bidra til å gi tilgang til de som trenger det og er opplært til det.

## Se også

[Definer aktiva](fa-setup.md)  
[Oversikt over analyse av aktiva](fa-analytics-overview.md)  
[Oversikt over finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
