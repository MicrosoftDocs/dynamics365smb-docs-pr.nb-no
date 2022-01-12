---
title: Definere et lokasjonskort og definere overføringsruter (inneholder video)
description: Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 1d65213d81c2a615481e753adb380675ff2ee691
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2021
ms.locfileid: "7940729"
---
# <a name="set-up-locations"></a>Definer lokasjoner

Hvis du kjøper, lagrer eller selger varer på flere lokasjoner eller lagre, må du definere hver lokasjon med et lokasjonskort og definere overføringsruter. [!INCLUDE [prod_short](includes/prod_short.md)] bruker lokasjoner til å holde oversikt over lageret både i enklere tilfeller og de mer sammensatte lagerprosessene.

Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner. Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## <a name="location-cards"></a>Lokasjonskort

Lokasjonskortet angir opplysninger om en lokasjon, for eksempel et lager eller distribusjonssenter. Du gir hver lokasjon et navn og en kode som representerer lokasjonen. Deretter kan du angi lokasjonskoden i andre deler av programmet når du vil registrere transaksjoner for en gitt lokasjon.  

Du kan angi opplysninger om hyller og lagerprinsipper for hver lokasjon. Basert på lagerprinsippet du velger, kan du bruke alternativene i hurtigfanen **Hyller** til å definere hyllene som skal brukes som standardhyller når du foretar transaksjoner. Hvis du bruker lagerstyring, bruker du de fleste av disse alternativene i hurtigfanen **Hylleprinsipp** til å definere hvordan du vil bruke de forskjellige avanserte lagerfunksjonene.  

Noen alternativfelt er nedtonet og deaktivert av andre innstillinger på siden **Lokasjonskort** for å begrense oppsettskombinasjoner som ikke støttes.  

Velg handlingen **Soner** eller **Hyller** for å vise informasjon om soner og hyller som kan være definert for lokasjonen.

### <a name="to-create-a-location-card"></a>Slik oppretter du et lokasjonskort

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gjenta trinn 2 og 3 for hver beholdninglokasjon.

> [!NOTE]  
> Mange felt på lokasjonskortet refererer til håndteringen av varer i inngående og utgående lagerprosesser. Feltene er ikke relevante for selskaper som ikke trenger den mer komplekse lagerfunksjonaliteten. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

Du kan endre konfigurasjonen for en lokasjon senere, men du kan ikke redigere oppsettet av lokasjoner som har vareposter.  

Hvis du har flere lokasjoner, kan du definere overføringsruter mellom lokasjonene.  

### <a name="to-create-a-transfer-route"></a>Slik oppretter du overføringsruter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsruter**, og velg deretter den relaterte koblingen.
2. Fra en **Lokasjonskort**-side kan du også velge handlingen **Overføringsruter**.
3. Velg handlingen **Ny**.
4. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nå kan du overføre lagervarer mellom to lokasjoner. Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).    

## <a name="bins"></a>Hyller

Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer. Når du har opprettet hyllene, kan du definere nøyaktig det innholdet du vil plassere i hver hylle, eller hyllen kan fungere som en mobil hylle uten angitt innhold. Hyller brukes for øyeblikket i enkle og avanserte lageroperasjoner. Hvis du administrerer lagerbeholdningen i et mer enkelt oppsett, trenger du sannsynligvis ikke hyller.

Hvis du vil bruke hyllefunksjonaliteten i en lokasjon, må du først aktivere funksjonaliteten på kortet **Lokasjon** ved å velge feltet **Hylle obligatorisk** på hurtigfanen **Lager**. Du utformer deretter vareflyten på lokasjonen ved å angi hyllekoder i oppsettsfeltene som representerer ulike flyter.

> [!NOTE]
> Før du kan angi hyllekoder på lokasjonskortet, må hyllekodene være opprettet.

Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).  

## <a name="zones"></a>Soner

Hvis du vil strukturere hyllene under soner, kan du gjøre det på siden **Soner**.

[!INCLUDE [prod_short](includes/prod_short.md)] kopierer feltene som du definerer for en bestemt sone, til hyllene som hører til den. På denne måten kan du tilordne en sone til en hylle eller en hyllemal (hyllefilter), og flere andre felter fylles ut automatisk.

Du kan også velge å definere bare en sone og organisere lageret bare ut fra hyllene. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

## <a name="see-also"></a>Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)  
[Opprette hyller](warehouse-how-to-create-individual-bins.md)  
[Definere hylletyper](warehouse-how-to-set-up-bin-types.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]