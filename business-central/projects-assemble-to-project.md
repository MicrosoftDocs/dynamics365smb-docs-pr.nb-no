---
title: Monter til prosjekt
description: Lær hvordan du bruker monter-til-ordre for prosjekt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'project management, task'
ms.search.form: '88, 275, 276, 1001, 1002, 1003, 1004, 1005, 1006, 1007, 1020'
ms.date: 08/03/2022
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="assemble-to-project"></a>Monter til prosjekt

Monter til prosjekt hjelper deg med å forbedre lagerstyringen ved å montere til ordre bare når det er nødvendig.

Når du velger en monter-til-ordre-vare på en prosjektplanleggingslinje, oppretter [!INCLUDE [prod_short](includes/prod_short.md)] en monteringsordre. Monteringsordren er basert på prosjektplanleggingslinjen, og linjene er basert på varens monteringsstykkliste. Hvis du vil ha mer informasjon om monteringsstykklister, går du til [Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md). Antall komponenter i monteringsstykklisten multipliseres med ordre antallet. Siden **Monter-til-ordrelinjer** viser detaljer om de koblede linjene for monteringsordren. Detaljene kan hjelpe deg med å tilpasse monteringsvaren. Som i salg kan du ikke bokføre koblede monteringsordrer direkte. Hvis du vil finne ut mer om monteringsordrer, kan du gå til [Selg lagervarer i monter-til-ordre-flyter](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).

Monteringsordrer er reservert for prosjekter, og [!INCLUDE [prod_short](includes/prod_short.md)] synkroniserer varesporing mellom prosjektplanleggingslinjer og monteringsordren.

## <a name="integrate-with-warehouse-management"></a>Integrer med lagerstyring

Monter til prosjekt integreres med lagerstyringsfunksjoner for å gjøre montering og levering enklere. Prosessen bidrar også til å sikre at flyten fra prosjektmontering til levering kjører problemfritt i interne lagerprosesser. Hvis du vil lære mer om interne lagerflyter for prosjekter, kan du gå til [Flyter for produksjon, montering og prosjekter](design-details-internal-warehouse-flows.md#flows-to-and-from-assembly-in-a-basic-warehouse-configuration).

Tabellen nedenfor beskriver lagerkonfigurasjonene som monter-til-ordre støtter

|Konfigurasjon  |Description  |
|---------|---------|
|**Ingen lagerhåndtering**|Bruk en prosjektkladd til å bokføre fullstendig eller delvis forbruk. Produksjon og forbruk av komponenter bokføres automatisk for monteringsordren.         |
|**Beholdningsplukk**|Bruk beholdningsplukk til å bokføre fullstendig eller delvis forbruk. Produksjon og forbruk av komponenter bokføres automatisk for monteringsordren.          |
|**Lagerplukk**|Opprett og registrer lagerplukk for komponenter, og bruk deretter en prosjektkladd til å bokføre forbruk. [!INCLUDE [prod_short](includes/prod_short.md)] verifiserer om de forbrukte monteringskomponentene ble plukket. Produksjon og forbruk av komponenter bokføres automatisk for monteringsordren.         |

## <a name="known-limitations"></a>Kjente begrensninger

Denne delen beskriver kjente begrensninger for monter til prosjekt.

* Feltet **Antall som skal monteres til ordre** er ikke tilgjengelig for prosjekter som er lukket.
* For lagerplukkscenarier kan **Antall som skal monteres for ordre** være enten null eller lik antallet. Du kan ikke blande montere til ordre og montere til lager på en prosjektplanleggingslinje. Du må opprette separate prosjektplanleggingslinjer.
* Monter til ordre påvirker ikke fakturerbare deler av et prosjekt. En montering er inkludert på salgsfakturaer, men ikke dens komponenter. Du kan ikke redigere feltet **Antall som skal monteres til ordre** for fakturerbare linjer.
* Ordreplanleggingen og planleggingsforslaget påvirkes ikke fordi prosjektet er inndataene for planleggingen. Planleggingsmotoren anser monteringen som behov.
* Du kan ikke angi et negativt antall i feltet **Antall som skal monteres til ordre**.
* Du kan ikke angre en montering.

## <a name="see-also"></a>Se også

[Prosjektstyring](projects-manage-projects.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Opprett prosjekter](projects-how-create-jobs.md)
