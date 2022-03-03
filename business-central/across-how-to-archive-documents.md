---
title: Arkiver salgs- og kjøpsdokumenter
description: Du kan arkivere salgs- og kjøpsordrer, tilbud, ordrereturer og rammeordrer slik at du kan bruke det arkiverte dokumentet til å gjenopprette dokumentet som den ble arkivert fra.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349
ms.date: 06/29/2021
ms.author: edupont
ms.openlocfilehash: dcb99e2c1231e95fca2eb9f8c36fc363a193cd82
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141628"
---
# <a name="archive-documents"></a>Arkivere dokumenter
Du kan arkivere ordrer, bestillinger, tilbud, ordrereturer og rammebestillinger, for eksempel fordi du vil lagre en kopi av et dokument til bruk senere. Du arkivere et salgs- eller kjøpsdokument flere ganger og lagre en annen arkiverte versjon hver gang.

For arkiverte salgsdokumenter der originalen fortsatt finnes og ikke er bokført, kan du bruke funksjonen **Gjenopprett** til å overskrive originalen med den arkiverte versjonen av dokumentet. Dette er nyttig hvis du trenger å gjenopprette innholdet i et dokument til en tidligere tilstand.

For arkiverte dokumenter der originalen er slettet, kan du bare bruke innholdet på nytt ved å kopiere dataene, for eksempel med funksjonen **Kopier fra dokument**.  

## <a name="to-set-up-automatic-document-archiving"></a>Konfigurere automatisk dokumentarkivering

Du kan konfigurere automatisk arkivering av salgs- og kjøpsordrer, tilbud, rammebestillinger og returordrer før du sletter dokumenter.

Fremgangsmåten nedenfor beskriver hvordan du konfigurerer automatisk arkivering av salgsdokumenter. Fremgangsmåten er den samme for kjøpsdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgsoppsett**, og velg deretter den relaterte koblingen.
2. På siden **Generelt bokføringsoppsett** må du fylle ut feltene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

Spesielt for **Arkiver tilbud** beskriver tabellen nedenfor forskjellen mellom alternativene.

|Alternativ|Beskrivelse|
|------|-----------|
|**Aldri**| Aldri arkiver tilbud når de slettes.|
|**Spørsmål**|Velg for å spørre brukeren om å arkivere tilbud når de slettes.|
|**Alltid**|Velg for å arkivere tilbud automatisk når de slettes.|

## <a name="to-archive-a-sales-order"></a>Arkivere ordrer

Fremgangsmåten nedenfor beskriver hvordan du arkiverer fra ordrer. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Åpne en ordre du vil arkivere.  
3. Velg handlingen **Arkiver dokument**.

Ordren arkiveres. Du kan se den på siden **Arkiverte ordrer**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Slik gjenoppretter du salgordrer som ikke er bokført, fra arkivet

Følgende fremgangsmåte beskriver hvordan du tar innholdet i en arkivert ordre tilbake den opprinnelige ordren. Dette er bare mulig når det opprinnelige dokumentet ikke er bokført. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Ordrearkiver**, og velg deretter den relaterte koblingen.
2. Velg den arkiverte ordren, eller versjonen av den, som du vil gjenopprette, og velg deretter **Gjenopprett**-handlingen.  

Innholdet i den opprinnelige ordren erstattes med den valgte arkiverte versjonen.

## <a name="to-delete-archived-sales-orders"></a>Slette arkiverte ordrer

Fremgangsmåten nedenfor beskriver hvordan du sletter arkiverte ordrer. Fremgangsmåten er den samme for alle andre salgs- og kjøpsdokumenter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Ordrearkiver**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Slett arkiverte ordreversjoner**, og velg deretter de aktuelle filtrene på siden **Slett arkiverte ordreversjoner**.  
3. Velg **OK**.

## <a name="see-also"></a>Se også

[Spore dokumentlinje](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
