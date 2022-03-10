---
title: Plassere varer
description: Plassering av varer etter at de er mottatt eller uttatt, utføres på ulike måter avhengig av hvordan lagerstyringsfunksjonene er satt opp.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5770, 5783, 5784, 5786, 5795, 7334, 7352, 7354, 7356, 7375, 7379, 7390, 7394, 7396, 9312, 9315, 9343
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 4643368181fa2f36c010f50ab6ce444d0a5fdce4
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8134512"
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
[Definere Warehouse Management](warehouse-setup-warehouse.md) 
[Monteringsstyring](assembly-assemble-items.md)
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]