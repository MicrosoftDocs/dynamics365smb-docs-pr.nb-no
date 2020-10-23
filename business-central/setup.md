---
title: Oversikt over oppgaver for å definere Business Central | Microsoft-dokumentasjon
description: Gir en oversikt over oppgaver for å definere, initialisere og konfigurere Business Central etter behov.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: configure, initialize
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 0f33f59975973d8b585c97b53a3801e8706346fc
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912824"
---
# <a name="setting-up-prodshort"></a>Konfigurere [!INCLUDE[prodshort](includes/prodshort.md)]

[!INCLUDE[prodshort](includes/prodshort.md)] inneholder standardkonfigurasjoner for de fleste forretningsprosesser, men du kan endre konfigurasjonen slik at den passer til behovene for organisasjonen.

Kontoplanen er for eksempel forhåndsutfylt med en rekke posteringskontoer som er klar til bruk. Du kan selvsagt endre kontoplanen til dine behov. Hvis du vil ha mer informasjon, kan du se [Finans](finance.md).

Fra menyen ![Sprocket-ikon for å åpne Innstillinger-meny](media/ui-experience/settings_icon_small.png) får du tilgang til hjelpelinjer for assistert installasjon, som hjelper deg med å konfigurere visse scenarier og legge til funksjoner i [!INCLUDE[prodshort](includes/prodshort.md)]. Hvis du vil ha informasjon om hvordan du får tilgang til og definerer sider manuelt, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md).

Noe funksjonalitet, både generell eller for bestemte forretningsprosesser, kan defineres manuelt i tillegg til den assisterte oppsettsveiledningen. Nedenfor vises noen av funksjonaliteten som du kan du kan angi manuelt.

| Hvis du vil | Se |
| --- | --- |
| Sett opp betalingsmåter, valutaer og kontoplanen, og definer regler og standarder for håndtering av finanstransaksjoner. |[Konfigurere finans](finance-setup-finance.md) |
| Sett opp din egen og leverandørenes bank kontoer og aktivere tjenester for import og eksport av bankfilene. |[Konfigurere banktjenester](bank-setup-banking.md) |
| Konfigurere regler og verdier som definerer selskapets policyer for salg, registrere nye kunder og definere hvordan du kommuniserer med kundene. |[Sette opp salg](sales-setup-sales.md) |
| Konfigurere regler og verdier som definerer selskapets innkjøpspolicyer, registrere nye leverandører og prioritere leverandørene for betalingsbehandling. |[Definere kjøp](purchasing-setup-purchasing.md) |
| Konfigurere regler og verdier som definerer firmaets lager, sette opp steder Hvis du beholder lager i flere lagre og kategorisere elementer for å forbedre søk og sortering. |[Definere lager](inventory-setup-inventory.md) |
| Konfigurer ressurser, timelister og jobber til å administrere prosjekter. |[Konfigurere prosjektstyring](projects-setup-projects.md) |
| Konfigurere hvordan du forsikrer, vedlikeholder og avskrivner aktiva, og hvordan du registrerer kostnadene for aktiva i bedriftsbøkene. |[Definere aktiva](fa-setup.md) |
|Definere generelle regler og verdier for lagerprosesser og den spesifikke håndteringen på hver lokasjon.|[Definere lagerstyring](warehouse-setup-warehouse.md)|
|Klargjør produksjonsstykklister og ruter til å definere hvordan sluttvarer produseres, og klargjør produksjonsressurser eller arbeidssentre til å utføre de nødvendige operasjonene.|[Definere produksjon](production-configure-production-processes.md)|
|Etablere standardtjenester, symptomer og feilkoder og sette opp servicevarer, ressurser og dokumentasjon som trengs for å gi service til kundene dine.|[Konfigurere servicehåndtering](service-setup-service.md)|
|Lese beste rutiner for å angi varene for beholdning og kostpris og forsyningsplanlegging.|[Konfigurere komplekse moduler ved å bruke anbefalte fremgangsmåter](set-up-complex-application-areas-using-best-practices.md)|
|Forbedre kvaliteten på implementering og forkort distribusjonstiden ved hjelp av et verktøysettet for å opprette et nytt selskap ved hjelp av veivisere, maler, forslag og kundespørreskjemaer.|[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)|
|Overfør informasjon om kunder, leverandører, lager og bankkonti fra et annet system til [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).|
|Bruk Outlook-tillegg for Business Central til å se økonomiske data relatert til kunder og leverandører, eller opprett og send økonomiske dokumenter, for eksempel tilbud og fakturaer.|[Bruke Business Central som forretningsinnboksen i Outlook](admin-outlook.md)|
|Få innsikt i Business Central-data med Power BI- og Business Central-innholdspakker.|[Aktivere forretningsdata for Power BI](admin-powerbi.md)|
|Bruke Business Central-data som en del av en arbeidsflyt i Power Automate.|[Bruke Business Central i en automatisk arbeidsflyt](across-how-use-financials-data-source-flow.md)|
|Gjør Business Central-data tilgjengelige som en datakilde i Power Apps.|[Koble til Business Central-dataene for å utvikle en forretningsapp ved hjelp av Power Apps](across-how-use-financials-data-source-powerapps.md)|
|Bruk dedikerte Quickbooks-migreringsveiledninger.|[Endre fra en QuickBooks-app til Business Central](across-quickbooks-to-business-edition.md)|
|Få tilgang til Business Central-data fra mobilenheten.|[Få Business Central på mobilenheten din](install-mobile-app.md)|
|Utfør massefakturering av avtaler som er opprettet i Bookings.|[Massefakturering for Microsoft Bookings](finance-bookings.md)|
|Definer en SMTP-server for å aktivere e-kommunikasjon inn og ut av [!INCLUDE[d365fin](includes/d365fin_md.md)].| [Konfigurere e-post manuelt eller bruke assistert oppsett](admin-how-setup-email.md)|
| Definer unike identifikasjonskodene for poster, for eksempel kort, bilag og kladdelinjer, til å spore dem i systemet. |[Opprette nummerserier](ui-create-number-series.md) |
|Definere og tilordner en hovedkalender til selskapet med forretningspartnere, for eksempel kunder, leverandører eller lokasjoner. Leverings- og mottaksdatoer i fremtidige ordrer, bestillinger, overføringsordrer og produksjonsordrelinjer beregnes i henhold til virkedagene som er angitt i kalenderen.|[Definere hovedkalendere](across-how-to-assign-base-calendars.md)|  

Noen områder krever at du er administrator i [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement. Se også [Administrasjon](admin-setup-and-administration.md) for mer informasjon.  

> [!NOTE]
> Som administrator kan du konfigurere et nytt selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)] med RapidStart Services. RapidStart Services er et verktøy som er utviklet for å forkorte distribusjonstiden, forbedre kvaliteten på implementeringen, introdusere en implementeringsmetode som kan gjentas og øke produktiviteten ved å automatisere og forenkle regelmessige oppgaver. Hvis du vil ha mer informasjon, kan du se [Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

## <a name="see-also"></a>Se også

[Administrasjon](admin-setup-and-administration.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Lager](inventory-manage-inventory.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Aktiva](fa-manage.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Produksjon](production-manage-manufacturing.md)  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Opprette nye seleskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)  
[Komme i gang](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
