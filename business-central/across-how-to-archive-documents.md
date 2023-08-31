---
title: Arkiver salgs- og kjøpsdokumenter
description: 'Du kan arkivere ordrer, bestillinger, tilbud, returordrer og rammeordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 08/18/2023
ms.custom: bap-template
ms.search.form: '42, 49, 50, 459, 460, 5159, 5162, 5164, 5167, 6627, 6630, 6644, 9305, 9306, 9346, 9347, 9348, 9349'
---
# <a name="archive-documents"></a>Arkiver dokumenter

Du kan arkivere ordrer, bestillinger, tilbud, returordrer og rammeordrer. Du arkivere et salgs- eller kjøpsdokument flere ganger og lagre en annen arkiverte versjon hver gang.

For arkiverte salgsdokumenter der originalen fortsatt finnes og ikke er bokført, kan du bruke handlingen **Gjenopprett** til å overskrive nåværende dokument med en arkivert versjon. Handlingen fungerer bare for salgsdokumenter.

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

## <a name="to-manually-archive-a-sales-order"></a>Slik arkivere du en ordre manuelt

Fremgangsmåten nedenfor beskriver hvordan du arkiverer en ordre manuelt. Fremgangsmåten er lik for alle ordrer, rammebestillinger, bestillingsreturer og tilbud.

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

Bruk en oppbevaringspolicy til å rydde opp i arkiverte dokumenter du ikke trenger lenger. Med oppbevaringspolicyer kan administratorer definere hvor lenge de vil lagre data. De kan for eksempel definere en policy som sletter data etter en utløpsdato. Hvis du vil ha mer informasjon, kan du se [Definere oppbevaringspolicyer](admin-data-retention-policies.md).

Det er et par ting du kan legge merke til om oppretting av oppbevarings policyer for arkiverte dokumenter:

* *Hvis det opprinnelige dokumentet ikke er slettet, sletter ikke Business Central de arkiverte versjonene. Arkiverte versjoner utløper ikke så lenge originalen finnes.
* Når du definerer oppbevaringspolicyen, kan du angi at du vil at policyen skal slette alle arkiverte versjoner av et dokument, unntatt den nyeste. Du kan for eksempel ha ti versjoner av et dokument og ønske å beholde en kopi av den nyeste. 
* Business Central beregner utløpsdatoen for dokumenter basert på datoen for den sist arkiverte versjonen.

## <a name="see-also"></a>Se også

[Spor dokumentlinjer](across-how-to-track-document-lines.md)  
[Salg](sales-manage-sales.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
