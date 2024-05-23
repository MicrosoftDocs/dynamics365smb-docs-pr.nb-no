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

Aktivafunksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] gir en oversikt over hvilke aktiva du har, og sørger for at avskrivningen er korrekt. De hjelper deg dessuten med å holde styr på vedlikeholdskostnadene, håndtere forsikringspoliser, bokføre aktivatransaksjoner og generere forskjellige rapporter og statistikker.

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

1. Kjør en rapport for å beregne periodisk avskrivning.
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

## Se også

[Definer aktiva](fa-setup.md)  
[Oversikt over aktivaanalyse](fa-analytics-overview.md)  
[Oversikt over finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
