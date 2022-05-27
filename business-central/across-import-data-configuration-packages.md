---
title: Bruke Excel til å importere data til Business Central
description: Bruk standard konfigurasjonspakke til å legge kundedata i Excel og importere dataene tilbake til Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migration, Excel
ms.date: 05/10/2022
ms.author: edupont
ms.openlocfilehash: a189f2f10ad9e8f2ab0063987fbafefd4ad1948f
ms.sourcegitcommit: 4853614c85beb347091c5c4c1ea8d974dec887fc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740368"
---
# <a name="import-business-data-from-other-finance-systems"></a>Importer forretningsdata fra andre økonomisystemer

Når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)], kan du velge å opprette et tomt firma, slik at du kan laste opp dine egne data og teste det nye [!INCLUDE[prod_short](includes/prod_short.md)]-firmaet. Avhengig av økonomiløsning som selskapet ditt bruker i dag, kan du overføre informasjon om kunder, leverandører, lager og bankkonti.  

Fra Rollesenteret kan du starte en assistert oppsettsveiledning som hjelper deg med å overføre forretningsdata fra en Excel-fil eller fra andre formater. Filtypene du kan laste opp, avhenger av utvidelsene som er tilgjengelige. Du kan for eksempel overføre opp data fra QuickBooks fordi [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en utvidelse som håndterer konverteringen fra QuickBooks. Hvis du vil overføre data fra andre økonomiløsninger, må du kontrollere om en utvidelse er tilgjengelig for denne løsningen eller importere fra Excel.  

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder maler for kontoer, kunder, leverandører og lagervarer, som du kan velge å bruke når du importerer dataene. For å importere varebilder kan du bruke en egen funksjon på siden **Lageroppsett**. Hvis du vil ha mer informasjon, se [Importere flere varebilder](inventory-how-import-item-pictures.md).

> [!TIP]  
> Vi anbefaler at du bruker veivisere for datamigrering til å importere data fra Dynamics GP, Dynamics NAV eller QuickBooks. Hvis du vil ha mer informasjon, kan du se [Overfør lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet eller [Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md).

## <a name="work-with-data-in-excel"></a>Arbeid med data i Excel

Du kan bruke Excel-tillegget til klargjøre eksisterende innhold for bruk i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Vise og redigere i Excel fra Business Central](across-work-with-excel.md).  

## <a name="import-data-from-configuration-packages"></a>Importer data fra konfigurasjonspakker

For større implementeringsarbeid kan du konfigurere løsningsspesifikke konfigurasjonspakker. Hvis du vil ha mer informasjon, kan du se [Konfigurer firmakonfigurasjonspakker](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (bare på engelsk) i utvikler- og administrasjonsinnholdet.  

> [!NOTE]  
> Arbeide med konfigurasjonspakker er avanserte funksjoner, og vi anbefaler at du kontakter forhandleren. Hvis du vil ha mer informasjon, kan du se [Konfigurer firmakonfigurasjonspakker](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages) (bare på engelsk).

Du kan importere hoveddata og noen transaksjonsdata fra andre finanssystemer som er basert på standard konfigurasjonspakke i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Konfigurasjonspakker** kan du arbeide med pakken for å importere og validere dataene før du bruker pakken. Du kan for eksempel eksportere konfigurasjonspakken til Excel og definere dataene der. Deretter kan du importere dataene fra Excel på nytt. Pakken består av 27 tabeller, inkludert hoveddata som kunder, leverandører, varer, og kontoer, andre grunnleggende oppsettstabeller, for eksempel frakt og transaksjonerstabeller, som salgshode og linjer.  

Når du eksporterer standard konfigurasjonspakke til Excel, inneholder generert arbeidsboken et regneark for hver tabell i pakken. Du kan forenkle oppgavene ved å bruke verktøyene for XML-manipulering i Excel. Du kan også bruke innebygde Excel-funksjoner for å få hjelp med dataformatering og plassering av data i riktig celle. Du kan for eksempel legge til et tomt regneark og kopiere de gamle dataene til det. Lag deretter en Excel-formel til å tilordne data i transformasjonsregnearket mellom feltene i det eksporterte regnearket og eldre kundedata. Når du har tilordnet alle dataene, kan du kopiere dataområdet til tabellforslaget.  

> [!IMPORTANT]  
> Ikke endre kolonnene i forslagene. Hvis du flytter, endrer eller sletter dem, kan ikke regnearket importeres til [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Felt av typen blob kan ikke eksporteres/importeres i Excel.

### <a name="tables-in-the-default-configuration-package"></a>Tabeller i standard konfigurasjonspakke

Standard konfigurasjonspakke støtter følgende tabeller:

- Betalingsbetingelser
- Kundeprisgruppe
- Leveringsmåte
- Selger/innkjøper
- Lokasjon
- Finanskonto
- Kunde
- Leverandør
- Element
- Salgshode
- Salgslinje
- Bestillingshode
- Bestillingslinje
- Finans- kladdelinje
- Varekladdelinje
- Bokføringsgruppe - kunde
- Bokføringsgruppe - leverandør
- Bokføringsgruppe - lager
- Enht.
- Finans- - firma
- Finans- - vare
- Generelt bokføringsoppsett
- Distrikt
- Varekategori
- Salgspris
- Kjøpspris

## <a name="see-also"></a>Se også

[Overføre lokale data til Business Central Online (bare på engelsk)](/dynamics365/business-central/dev-itpro/administration/migrate-data)  
[Konfigurer selskapskonfigurasjonspakker](/dynamics365/business-central/dev-itpro/administration/set-up-standard-company-configuration-packages)  
[Datamigrering for QuickBooks](ui-extensions-quickbooks-data-migration.md)  
[Importere flere varebilder](inventory-how-import-item-pictures.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]