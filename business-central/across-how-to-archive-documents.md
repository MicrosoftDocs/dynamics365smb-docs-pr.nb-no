---
title: Arkiver salgs- og kjøpsdokumenter
description: Du kan arkivere ordrer og bestillinger, tilbud, returordrer og rammeordrer og gjenopprette originalene hvis du vil det.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 03/06/2022
ms.author: bholtorf
ms.openlocfilehash: c81248844f603f80304822c0ce089c666f9be9bc
ms.sourcegitcommit: 7b6d70798b4da283d1d3e38a05151df2209c2b72
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/12/2022
ms.locfileid: "8950332"
---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere ordrer, bestillinger, tilbud, returordrer og rammeordrer. Når du arkiverer dokumenter, kan du gjenopprette originalen hvis det er nødvendig. Du arkivere et salgs- eller kjøpsdokument flere ganger og lagre en annen arkiverte versjon hver gang.

For arkiverte salgsdokumenter der originalen fortsatt finnes og ikke er bokført, kan du bruke handlingen **Gjenopprett** til å overskrive nåværende dokument med en arkivert versjon. 

For arkiverte dokumenter der originalen er slettet, kan du bare bruke innholdet på nytt ved å kopiere dataene, for eksempel med handlingen **Kopier fra dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Konfigurere automatisk dokumentarkivering

Du kan konfigurere automatisk arkivering av ordrer og bestillinger, tilbud, rammebestillinger og returordrer. Når automatisk arkivering er aktivert, opprettes en ny versjon av det arkiverte dokumentet når noen gjør følgende:

* endrer eller sletter et dokument
* skriver ut, laster ned eller sender et dokument med e-post
* konverterer et tilbud til en ordre eller faktura
* bokfører en ordre

Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter. Fremgangsmåten er den samme for kjøpsdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På hurtigfanen **Arkivering** angir du om automatisk arkivering skal aktiveres for de ulike typene salgsdokumenter. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Tabellen nedenfor beskriver alternativene for feltet **Arkiver tilbud**.

|Alternativ|Description|
|------|-----------|
|**Aldri**| Ikke arkiver tilbud når de slettes.|
|**Spørsmål**|Be brukeren om å arkivere tilbud når de slettes.|
|**Alltid**|Arkiver tilbud automatisk når de slettes.|

## <a name="to-archive-a-sales-order"></a>Arkivere ordrer

Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne en ordre du vil arkivere.  
3. Velg handlingen **Arkiver dokument**.

Ordren arkiveres. Du kan se den på siden **Arkiverte ordrer**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Slik gjenoppretter du salgordrer som ikke er bokført, fra arkivet

Følgende fremgangsmåte beskriver hvordan du gjenoppretter en arkivert ordre tilbake den opprinnelige ordren. Gjenoppretting av et dokument er bare mulig når det opprinnelige dokumentet ikke er bokført. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Ordrearkiver**, og velg deretter den relaterte koblingen.
2. Velg den arkiverte ordren, eller versjonen av den, som du vil gjenopprette, og velg deretter **Gjenopprett**-handlingen.  

Innholdet i den opprinnelige ordren erstattes med den arkiverte versjonen.

## <a name="to-delete-archived-sales-orders"></a>Slette arkiverte ordrer

Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer. Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Ordrearkiver**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Slett eldre versjoner**, og velg deretter de aktuelle filtrene på siden **Slett arkiverte ordreversjoner**.  
3. Velg **OK**.

## <a name="see-also"></a>Se også

[Spore dokumentlinje](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
