---
title: Administrere aktiva (inneholder video)
description: 'Les om aktivafunksjonaliteten, og få en oversikt over hvordan du arbeider med aktiva og administrere aktiva.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 03/25/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# Administrer aktiva

Aktivafunksjonene i [!INCLUDE[prod_short](includes/prod_short.md)] gir en oversikt over hvilke aktiva du har, og hjelper deg med å utføre riktig periodisk avskrivning. De hjelper deg dessuten med å styre vedlikeholdskostnadene, håndtere forsikringspoliser, bokføre aktivatransaksjoner og generere forskjellige rapporter og statistikker.

## Videooversikt

Følgende video dekker det grunnleggende ved aktiva:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## Oversikt over aktiva

For hvert enkelt aktiva må du definere et kort som inneholder opplysninger om aktivaet. Du kan definere bygninger eller produksjonsutstyr som hovedaktiva i en komponentoversikt, og du kan gruppere dem på forskjellige måter, som etter klasse, avdeling eller lokasjon. Deretter kan du begynne å kjøpe, vedlikeholde og selge aktiva. Du kan også definere budsjetterte aktiva. Med budsjettering kan du ta med forventede anskaffelser og salg i rapporter.

> [!IMPORTANT]
> Før du kan administrere aktiva, må du fullføre følgende oppsett:
>
> * Standardverdier
> * Aktivaregnskap
> * Bokføringsgrupper
> * Fordelingsnøkler
> * Aktivakladder
>
> Hvis du vil ha mer informasjon, kan du se [Definere aktiva](fa-setup.md).

Hvis du vil spore aktivaavskrivninger og andre finansielle transaksjoner for aktiva, definerer du et eller flere avskrivningstablåer for hver. Avskrivning gjøres ved å kjøre en rapport for å beregne periodiske avskrivninger, fylle ut en kladd med de resulterende postene og deretter bokføre kladden. [!INCLUDE[prod_short](includes/prod_short.md)] støtter flere ulike avskrivningsmetoder. Hvis du vil ha mer informasjon, kan du se [Avskrivningsmetoder](fa-depreciation-methods.md). Du kan definere flere avskrivningstablåer per aktiva for ulike formål, for eksempel ett for mva-rapportering og et annet for intern rapportering.

For hvert enkelt aktiva kan du registrere vedlikeholdskostnader og dato for neste service. Sporing av vedlikeholdsutgifter kan være viktig for budsjettering og avgjørelser om utskiftning av aktiva.

Du kan knytte hvert aktiva til en eller flere forsikringspoliser og kontrollere at polisepremiene samsvarer med verdien av aktivaene.

> [!NOTE]  
> Du kan registrere aktivatransaksjoner på siden **Aktivafinanskladd** eller **Aktivakladd**, avhengig av om transaksjonene er for finansiell rapportering eller intern håndtering. Hjelp for aktiva beskriver bare hvordan du bruker **Aktiva finanskladd**-siden. Hvis du vil ha mer informasjon, kan du se [Definere avskriving av aktiva](fa-how-setup-depreciation.md).

## Slik bruker du aktiva

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

| Til  | Se |
| --- | --- |
| Konfigurer forutsetning for å bruke aktivafunksjonen (definere standardverdier, aktivaregnskap, bokføringsgrupper, fordelingsnøkler, kladder og bokføringstyper). | [Definer aktiva](fa-setup.md)|
| Administrere aktivabudsjetter, og budsjettere anskaffelseskostnader, salg av aktiva og avskrivninger. |[Administrer budsjetter for aktiva](fa-how-manage-budgets.md) |
| Opprette aktiva, tilordne avskrivningsmetoder, bokføre anskaffelser, skrapverdier og skrive ut aktivaoversikter. |[Anskaff aktiva](fa-how-acquire.md) |
| Lær mer om ulike avskrivningsmetoder for aktiva. |[Avskrivningsmetoder](fa-depreciation-methods.md) |
| Beregne avskrivning, bokføre avskrivning og analysere avskrivning i aktivarapporter. |[Avskriv eller amortiser aktiva](fa-how-depreciate-amortize.md) |
| Finn ut mer om innebygde rapporterings- og analysefunksjoner for aktiva. | [Oversikt over aktivaanalyse](fa-analytics-overview.md) |
| Registrere servicebesøk, bokføre vedlikeholdskostnader og overvåke vedlikeholdskostnader. |[Vedlikehold aktiva](fa-how-maintain.md) |
| Oppdatere forsikringsopplysninger, bokføre anskaffelseskostnader til forsikringspoliser, endre forsikringsdekningen, vise forsikringsstatistikk og vise forsikringspoliser. |[Forsikre aktiva](fa-how-insure.md) |
| Klassifisere aktiva på nytt, overføre aktiva til ulike lokasjoner, og dele opp eller knytte sammen aktiva. |[Overføre, dele opp eller kombinere aktiva](fa-how-trans-split-combine.md) |
| Justere verdier for aktiva og bokføre oppskrivnings- og nedskrivningstransaksjoner. |[Revaluer aktiva](fa-how-revalue.md) |
| Bokføre salgstransaksjoner, vise salgsposter og bokføre delvise salg. |[Avhend eller tilbaketrekk aktiva](fa-how-dispose-retire.md) |


## Se også

[Definer aktiva](fa-setup.md)  
[Oversikt over aktivaanalyse](fa-analytics-overview.md)   
[Oversikt over finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
