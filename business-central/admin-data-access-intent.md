---
title: Administrere databasetilgangsformål i Business Central | Microsoft Docs
description: Endre databasetilgangsformålet for rapporter, API-sider og spørringer.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/30/2020
ms.author: jswymer
ms.openlocfilehash: b46786b60d7c5799b056c49188785bd595db57ff
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333911"
---
# <a name="managing-database-access-intent"></a>Administrere databasetilgangsformål 

Som superbruker eller administrator kan du endre databasetilgangsformålet i rapporter, sider av typen API og spørringer for å forbedre tjenestens ytelse.

## <a name="overview"></a>Oversikt

[!INCLUDE[d365fin](includes/d365fin_md.md)] kan konfigureres til å bruke skrivebeskyttede replikaer for den primære (lese-skrive) databasen. Når du bruker databasereplikaen, reduseres belastningen på den primære databasen. I noen tilfeller vil det også forbedre ytelsen ved visning av data i klienten. Replikaer er nyttige for objekter, for eksempel rapporter, spørringer og API-sider, som brukes til å vise data, og som ikke endrer data.

Når objekter kjøres, bestemmer databasetilgangsformålet om det skal brukes en skrivebeskyttet replika, hvis en slik er tilgjengelig, eller den primære databasen. Rapporter, API-sider og spørringer er utviklet med et forhåndsdefinert databasetilgangsformål (se [Egenskapen DatabaseAccessIntent](/dynamics365/business-central/dev-itpro/developer/properties/devenv-dataaccessintent-property)).

Siden **Liste over databasetilgangsformål** gjør det mulig å overstyre det forhåndsdefinerte databasetilgangsformålet for objekter når de kjøres.

I databasevilkårene kalles denne funksjonen vanligvis *leseutskalering*. Hvis du vil ha mer informasjon om leseutskalering og datatilgangsformål i [!INCLUDE[prodshort](includes/prodshort.md)], kan du se [Bruke leseutskalering for bedre ytelse](/dynamics365/business-central/dev-itpro/administration/database-read-scale-out-overview) i [!INCLUDE[prodshort](includes/prodshort.md)] Developer og hjelpen for administrasjon.

## <a name="to-change-the-database-access-intent"></a>Slik endrer du databasetilgangsformålet

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Liste over databasetilgangsformål**, og velg deretter den relaterte koblingen.

    Siden viser alle rapporter, sider og spørringer. Kolonnen **Tilgangsformål** inneholder én av følgende verdier:

    |**Innstilling**|**Beskrivelse**|  
    |------------|-------------|  
    |**Standard**|Angir at objektet bruker det forhåndsdefinerte databasetilgangsformålet.|
    |**Tillat skriving**|Angir at objektet skal bruke den primære databasen, slik at brukeren kan endre data.|
    |**Skrivebeskyttet**|Angir at objektet skal bruke databasereplikaen, noe som betyr at brukeren bare kan vise data og ikke endre data.|

2. Velg handlingen **Rediger oversikt**.

3. På siden **Rediger – Liste over databasetilgangsformål** endrer du verdien i feltet **Tilgangsformål** for objektene.

    > [!NOTE]
    > Hvis et objekt som kan redigeres, for eksempel kundekortet, er satt til **Skrivebeskyttet**, vil den primære databasen fortsatt brukes, uavhengig av tilgangsformålet. Dermed kan brukere foreta endringer som normalt.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Forretningsfunksjoner](across-business-functionality.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Komme i gang](product-get-started.md)    

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
