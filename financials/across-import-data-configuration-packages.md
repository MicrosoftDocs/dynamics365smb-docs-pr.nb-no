---
title: "Bruke Excel til å hente inn eldre data til Financials | Microsoft-dokumentasjon"
description: "Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0151b1c3d8bddd4692c494d1c0e5d1c036da424e
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="importing-data-from-legacy-accounting-software-using-a-configuration-package"></a>Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke
Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[d365fin](includes/d365fin_md.md)]. I vinduet **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.  

Hvis du er kjent med RapidStart-tjenester for Microsoft Dynamics, er du også kjent med konfigurasjonspakker. Standard konfigurasjonspakke støtter de fleste vanlige typer data som du vil importere fra et eldre system. I Excel kan du deretter legge til data fra det gamle systemet og konfigurere dem i henhold til forretningslogikken i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
