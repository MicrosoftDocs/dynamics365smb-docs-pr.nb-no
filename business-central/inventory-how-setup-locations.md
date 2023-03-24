---
title: Definere et lokasjonskort og definere overføringsruter (inneholder video)
description: 'Hvis du kjøper, lagrer eller selger varer på mer enn ett sted, kan du definere hvert sted som en lokasjon.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'warehouse, distribution center'
ms.search.forms: '5703, 15'
ms.date: 07/05/2022
ms.author: bholtorf
---
# Definer lokasjoner

Lokasjoner er steder som lagre der du kjøper, lagrer eller selger varer. [!INCLUDE [prod_short](includes/prod_short.md)] bruker lokasjoner til å holde oversikt over lageret både i enklere tilfeller og de mer sammensatte lagerprosessene.

Deretter kan du opprette dokumentlinjer for en bestemt lokasjon, vise tilgjengelighet etter lokasjon og overføre beholdning mellom lokasjoner. Hvis du vil ha mer informasjon, kan du se [Håndtere lager](inventory-manage-inventory.md).
<br><br>  
  
> [!Video https://www.microsoft.com/videoplayer/embed/RE4aQvq?rel=0]

## Lokasjonskort

Du angir opplysninger om en lokasjon, for eksempel et lager eller distribusjonssenter, på siden **Lokasjonskort**. Du gir hver lokasjon et navn og en kode som representerer lokasjonen. Deretter kan du angi lokasjonskoden i andre deler av programmet når du vil registrere transaksjoner for en gitt lokasjon.  

Du kan angi opplysninger om hyller og lagerprinsipper for hver lokasjon. Basert på lagerpolicyene kan du bruke alternativene i hurtigfanen **Hyller** til å angi hyllene som skal brukes som standard for transaksjoner. Hvis du bruker lagerstyring, kan du med alternativene i hurtigfanen **Hylleprinsipp** definere hvordan du vil bruke de forskjellige avanserte lagerfunksjonene.  

Noen alternativfelt er avhengig av innstillinger på siden **Lokasjonskort** for å begrense oppsettskombinasjoner som ikke støttes.  

Velg handlingene **Soner** eller **Hyller** for å vise informasjon om soner og hyller som er definert for lokasjonen.

### Slik definerer du lokasjoner

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Gjenta trinn 2 og 3 for hver beholdninglokasjon.

> [!NOTE]  
> Mange felt på siden Lokasjonskort er knyttet til håndteringen av varer i inngående og utgående lagerprosesser. Disse feltene er ikke relevante for selskaper som ikke trenger den komplekse lagerfunksjonaliteten. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

Du kan endre konfigurasjonen av en lokasjon så lenge det ikke finnes vareposter.  

Hvis du har flere lokasjoner, kan du definere overføringsruter mellom lokasjonene. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du overføringsruter](inventory-how-setup-locations.md#to-create-a-transfer-route).

### Slik oppretter du overføringsruter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsruter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
4. På siden **Lokasjonskort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Nå kan du overføre lagervarer mellom to lokasjoner. Hvis du vil ha mer informasjon, kan du se [Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md).    

## Hyller

Hyller representerer den grunnleggende lagerstrukturen og kan foreslå hvor varene skal plasseres. Hyllene kan ha innhold, eller være fristilte hyller uten bestemt innhold. 

Hvis du vil bruke hyllefunksjonaliteten i en lokasjon, må du aktivere funksjonaliteten på siden **Lokasjonskort** ved å slå på vekslebryteren **Hylle obligatorisk** på hurtigfanen **Lager**. Du kan utforme vareflyten på lokasjonen ved å angi hyllekoder i feltene for lagerprosessene i hurtigfanene **Hyller** og **Hylleprinsipp**.

> [!NOTE]
> Før du kan angi hyllekoder på en lokasjon, må du opprette hyllekoder. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md) og [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).  

## Soner

Hvis du vil strukturere hyllene under soner, kan du gjøre det på siden **Soner**. Når du tildeler en sone til hyller, kopierer [!INCLUDE [prod_short](includes/prod_short.md)] informasjon fra sonen til hyllene. Du kan også velge å definere en sone og bruke hyller alene til å organisere lageret. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

## Standarddimensjoner for lokasjoner

Du angir standarddimensjoner for en lokasjon på siden **Lokasjonskort** ved å velge **Dimensjoner**. Etterpå tildeles lokasjonens standarddimensjoner til dokumenter når du velger lokasjon på en linje. Du kan slette eller endre dimensjonene på linjen etter behov. I feltet **Verdipostering** kan du kreve at brukerne angir dimensjoner for bestemte lokasjoner før de kan bokføre en post. Hvis du vil at brukerne bare skal kunne velge bestemte dimensjonsverdier, kan du angi verdiene i feltet **Tillatt verdifilter**. Du kan også inkludere lokasjonsdimensjonsverdier på siden **Standard dimensjonsprioriteter** og for kombinasjoner av prioritets- og dimensjonsregler på siden **Dimensjonskombinasjoner**.

## Se relatert opplæring på [Microsoft Learn](/learn/modules/trade-set-up-dynamics-365-business-central/)

## Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Overføre beholdning mellom lokasjoner](inventory-how-transfer-between-locations.md)  
[Opprette hyller](warehouse-how-to-create-individual-bins.md)  
[Definere hylletyper](warehouse-how-to-set-up-bin-types.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
