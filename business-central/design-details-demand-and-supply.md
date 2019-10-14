---
title: Designdetaljer – Behov og forsyning | Microsoft-dokumentasjon
description: Behov er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre. I tillegg tillater programmet mer tekniske typer behov, for eksempel negativ beholdning og bestillingsreturer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.openlocfilehash: 8ef7211aa812b1faf784ecf36f1873a6e2dcc6fc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303632"
---
# <a name="design-details-demand-and-supply"></a>Designdetaljer: Behov og forsyning
Behov er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel ordre- og komponentbehov fra en produksjonsordre. I tillegg tillater programmet mer tekniske typer behov, for eksempel negativ beholdning og bestillingsreturer.  

 Forsyning er den vanlige betegnelsen som brukes om alle typer positive eller inngående antall, for eksempel beholdning, kjøp, montering, produksjon eller inngående overføringer. I tillegg kan en ordreretur også representere forsyning.  

 For å sortere ut de mange kildene til behov og forsyning organiserer planleggingssystemet dem på to tidslinjer kalt beholdningsprofiler. Én profil inneholder behovshendelser, og den andre inneholder tilsvarende forsyningshendelser. Hver hendelse representerer én ordrenettverksenhet, for eksempel en salgsordrelinje, en varepost eller en produksjonsordrelinje.  

 Når du beholdningsprofiler lastes inn, balanseres de ulike settene med behov/forsyning for å gi en forsyningsplan som oppfyller de angitte målene.  

 Planleggingsparametre og lagernivåer er henholdsvis andre typer behov og forsyning som gjennomgå integrert balansering for å etterfylle lagervarer. Hvis du vil ha mer informasjon, se [Designdetaljer: Håndtere gjenbestillingsprinsipper](design-details-handling-reordering-policies.md).  

## <a name="see-also"></a>Se også  
 [Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
 [Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
 [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
