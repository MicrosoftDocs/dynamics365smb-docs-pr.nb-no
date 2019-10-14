---
title: Eksportere poster for SEPA Direct Debit-oppkreving | Microsoft-dokumentasjon
description: Opprett en direct debet-oppkreving, som inneholder informasjon om kundens bankkonto, berørte salgsfakturaer og direct debet-mandatet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: c6a7231fa72e18a31a7971a333e9984aed7e5b8b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2306343"
---
# <a name="create-sepa-direct-debit-collection-entries-and-export-to-a-bank-file"></a>Opprette poster for SEPA Direct Debit-oppkreving og eksportere til en bankfil
Hvis du vil instruere banken om å overføre beløpet fra kundens bankkonto til firmaets konto, kan du opprette en post for direct debit-samlingen som inneholder informasjon om kundens bankkonto, berørte salgsfakturaer og direct debit-belastningsfullmakten. Fra den resulterende posten for avtalegirosamlingen eksporterer du deretter en XML-fil som du sender eller laste opp til nettbanken for behandling. Eventuelle betalinger som ikke kunne behandles av banken blir kommunisert til deg av banken din, og du må deretter manuelt avvise de aktuelle postene for direct debit-samlingen.  

> [!NOTE]  
>  Hvis du vil innkreve betalinger ved hjelp av SEPA Direct Debit, må valutaen på salgsfakturaen være EURO.  

### <a name="to-create-a-direct-debit-collection"></a>Slik oppretter du en avtalegirooppkreving  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Direct Debit-oppkrevinger**, og velg deretter den relaterte koblingen.  
2. På siden **Direct Debit-oppkrevinger**, i fanebladet **Hjem** under **Ny**, velger du **Opprett direct debit-oppkreving**.  
3. På siden **Opprett Direct Debit-oppkreving** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Fra forfallsdato**|Angi den tidligste betalingsforfallsdatoen på salgsfakturaer som du vil opprette en avtalegirosamling for.|  
    |**Til forfallsdato**|Angi den siste betalingsforfallsdatoen på salgsfakturaer som du vil opprette en avtalegirosamling for.|  
    |**Partnertype**|Angi om avtalegirosamlingen opprettes for kundetypen **Firma** eller **Person**.|  
    |**Bare kunder med gyldig belastningsfullmakt**|Angi om en direct debit-samling opprettes for kunder som har en gyldig direct debit-belastningsfullmakt. **Obs!:**  Det blir opprettet en avtalegirosamling selv om feltet **ID for Direct Debit-belastningsfullmakt** ikke er fylt ut på salgsfakturaen.|  
    |**Bare fakturaer med gyldig belastningsfullmakt**|Angi om en Direct Debit-oppkreving bare blir opprettet for salgsfakturaer hvis en gyldig Direct Debit-belastningsfullmakt er valgt i feltet **ID for Direct Debit-belastningsfullmakt** på salgsfakturaen.|  
    |**Bankkontonr.**|Angi hvilke av firmaets bankkontoer som den samlede betalingen blir overført til fra kundens bankkonto.|  
    |**Bankkontonavn**|Angir navnet på bankkontoen som du velger i feltet **Bankkontonr.**. Dette feltet fylles ut automatisk.|  

4. Velg **OK**.  

     En avtalegirosamling legges til på siden **Direct Debit-oppkrevinger**, og én eller flere poster for avtalegirosamlingen blir opprettet.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file"></a>Slik oppretter du en post for avtalegirosamling til en bankfil  
1. På siden **Direct Debit-oppkrevinger**, i fanebladet **Hjem** under **Prosess**, velger du **Poster for Direct Debit-oppkreving**.  
2. På siden **Direct Debit Collect. Entries** merker du av for posten som du vil eksportere, og deretter går du til **Prosess**-gruppen i kategorien **Hjem** og velger **Opprett direct debit-fil**.  
3. Lagre den eksporterte filen på plasseringen der du sender eller laste den opp til nettbanken.  

     På siden **Poster for Direct Debit-oppkreving** endres feltet **Status for Direct Debit-oppkreving** til Fil opprettet. På siden **SEPA Direct Debit-belastningsfullmakter** oppdateres feltet **Debetteller** med én.  

Hvis den eksporterte filen ikke kan behandles, for eksempel fordi kunden er insolvent, kan du avvise posten for avtalegirosamlingen. Hvis den eksporterte filen er behandlet av banken, samles automatisk utestående betalinger for de aktuelle salgsfakturaene fra de aktuelle kundene. I slike tilfeller kan du lukke samlingen.  

### <a name="to-reject-a-direct-debit-collection-entry"></a>Slik avviser du poster for avtalegirosamlinger  

* På siden **Poster for Direct Debit-oppkreving** merker du av for posten som ikke ble behandlet, og deretter går du til **Prosess**-gruppen i kategorien **Hjem** og velger **Avvis post**.  

     Verdien i **Status**-feltet på siden **Poster for Direct Debit-oppkreving** endres til **Avvist**.  

### <a name="to-close-a-direct-debit-collection"></a>Slik lukker du en avtalegirosamling  
*  På siden **Poster for Direct Debit-oppkreving** merker du av for posten som ble behandlet, og deretter går du til **Prosess**-gruppen i kategorien **Hjem** og velger **Lukk oppkreving**.  

     Den relaterte avtalegirosamlingen er lukket.  

Du kan deretter fortsette å bokføre kvitteringer for betaling for de aktuelle salgsfakturaene. Dette kan du gjøre slik du vanligvis bokfører kvitteringer, for eksempel på siden **Betalingsregistrering**, eller du kan bokføre de relaterte kvitteringene direkte fra siden **Poster for Direct Debit-oppkreving** . Hvis du vil ha mer informasjon, kan du se [Bokføre kvitteringer for SEPA Direct Debit](finance-how-to-post-sepa-direct-debit-payment-receipts.md).  

## <a name="see-also"></a>Se også  
[Definere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)  
[Bokføre kvitteringer for SEPA Direct Debit](finance-how-to-post-sepa-direct-debit-payment-receipts.md)  
[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)  
