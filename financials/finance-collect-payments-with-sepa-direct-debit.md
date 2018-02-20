---
title: SEPA Direct Debit i Finance and Operations, Business edition | Microsoft-dokumentasjon
description: Du kan samle inn betaling direkte fra kundens bankkonto i henhold til SEPA-formatet.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cf07a08eebe8bfffc99f7351a96526452728552e
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a>Innkreve betalinger med SEPA Direct Debit
Med kundens samtykke kan du samle inn betaling direkte fra kundens bankkonto i henhold til SEPA-formatet.  

 Konfigurer først eksportformatet for bankfilen som instruerer banken om å utføre en direct debit. Konfigurer deretter kundens betalingsmåte. Til slutt angir du direct debit-belastningsfullmakten som gjenspeiler avtalen med kunden om å samle sine betalinger i en bestemt avtaleperiode.  

 Hvis du vil instruere banken om å overføre beløpet fra kundens bankkonto til firmaets konto, kan du opprette en post for direct debit-samlingen som inneholder informasjon om bankkonti, berørte salgsfakturaer og direct debit-belastningsfullmakten. Deretter eksporterer du en XML-fil som er basert på samlingsposten, som du sender til banken for behandling. Eventuelle betalinger som ikke kunne behandles blir kommunisert til deg av banken din, og du må deretter manuelt avvise de aktuelle postene for direct debit-samlingen.  

 Du kan konfigurere standard kundesalgskoder med direct debit-betalingsmåten og belastningsfullmaktsinformasjonen. Du kan deretter bruke kjørselen **Opprett standard kundefakturaer** til å generere flere salgsfakturaer med forhåndsutfylt avtalegiroinformasjon. Dette kan gjøres manuelt eller automatisk, i henhold til forfallsdatoen for betalingen.  

 Når betalinger er behandlet, som formidlet av banken din, kan du bokføre kvitteringene direkte fra vinduet **Poster for Direct Debit-oppkreving** eller ved å flytte betalingslinjene i kladden der du bokfører kvitteringer, for eksempel vinduet **Innbetalingskladd**. Du kan også, avhengig av kontantstyringsprosessen, vente og bare bruke bare betalinger som en del av bankkontoavstemmingen.  

> [!NOTE]  
>  Hvis du vil innkreve betalinger ved hjelp av SEPA Direct Debit, må valutaen på salgsfakturaen være EURO.  

 Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Klargjør bankkontoformater, betalingsmetoder og kundeavtaler for SEPA direct debit.|[Definere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)|  
|Instruere banken om å overføre betalingsbeløpet fra kundenes bankkonti til firmaets konto i henhold til oppsettet av SEPA direct debit.|[Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Konfigurer standard kundesalgskoder for avtalegirofakturaer og generer salgsfakturaer med avtalegiroinformasjon når fakturaene forfaller.|[Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md)|  
|Bokfør betalinger som SEPA direct debit.|[Bokføre kvitteringer for SEPA Direct Debit](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a>Se også  
[Håndtere fordringer](receivables-manage-receivables.md)

