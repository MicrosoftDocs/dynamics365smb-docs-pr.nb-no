---
title: Konfigurering av datautveksling for å sende og motta filer
description: 'Konfigurer rammeverket for datautveksling for å kunne utveksle data med eksterne filer: sende og motta elektroniske dokumenter eller importere og eksportere bankfiler.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 9736a1ea6c0da0381a14c8e77eabaaf752ea9f34
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133281"
---
# <a name="setting-up-data-exchange"></a>Definere datautveksling
Før du kan sende og motta elektroniske dokumenter eller importere og eksportere bankfiler, må du definere rammeverket for datautveksling til å behandle filer som er involvert. I tillegg må du definere tilknyttede områder, for eksempel kundene du sender elektroniske fakturaer til, eller utvidelsen AMC Banking 365 Fundamentals hvis du bruker den eksterne tjenesteleverandøren til å konvertere bankfilene. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

 Når [!INCLUDE[prod_short](includes/prod_short.md)] er konfigurert til å utveksle data med eksterne filer, kan brukere bruke oppsettet i vanlige forretningsoppgaver, for eksempel sending og mottak av elektroniske dokumenter og import og eksport av bankfiler.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.  

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Definer den forhåndskonfigurerte dokumentutvekslingstjenesten til å aktivere sending og mottak av elektroniske dokumenter fra og til [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurere en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md)|  
|Definer den forhåndskonfigurerte OCR-tjenesten til å omgjøre PDF- eller bildefiler til elektroniske dokumenter som kan konverteres til dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurere inngående dokumenter](across-how-setup-income-documents.md)|  
|Definer ett av to forhåndskonfigurerte tjenester for oppdaterte valutakurser for å få de siste valutakursene på **Valutaer**-siden.|[Oppdatere valutakurser](finance-how-update-currencies.md)|  
|Definer forskjellige hoveddata, for eksempel firmainformasjon, kunder, leverandører, varer og enheter, relatert til tilordning av data i [!INCLUDE[prod_short](includes/prod_short.md)].|[Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Definere en bankkonto, leverandør og en utbetalingskladd for SEPA-kredittoverføring.|[Definere SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Klargjør bankkontoformater, betalingsmetoder og kundeavtaler for SEPA direct debit.|[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)|  
|Konfigurer brukergodkjenning og URL-adressen til leverandøren av utvidelsen AMC Banking 365 Fundamentals som kreves for å få bankfiler konvertert til bankens format.|[Bruke utvidelsen AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)|  
|Konfigurer og aktiver en ekstern tjeneste som lar deg importere bankkontoutdrag direkte som bankfeeder.|[Konfigurere tjeneste for konvertering av bankdata](bank-how-setup-bank-statement-service.md)|  
|Når tjenesten for bankkontoutdrag er aktivert, må du koble bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)].|[Opprette bankkonti](bank-how-setup-bank-accounts.md)|  
|Gjør klar til å sette opp en ny datautvekslingsdefinisjon for en datafil eller datastrøm ved å bruke XML-skjemaet for filen til å forhåndsutfylle hurtigfanen **Kolonnedefinisjoner** på siden **Definisjoner av bokføringsutveksling**.|[Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Definer rammeverket for datautveksling for å la brukerne motta et nytt kjøpsdokumentformat, sende et nytt salgsdokumentformat, importere en ny bankfil, eller annen datautveksling.|[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Se også  
[Utveksle data elektronisk](across-data-exchange.md)  
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]