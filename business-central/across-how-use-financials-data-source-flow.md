---
title: Bruk Business Central i Power Automate-flyter
description: Definer og bruk Power Automate-flyter som oppretter eller endrer Business Central-data.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: 056fe537df2fba23e02cb4e70675937cde724fbf
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9533028"
---
# <a name="use-prod_short-in-power-automate-flows"></a>Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate-flyter

Du kan bruke dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av en arbeidsflyt i Microsoft Power Automate. Opprett dine egne flyter og koble dataene til [!INCLUDE [prod_short](includes/prod_short.md)]-koblingen.  

> [!NOTE]  
> Du må ha en gyldig konto med [!INCLUDE[prod_short](includes/prod_short.md)] og med Power Automate.  

> [!TIP]
> I tillegg til Power Automate kan du bruke godkjenningsarbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Selv om de er to separate arbeidsflytsystemer, legges en godkjenningsarbeidsflytmal som du oppretter med Power Automate, til i listen over arbeidsflyter i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Arbeidsflyter](across-workflow.md).  

## <a name="automated-workflows"></a>Automatiserte arbeidsflyter

Med Power Automate kan du opprette forretningsflyter direkte internt og stole på selvlærte utviklere. Hvis du vil ha mer informasjon, kan du se [Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrasjonsinnholdet.  

## <a name="manual-instant-flows"></a>Manuelle direkteflyter

Fra og med mai 2022 kan en administrator for [!INCLUDE [prod_short](includes/prod_short.md)] på nettet [slå på en funksjon](admin-feature-management.md) for å gjøre det mulig å kjøre en Power Automate-flyt fra de fleste sider. Hvis du vil ha mer informasjon, kan du se [Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrasjonsinnholdet.  

Når administratoren har koblet [!INCLUDE [prod_short](includes/prod_short.md)] til Power Automate, ser du eventuelle flyter som organisasjonen har lagt til når du velger handlingen **Automatiser** på de aktuelle sidene. Du kjører flytene uten å forlate [!INCLUDE [prod_short](includes/prod_short.md)].  

Disse automatiserte arbeidsflytene åpnes i en rute i [!INCLUDE [prod_short](includes/prod_short.md)] på nettet slik at du forblir innenfor konteksten til forretningsprosessen du holdt på med. På noen sider skjules handlingen **Automatiser** under **Flere alternativer**-menyen, men du finner den, velger **Power Automate**-menyelementet og velger deretter den relevante koblingen som skal utløse arbeidsflyten. Tilkoblingen til Power Automate er allerede satt opp for deg.  

De fleste flyter krever at du fyller ut et felt eller to før du velger handlingen **Kjør flyt**.  

> [!TIP]
> Hvis du ikke ser en **Automatiser**-handling, har [!INCLUDE [prod_short](includes/prod_short.md)] trolig ikke blitt konfigurert til å bruke Power Automate ennå. Spør administratoren for mer informasjon.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Legg til flere automatiserte flyter og manuelle direkteflyter

Du kan opprette flyter på nettstedet [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Hvis administratoren imidlertid har endret muligheten til å kjøre Power Automate-flyter fra [!INCLUDE [prod_short](includes/prod_short.md)] på nettet, kan du starte prosessen med å bygge en flyt fra handlingen **Automatiser** på de aktuelle sidene. På noen sider skjules handlingen **Automatiser** under **Flere alternativer**-menyen, men du finner den, velger **Power Automate**-menyelementet og velger deretter handlingen **Opprett en flyt**. Power Automate åpnes deretter i en ny nettleserfane, og du er logget på automatisk.

## <a name="manage-workflows"></a>Administrer arbeidsflyter

Du kan få en oversikt over alle arbeidsflytene du har tilgang til, ved å velge handlingen **Administrer arbeidsflyter** på **Power Automate**-menyen. Listen åpnes i en ny nettleserfane, og du er logget på Power Automate automatisk. Der kan du se når hver flyt ble kjørt sist.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/use-power-automate/)

## <a name="see-also"></a>Se også

[Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeidsflyter](across-workflow.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Konfigurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
