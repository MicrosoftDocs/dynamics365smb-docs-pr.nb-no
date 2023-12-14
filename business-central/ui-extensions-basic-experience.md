---
title: Grunnleggende opplevelse-utvidelsen | Microsoft Docs
description: Denne utvidelsen er et moderne alternativ til Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 11/10/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---

# Grunnleggende opplevelse-utvidelsen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Hvis du har brukt Microsoft Dynamics C5, kan Microsoft-partnere hjelpe deg med å gå over til en mer moderne løsning som er basert på [!INCLUDE[prod_short](includes/prod_short.md)], slik at du kan fortsette å nyte de samme strømlinjeformede funksjonene som Dynamics C5.

Denne utvidelsen er beregnet for små bedrifter og kan støtte opptil tre brukere. Hvis du trenger flere brukere, må du oppgradere til en [!INCLUDE[prod_short](includes/prod_short.md)]-lisens og avinstallere denne utvidelsen.

> [!NOTE]
> Per nå er denne utvidelsen bare tilgjengelig til kunder i Danmark og Island.

## Hva som er tilgjengelig

Tabellen nedenfor beskriver funksjonene som er tilgjengelige hvis du installerer den grunnleggende opplevelsesutvidelsen.

|Område  |Funksjonalitet  |
|---------|---------|
|**Finans** |Grunnleggende økonomi, finansrapporter, aktiva, bankbehandling, bankavstemming, betalinger, Direct Debit, dimensjoner, flere valutaer, budsjetter, arbeidsflyt, dokumentbehandling/OCR, konsolidering, ubegrensede selskaper|
|**Kunder/salg** |Grunnleggende salg, salgsfakturering, salgsrabatt, prising, mva, kontakthåndtering |
|**Leverandør/kjøp** |Grunnleggende kjøp, kjøpsfakturering |
|**Prosjektstyring** |Prosjekter, prosjektprising, timelister, tildeling, oppgaver, ressurser |
|**Lager** |Grunnleggende lager, vareerstatninger, varekryssreferanse |

## Komme i gang

Denne utvidelsen er litt annerledes enn de fleste, og du vil trenge hjelp fra en Microsoft-partner for å installere og konfigurere den. Slik at du vet hva du kan forvente, får du her en overordnet oversikt over hva Microsoft-partneren gjør.

1. Opprett en ny [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker. Dette kan være enten en prøveversjon eller en CSP-versjon (leverandør av skytjenester).
2. Legg til minst én bruker som er tilordnet til en grunnleggende opplevelse-lisens i Microsoft Entra-kontoen.
3. Fjern alle selskaper, inkludert eksempelselskapet CRONUS.
4. Opprett et nytt selskap som ikke inneholder eksempeldata eller oppsett.
5. Legg til **Demo RapidStart**-pakken. <!--what does the package contain?-->
6. Last ned og installer utvidelsen for grunnleggende opplevelse fra AppSource.

## Overføring av data

Ta med Dynamics C5-dataene dine. Når Microsoft-partneren har installert den grunnleggende opplevelsesutvidelsen, vil du ha et tomt selskap. En enkel måte å flytte dataene fra Dynamics C5 til grunnleggende opplevelse er å bruke dataoverføringsutvidelsen i C5, som er inkludert i [!INCLUDE[prod_short](includes/prod_short.md)]. Utvidelsen migrerer kunder, leverandører, varer og finanskontoer og tilhørende poster.

## Se også

[Utvidelsen C5-datamigrering](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
