---
title: Definere datautveksling | Microsoft-dokumentasjon
description: Definere rammeverket for datautveksling i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 5fa6f0ea5f12d44ae538df5a2be3489819963e47
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692827"
---
# <a name="setting-up-data-exchange"></a>Definere datautveksling
Før du kan sende og motta elektroniske dokumenter eller importere og eksportere bankfiler, må du definere rammeverket for datautveksling til å behandle filer som er involvert. I tillegg må du definere tilknyttede områder, for eksempel kundene du sender elektroniske fakturaer til, eller utvidelsen AMC Banking 365 Fundamentals hvis du bruker den eksterne tjenesteleverandøren til å konvertere bankfilene. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

 Når [!INCLUDE[d365fin](includes/d365fin_md.md)] er konfigurert til å utveksle data med eksterne filer, kan brukere bruke oppsettet i vanlige forretningsoppgaver, for eksempel sending og mottak av elektroniske dokumenter og import og eksport av bankfiler.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definer den forhåndskonfigurerte dokumentutvekslingstjenesten til å aktivere sending og mottak av elektroniske dokumenter fra og til [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)|  
|Definer den forhåndskonfigurerte OCR-tjenesten til å omgjøre PDF- eller bildefiler til elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Konfigurere inngående dokumenter](across-how-setup-income-documents.md)|  
|Definer ett av to forhåndskonfigurerte tjenester for oppdaterte valutakurser for å få de siste valutakursene på **Valutaer**-siden.|[Oppdatere valutakurser](finance-how-update-currencies.md)|  
|Definer forskjellige hoveddata, for eksempel firmainformasjon, kunder, leverandører, varer og enheter, relatert til tilordning av data i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Definere en bankkonto, leverandør og en utbetalingskladd for SEPA-kredittoverføring.|[Definere SEPA-kredittoverføring](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Klargjør bankkontoformater, betalingsmetoder og kundeavtaler for SEPA direct debit.|[Definere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)|  
|Konfigurer brukergodkjenning og URL-adressen til leverandøren av tjenesten for bankdatakonvertering som kreves for å få bankfiler konvertert til bankens format.|[Bruke utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)|  
|Konfigurer og aktiver en ekstern tjeneste som lar deg importere bankkontoutdrag direkte som bankfeeder.|[Konfigurere tjeneste for konvertering av bankdata](bank-how-setup-bank-statement-service.md)|  
|Når tjenesten for bankkontoutdrag er aktivert, må du koble bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Opprette bankkonti](bank-how-setup-bank-accounts.md)|  
|Gjør klar til å sette opp en ny datautvekslingsdefinisjon for en datafil eller datastrøm ved å bruke XML-skjemaet for filen til å forhåndsutfylle hurtigfanen **Kolonnedefinisjoner** på siden **Definisjoner av bokføringsutveksling**.|[Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Definer rammeverket for datautveksling for å la brukerne motta et nytt kjøpsdokumentformat, sende et nytt salgsdokumentformat, importere en ny bankfil, eller annen datautveksling.|[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Se også  
[Utveksle data elektronisk](across-data-exchange.md)  
[Utveksle data](across-exchange-data.md)   
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
