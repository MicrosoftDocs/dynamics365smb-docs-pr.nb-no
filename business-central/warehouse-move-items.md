---
title: Flytte varer
description: Lær om å flytte varer mellom hyller i lageret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.service: dynamics365-business-central
ms.topic: Conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7315, 7349, 7351, 7382, 7384, 7386, 7387, 7399, 7400, 9314, 9330, 9345'
---
# <a name="moving-items"></a><a name="moving-items"></a>Flytte varer

Du kan flytte varer i lageret på ulike måter, avhengig av hvordan du har konfigurert lageret. Kompleksiteten kan variere:

* Små lagre kan bruke grunnleggende lageroppsett til å håndtere ordrer enkeltvis, i ett eller flere trinn.
* Store lagre kan bruke avanserte oppsett der alle lageraktiviteter koordineres med en styrt arbeidsflyt. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).

Varer må kanskje flyttes mellom hyller, for eksempel på grunn av interne operasjoner:

* En produksjonsordre krever komponenter levert eller at ferdigvarer er plassert.
* En lagerleder ønsker å optimalisere plassen.
* Ikke-planlagte flyttinger til og fra operasjoner.
* Etterplukk hyller eller butikkhyller.
* Oppdater hylleinnhold.

Telling, justering og reklassifisering av varene kan omfatte lagerppgaver som må utføres i lagerpostene før de kan synkroniseres med varepostene. Finn ut mer under [Telle, justere og reklassifisere lagerbeholdning](inventory-how-count-adjust-reclassify.md).  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til artiklene som beskriver dem.

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Flytt varer mellom lokasjoner|[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)|
|Flytte varer mellom hyller i enkle lageroppsett når som helst og uten kildedokumenter.|[Flytte varer i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)|
|Bruk lagerflytteforslaget, intern plukking og plassering til å flytte varer i avanserte lageroppsett med lagerstyring.|[Flytte varer i avanserte lageroppsett](warehouse-how-to-move-items-in-advanced-warehousing.md)|  
|Omstrukturer lageret med nye hyllekoder og nye hylleegenskaper og flytt dem eventuelt rundt.|[Omstrukturere lagre](warehouse-how-to-restructure-warehouses.md)|  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/manage-internal-warehouse-processes/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
