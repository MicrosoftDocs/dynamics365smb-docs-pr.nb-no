---
title: Bruke Excel til å importere data til Business Central
description: Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 413e9b2f6ec872a03ca2e7e95df240fc3308cab2
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754445"
---
# <a name="importing-business-data-from-other-finance-systems"></a>Importere forretningsdata fra andre økonomisystemer

Når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)], kan du velge å opprette et tomt firma, slik at du kan laste opp dine egne data og teste det nye [!INCLUDE[prod_short](includes/prod_short.md)]-firmaet. Avhengig av økonomiløsning som selskapet ditt bruker i dag, kan du overføre informasjon om kunder, leverandører, lager og bankkonti.  

Fra Rollesenteret kan du starte en assistert oppsettsveiledning som hjelper deg med å overføre forretningsdata fra en Excel-fil eller fra andre formater. Filtypene du kan laste opp, avhenger av utvidelsene som er tilgjengelige. Du kan for eksempel overføre opp data fra QuickBooks fordi [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en utvidelse som håndterer konverteringen fra QuickBooks. Hvis du vil overføre data fra andre økonomiløsninger, må du kontrollere om en utvidelse er tilgjengelig for denne løsningen eller importere fra Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder maler for kontoer, kunder, leverandører og lagervarer, som du kan velge å bruke når du importerer dataene.

Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken.  

> [!TIP]  
> Vi anbefaler at du bruker veivisere for datamigrering til å importere data fra Dynamics GP, Dynamics NAV eller QuickBooks. Hvis du vil ha mer informasjon, kan du se [Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet eller [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md).

> [!NOTE]  
> For omfattende implementasjonsarbeid kan du bruke RapidStart Services for [!INCLUDE[prod_short](includes/prod_short.md)], et omfattende verktøy for å definere nye løsninger basert på kundens forretningskrav og oppsettsdata. RapidStart Services har dessuten funksjoner for import av forretningsdata. Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

For å importere varebilder kan du bruke en egen funksjon på siden **Lageroppsett**. Hvis du vil ha mer informasjon, se [Importere flere varebilder](inventory-how-import-item-pictures.md).

## <a name="importing-data-from-configuration-packages"></a>Importere data fra konfigurasjonspakker
[!INCLUDE[prod_short](includes/prod_short.md)] inkluderer en konfigurasjonspakke som du kan eksportere til Excel og definere dataene der. Deretter kan du importere dataene fra Excel på nytt. Pakken består av 27 tabeller, inkludert hoveddata som kunder, leverandører, varer, og kontoer, andre grunnleggende oppsettstabeller, for eksempel frakt og transaksjonerstabeller, som salgshode og linjer.  

> [!NOTE]  
>   Arbeide med konfigurasjonspakker er avanserte funksjoner, og vi anbefaler at du kontakter systemansvarlig. For mer informasjon, se [Importere data fra eldre regnskapsprogramvare ved hjelp av en konfigurasjonspakke](across-import-data-configuration-packages.md).

## <a name="working-with-data-in-excel"></a>Arbeide med data i Excel
Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken. Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel. Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle. Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det. Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata. Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.  

> [!IMPORTANT]  
>  Ikke endre kolonnene i forslagene. Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Felt av typen blob kan ikke eksporteres/importeres i Excel.

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
-   Finans- kladdelinje
-   Varekladdelinje
-   Bokføringsgruppe - kunde
-   Bokføringsgruppe - leverandør
-   Bokføringsgruppe - lager
-   Enht.
-   Finans- - firma
-   Finans- - vare
-   Generelt bokføringsoppsett
-   Distrikt
-   Varekategori
-   Salgspris
-   Kjøpspris

## <a name="see-also"></a>Se også
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Importere flere varebilder](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  
