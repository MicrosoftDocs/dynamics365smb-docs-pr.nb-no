---
title: Definere et lokasjonskort og definere overføringsruter (inneholder video)
description: Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.search.forms: 5703, 15
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9de6580971f25d092de474c0720b86fab420bbf8
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8515514"
---
# <a name="set-up-locations"></a>Definer lokasjoner

Lokasjoner er steder som lagre der du kjøper, lagrer eller selger varer. [!INCLUDE [prod_short](includes/prod_short.md)] bruker lokasjoner til å holde oversikt over lageret både i enklere tilfeller og de mer sammensatte lagerprosessene.

Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner. Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lokasjonskort
Du angir opplysninger om en lokasjon, for eksempel et lager eller distribusjonssenter, på siden **Lokasjonskort**. Du gir hver lokasjon et navn og en kode som representerer lokasjonen. Deretter kan du angi lokasjonskoden i andre deler av programmet når du vil registrere transaksjoner for en gitt lokasjon.  

Du kan angi opplysninger om hyller og lagerprinsipper for hver lokasjon. Basert på lagerprinsippet du velger, kan du bruke alternativene i hurtigfanen **Hyller** til å definere hyllene som skal brukes som standardhyller når du foretar transaksjoner. Hvis du bruker lagerstyring, bruker du de fleste av disse alternativene i hurtigfanen **Hylleprinsipp** til å definere hvordan du vil bruke de forskjellige avanserte lagerfunksjonene.  

Noen alternativfelt er avhengig av innstillinger på siden **Lokasjonskort** for å begrense oppsettskombinasjoner som ikke støttes.  

Velg handlingene **Soner** eller **Hyller** for å vise informasjon om soner og hyller som er definert for lokasjonen.

### <a name="to-set-up-a-location"></a>Slik definerer du lokasjoner

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gjenta trinn 2 og 3 for hver beholdninglokasjon.

> [!NOTE]  
> Mange felt på siden Lokasjonskort er knyttet til håndteringen av varer i inngående og utgående lagerprosesser. Disse feltene er ikke relevante for selskaper som ikke trenger den komplekse lagerfunksjonaliteten. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

Du kan endre konfigurasjonen for en lokasjon senere, men du kan ikke redigere oppsettet av lokasjoner som har vareposter.  

Hvis du har flere lokasjoner, kan du definere overføringsruter mellom lokasjonene. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du overføringsruter](inventory-how-setup-locations.md#to-create-a-transfer-route). 

### <a name="to-create-a-transfer-route"></a>Slik oppretter du overføringsruter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsruter**, og velg deretter den relaterte koblingen.
2. Fra en **Lokasjonskort**-side kan du også velge handlingen **Overføringsruter**.
3. Velg handlingen **Ny**.
4. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nå kan du overføre lagervarer mellom to lokasjoner. Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Hyller

Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer. Når du har opprettet hyllene, kan du definere innholdet, eller de kan fungere som mobile hyller uten angitt innhold. Hyller brukes for øyeblikket i enkle og avanserte lageroperasjoner. Hvis du administrerer lagerbeholdningen i et mer enkelt oppsett, trenger du sannsynligvis ikke hyller.

Hvis du vil bruke hyllefunksjonaliteten i en lokasjon, må du først aktivere funksjonaliteten på siden **Lokasjonskort** ved å velge feltet **Hylle obligatorisk** på hurtigfanen **Lager**. Du utformer deretter vareflyten på lokasjonen ved å angi hyllekoder i oppsettsfeltene som representerer ulike flyter.

> [!NOTE]
> Før du kan angi hyllekoder på en lokasjon, må du opprette hyllekoder. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Soner

Hvis du vil strukturere hyllene under soner, kan du gjøre det på siden **Soner**.

[!INCLUDE [prod_short](includes/prod_short.md)] kopierer feltene som du definerer for en bestemt sone, til hyllene som hører til den. På denne måten kan du tilordne en sone til en hylle eller en hyllemal (hyllefilter), og flere andre felter fylles ut automatisk.

Du kan også velge å definere bare en sone og organisere lageret bare ut fra hyllene. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

## <a name="default-dimensions-for-locations"></a>Standarddimensjoner for lokasjoner
Du angir standarddimensjoner for en lokasjon på siden **Lokasjonskort** ved å velge **Lokasjon** og deretter **Dimensjoner**. Lokasjonens standarddimensjoner kopieres til kladder og dokumenter når du angir lokasjonen på en linje, men du kan slette eller endre dimensjonen på linjen hvis det er nødvendig. Du kan kreve at brukerne angir dimensjoner for bestemte lokasjoner før de kan bokføre en post. Du kan også inkludere lokasjonsdimensjonsverdier i **Standard dimensjonsprioriteter** og **Dimensjonskombinasjoner** for kombinasjoner av prioritets- og dimensjonsregler.

## <a name="see-also"></a>Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)  
[Opprette hyller](warehouse-how-to-create-individual-bins.md)  
[Definere hylletyper](warehouse-how-to-set-up-bin-types.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]