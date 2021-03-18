---
title: Definere servicekontrakter | Microsoft-dokumentasjon
description: Finn ut hvordan du definerer servicekontrakter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e89b2257db6d1c07fb08011c7188855799485264
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391727"
---
# <a name="set-up-service-contracts"></a>Definere servicekontrakter
Før du kan arbeide med kontrakter må du definere følgende: 

* **Servicekontraktgrupper**, som inneholder servicekontrakter som på én eller annen måte er tilknyttet hverandre.
* **Kontogrupper for servicekontrakter**, som brukes til å gruppere kontoene for servicekontrakter for servicefakturaer som opprettes for servicekontrakter. Du kan tilordne disse gruppene til servicekontrakter.  
* **Kontraktmaler** som definerer oppsett for kontrakter som omfatter de vanligste opplysningene om servicekontrakter. Når du oppretter servicekontrakttilbud, kan du opprette dem ved hjelp av maler. Når du oppretter et kontrakttilbud, innholdet feltene automatisk innholdet i feltene i malen.
* **Kundemaler** som lar deg opprette tilbud for kontakter eller potensielle kunder som ikke er registrert som kunder i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Slik definerer du servicekontraktgrupper  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontraktgrupper**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Merk av for **Rab. bare på kontr. ordrer** hvis du vil at kontrakt- eller servicerabatter bare skal være gyldige for servicekontraktordrer, for eksempel vedlikehold.  

## <a name="to-set-up-a-service-contract-account-group"></a>Slik definerer du kontogrupper for servicekontrakter  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontogrp. for servicekontr.**, og velg deretter den relaterte koblingen.  
2. Opprett en ny kontogruppe for servicekontrakter.   
3. Fyll ut feltene **Kode** og **Beskrivelse**. Disse feltene beskriver servicekontogruppen.  
4. Fyll ut feltet **Ikke-forh.bet. kontraktkonto**, og velg finanskontonummeret for ikke-forhåndsbetalte konti.  
5. I feltet **Ikke-forh.bet. kontraktkonto** velger du finanskontonummeret for forhåndsbetalte konti.  

## <a name="to-set-up-a-contract-template"></a>Slik definerer du kontraktmaler  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontraktmaler**, og velg deretter den relaterte koblingen.  
2. Opprett en ny servicekontraktmal.  
3. I feltet **Nr.** -feltet angir du et nummer for kontraktmalen.  
  
     Hvis du har definert en nummerserie for kontraktmaler på siden **Serviceoppsett**, kan du eventuelt trykke på Enter-tasten for at programmet skal angi det neste tilgjengelige kontraktmalnummeret. Fyll eventuelt ut de andre feltene.  
  
4. I hurtigfanen **Faktura** fyller du ut feltet **Serv.kontr.kontogrp. - kode**, **Fakturaperiode** og så videre. Fyll eventuelt ut de andre feltene.  
5. Velg handlingen **Servicerabatter** for å legge til kontraktrabatter.  

## <a name="to-set-up-a-customer-template"></a>Slik definerer du kundemaler  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kundemaler**, og velg deretter den relaterte koblingen.  
2. Opprett et nytt kundemalkort.  
3. På hurtigfanen **Generelt** angir du koden og en beskrivelse for kundemalen i feltene **Kode** og **Beskrivelse**. 
4. Hvis du vil definere søkekriterier, fyller du ut de andre feltene, for eksempel **Lands-/regionkode**, **Distriktskode** og **Språkkode**.  
5. Fyll ut feltene **Bokføringsgruppe - firma** og **Bokføringsgruppe - kunde**.  

## <a name="see-also"></a>Se også
[Konfigurere servicehåndtering](service-setup-service.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]