---
title: Definere bransjegrupper for kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du definerer en bransjegruppe og tilordner den til et kontaktselskap, for eksempel detaljistbransjen eller bilbransjen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d2e331536de615b5a3ad84db526f86c79e56774c
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a>Definere bransjegrupper for kontaktselskaper
Du bruker bransjegrupper for å angi hvilken bransje kontaktene tilhører, for eksempel detaljistbransjen eller bilbransjen.

Bruk av bransjegrupper på kontakter er en totrinnsprosess. Først må definere du koden for bransjegruppen. Du trenger bare utføre dette trinnet én gang for hver bransjegruppe. Når du har en kode for bransjegruppe, kan du begynne å tilordne koden til kontaktselskaper.

> [!NOTE]  
>   Hvis du planlegger å synkronisere kontaktene med leverandører, kunder eller bankkonti i andre deler av programmet, bør du definere en forretningsforbindelse for disse.

## <a name="to-define-an-industry-group-code"></a>Definere en kode for bransjegruppe
Koden for bransjegruppen definerer typen eller kategorien for gruppen, for eksempel REKLAME for reklame, eller PRESSE, for TV og radio. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du vinduet **Bransjegrupper**.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bransjegrupper**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

## <a name="AssignIndustryGroupContact"></a> Tilordne bransjegrupper til en kontakt
Du kan ikke tilordne bransjegrupper til en kontaktperson, bare selskaper.

1. Åpne kontakten.
2. Velg handlingen **Selskap**, og deretter handlingen **Bransjegrupper**. Vinduet **Kontaktbransjegrupper** åpnes.
3. Velg bransjegruppen du vil tilordne, i feltet **Bransjegruppe - kode**.

Gjenta disse trinnene hvis du vil tilordne flere bransjegrupper. Du kan også tilordne bransjegrupper fra kontaktlisten ved å følge samme fremgangsmåte.

Antallet bransjegrupper du har tilordnet kontakten, vises i feltet **Ant. bransjegrupper** i inndelingen **Segmentering** i vinduet **Kontakt**.

Når du har tilordnet bransjegrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Opprette kontaktselskaper](marketing-create-contact-companies.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

