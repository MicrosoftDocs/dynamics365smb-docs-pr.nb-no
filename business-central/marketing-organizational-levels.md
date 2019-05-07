---
title: Definere organisasjonsnivåer for kontaktpersoner | Microsoft-dokumentasjon
description: Du kan definere et organisasjonsnivå og tilordne det til kontakten for å angi hvilken stilling de har i selskapet sitt, for eksempel en stilling i toppledelsen.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 68f20af84652f684eaa0d69c98e0dc3cb722ee91
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "931341"
---
# <a name="set-up-organizational-levels-for-contact-persons"></a>Definere organisasjonsnivåer for kontaktpersoner
Du kan bruke organisasjonsnivåer på kontaktene for å angi hvilken stilling de har i selskapet, for eksempel en stilling i toppledelsen. Du kan bruke denne informasjonen når du oppgir opplysninger om kontaktene.

Bruk av organisasjonsnivåer på kontakter er en totrinnsprosess. Først må du definere koden for organisasjonsnivået. Du trenger bare utføre dette trinnet én gang for hvert organisasjonsnivå. Når du har en kode for organisasjonsnivå, kan du begynne å tilordne koden til kontaktpersoner.

## <a name="to-define-an-organizational-level-code"></a>Slik definerer du en kode for organisasjonsnivå
Koden for organisasjonsnivå definerer jobbtype eller -kategori for organisasjonsnivået, for eksempel ADMDIR eller ØKDIR. Du kan ha flere koder for organisasjonsnivå. Hvis du vil definere organisasjonsnivået, bruker du siden **Organisasjonsnivåer**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Organisasjonsnivåer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**, og fyll ut en kode og en beskrivelse. Koden kan bestå av opptil 11 tegn, og kan inneholde en kombinasjon av tall og bokstaver.

## <a name="to-assign-organizational-levels-to-a-contact-person"></a>Slik tilordner du organisasjonsnivåer til en kontaktperson
Du kan bare tilordne organisasjonsnivåer til kontaktpersoner, ikke selskaper. Du kan bare tilordne ett organisasjonsnivå til hver enkelt kontakt.

1. Åpne kontakten.
2. I feltet **Organisasjonsnivåer** velger du koden du vil tilordne.

Når du har tildelt organisasjonsnivåer til kontaktene, kan du bruke disse opplysningene til å opprette segmenter.

Når du har tilordnet ansvarsområder til kontaktene, kan du bruke disse opplysningene til å velge kontakter for segmentene. Hvis du vil ha mer informasjon, kan du se [Legge til kontakter i segmenter](marketing-add-contact-segment.md).

## <a name="see-also"></a>Se også
[Opprette kontakter](marketing-create-contact-companies.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
