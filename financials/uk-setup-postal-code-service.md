---
title: Konfigurere GetAddress.io UK Postcodes-utvidelsen | Microsoft-dokumentasjon
description: "Beskriver de generelle funksjonene du bruker til å arbeide med data i Financials, for eksempel angi verdier, sortere data og bytte visninger."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a>Konfigurere GetAddress.io UK Postcodes-utvidelsen
Denne utvidelsen gjør det enkelt å angi adressene i Storbritannia for enheter som kunder, kontakter, ansatte, leverandører, bankkonti og så videre. 

GetAddress.io UK Postcodes-utvidelsen bruker getAddress API til å finne adresser i postnumre i Storbritannia. Hvis du vil bruke utvidelsen, må du få en plan og en API-nøkkel for getAddress API. Det er enkelt, og vi hjelper deg med å gjøre det når du setter opp GetAddress.io UK Postcodes-utvidelsen. Planer er basert på bruk eller det som noen ganger blir referert til som samtaler. En samtale, i dette tilfellet er når [!INCLUDE[d365fin](includes/d365fin_md.md)] viser en liste over adresser i et postnummer. Avhengig av hvor ofte du legger til adresser, velger du planen som passer best for deg. Hvis du velger **Få API-nøkkel** på siden, bruker du **Ledig**-planen, som lar deg legge til 20 adresser per dag, og som er gyldig i 30 dager. 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a>Konfigurere GetAddress.io UK Postcodes-utvidelsen 
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Tjenestetilkoblinger**, og velg deretter den relaterte koblingen.  
2. I vinduet **Tjenestetilkoblinger** velger du **UK Postcode Service**.
3. På siden **Konfigurasjon av postnummerleverandør** velger du **Deaktivert**.
4. I vinduet **Valg av postnummertjeneste** velger du **GetAddress.io**.
5. I vinduet **GetAddress.io Config** velger du **Få API-nøkkel** for å åpne **Planer**-siden på nettstedet for getAddress API.  

    > [!NOTE]  
>   Du må kanskje tillate popup-vinduer i nettleseren.
6. Kjøp en plan, eller velg bare **Få API-nøkkel**, og angi e-postadressen din.
7. Åpne e-postmeldingen fra getAddress.io, og kopier API-nøkkelen. Nøkkelen er under overskriften **Din API-nøkkel**.
8. I vinduet **GetAddress.io Config** limer du inn API-nøkkelen i feltet **API-nøkkel** og velger deretter **OK**.
9. På siden **Tjenestetilkoblinger** må du kontrollere at feltet **Adresseleverandør** viser **GetAddress.io**. I så fall er tjenesten aktivert.

## <a name="see-also"></a>Se også
[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
