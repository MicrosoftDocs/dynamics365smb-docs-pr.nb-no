---
title: "Bruke Excel til å importere data til Financials | Microsoft-dokumentasjon"
description: "Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 591d8100100ee717a932d188a87545fe4098a001
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke
Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.  

> [!NOTE]  
> Konfigurasjonpakker er en del av RapidStart Services for [!INCLUDE[d365fin](includes/d365fin_md.md)], et omfattende verktøy for å definere nye løsninger basert på kundens forretningskrav og oppsettsdata. RapidStart Services har dessuten funksjoner for import av eldre data. Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

> [!TIP]  
>   Du kan også bruke veivisere for datamigrering til å importere data fra QuickBooks eller Dynamics GP. Hvis du vil ha mer informasjon, kan du se [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md) eller [Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="working-with-data-in-excel"></a>Arbeide med data i Excel
Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken. Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel. Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle. Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det. Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata. Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.  

> [!IMPORTANT]  
>  Ikke endre kolonnene i forslagene. Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="tables-in-the-default-configuration-package"></a>Tabeller i standard konfigurasjonspakke
Standard konfigurasjonspakke støtter følgende tabeller:

-   Betalingsbetingelser
-   Kundeprisgruppe
-   Leveringsmåte
-   Selger/innkjøper
-   Lokasjon
-   Finanskonto
-   Kunde
-   Leverandør
-   Element
-   Salgshode
-   Salgslinje
-   Bestillingshode
-   Bestillingslinje
-   Finanskladdelinje
-   Varekladdelinje
-   Bokføringsgruppe - kunde
-   Bokføringsgruppe - leverandør
-   Bokføringsgruppe - lager
-   Enht.
-   Bokføringsgruppe - firma
-   Bokføringsgruppe - vare
-   Generelt bokføringsoppsett
-   Distrikt
-   Varekategori
-   Salgspris
-   Kjøpspris

## <a name="importing-customer-data"></a>Importere kundedata
Når kundedataene er angitt i Excel, importerer du dataee til [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Konfigurasjonspakker** importerer du data fra Excel-filen, og du kan bekrefte at dataene er i samsvar med [!INCLUDE[d365fin](includes/d365fin_md.md)] før du installerer pakken.

## <a name="see-also"></a>Se også
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Dynamics GP-datamigrering](ui-extensions-dynamicsgp-data-migration.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

