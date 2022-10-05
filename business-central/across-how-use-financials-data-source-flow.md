---
title: Bruk Power Automate-flyter i Business Central
description: Definer og bruk Power Automate-flyter for å opprette eller endre Business Central-data.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 369ee2b4aded272a8a3a21fe810b4b6c62dd1de0
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585463"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Bruk Power Automate-flyter i [!INCLUDE[prod_short](includes/prod_short.md)]

Du kan bruke dine [!INCLUDE[prod_short](includes/prod_short.md)]-data som en del av en arbeidsflyt i Microsoft Power Automate. Opprett dine egne flyter og koble dataene fra interne og eksterne kilder med [!INCLUDE [prod_short](includes/prod_short.md)]-koblingen.

> [!NOTE]
> Du må ha en gyldig konto med både [!INCLUDE[prod_short](includes/prod_short.md)] og Power Automate.  

> [!TIP]
> I tillegg til Power Automate kan du bruke godkjenningsarbeidsflytmaler i [!INCLUDE[prod_short](includes/prod_short.md)]. Selv om de er to separate arbeidsflytsystemer, legges en godkjenningsarbeidsflytmal som du oppretter med Power Automate, til i listen over arbeidsflyter i [!INCLUDE[prod_short](includes/prod_short.md)]. Finn ut mer under [Arbeidsflyter](across-workflow.md).

Power Automate-flyter utløses av hendelser som oppretting, endring eller sletting (automatiserte flyter) av oppføring eller dokument. Flytene kan også kjøres i en brukerdefinert plan (planlagte flyter) eller på forespørsel (direkteflyt).

## <a name="power-automate-features-in-prod_short"></a>Power Automate-funksjoner i [!INCLUDE[prod_short](includes/prod_short.md)]

Flytene viser de innebygde funksjonene for godkjenning av arbeidsflyter som er tilgjengelige i [!INCLUDE[prod_short](includes/prod_short.md)] uten å kreve kodekunnskap, og kan knyttes til et bredt spekter av hendelser og svar, for eksempel oppføringsendringer, oppdateringer av eksterne filer, bokførte dokumenter, i tillegg til forskjellige Microsoft- og tredjepartstjenester, for eksempel Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps med mer.

Det kan for eksempel hende at en ny salgsfaktura utløser en arbeidsflyt for en godkjenningsforespørsel, som kan ha ulike hendelser angitt, avhengig av svaret fra godkjenneren. Et negativt svar sender en varsling og e-post til godkjenningsbestilleren. Et positivt svar oppdaterer samtidig et Excel-regneark som er plassert i en SharePoint-mappe, og sender en oppdatering til en Teams-nettprat.

Direkteflyter fungerer på samme måte som satsvise snarveier, noe som utfører flere lange trinn med noen knappetrykk og startes fra bestemte sider eller tabeller. En flyt kan for eksempel legge til en knapp på handlingsmenyen på **Leverandører**- siden for å sperre betalinger til en leverandør og samtidig sende e-postmeldinger til leverandørens kontakt og innkjøpere, i tillegg til å oppdatere kontakten i Outlook.

## <a name="automated-workflows"></a>Automatiserte arbeidsflyter

Med Power Automate kan du opprette forretningsflyter direkte internt og stole på selvlærte utviklere. Automatiserte arbeidsflyter kan bli påbegynt av både interne og eksterne hendelser i [!INCLUDE[prod_short](includes/prod_short.md)] og er også angitt til å kjøres periodisk. Finn ut mer og få instruksjoner om hvordan du oppretter arbeidsflyter i artikkelen [Definer automatiserte arbeidsflyt](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrasjonsinnholdet.

## <a name="instant-flows"></a>Direkteflyter

Fra og med lanseringsbølge 1 i 2022 (mai 2022) kan en administrator for [!INCLUDE [prod_short](includes/prod_short.md)] på nettet [slå på en funksjon](admin-feature-management.md) for å gjøre det mulig å kjøre en Power Automate-flyt fra de fleste lister, kort og dokumentsider. Finn ut mer i artikkelen [Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrasjonsinnholdet.

Når administratoren har koblet [!INCLUDE [prod_short](includes/prod_short.md)] til Power Automate, ser du eventuelle flyter organisasjonen har lagt til, når du velger handlingen **Automatiser** på de aktuelle sidene. Direkteflyter kjøres uten å forlate [!INCLUDE [prod_short](includes/prod_short.md)].

Disse direktearbeidsflytene åpnes på en side i [!INCLUDE [prod_short](includes/prod_short.md)] på nettet slik at du kan forbli innenfor konteksten til forretningsprosessen du holdt på med. Velg **Automatiser**-handlingen – på noen sider nestet under **Flere alternativer**-menyen – velg **Power Automate**-menyelementet, og velg deretter den relevante koblingen som skal utløse arbeidsflyten. Tilkoblingen til Power Automate er allerede satt opp for deg.

De fleste flyter krever at du fyller ut et felt eller to før du velger handlingen **Kjør flyt**.

> [!TIP]
> Hvis du ikke ser en **Automatiser**-handling, har [!INCLUDE [prod_short](includes/prod_short.md)] trolig ikke blitt konfigurert til å bruke Power Automate ennå. Finn ut mer fra administratoren.

## <a name="add-more-automated-flows-and-instant-flows"></a>Legg til flere automatiserte flyter og direkteflyter

Du kan opprette flyter gjennom nettstedet [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Hvis administratoren imidlertid har byttet til funksjoner for å kjøre Power Automate-flyter fra [!INCLUDE [prod_short](includes/prod_short.md)] online, kan du starte prosessen med å bygge en flyt fra handlingen **Automatiser** på de aktuelle sidene, som du finner på menyen **Flere alternativer** avhengig av siden. Velg deretter **Power Automate**-menyelementet og deretter handlingen **Opprett en flyt**. Power Automate åpnes deretter i en ny nettleserfane, og du er logget på automatisk.

Du kan finne eksempel maler som kan tilpasses selskapet, og alle tilgjengelige utløserhendelser ved hjelp av både [!INCLUDE [prod_short](includes/prod_short.md)] og eksterne verktøy ved å velge **Koblinger**-menyen på Power Automate-nettstedet. Finn ut om tilgjengelige maler og utløsere i artikkelen [Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) i administrasjonsinnholdet.

## <a name="manage-automated-workflows"></a>Administrer automatiserte arbeidsflyter

Du kan opprette nye flyter eller håndtere eksisterende Power Automate-flyter i [!INCLUDE [prod_short](includes/prod_short.md)] på siden **Administrer Power Automate-flyter**. Finn ut mer i artikkelen [Administrer Power Automate-flyter](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows.md) i administrasjonsinnholdet.

Du kan også administrere tilgjengelige Power Automate-arbeidsflyter på siden **Arbeidsflyter** i [!INCLUDE[prod_short](includes/prod_short.md)]. Siden viser både innebygd godkjenning og Power Automate-arbeidsflyter, med alternativer for sistnevnte for å aktivere/deaktivere, slette og vise arbeidsflyten på Power Automate-nettstedet.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/use-power-automate/)

## <a name="see-also"></a>Se også

[Feilsøk automatiserte arbeidsflyter for [!INCLUDE[prod_short](includes/prod_short.md)]](across-flow-troubleshoot.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeidsflyter](across-workflow.md)  
[Importer forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tildel tillatelser til brukere og grupper](ui-define-granular-permissions.md)  
[Konfigurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  
[Administrer Power Automate-flyter](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Konfigurer automatiserte arbeidsflyter](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Slå på direkteflyter](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
