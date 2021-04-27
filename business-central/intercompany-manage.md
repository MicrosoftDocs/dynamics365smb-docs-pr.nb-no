---
title: Transaksjoner mellom selskaper i samme organisasjon | Microsoft-dokumentasjon
description: Med de konserninterne funksjonene kan du forenkle forretningsprosesser og transaksjoner mellom selskaper i samme organisasjon.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: fbe84deebc00b07536cda6cb36a3a0784450d62f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786151"
---
# <a name="managing-intercompany-transactions"></a>Behandle konserninterne transaksjoner
Organisasjonen kan bestå av flere selskaper, men har kanskje ikke samme antall regnskapsteam og administrative team. De konserninterne funksjonene lar deg gjøre forretninger med datterselskaper og interne partnerorganisasjoner på samme måte som med eksterne leverandører og kunder. Du angir informasjon om konserninterne transaksjoner bare én gang i de tilhørende dokumentene. Du kan bruke funksjoner du allerede kjenner, for eksempel styring av kjøp og salg. Tilordningsfunksjoner for kontoplanen og dimensjonene hjelper deg med å sikre at informasjonen vises på riktige steder.  

Det er fire hovedfordeler med de konserninterne funksjonene:  

- Økt produktivitet som et resultat av spart tid og forenklede transaksjoner  
- Redusert potensial for feil med éngangsregistrering av informasjon og systemomfattende, automatiske oppdateringer  
- Fullstendig sporing og full synlighet i forretningsaktiviteter og transaksjonslogger  
- Effektive, kostnadsbesparende transaksjoner med partner- og datterselskaper  

Du har full kontroll over alle transaksjonsdokumenter. Du kan for eksempel avvise et dokument som sendes til deg, og på den måten tilbakeføre kladdebokføringer og angre mottak/leveringer som var feil. Og når du foretar et kjøp fra et partner- eller datterselskap, kan du oppdatere bestillingen så lenge salgsselskapet ikke har sendt varene ennå.  

Når du angir en transaksjon, trenger du ikke å angi kontoene for et individuelt sett med bøker, men ganske enkelt gi identifikasjonen av partnerselskapet. De konserninterne funksjonene oppretter finanskladdelinjer som fører til balansering av bøkene i begge selskapene som er involvert i en transaksjon. I Kundekonto og Leverandørkonto kan du tilordne en konsernintern partnerkode til hvilken som helst kunde eller leverandør. Fra det øyeblikket vil alle ordrer og fakturaer som genereres i forbindelse med transaksjoner med disse selskapene, produsere tilhørende bilag i partnerselskapet, noe som fører til riktig balansering av kontoene.  

 Når du har definert forretningspartnerne som kunder og leverandører i systemet og tilordnet konserninterne partnerkoder til dem, er det mulig å utveksle konserninterne kjøps- og salgsdokumenter, inkludert varer og varegebyrer. De konserninterne funksjoenen tillater konserninterne bokføringer transaksjoner mellom selskaper mellom flere -databaser, for eksempel i forskjellige land/regioner, i tillegg til forskjellige valutaer, kontoplaner, dimensjoner og varenummereringer.  

Konsolidere økonomisk data kan være spesielt aktuelt i forbindelse med konserninterne prosesser. Hvis du vil ha mer informasjon, se [Konsolidere finansielle data fra flere selskap](finance-consolidated-company-reporting.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

|Til |Se|
|---|---|
|Opprett konserninterne leverandører og kunder som såkalte konserninterne partnere, og definer en konsernintern kontoplan.|[Oppsett av konserninternt](intercompany-how-setup.md)|
|Bruk konserninterne dokumenter eller kladder til å bokføre transaksjoner med de konserninterne partnerne.|[Arbeide med konserninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)|
|Organisere og behandle inngående og utgående transaksjoner som du kan utveksle med de konserninterne partnerne.|[Administrere den konserninterne innboksen og utboksen](intercompany-how-manage-intercompany-inbox.md)|
|Bruk konserninterne bokføringer til å fordele kost mellom partnerselskaper.|[Fordel kost til konserninterne partnere](intercompany-allocate-costs.md)|

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]