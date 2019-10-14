---
title: Bruk dataene til å lage en app | Microsoft-dokumenter
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle en forretningsapp ved hjelp av PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305029"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av PowerApps
Du kan gjøre [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tilgjengelige som en datakilde i PowerApps.  

> [!NOTE]  
>   Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med PowerApps.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i PowerApps
1. I leseren, kan du gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), og deretter logge på.
2. På startsiden velger du **Apper**, **Opprett en app** og **Lerret** for å opprette en ny lerretsapp. Denne appen blir utformet for bruk på en mobil enhet, men du kan også velge å bruke en annen mal.

    Neste trinn for å opprette en PowerApp er å velge data. Velg pilikonet og deretter velge **Ny tilkobling** i øvre venstre side av siden.
3. Velg **Business Central** i listen over tilgjengelige tilkoblinger, og velg deretter **Opprett**-knappen.

    PowerApps kobler til [!INCLUDE [prodshort](includes/prodshort.md)] med legitimasjonen du logget på med. Hvis du ikke er administrator i [!INCLUDE [prodshort](includes/prodshort.md)], må du kanskje logge på med en annen konto.  

4.  PowerApps viser en liste over *Miljøer og selskaper* som er tilgjengelige fra [!INCLUDE [prodshort](includes/prodshort.md)]. Velg miljøet og selskapet som inneholder dataene du vil koble til. Nå skal du se en liste over APIer. Velg en **API** du vil koble til.

Disse såkalte tabellene er en del av [!INCLUDE [prodshort](includes/prodshort.md)]-API-en. Du trenger ikke konfigurere endepunktene selv, [!INCLUDE [prodshort](includes/prodshort.md)]-koblingen for PowerApps gjør det for deg.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

Nå har du koblet til [!INCLUDE [prodshort](includes/prodshort.md)]-dataene og er klar til å begynne å bygge din PowerApp. Du kan legge til flere skjermbilder og koble til flere data fra [!INCLUDE [prodshort](includes/prodshort.md)]. Hvis du vil ha mer informasjon, kan du se [Opprette en lerretsapp fra en mal i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Når du har utformet og bygd appen, kan du dele den med kollegene dine. Hvis du vil ha mer informasjon, kan du se [Lagre og publisere en lerretsapp i PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Hvis du vil koble til [!INCLUDE [prodshort](includes/prodshort.md)] lokalt, må du velge **Business Central (lokalt)**-koblingen i trinn 3.  

## <a name="see-also"></a>Se også

[Opprette en lerretsapp fra en mal i PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Komme i gang med å utvikle tilkoblingsapper for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
