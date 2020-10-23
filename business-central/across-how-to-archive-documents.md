---
title: Arkivere salgs- og kjøpsdokumenter | Microsoft-dokumentasjon
description: Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer, og du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0479efcd967c7188e38fff2fb1da76e461a1bda6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3919591"
---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere ordrer, bestillinger, tilbud, ordrereturer og rammebestillinger, for eksempel fordi du vil lagre en kopi av et dokument til bruk senere. Du arkivere et salgs- eller kjøpsdokument flere ganger og lagre en annen arkiverte versjon hver gang.

For arkiverte dokumenter der originalen fortsatt finnes og ikke er bokført, kan du bruke funksjonen **Gjenopprett** til å overskrive originalen med den arkiverte versjonen av dokumentet. Dette er nyttig hvis du trenger å gjenopprette innholdet i et dokument til en tidligere tilstand.

For arkiverte dokumenter der originalen er slettet, kan du bare bruke innholdet på nytt ved å kopiere dataene, for eksempel med funksjonen **Kopier fra dokument**.   

## <a name="to-set-up-automatic-document-archiving"></a>Konfigurere automatisk dokumentarkivering  
Du kan konfigurere automatisk arkivering av salgs- og kjøpsordrer, tilbud, rammebestillinger og returordrer før du sletter dokumenter.

Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter. Fremgangsmåten er den samme for kjøpsdokumenter.
1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Generelt bokføringsoppsett** må du fylle ut følgende felt.

|Felt|Description|
|-----|-----------|
|**Arkivere tilbud**|**Aldri** for aldri å arkivere tilbud når de slettes. **Spørsmål** for å spørre brukeren om å arkivere tilbud når de slettes. **Alltid** for å arkivere tilbud automatisk når de slettes.|
|**Arkivere rammeordrer**|Velg for å arkivere rammeordrer automatisk hver gang de slettes.|
|**Arkivere ordrer og best.returer**|Velg for å arkivere ordrer automatisk hver gang de slettes.|

## <a name="to-archive-a-sales-order"></a>Arkivere ordrer
Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Åpne en ordre du vil arkivere.  
3.  Velg handlingen **Arkiver dokument**.

Ordren arkiveres. Du kan se den på siden **Arkiverte ordrer**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Slik gjenoppretter du salgordrer som ikke er bokført, fra arkivet
Følgende fremgangsmåte beskriver hvordan du tar innholdet i en arkivert ordre tilbake den opprinnelige ordren. Dette er bare mulig når det opprinnelige dokumentet ikke er bokført. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Arkiverte ordrer**, og velg deretter den relaterte koblingen.
2. Velg den arkiverte ordren, eller versjonen av den, som du vil gjenopprette, og velg deretter **Gjenopprett**-handlingen.  

Innholdet i den opprinnelige ordren erstattes med den valgte arkiverte versjonen.

## <a name="to-delete-archived-sales-orders"></a>Slette arkiverte ordrer
Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer. Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett arkiverte ordreversjoner**, og velg deretter den relaterte koblingen.  
2.  På siden **Slett arkiverte ordreversjoner** velger du de aktuelle filtrene.  
3.  Velg **OK**.

## <a name="see-also"></a>Se også
[Spore dokumentlinje](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
