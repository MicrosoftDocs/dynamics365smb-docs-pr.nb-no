---
title: Definere webkilder for kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker webkilder for kontakter i Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8a452619aeeee907cf61fd5d1a8fce409ad2e42d
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-web-sources-for-contact-companies"></a>Definere webkilder for kontaktselskaper
Du kan for eksempel bruke webkilder med kontaktselskaper for å identifisere søkemotorer og webområder på Internett, som du vil bruke til å søke etter informasjon om kontaktene. Når du tilordner webkilder, angir du hvilken søkemotor og søkeord programmet skal bruke for å finne de forespurte opplysningene.

Bruk av webkilder på kontakter er en totrinnsprosess. Først må du definere koden for webkilden. Du trenger bare utføre dette trinnet én gang for hver webkilde. Når du har en kode for webkilde, kan du begynne å tilordne koden til kontaktpersoner.

## <a name="to-define-a-web-source-code"></a>Definere en kode for webkilde
1. I øvre høyre hjørne velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Webkilder**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene **Kode**, **Beskrivelse** og **URL**.

    Skriv inn %1 i feltet **Nettadresse** for å sette inn en plassholder for et søkeord i nettadressen. Når du starter webkilden fra et kontaktkort, erstattes %1 med søkeordet (for eksempel navnet på selskapet) som du angav i vinduet **Kontaktens webkilder**.

Gjenta disse trinnene hvis du vil definere flere webkilder.

## <a name="to-assign-web-sources-to-a-contact-company"></a>Tilordne webkilder til et kontaktselskap
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

