---
title: Slik sperrer du varer fra salg eller kjøp
description: I Business Central kan en vare være merket som sperret for salg, sperret for kjøp eller sperret for alt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: e13d59e939e71a252e08afc26d2fb1ec76b247c9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "917529"
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

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret salg**.  

Hvis du prøver å angi varen i et salgsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Sperre en vare fra å legges inn på kjøpslinjer  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.  
2.  Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret kjøp**.  

Hvis du prøver å angi varen i et kjøpsdokument eller kladdelinjen, vil du få en feilmelding om at varen ble sperret.

## <a name="to-block-an-item-from-being-posted"></a>Sperre en vare fra å bli bokført
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil sperre, og velg deretter avmerkingsboksen **Sperret**.

Hvis du prøver å bokføre en transaksjonstype for varen, vil du få en feilmelding om at varen er sperret.

## <a name="see-also"></a>Se også  
[Registrere nye varer](inventory-how-register-new-items.md)  
[Lager](inventory-manage-inventory.md)  
