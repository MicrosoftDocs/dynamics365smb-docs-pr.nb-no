---
title: Definere webkilder for kontaktselskaper | Microsoft-dokumentasjon
description: "Du kan definere Internett-kilder eller webkilder og tilordne dem til et kontaktselskap for å bidra til å identifisere hvor du vil søke etter informasjon om kontaktene."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b80edfbbad575cfcaa15b2c1b79a4feacb077371
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a>Definere webkilder for kontaktselskaper
Du kan for eksempel bruke webkilder med kontaktselskaper for å identifisere søkemotorer og webområder på Internett, som du vil bruke til å søke etter informasjon om kontaktene. Når du tilordner webkilder, angir du hvilken søkemotor og søkeord programmet skal bruke for å finne de forespurte opplysningene.

Bruk av webkilder på kontakter er en totrinnsprosess. Først må du definere koden for webkilden. Du trenger bare utføre dette trinnet én gang for hver webkilde. Når du har en kode for webkilde, kan du begynne å tilordne koden til kontaktpersoner.

## <a name="to-define-a-web-source-code"></a>Slik definerer du en kode for webkilde
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Webkilder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene **Kode**, **Beskrivelse** og **URL**.

    Skriv inn %1 i feltet **Nettadresse** for å sette inn en plassholder for et søkeord i nettadressen. Når du starter webkilden fra et kontaktkort, erstattes %1 med søkeordet (for eksempel navnet på selskapet) som du angav i vinduet **Kontaktens webkilder**.

Gjenta disse trinnene hvis du vil definere flere webkilder.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Slik tilordner du webkilder til et kontaktselskap
Når du tilordner webkilder, angir du hvilken søkemotor og søkeord som programmet skal bruke for å finne de forespurte opplysningene.

1. Åpne kontakten.
2. Velg handlingen **Selskap**, og velg deretter handlingen **Webkilder**. Vinduet **Kontaktens webkilder** åpnes.
3. Velg webkilden du vil tilordne i feltet **Webkilde - kode**.
4. I feltet **Søkeord** angir du et søkeord som du vil bruke for å finne opplysningene.

Gjenta disse trinnene hvis du vil tilordne flere webkilder.

Ved å følge samme fremgangsmåte kan du også tilordne webkilder fra vinduet **Kontaktoversikt**.

## <a name="see-also"></a>Se også
[Opprette kontaktselskaper](marketing-create-contact-companies.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

