---
title: Grunnleggende opplevelse-utvidelsen | Microsoft Docs
description: Denne utvidelsen er et moderne alternativ til Microsoft Dynamics C5.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: C5, financials, extension
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 58c8a66e9fbe1609dc2e65c764dd3c4f60b4bc54
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757345"
---
# <a name="the-basic-experience-extension"></a>Grunnleggende opplevelse-utvidelsen
Hvis du har brukt Microsoft Dynamics C5, kan Microsoft-partnere hjelpe deg med å gå over til en mer moderne løsning som er basert på [!INCLUDE[prod_short](includes/prod_short.md)], slik at du kan fortsette å nyte de samme strømlinjeformede funksjonene som Dynamics C5.

Denne utvidelsen er beregnet for små bedrifter og kan støtte opptil tre brukere. Hvis du trenger flere brukere, må du oppgradere til en [!INCLUDE[prod_short](includes/prod_short.md)]-lisens og avinstallere denne utvidelsen.

> [!NOTE]
> Per nå er denne utvidelsen bare tilgjengelig for kunder i Danmark og Island. 

## <a name="whats-available"></a>Hva som er tilgjengelig
Tabellen nedenfor beskriver funksjonene som er tilgjengelige hvis du installerer den grunnleggende opplevelsesutvidelsen.

|Distrikt  |Funksjonalitet  |
|---------|---------|
|**Finans** |Grunnleggende økonomi, kontoskjemaer, aktiva, bankbehandling, bankavstemming, betalinger, Direct Debit, dimensjoner, flere valutaer, budsjetter, arbeidsflyt, dokumentbehandling/OCR, konsolidering, ubegrensede selskaper|
|**Samlekonto (kunde) / salg** |Grunnleggende salg, salgsfakturering, salgsrabatt, prising, mva, kontakthåndtering |
|**Samlekonto (leverandør) / kjøp** |Grunnleggende kjøp, kjøpsfakturering |
|**Prosjektstyring** |Prosjekter, prosjektprising, timelister, tildeling, oppgaver, ressurser |
|**Lager** |Grunnleggende lager, vareerstatninger, varekryssreferanse |

## <a name="getting-started"></a>Komme i gang
Denne utvidelsen er litt annerledes enn de fleste, og du vil trenge hjelp fra en Microsoft-partner for å installere og konfigurere den. Slik at du vet hva du kan forvente, får du her en overordnet oversikt over hva Microsoft-partneren vil gjøre.

1. Opprett en ny [!INCLUDE[prod_short](includes/prod_short.md)]-leietaker. Dette kan være enten en prøveversjon eller en CSP-versjon.
2. Legg til minst én bruker som er tilordnet til en grunnleggende opplevelse-lisens i Azure Active Directory-kontoen.
3. Fjern alle selskaper, inkludert eksempelselskapet CRONUS.
4. Opprett et nytt selskap som ikke inneholder eksempeldata eller oppsett.
5. Legg til **Demo RapidStart**-pakken. <!--what does the pockage contain?-->
6. Last ned og installer utvidelsen for grunnleggende opplevelse fra AppSource.

## <a name="migrating-data"></a>Migrere data
Ta med Dynamics C5-dataene dine. Når Microsoft-partneren har installert den grunnleggende opplevelsesutvidelsen, vil du ha et tomt selskap. En enkel måte å flytte dataene fra Dynamics C5 til grunnleggende opplevelse er å bruke dataoverføringsutvidelsen i C5, som er inkludert i [!INCLUDE[prod_short](includes/prod_short.md)]. Utvidelsen migrerer kunder, leverandører, varer og finanskontoer og tilhørende poster.

## <a name="see-also"></a>Se også
[Utvidelsen C5-datamigrering](ui-extensions-c5-data-migration.md)