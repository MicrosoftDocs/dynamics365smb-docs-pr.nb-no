---
title: Rapportering av 1099-transaksjoner i USA | Microsoft-dokumentasjon
description: "På kjøpsdokumentene kan du angi at dokumentet er 1099-pliktig, og du kan angi 1099-koden for leverandøren."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a0a31c28b6c96dc80593ac3862b97b36c3ec81c7
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="reporting-1099-transactions-in-the-us"></a>Rapportering av 1099-transaksjoner i USA.
IRS (Internal Revenue Service) krever én eller flere versjoner av 1099-avgiftsskjemaet for betalinger til leverandører. Kopier av disse skjemaene må sendes til leverandører årlig på eller før den siste dagen i januar. På kjøpsdokumentene kan du angi at dokumentet er 1099-pliktig, og du kan angi 1099-koden for leverandøren.  

## <a name="1099-codes"></a>1099-koder
I [!INCLUDE[d365fin](includes/d365fin_md.md)] er de vanligste 1099-kodene allerede definert for deg, slik at du er klar til å generere nødvendige rapporter. Kodene er definert i vinduet **IRS 1099-skjemafelt** der du også kan legge til nye 1099-koder. For hver avgiftspliktige leverandør kan du deretter angi den aktuelle 1099-koden på i hurtigfanen **Betalinger** på leverandørkortet.  

Med rapporten **1099-informasjon for leverandør** kan du se gjennom 1099-transaksjoner betalt i løpet av en bestemt periode. På slutten av året kan du skrive ut 1099-transaksjoner på forhåndstrykte skjemaer.  

## <a name="printing-1099-tax-forms"></a>Skriver ut 1099-avgiftsskjemaer
Fra den **IRS 1099-skjemaet for** -vinduet, kan du gå til følgende mva-skjemaer:  

* 1099-DIV for leverandør  

  Skriver ut det føderale skjemaet 1099-DIV for utbytte og distribusjon. Du kan skrive ut alle eller bestemte 1099-DIV-skjemaer. Rapporten bruker kodene som gjelder for beløpsfeltene for DIV-skjemaet fra vinduet **IRS 1099-skjemafelt**.  
* 1099-INT for leverandør  

  Skriver ut det føderale skjemaet 1099-INT for finansinntekter. Du kan skrive ut alle eller bestemte 1099-INT-skjemaer. Rapporten bruker kodene som gjelder for beløpsfeltene for INT-skjemaet fra vinduet **IRS 1099-skjemafelt**.  
* 1099-MISC for leverandør – diverse inntekter  

  Skriver ut det føderale skjemaet 1099-MISC for diverse inntekter. Du kan skrive ut alle eller bestemte 1099-MISC-skjemaer. Rapporten bruker kodene som gjelder for beløpsfeltene for MISC-skjemaet fra vinduet **IRS 1099-skjemafelt**.  

Forskriftsmessige endringer som påvirker denne rapporten og tabelldataene håndteres vanligvis under oppdateringer på slutten av året.
Det kan være nyttig å kjøre rapporten **1099-informasjon for leverandør** for å se gjennom dataene før du skriver ut skjemaene.

## <a name="submitting-1099-tax-forms-electronically"></a>Innsending av 1099-avgiftsskjemaer elektronisk
Hvis du vil sende 1099-avgiftsskjemaene elektronisk, kan du bruke rapporten **Magnetiske 1099-data for leverandør**. Angir 1099-skjemaene som kan eksporteres. Skjemainformasjonen som eksporteres av denne rapporten, er den samme som rapportene som skriver ut 1099-skjemaer som er beskrevet i det forrige avsnittet.  

Rapporten bruker kodene som gjelder for beløpsfeltene for skjemaet fra vinduet **IRS 1099-skjemafelt**. Kodene er tilordnet til skjemafeltene i filoppsettene for denne rapporten, og tabelldataene og rapportversjonen for et bestemt avgiftsår må derfor samsvare. Hvis eventuelle egendefinerte koder er lagt til i tabellen, må disse tilordnes skjemafeltene i dette objektet.  

Forskriftsmessige endringer som påvirker denne rapporten og tabelldataene håndteres vanligvis under oppdateringer på slutten av året.
Det kan være nyttig å kjøre rapporten **1099-informasjon for leverandør** for å se gjennom dataene før du genererer den elektroniske filen.  

## <a name="see-also"></a>Se også
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

