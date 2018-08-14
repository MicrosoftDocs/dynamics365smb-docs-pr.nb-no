---
title: "Slik sperrer du varer fra salg eller kjøp"
description: "I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: nb-no
ms.lasthandoff: 07/31/2018

---
# <a name="block-items-from-sales-or-purchasing"></a>Blokkere varer fra salg eller kjøp
Du kan blokkere en vare fra å bli lagt inn på salgs- eller bestillingslinjene, og du kan blokkere den fra å bli bokført i en transaksjon.  

Tabellen nedenfor viser hva som skjer når varer er sperret.  

|Alternativ|Description|  
|--------------------|------------|  
|**Sperret salg**|Du kan ikke legge inn varen i et salgsdokument eller i en salgsvarekladd.|  
|**Innkjøp blokkert**|Du kan ikke legge inn varen i et kjøpsdokument, i en varekladd for kjøp eller i kjøpsplanleggingsprosesser.|  
|**Sperret**|Du kan ikke bruke varen til noen varetransaksjon. Hvis du vil ha mer informasjon om sperring av en vare for alle formål, kan du se varekortet.|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Sperre en vare fra å legges inn på salgslinjer  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.  

Hvis du prøver å angi varen i et salgsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Sperre en vare fra å legges inn på kjøpslinjer  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.  

Hvis du prøver å angi varen i et kjøpsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.

## <a name="to-block-an-item-from-being-posted"></a>Sperre en vare fra å bli bokført
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.

Hvis du prøver å bokføre en transaksjonstype for varen, vil du få en feilmelding om at varen er sperret.

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  

