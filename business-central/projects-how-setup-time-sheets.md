---
title: Definere timelister og godkjenningen av dem | Microsoft-dokumentasjon
description: "Du definerer timelister for å spore tiden som brukes på prosjekter, og bruk av ressurser. Dette er til hjelp ved prosjektstyring, bemanning og kapasitet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 057497cfee69ed91c5d37828ea290749585f93d8
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-time-sheets"></a>Definere timelister
Timelister i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndterer tidsregistrering i ukentlige intervaller på sju dager. Du kan bruke dem til å spore tiden som brukes på prosjekter, og du kan bruke dem til å registrere enkel registrering av ressurstid. Før du kan bruke timelister, må du angi hvordan du vil at de skal settes opp og konfigureres.

Når du har definert hvordan organisasjonen vil bruke timelister, kan du angi om og hvordan timelister er godkjent. Avhengig av behovene i organisasjonen, kan du angi:

* En eller flere brukere som administrator for timeliste og godkjenning for alle timelister.
* En godkjenner av timelister for hver ressurs.

Når du har definert timelister, kan du opprette timelister for ressurser, tilordne dem til planleggingslinjer og bokføre timelistelinjer. Hvis du vil ha mer informasjon, kan du se [Bruke timelister](projects-how-use-time-sheets.md).

## <a name="to-set-up-general-information-for-time-sheets"></a>Slik definerer du generell informasjon for timelister
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressursoppsett**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For feltet **Timeliste etter prosjektgodkjenning** velger du ett av følgende alternativer.

| Alternativ | Beskrivelse |
| --- | --- |
| **Aldri** |Brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet godkjenner timelisten. |
| **Alltid** |Brukeren i feltet **Ansvarlig person** på prosjektkortet godkjenner timelisten. |
| **Bare maskin** |Hvis timelisten for maskin er knyttet til et prosjekt, godkjenner brukeren i feltet **Ansvarlig person** på prosjektkortet, timelisten. Hvis timelisten for maskin er knyttet til en ressurs, godkjenner brukeren i feltet **Bruker-ID for godkjenner av timeliste:** på ressurskortet, timelisten. |

## <a name="to-assign-a-time-sheet-administrator"></a>Slik tilordner du en timelisteadministrator
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett**, og velg deretter den relaterte koblingen.  
2. Legg til en ny bruker hvis brukerlisten ikke inkluderer personen som du vil skal være ansvarlig for timelisteregistrering. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).
3. Velg en bruker som administrator for en timeliste, og merk deretter av for **Administrator for timeliste**  

> [!TIP]  
>   Det anbefales at du velger bare én bruker som administrator for timelisten i et selskap. I den følgende fremgangsmåten setter du opp en timelisteeier og -godkjenner, der godkjenneren av timelisten er tilordnet for hver ressurs.  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a>Slik tilordner du en timelisteeier og -godkjenner
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ressurser**, og velg deretter den relaterte koblingen.
2. Merk ressursen du vil definere muligheten til å bruke timelister for, og merk deretter av for **Bruk timeliste**.  
3. Angi ID-en for eieren av timelisten i feltet **Bruker-ID for eier av timeliste:**. Eieren kan angi tidsbruk på en timeliste og sende den til godkjenning. Når ressursen er en person, er denne personen vanligvis også eieren.  
4. Angi ID-en for godkjenneren av timelisten i feltet **Bruker-ID for godkjenner av timeliste**. Godkjenneren kan godkjenne, avvise eller åpne på nytt en timeliste.  

> [!NOTE]  
>   Du kan ikke endre IDen for godkjenneren av timelisten hvis det finnes timelister som ennå ikke er behandlet og som har statusen **Sendt** eller **Åpen**.

## <a name="see-also"></a>Se også
[Konfigurere prosjektstyring](projects-setup-projects.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

