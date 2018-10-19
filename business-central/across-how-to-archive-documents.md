---
title: "Arkivere salgs- og kjøpsdokumenter | Microsoft-dokumentasjon"
description: "Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6b1b23c062fdb1c4558a292c7aa454ae24ff3c71
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra.

## <a name="to-set-up-automatic-document-archiving"></a>Konfigurere automatisk dokumentarkivering  
Du kan konfigurere automatisk arkivering av salgs- og kjøpsordrer, tilbud, rammebestillinger og returordrer før du sletter dokumenter.

Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter. Fremgangsmåten er den samme for kjøpsdokumenter.
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Generelt bokføringsoppsett** må du fylle feltene som følger:

|Felt|Description|
|-----|-----------|
|**Arkivere tilbud**|**Aldri** for aldri å arkivere tilbud når de slettes. **Spørsmål** for å spørre brukeren om å arkivere tilbud når de slettes. **Alltid** for å arkivere tilbud automatisk når de slettes.|
|**Arkivere rammeordrer**|Velg for å arkivere rammeordrer automatisk hver gang de slettes.|
|**Arkivere ordrer og best.returer**|Velg for å arkivere ordrer automatisk hver gang de slettes.|

## <a name="to-archive-a-sales-order"></a>Arkivere ordrer
Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Åpne en ordre du vil arkivere.  
3.  Velg handlingen **Arkiver dokument**.

Ordren arkiveres. Du kan se den i vinduet **Arkiverte ordrer**. Herfra kan du også bruke det til å opprette ordren på nytt som den ble arkivert fra.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Opprette en ordre fra arkivet
Fremgangsmåten nedenfor beskriver hvordan du oppretter en ordre på nytt. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Arkiverte ordrer**, og velg deretter den relaterte koblingen.
2.  Velg den arkiverte ordren som skal opprettes på nytt, og velg deretter **Gjenopprett**-handlingen.  

Ordren opprettes og legges til i vinduet **Ordrer**.

## <a name="to-delete-archived-sales-orders"></a>Slette arkiverte ordrer
Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer. Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Slett arkiverte ordreversjoner**, og velg deretter den relaterte koblingen.  
2.  I vinduet **Slett arkiverte ordreversjoner** velger du de aktuelle filtrene.  
3.  Velg **OK**-knappen.

## <a name="see-also"></a>Se også
[Spore dokumentlinje](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

