---
title: Definere koder for forretningsforbindelse for kontakter | Microsoft-dokumentasjon
description: Bruk forretningsforbindelser i Business Central til å hjelpe til med markedsføring, og til å angi hvilket forretningsforhold du har til prospekter, klienter og kunder, for eksempel en bank eller serviceleverandør.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ffeb19820b29453750ca9c03258d455dddff287c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239340"
---
# <a name="setting-up-business-relations-on-contacts"></a>Definere forretningsforbindelser for kontakter
Du kan bruke forretningsforbindelser til å angi hvilket forretningsforhold du har til kontaktene, for eksempel prospekter, banker, konsulenter, serviceleverandører og så videre.

Bruk av forretningsforbindelser på kontakter er en totrinnsprosess. Først må definere du koden for forretningsforbindelsen. Du trenger bare utføre dette trinnet én gang for hver forretningsforbindelse. Når du har en kode for forretningsforbindelse, kan du begynne å tilordne koden til kontaktselskaper.

> [!NOTE]  
>   Hvis du planlegger å synkronisere kontaktene med leverandører, kunder eller bankkonti i andre deler av programmet, bør du definere en forretningsforbindelse for disse.

## <a name="to-define-a-business-relation-code"></a>Definere en kode for forretningsforbindelse
Koden for forretningsforbindelsen definerer en kategori eller type for forretningsforbindelsen, for eksempel BANK eller Juridisk. Du kan ha flere forretningsforbindelseskoder. Hvis du vil definere forretningsforbindelsen, bruker du siden **Forretningsforbindelser**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Forretningsforbindelser**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

## <a name="AssignBusRelContact"></a> Tilordne forretningsforbindelser til en kontakt
Du kan ikke tilordne forretningsforbindelser til en kontaktperson, bare selskaper.

1. Åpne kontakten.
2. Velg handlingen **Selskap**, og deretter handlingen **Forretningsforbindelser**.

    Siden **Kontaktens forretn.forbind.** åpnes.
3. Velg forretningsforbindelsen du vil tilordne, i feltet **Forretn.forbindelseskode**.

Gjenta disse trinnene hvis du vil tilordne flere forretningsforbindelser. Du kan også tilordne forretningsforbindelser fra kontaktlisten ved å følge samme fremgangsmåte.

Antall forretningsforbindelser du har tilordnet kontakten, vises i feltet **Ant. forretningsforbindelser** i inndelingen **Segmentering** på siden **Kontakt**.

Når du har tilordnet forretningsforbindelser til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
