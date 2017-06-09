---
title: Definere salgssykluser for salgsmuligheter og syklusfaser | Microsoft-dokumentasjon
description: Beskriver hvordan du definerer salgssykluser for salgsmuligheter og syklusfaser i Financials.
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
ms.openlocfilehash: 63d3e4689a751e8e56363efcfde1d609762a419e
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-set-up-opportunity-sales-cycles-and-cycle-stages"></a>Definere salgssykluser for salgsmuligheter og syklusfaser
Før du kan begynne å bruke salgsmuligheter, må du definere salgssykluser og salgssyklusfaser. En salgssyklus består av en serie med faser som går fra den første kontakten til avslutningen av et salg. Hver fase kan ha bestemte krav som må oppfylles, for eksempel at et tilbud er påkrevd, før en salgsmulighet kan gå til neste fase. Du kan også angi om en fase kan utelates. Du kan definere så mange salgssykluser du trenger, og du kan definere så mange salgssyklusfaser som nødvendig i en salgssyklus.

Implementering av salgssykluser for salgsmulighet innebærer å definere salgssykluskode, definere de ulike syklusfasene, og deretter tilordne syklusen til salgsmuligheter.

## <a name="to-set-up-an-opportunity-sales-cycle-code"></a>Definere salgssykluskode for salgsmulighet
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Salgssykluser**, og deretter velger du den beslektede koblingen. Vinduet **Salgssykluser** åpnes, og det viser alle eksisterende salgssykluser.
2. Velg handlingen **Ny**, og fyll ut feltene.

Gjenta disse trinnene for å konfigurere så mange salgssykluser som du vil. Etter at du har definert salgssykluser for salgsmuligheter, bør du definere ulike faser i hver enkelt syklus.

## <a name="to-define-opportunity-sales-cycle-stages"></a>Definere salgssyklusfaser for salgsmulighet
1. I vinduet **Salgssykluser** velger du salgssyklusen for salgsmuligheten du vil definere faser for, og deretter velger du handlingen **Faser**. Vinduet **Salgssyklusfaser** åpnes.
2. Velg handlingen **Ny** for å angi en ny fase i salgssyklusen.

Gjenta disse trinnene hvis du vil definere flere faser i salgssyklusen.

## <a name="to-assign-stage-cycle-to-an-opportunity"></a>Tilordne fasesyklus til en salgsmulighet
Når du legger til fasesyklusen for salgsmulighet, kan du begynne å legge til salgsmuligheter og deretter tilordne fasesyklusen til salgsmuligheter ved å bruke feltet **Salgssykluskode**. Hvis du vil ha mer informasjon, kan du se [Opprette salgsmuligheter](marketing-how-create-opportunities.md).

## <a name="see-also"></a>Se også
[Behandle salgsmuligheter](marketing-processing-sales-opportunities.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

