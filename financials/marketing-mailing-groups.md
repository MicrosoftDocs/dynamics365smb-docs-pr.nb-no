---
title: Definere postgrupper for kontakter| Microsoft-dokumentasjon
description: Beskriver postgrupper for kontakter i Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: fc29f5a6238373db3e862058eb327398e624882e
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-mailing-groups-for-contacts"></a>Definere postgrupper for kontakter
Du kan bruke postgrupper til å identifisere grupper av kontakter som du ønsker skal motta like opplysninger. Du kan for eksempel definere en postgruppe for kontaktene du vil sende en melding om kontorflytting til, eller en annen gruppe for sending av julegavene.

Bruk av postgrupper på kontakter er en totrinnsprosess. Først må definere du koden for postgruppen. Du trenger bare utføre dette trinnet én gang for hver postgruppe. Når du har en kode for postgruppe, kan du begynne å tilordne koden til kontaktselskaper.

## <a name="defining-mailing-group-codes"></a>Definere postgruppekoder
Koden for postgruppen definerer typen eller kategori for gruppen, for eksempel FLYTTE for kontorflytting eller GAVE julegave. Du kan ha flere koder for bransjegruppe. Hvis du vil definere bransjegrupper, bruker du vinduet **Postgrupper**.

1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Postgrupper**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

## <a name="AssignMailGroupContact"></a> Slik tilordner du postgrupper til en kontakt
1. Åpne kontakten.
2. Velg handlingen **Postgrupper**. Vinduet **Kontaktens postgrupper** åpnes.
3. Velg postgruppen du vil tilordne, i feltet **Postgruppekode**.

Gjenta disse trinnene hvis du vil tilordne flere postgrupper. Ved å følge samme fremgangsmåte kan du også tilordne postgrupper fra kontaktlisten.

Antallet postgrupper du har tilordnet kontakten, vises i feltet **Ant. postgrupper** i inndelingen **Segmentering** i vinduet **Kontakt**.

Når du har tilordnet postgrupper til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Opprette kontaktselskaper](marketing-create-contact-companies.md)  
[Opprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeide med Financials](ui-work-product.md)

