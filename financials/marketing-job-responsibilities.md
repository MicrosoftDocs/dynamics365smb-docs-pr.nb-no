---
title: "Definere ansvarsområder for kontakter | Microsoft-dokumentasjon"
description: "Du kan definere en kode for ansvarsområde og tilordne den til en kontakt for å angi oppgavene som kontakten er ansvarlig for i selskapet, for eksempel IT eller produksjon."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: task, to-do, relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 673c7a118c5f589319bd967bfaea3bedef84f9ff
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-job-responsibilities-for-contact-persons"></a>Definere ansvarsområder for kontaktpersoner
Du kan legge til informasjon om ansvarsområder for kontaktpersoner for å angi hva kontaktpersonen har ansvaret for i selskapet, for eksempel IT, ledelse eller produksjon. Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.

Bruk av ansvarsområder på kontakter er en totrinnsprosess. Først må definere du koden for ansvarsområdet. Du trenger bare utføre dette trinnet én gang for hvert ansvarsområde. Når du har en kode for ansvarsområde, kan du begynne å tilordne koden til kontaktpersoner.

## <a name="to-define-a-job-responsibility-code"></a>Definere en kode for ansvarsområde
Koden for ansvarsområde definerer jobbtype eller -kategori, for eksempel MARKEDSFØRING eller INNKJØP. Du kan ha flere koder for ansvarsområde. Hvis du vil definere ansvarsområde, bruker du vinduet **Ansvarsområder**.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Ansvarsområder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

## <a name="to-assign-job-responsibilities-to-a-contact-person"></a>Tilordne ansvarsområder til en kontaktperson
Du kan ikke tilordne ansvarsområder til kontaktselskaper.

1. Åpne kontaktpersonen.
2. Velg handlingen **Person**, og velg deretter handlingen **Ansvarsområder**. Vinduet **Kontaktens ansvarsområder** åpnes.
3. Velg ansvarsområdet som du vil tilordne, i feltet **Ansvarsområde - kode**.

Gjenta disse trinnene hvis du vil tilordne flere ansvarsområder. Ved å følge samme fremgangsmåte kan du også tilordne ansvarsområder fra kontaktlisten.

Antallet ansvarsområder du har tilordnet kontakten, vises i feltet **Ant. ansvarsområder** i inndelingen **Segmentering** i vinduet **Kontakt**.

Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Opprette kontaktpersoner](marketing-create-contact-persons.md)  
[Opprette kontaktselskaper](marketing-create-contact-companies.md)  
[Arbeide med Financials](ui-work-product.md)

