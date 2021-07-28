---
title: Legge til selskaper i selskapshuben
description: Lær hvordan du legger til selskaper fra andre Business Central-miljøer i selskapshuben, slik at du kan håndtere arbeid på tvers av miljøer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: accountant, accounting, company hub
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 4954287f93ed012709a51f6fbb19d00494c63d54
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436979"
---
# <a name="add-companies-to-your-company-hub"></a>Legge til selskaper i selskapshuben

Med selskapshuben kan du få tilgang til arbeidet fra flere selskaper fra flere [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer. Du kan legge til miljøer og selskaper manuelt hvis selskapene ikke vises automatisk i selskapshuben.  

Rett på målsiden for selskapshub finner du **Oppsett**-menyen der du får tilgang til siden **Miljøkoblinger**. Velg ganske enkelt **Ny**, og fyll deretter ut feltene. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

> [!NOTE]
> Du kan koble selskapssenteret til så mange selskaper du vil. Du kan imidlertid bare koble selskapssenteret til selskaper som er driftet i [!INCLUDE [prod_short](includes/prod_short.md)] på nett.

## <a name="environment-links"></a>Miljøkoblinger

En miljøkobling er et kort der du angir [!INCLUDE [prod_short](includes/prod_short.md)]-miljøet som er vert for ett eller flere firmaer du arbeider i. Dataene på kortet for hvert miljø angis av deg, og du kan endre dem etter behov. Feltet **Miljøkobling** er avgjørende – det er slik du får tilgang til hvert selskap i [!INCLUDE [prod_short](includes/prod_short.md)]. Bruk handlingen **Test tilkoblingen** på båndet for å teste at du har angitt riktig kobling. Koblingen du må angi, peker til miljø som er vert for selskapet du legger til, og den må inkludere Azure Active Directory (Azure AD)-ID-en eller organisasjonens domenenavn. Hvis de for eksempel har angitt domenet mittfirma.com, vil koblingen til [!INCLUDE [prod_short](includes/prod_short.md)] være ```https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1```. Ellers vil det se omtrent slik ut: ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```  

Koblingen brukes når du velger firmaet i firmahuben.  

:::image type="content" source="media/company-hub-company-list-actions.png" alt-text="Handlinger for et selskap som er oppført i selskapshuben.":::

> [!TIP]
> Hvis du arbeider i en gratis prøveversjon av [!INCLUDE [prod_short](includes/prod_short.md)], er det enkelt å legge til selskapene i leieren. Du kan finne miljøkoblingen ved å kopiere Azure Active Directory-ID-en fra **Feilsøking**-delen på siden Hjelp og støtte. Miljønavnet er sannsynligvis standardverdien PRODUKSJON. Legg til denne informasjonen i feltet **Miljøkobling**, for eksempel ```https://businesscentral.dynamics.com/1a23b456-789c-0123-45de-678910fg12h/production?redirectedfromsignup=1```, og velg deretter **Test tilkoblingen**. Evalueringsselskapet blir lagt til i listen.
>
> Hvis du har flyttet til det tretti-dagers prøveselskapet, Mitt selskap, kan du legge det til i listen ved å velge handlingen **Last inn på nytt / Last inn alle selskaper på nytt** i listen.

## <a name="load-companies"></a>Last inn selskaper

Når du har lagt til miljøene, vises selskapene automatisk. Hvis du imidlertid vet at et nytt selskap er lagt til i et miljø, kan du velge handlingen **Last inn alle selskaper på nytt** for å oppdatere listen. Bruk samme handling for å oppdatere data fra de forskjellige selskapene dine.  

> [!TIP]
> Hvis du vil oppdatere dataene i selskapshuben, må du ha tilgang til dataene i selskapene som dataene kommer fra.

## <a name="see-also"></a>Se også

[Administrere arbeid på tvers av flere selskaper i selskapshuben](company-hub.md)  
[Ressurser for hjelp og støtte](product-help-and-support.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]