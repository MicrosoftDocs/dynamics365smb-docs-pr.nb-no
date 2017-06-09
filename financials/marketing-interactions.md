---
title: Samhandlinger | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker samhandlinger med kontaktene i Financials.
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
ms.openlocfilehash: a423f5581f6803b60a0351d0b91f2c08ebafeba7
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="managing-interactions-with-contacts"></a>Håndtere samhandlinger med kontakter
I [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] betraktes all slags kommunikasjon mellom selskapet og kontaktene som samhandlinger. Kommunikasjon kan for eksempel være per brev, telefaks, e-post, telefonsamtaler, møter og så videre.

Området for relasjonshåndtering lar deg registrere alle samhandlingene med kontaktene, slik at du kan følge opp salgs- og markedsføringskampanjene som er rettet mot kontaktene, og forbedre fremtidige forretningssamhandlinger med dem. Konfigurasjon av programmet til å registrere samhandlinger består av disse oppgavene:

* Definere samhandlingsmaler  
* Opprette samhandlinger på kontakter eller segmenter  
* Vise og administrere registrerte samhandlinger  

##  <a name="set-up-interaction-templates"></a>Definere samhandlingsmaler
Før du kan opprette og registrere samhandlinger, må du definere samhandlingsmaler. Når du oppretter samhandlinger, må du angi hvilke samhandlingsmaler de baserer seg på. En samhandlingsmal en modell som definerer de grunnleggende egenskapene for en samhandling.
Du kan definere en samhandlingsmal i vinduet **Samhandlingsmaler**.  

## <a name="create-interactions"></a>Opprett samhandlinger
Du kan registrere samhandlinger på to ulike måter:

* Du kan manuelt opprette samhandlinger som er knyttet til en enkelt kontakt eller til et segment. Hvis du vil ha mer informasjon, kan du se [Opprette samhandlinger på kontakter og segmenter](marketing-how-create-interactions.md).  
* Du kan angi at samhandlinger skal registreres automatisk når du utfører handlinger i programmet, for eksempel når du skriver ut en faktura eller et tilbud. Hvis du vil ha mer informasjon, kan du se [Automatisk registrere samhandlinger med kontaktene](marketing-auto-record-interactions.md).

## <a name="view-and-manage-recorded-interactions"></a>Vise og administrere registrerte samhandlinger
Du kan vise alle registrerte samhandlinger som ikke er slettet, i vinduet **Samhandlingsposter**. Du kan åpne dette vinduet ved å gjøre følgende:

* Bruke **Søk etter side eller rapport**-ikonet for å søke etter **Samhandlingsposter**.
* Velge handlingen **Samhandlingsposter** på en kontakt eller et segment.
  Vinduet **Samhandlingspost** viser hvilke samhandlinger du oppretter manuelt og hvilke samhandlinger som programmet registrerer automatisk.

I dette vinduet kan du gjøre følgende:

* Vise statusen til samhandlinger
* Merke samhandlinger som annullert.

Du kan slette samhandlingsposter som er annullert. Hvis du vil slette samhandlingsposter, går du til øvre høyre hjørne, velger ikonet**Søk etter side eller rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Slett annullerte samhandlingsposter**, velg den relaterte koblingen og fyll ut informasjonen.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md)  
[Arbeide med Financials](ui-work-product.md)  

