---
title: Definere timelister| Microsoft-dokumentasjon
description: "Beskriver hvordan du klargjør systemet til å bruke timelister til å administrere prosjekter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: aa93e7fe867893c52e3b3973a58ea8a43291c1b1
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-time-sheets"></a>Definere timelister
Timelister i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndterer tidsregistrering i ukentlige intervaller på sju dager. Du kan bruke dem til å spore tiden som brukes på prosjekter, og du kan bruke dem til å registrere enkel registrering av ressurstid. Før du kan bruke timelister, må du angi hvordan du vil at de skal settes opp og konfigureres.

Når du har definert hvordan organisasjonen vil bruke timelister, kan du angi om og hvordan timelister er godkjent. Avhengig av behovene i organisasjonen, kan du angi:

* En eller flere brukere som administrator for timeliste og godkjenning for alle timelister.
* En godkjenner av timelister for hver ressurs.

Når du har definert timelister, kan du opprette timelister for ressurser, tilordne dem til planleggingslinjer og bokføre timelistelinjer. Se [Bruke timelister](projects-how-use-time-sheets.md) for mer informasjon.

## <a name="to-set-up-general-information-for-time-sheets"></a>Slik definerer du generell informasjon for timelister
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Ressursoppsett**, og deretter velger du den beslektede koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For feltet **Timeliste etter prosjektgodkjenning** velger du ett av følgende alternativer.

| Alternativ | Beskrivelse |
| --- | --- |
| **Aldri** |Brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet godkjenner timelisten. |
| **Alltid** |Brukeren i feltet **Ansvarlig person** på prosjektkortet godkjenner timelisten. |
| **Bare maskin** |Hvis timelisten for maskin er knyttet til et prosjekt, godkjenner brukeren i feltet **Ansvarlig person** på prosjektkortet, timelisten. Hvis timelisten for maskin er knyttet til en ressurs, godkjenner brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet, timelisten. |

## <a name="to-assign-a-time-sheet-administrator"></a>Slik tilordner du en timelisteadministrator
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Brukeroppsett**, og deretter velger du den beslektede koblingen.  
2. Legg til en ny bruker hvis brukerlisten ikke inkluderer personen som du vil skal være ansvarlig for timelisteregistrering. Hvis du vil ha mer informasjon, se delen Opprette brukere i [Komme i gang med forretninger](ui-get-ready-business.md).  
3. Velg en bruker som administrator for en timeliste, og merk deretter av for **Administrator for timeliste** .  

**Tips**: Det anbefales at du velger bare én bruker som administrator for timelisten i et selskap. I den følgende fremgangsmåten setter du opp en timelisteeier og -godkjenner, der godkjenneren av timelisten er tilordnet for hver ressurs.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Slik tilordner du en timelisteeier og -godkjenner
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Ressurser**, og deretter velger du den beslektede koblingen.
2. Merk ressursen du vil definere muligheten til å bruke timelister for, og merk deretter av for **Bruk timeliste**.  
3. Angi ID-en for eieren av timelisten i feltet **Bruker-ID for eier av timeliste:**. Eieren kan angi tidsbruk på en timeliste og sende den til godkjenning. Når ressursen er en person, er denne personen vanligvis også eieren.  
4. Angi ID-en for godkjenneren av timelisten i feltet **Bruker-ID for godkjenner av timeliste**. Godkjenneren kan godkjenne, avvise eller åpne på nytt en timeliste.  

**Merk**: Du kan ikke endre ID-en for godkjenneren av timelisten hvis det finnes timelister som ennå ikke er behandlet og som har statusen **Sendt** eller **Åpen**.

## <a name="see-also"></a>Se også
[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

