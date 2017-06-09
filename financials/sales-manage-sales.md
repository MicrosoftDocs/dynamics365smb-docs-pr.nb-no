---
title: Salg| Microsoft-dokumentasjon
description: "Beskriver hvordan du håndterer salgsaktiviteter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 04/27/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: d8b73dcf1ee000bd13aec200c82275eb3c0f9d1d
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="sales"></a>Salg
Du kan opprette en salgsfaktura eller ordre for å registrere avtalen med en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser.

Du må bruke ordrer hvis salgsprosessen krever at du kan sende deler av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke er tilgjengelig samtidig. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke ordrer. I alle andre henseender fungerer ordrer på samme måte som salgsfakturaer.

God salgs- og markedsføringspraksis handler om å ta de rette avgjørelsene til rett tid. Markedsføringsfunksjoner i [!INCLUDE[d365fin](includes/d365fin_md.md)] gir deg en nøyaktig oversikt over kontaktinformasjonen når du har behov for den, slik at du kan ta deg av potensielle kunder på en mer effektiv måte, og øke kundetilfredsheten. Hvis du vil ha mer informasjon, kan du se [Forbindelser](marketing-relationship-management.md).

Du kan forhandle med kunden ved først å opprette et tilbud, som du kan konvertere til en salgsfaktura når dere blir enige om salget. Etter at kunden har bekreftet avtalen, for eksempel etter en tilbudsprosess, kan du sende en ordrebekreftelse for å registrere din forpliktelse til å levere produktene som avtalt.

Når du leverer produkter, helt eller delvis, kan du bokføre salgsfakturaen eller ordren som levert eller som levert og fakturert for å opprette de beslektede vare- og kundepostene i systemet.

I forretningsmiljøer der kunden må betale før produkter leveres, for eksempel i detaljhandel, må du vente til mottak av betalingen før du leverer produktene. I de fleste tilfeller kan du behandle innkommende betalinger noen uker etter levering ved å utligne betalingene mot deres tilknyttede bokførte, ubetalte salgsfakturaer. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

Du kan enkelt korrigere eller annullere en bokført salgsfaktura før den er betalt. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis kunden ber om en endring tidlig i ordreprosessen. Hvis den bokførte salgsfakturaen er betalt, må du opprette en salgskreditnota for å reversere salget.

Salgsdokumenter kan sendes som PDF-filer vedlagt i e-post. Brødteksten i e-posten inneholder et utdrag av salgsdokument, for eksempel produkter, totalt beløp og en kobling til PayPal-nettstedet. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md).

Du kan inkludere en godkjenningsarbeidsflyt for alle salgsprosesser, for eksempel hvis du vil kreve at store salg til bestemte kunder godkjennes av regnskapssjefen. Hvis du vil ha mer informasjon, kan du se [Bruke godkjenningsarbeidsflyter](across-how-use-approval-workflows.md).

Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.

| Hvis du vil | Se |
| --- | --- |
| Opprett et tilbud der du tilbyr produkter på betingelser det kan forhandles om, før du konverterer tilbudet til en salgsfaktura. |[Gi tilbud](sales-how-make-offers.md) |
| Opprett en salgsfaktura for å registrere avtalen med en kunde om å selge produkter på bestemte leverings- og betalingsbetingelser. |[Fakturere salg](sales-how-invoice-sales.md) |
| Behandle en ordre som involverer delvis levering eller direkte levering. |[Selge produkter](sales-how-sell-products.md) |
| Koble en ordre til en bestilling for å selge en vare med direkte levering som skal leveres direkte fra leverandøren til kunden. |[Foreta direkte leveringer](sales-how-drop-shipment.md) |
| Utfør en handling på en ubetalt bokført salgsfaktura for å opprette en kreditnota automatisk og enten annullere salgsfakturaen eller opprette den på nytt, slik at du kan foreta korrigeringer. |[Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md) |
| Opprett en salgskreditnota for å tilbakestille en bestemt bokført salgsfaktura for å vise hvilke produkter kunden returnerer, og hvilket betalingsbeløp du vil refundere. |[Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md) |
| Opprett et kundekort for hver kunde du selger til. |[Registrere nye kunder](sales-how-register-new-customers.md) |

## <a name="see-also"></a>Se også
[Sette opp salg](sales-setup-sales.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Administrere skyldige beløp](payables-manage-payables.MD)  
[Prosjektstyring](projects-manage-projects.md)    
[Forsyningskjede](madeira-supply-chain.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
