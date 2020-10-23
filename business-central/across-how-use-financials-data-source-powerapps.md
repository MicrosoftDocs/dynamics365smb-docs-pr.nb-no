---
title: Bruk dataene til å lage en app | Microsoft-dokumenter
description: Du kan gjøre Business Central-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle en forretningsapp ved hjelp av Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 718d4378a897b187ba3073449869184fef5cec98
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924831"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av Power Apps

Du kan gjøre [!INCLUDE[prodshort](includes/prodshort.md)]-data tilgjengelige som en datakilde i Power Apps.  

> [!NOTE]  
> Du må ha en gyldig konto med [!INCLUDE[prodshort](includes/prodshort.md)] og med Power Apps.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>Legge til [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power Apps

1. I leseren, kan du gå til [powerapps.microsoft.com](https://powerapps.microsoft.com/), og deretter logge på.
2. På startsiden, i **Start fra data**-delen, velger du flisen **Andre data kilder**.  

    Dette åpner Power Apps Studio. Ved første pålogging må du angi landet/området.  
3. Velg **Business Central** i listen over tilgjengelige tilkoblinger, og velg deretter **Opprett**-knappen.

    Power Apps kobler til [!INCLUDE[prodshort](includes/prodshort.md)] med legitimasjonen du logget på med. Hvis du ikke er administrator i [!INCLUDE[prodshort](includes/prodshort.md)], må du kanskje logge på med en annen konto.  

4. Power Apps viser en liste over *Miljøer og selskaper* som er tilgjengelige fra [!INCLUDE[prodshort](includes/prodshort.md)]. Velg miljøet og selskapet som inneholder dataene du vil koble til, for ekssempel *PRODUKSJON – Mitt selskap*.  

5. Deretter vises en liste over tabeller som vises som en del av API-et for ditt miljø. Velg tabellen du vil koble til, og velg deretter **Koble til**.

Disse tabellene vises som endepunkter av [!INCLUDE[prodshort](includes/prodshort.md)]-koblingen for Power Apps.  

> [!NOTE]
> Hvis du vil inkludere data fra andre tabeller i [!INCLUDE[prodshort](includes/prodshort.md)] i appen, må du samarbeide med en utvikler for å definere en egendefinert API i [!INCLUDE[prodshort](includes/prodshort.md)], og deretter forbruke denne tilpassede API-en via en egendefinert kobling i Power Apps. Hvis du vil ha mer informasjon, kan du se [Opprette en egendefinert kobling fra grunnen av](/connectors/custom-connectors/define-blank).  

Nå har du koblet til [!INCLUDE[prodshort](includes/prodshort.md)]-dataene og er klar til å begynne å bygge din PowerApp. Du kan legge til flere skjermbilder og koble til flere data fra [!INCLUDE[prodshort](includes/prodshort.md)]. Hvis du vil ha mer informasjon, kan du se [Opprette en lerretsapp fra et eksempel i Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Når du har utformet og bygd appen, kan du dele den med kollegene dine. Hvis du vil ha mer informasjon, kan du se [Lagre og publisere en lerretsapp i Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Hvis du vil koble til [!INCLUDE[prodshort](includes/prodshort.md)] lokalt, må du velge **Business Central (lokalt)**-koblingen i trinn 3.  

## <a name="see-also"></a>Se også

[Opprette en lerretsapp fra en mal i Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Komme i gang med å utvikle tilkoblingsapper for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
