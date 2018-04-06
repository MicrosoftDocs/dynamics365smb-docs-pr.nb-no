---
title: Importere gamle forretningsdata til Business Central | Microsoft-dokumentasjon
description: "Du kan overføre data for kunder, leverandører og lager, for eksempel fra Excel, QuickBooks eller Dynamics GP, til Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 25005f972cf541f12419ad34c76d1997c070a6d8
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Importere forretningsdata fra andre økonomisystemer
Når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du velge å opprette et tomt firma, slik at du kan laste opp dine egne data og teste det nye [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet. Avhengig av økonomiløsning som selskapet ditt bruker i dag, kan du overføre informasjon om kunder, leverandører, lager og bankkonti.  

Fra Rollesenteret kan du starte en assistert oppsettsveiledning som hjelper deg med å overføre forretningsdata fra en Excel-fil eller fra andre formater. Filtypene du kan laste opp, avhenger av utvidelsene som er tilgjengelige. Du kan for eksempel overføre opp data fra QuickBooks fordi [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder en utvidelse som håndterer konverteringen fra QuickBooks. Hvis du vil overføre data fra andre økonomiløsninger, må du kontrollere om en utvidelse er tilgjengelig for denne løsningen eller importere fra Excel.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder maler for kontoer, kunder, leverandører og lagervarer, som du kan velge å bruke når du importerer dataene.

> [!NOTE]  
> For omfattende implementasjonsarbeid kan du bruke RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], et omfattende verktøy for å definere nye løsninger basert på kundens forretningskrav og oppsettsdata. RapidStart Services har dessuten funksjoner for import av forretningsdata. Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Importere data fra QuickBooks Desktop, QuickBooks Online eller Dynamics GP
Hvis virksomheten din bruker QuickBooks eller Dynamics GP i dag, kan du eksportere relevant informasjon til en fil. Du kan deretter åpne den assistert oppsettsveiledningen for å overføre dataene.
Hvis filen for eksempel inneholder kunder og leverandører, kan du velge å overføre bare kundedata. Du kan deretter overføre resten av informasjonen senere.  

Det assisterte oppsettet inneholder et alternativ for å endre standardkonfigurasjonen for overføringen, men vi anbefaler at du bare bruker dette avanserte oppsettet hvis du har kjennskap til databasetabeller. I de aller fleste bedrifter vil standardtilordningen fra QuickBooks eller Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)] overføre informasjonen du vil bruke.  

Hvis du vil ha mer informasjon, se [Datamigrering for QuickBooks Desktop](ui-extensions-quickbooks-data-migration.md), [Datamigrering for QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md) og [Datamigrering for Dynamics GP](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Importere data fra konfigurasjonspakker
[!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer en konfigurasjonspakke som du kan eksportere til Excel og definere dataene der. Deretter kan du importere dataene fra Excel på nytt. Pakken består av 27 tabeller, inkludert hoveddata som kunder, leverandører, varer, og kontoer, andre grunnleggende oppsettstabeller, for eksempel frakt og transaksjonerstabeller, som salgshode og linjer.  

> [!NOTE]  
>   Arbeide med konfigurasjonspakker er avanserte funksjoner, og vi anbefaler at du kontakter systemansvarlig. For mer informasjon, se [Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke](across-import-data-configuration-packages.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Datamigrering for QuickBooks Desktop](ui-extensions-quickbooks-data-migration.md)  
[Datamigrering for QuickBooks Online](ui-extensions-quickbooks-online-data-migration.md)  
[Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)   
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

