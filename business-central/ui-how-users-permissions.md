---
title: Tilordne eller redigere brukertillatelser | Microsoft-dokumentasjon
description: Beskriver hvordan du legger til Office 365-brukere i Business Central og deretter tilordner tillatelser, tilgangsrettigheter og sikkerhetsinnstillinger.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 03/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 602c429733104a792a49f4a7f38e2a3090420c9d
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="manage-users-and-permissions"></a>Administrere brukere og tillatelser
For å legge til brukere i [!INCLUDE[d365fin](includes/d365fin_md.md)] må selskapets Office 365-administrator først opprette brukere i administrasjonssenteret for Office 365. For mer informasjon, se [Legge til brukere i Office 365 for bedrifter](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Når brukere er opprettet i Office 365, kan de importeres i **Brukere**-vinduet ved å velge handlingen **Hent brukere fra Office 365**. Brukere er tilordnet tillatelsessett avhengig av planen som er tilordnet til brukeren i Office 365.

Du kan deretter fortsette med å tildele tillatelser til brukere til å definere hvilke databaseobjekter, og dermed hvilke grensesnittelementer, de har tilgang til, og i som bedrifter. Du kan legge til brukere i grupper. Dette gjør det enklere å tilordne samme tillatelsessett til flere brukere.

Et tillatelsessett er en samling tillatelser for bestemte objekter i databasen. Alle brukere må være tilordnet ett eller flere tillatelsessett før de kan åpne [!INCLUDE[d365fin](includes/d365fin_md.md)]. Et antall forhåndsdefinerte tillatelsessett leveres som standard. Du kan bruke disse tillatelsessettene slik de allerede er definert, endre standardtillatelsessettene eller opprette flere egne tillatelsessett.

Administratorer kan bruke vinduet **Brukeroppsett** til å definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på.

## <a name="to-assign-permissions-to-a-user"></a>Slik tilordner du tillatelser til en bruker til
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukere**, og velg deretter den relaterte koblingen.
2. Velg brukeren du vil tilordne tillatelse til.
Eventuelle tillatelsessett som allerede er tilordnet til brukeren, vises i faktaboksen **Tillatelsessett**.
3. Velg handlingen **Rediger** for å åpne **Brukerkort**-vinduet.
4. På hurtigfanen **Brukertillatelsessett** fyller du ut feltene etter behov på en ny linje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-group-users-in-user-groups"></a>Slik grupperer du brukere i brukergrupper
Du kan definere brukergrupper til å administrere tillatelsessett for grupper av brukere i firmaet. Du kan bruke en funksjon til å kopiere alle tillatelsessett fra en eksisterende brukergruppe til den nye brukergruppen. Medlemmene i brukergruppen kopieres ikke.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukergrupper**, og velg deretter den relaterte koblingen.
2. Du kan også gå til vinduet **Brukere** og velge handlingen **Brukergrupper**.
3. Gå til vinduet **Brukergruppe** og velg handlingen **Brukergruppemedlemmer**.
6. Gå til vinduet **Brukergruppemedlemmer** og velg handlingen **Legg til brukere**.
7. For å legge til nye eller ekstra tillatelsessett, går du til **Brukergrupper**-vinduet, og velger du handlingen **Tillatelsessett for brukergruppe**.
8. I vinduet **Tillatelsessett for brukergruppe** på en ny linje, fyller du ut feltene etter behov ved å velge fra eksisterende tillatelsessett.

## <a name="to-set-up-user-time-constraints"></a>Slik definerer du tidsbegrensninger for brukere:
Administratorer kan definere hvor lenge angitte brukere skal kunne bokføre, og også angi om systemet skal logge hvor lenge brukere er logget på. Administratorer kan også tilordne ansvarssentre til brukere. Hvis du vil ha mer informasjon, kan du se [Arbeide med ansvarssentre](inventory-responsibility-centers.md).

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.
2. I vinduet **Brukeroppsett** velger du handlingen **Ny**.
3. I feltet **Bruker-ID** angir du ID-en for en bruker eller velger feltet for å vise alle gjeldende Windows-brukere i systemet.
4. Fyll ut feltene etter behov.

## <a name="see-also"></a>Se også
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Oppsett og administrasjon i [!INCLUDE[d365fin](includes/d365fin_md.md)]](admin-setup-and-administration.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

