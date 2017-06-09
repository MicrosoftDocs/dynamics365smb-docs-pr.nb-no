---
title: Definere bransjegrupper for kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker bransjegrupper med kontaktene i Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Definere bransjegrupper for kontaktselskaper
Du bruker bransjegrupper for å angi hvilken bransje kontaktene tilhører, for eksempel detaljistbransjen eller bilbransjen.

Bruk av bransjegrupper på kontakter er en totrinnsprosess. Først må definere du koden for bransjegruppen. Du trenger bare utføre dette trinnet én gang for hver bransjegruppe. Når du har en kode for bransjegruppe, kan du begynne å tilordne koden til kontaktselskaper.

**Merk**: Hvis du vil synkronisere kontaktene med leverandører, kunder eller bankkonti i andre deler av applikasjonen, bør du definere en forretningsforbindelse for disse.

## <a name="to-define-an-industry-group-code"></a>Definere en kode for bransjegruppe
Koden for bransjegruppen definerer typen eller kategorien for gruppen, for eksempel REKLAME for reklame, eller PRESSE, for TV og radio. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du vinduet **Bransjegrupper**.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Bransjegrupper**, og deretter velger du den beslektede koblingen.
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

