---
title: Plukke varer | Microsoft-dokumentasjon
description: "Lageraktiviteten med å plukke varer før de er leveres eller forbrukes, utføres på ulike måter avhengig av hvordan lagerstyringsfunksjonene er satt opp. [Oppsettets](../configure-warehouse-processes.md) kompleksitet kan variere fra ingen lagerfunksjoner, via grunnleggende lagerkonfigurasjoner der bestilling for bestilling behandles ved hjelp av bare en eller flere aktiviteter, til avanserte oppsett der alle lageraktiviteter utføres i en styrt arbeidsflyt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 132408d095edbfa1a60577cdd19022920088670b
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="pick-items"></a>Plukke varer
Lageraktiviteten med å plukke varer før de er leveres eller forbrukes, utføres på ulike måter avhengig av hvordan lagerstyringsfunksjonene er satt opp. Kompleksiteten kan variere fra ingen lagerfunksjoner, via grunnleggende lagerkonfigurasjoner der bestilling for bestilling behandles ved hjelp av bare en eller flere aktiviteter, til avanserte oppsett der alle lageraktiviteter utføres i en styrt arbeidsflyt. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

Hvis du velger å organisere og registrere plukkingsaktivitet med lagerdokumenter, setter du en hake i feltet **Plukk nødv.** på lokasjonskortet. Dette angir at når du har varer som skal plukkes for et utgående kildedokument, vil du at systemet skal kontrollere plukkingen av disse varene. Et utgående kildedokument kan være en ordre, en bestillingsretur, en utgående overføringsordre, en serviceordre eller en produksjonsordre som det skal plukkes komponenter til.

> [!NOTE]
> Selv om innstillingen kalles **Plukk nødv.**, kan du bokføre følgesedler direkte fra kildedokumentet på lokasjonen der du velger denne avmerkingsboksen.

Hvis lokasjonen er definert til å kreve plukkbehandling, men ikke leveringsbehandling, bruker du vinduet **Lagerplukk** til å organisere opplysningene om plukkingen, skrive ut informasjonen om plukkingen, angi resultatet av plukkingen, og bokføre plukkingsopplysningene, noe som fører til at leveringen av varene bokføres. Hvis du plukker komponenter til en produksjonsordre, vil også forbruket bokføres når du bokfører plukkingen.

Hvis du har definert lokasjonen til å kreve både plukk- og leveringsbehandling, det vil si at du har merket av for feltet **Plukk nødv.** og **Levering nødv.** på lokasjonskortet, bruker du vinduet **Plukk** til å håndtere plukkingen. Plukk fungerer på samme måte som Lagerplukk, bortsett fra at du registrerer plukkingen i stedet for å bokføre opplysningene om den. Denne registreringsprosessen bokfører ikke leveringen, men gjør bare varene tilgjengelig for levering. Som lagerleder kan du bruke plukkforslag til å organisere opplysninger om plukking før du oppretter de enkelte plukkinstruksjonene.

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|
|------------|-------------|  
|Bokføre levering av varer direkte i det utgående bestillingsdokumentet, fordi det ikke finnes noen lagerfunksjoner. (Fungerer på samme måte som for ordrer, utgående overføringsordrer og returforsendelser.)|[Levere varer](warehouse-how-ship-items.md)|  
|Plukke varer bestilling for bestilling, og bokføre leveringen i samme aktivitet, i et grunnleggende lageroppsett.|[Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md)|
|Plukke varer for flere ordrer i et avansert lageroppsett.|[Plukke varer med lagerplukk](warehouse-how-to-pick-items-for-warehouse-shipment.md)|  
|Plukke komponenter for produksjon eller montering i et enkelt eller avansert lageroppsett.|[Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md)|  
|Planlegge optimaliserte plukkinstruksjoner for flere leveringer, i stedet for at lagermedarbeiderne skal gjøre dette i de aktuelle, bokførte leveringene.|[Planlegge plukkinger i forslaget](warehouse-how-to-plan-picks-in-worksheets.md)|  
|Plukke varer til et bestemt formål, for eksempel en produksjonsenhet som har bruk for flere komponenter, på en slik måte at varene teknisk sett ikke forlater lageret.|[Plukke og plassere uten et kildedokument](warehouse-how-to-create-put-aways-from-internal-put-aways.md)|
|Forstå hvordan du plukker varer automatisk i henhold til utløpsdatoen, for eksempel varer som ikke kan oppbevares over lang tid.|[Plukking etter FEFO](warehouse-picking-by-fefo.md)|
|Del en plukklinje i flere linjer, for eksempel fordi det ikke er nok varer å ta fra den angitte hyllen.|[Dele lageraktivitetslinjer](warehouse-how-to-split-warehouse-activity-lines.md)|
|Få tilgang umiddelbart til plukkinger som er tilordnet til deg som lagermedarbeider.|[Finne lageroppgavene dine](warehouse-how-to-find-your-warehouse-assignments.md)|  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

