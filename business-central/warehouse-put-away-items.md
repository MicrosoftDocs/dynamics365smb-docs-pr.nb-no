---
title: Plassere varer | Microsoft-dokumentasjon
description: Lageraktiviteten med å plassere varer etter at de er mottatt eller uttatt, utføres på ulike måter avhengig av hvordan lagerstyringsfunksjonene er satt opp.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e50e9e7ae7c876ad39a62bd0c0307cdb2532734b
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196047"
---
# <a name="putting-items-away"></a>Plassere varer
Lageraktiviteten med å plassere varer etter at de er mottatt eller uttatt, utføres på ulike måter avhengig av hvordan lagerstyringsfunksjonene er satt opp. Kompleksiteten kan variere fra ingen lagerfunksjoner, via grunnleggende lagerkonfigurasjoner der bestilling for bestilling behandles ved hjelp av bare en eller flere aktiviteter, til avanserte oppsett der alle lageraktiviteter utføres i en styrt arbeidsflyt. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

Hvis du velger å organisere og registrere plasseringsopplysninger med lagerdokumenter, setter du en hake i feltet **Plassering nødv.** på lokasjonskortet. Det betyr at når varer kommer inn på lagerlokasjonen via et inngående kildedokument, vil du at plukkingen av disse varene skal kontrolleres av systemet. Et inngående kildedokument kan være en bestilling, en ordreretur, en inngående overføringsordre eller en produksjonsordre med avgang som er klar til plassering.  

Hvis lokasjonen er definert til å bruke plasseringsbehandling, men ikke mottaksbehandling, bruker du siden **Lagerplassering** til å organisere opplysningene om plasseringen, skrive dem ut, angi resultatet av den aktuelle plasseringen og bokføre plasseringsopplysningene, noe som fører til at mottaksopplysningene for kildedokumentet bokføres. Når det gjelder en produksjonsordre, bokfører bokføringsprosessen avgangen for ordren og fullfører produksjonsordren.

Hvis lokasjonen er definert til å kreve både mottaksbehandling og plasseringsbehandling, det vil si at du har merket av for feltet **Mottak nødv.** og **Plassering nødv.** på lokasjonskortet, bruker du en annen fremgangsmåte når du plasserer varer. I dette tilfellet vil du bruke siden **Plassering** til å håndtere plasseringen. Plassering fungerer på samme måte som Lagerplassering, bortsett fra at du registrerer plasseringen i stedet for å bokføre opplysninger om den. Merk at registrering av lagerplassering ikke bokfører mottaket av varene. Den bare oppdaterer hylleinnholdet. Som lagerleder kan du bruke plasseringsforslag til å organisere opplysninger om plassering før du oppretter de enkelte plasseringsinstruksjonene.

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Bokfør mottaket av varer direkte fra det inngående bestillingsdokumentet og dermed registrer plasseringen, fordi det ikke finnes noe lageroppsett.|[Motta varer](warehouse-how-receive-items.md)|  
|Plassere varer bestilling for bestilling, og bokføre mottaket i samme aktivitet, i et grunnleggende lageroppsett.|[Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Plassere varer for flere ordrer i et avansert lageroppsett.|[Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  
|Plasser produserte eller monterte varer i et enkelt eller avansert lageroppsett.|[Plassere produksjonsavgang eller monteringsavgang](warehouse-how-to-put-away-production-output.md)|
|Planlegge optimaliserte plasseringsinstruksjoner for flere bokførte lagermottak, i stedet for at lagermedarbeiderne skal gjøre dette ved mottak.|[Planlegge plasseringer i forslag](warehouse-how-to-plan-put-aways-in-worksheets.md)|  
|Sette tilbake varer som ble plukket automatisk ved hjelp av en intern plukk, for eksempel til en produksjonsordre som ikke forbrukte det forventede antallet.|[Plukke og plassere uten et kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Dele en plasseringslinje for å plassere en del av antallet i plasseringen i tilgjengelige hyller, fordi den angitte hyllen er full.|[Dele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få tilgang umiddelbart til plasseringer som er tilordnet til deg som lagermedarbeider.|[Finne lageroppgavene dine](warehouse-how-to-find-your-warehouse-assignments.md)|    

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
