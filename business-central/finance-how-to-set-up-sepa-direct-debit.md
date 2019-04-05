---
title: Definere SEPA Direct Debit | Microsoft-dokumentasjon
description: Lær hvordan du definerer SEPA Direct Debit i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: finance-collect-payments-with-sepa-direct-debit
ms.openlocfilehash: 9e2ef9ec3b454e5a9bb5097ba3ed30c5756d2352
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802655"
---
# <a name="set-up-sepa-direct-debit"></a>Definere SEPA Direct Debit
Fra **Direct Debit-oppkrevinger**-siden kan du eksportere instruksjoner til den elektroniske banken for å utføre en direct debit-samling fra kundens bankkonto til din bankkonto. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter formatet for SEPA Direct Debit, men andre formater for elektroniske betalinger kan være tilgjengelige i ditt land/region.  

Du kan gjøre det mulig å eksportere et bankfilformat som ikke støttes som standard i [!INCLUDE[d365fin](includes/d365fin_md.md)], ved å definere en datautvekslingsdefinisjon ved hjelp av rammeverket for datautveksling. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

Før du kan behandle kundebetalinger elektronisk ved å eksportere direct debit-instruksjoner i SEPA Direct Debit-formatet, må du utføre følgende konfigureringstrinn:  

* Konfigurer eksportformatet for bankfilen som instruerer banken om å utføre en direct debit-samling fra kundens bankkonto til din bankkonto.  
* Konfigurer kundens betalingsmåte.  
* Konfigurer direct debit-belastningsfullmakten som gjenspeiler avtalen med kunden om å samle sine betalinger i en bestemt avtaleperiode.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit"></a>Slik konfigurerer du din bankkonto for SEPA direct debit  
1. Skriv inn **Bankkontoer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Åpne bankkontoen som du vil bruke til direct debit.  
3. Velg alternativet for SEPA direct debit i feltet **Eksportformat for SEPA Direct Debit** i hurtigfanen **Overfør**.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit"></a>Slik konfigurerer du kundens betalingsmåte for SEPA direct debit  
1. Skriv inn **Betalingsmåter** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Konfigurer betalingsmåter. Fyll ut de spesifikke feltene for direct\- debit som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit**|Angi om betalingsmåten er for SEPA direct debit-samlinger.|  
    |**Betalingsbet.kode for Direct Debit**|Angi betalingsbetingelsene, for eksempel IKKE BETAL, som vises på salgsfakturaer som betales med SEPA direct debit, for å angi for kunden at betalingen blir innkrevd automatisk. Du kan også la feltet stå tomt.|  

    > [!NOTE]  
    >  Ikke angi en verdi i feltet **Motkontonr.**  

4. Velg **OK**-knappen for å lukke siden **Betalingsmåter**.  
5. Skriv inn **Kunder** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
6. Åpne kundekortet for kunden som du vil konfigurere SEPA direct debit-samling for.  
7. Velg feltet **Betalingsmåte - kode**, og velg deretter koden for betalingsmåte som du angav i trinn 3.  
8. Gjenta trinn 6 og 7 for alle kundene du vil konfigurere SEPA direct debit-samling for.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement"></a>Slik konfigurerer du direct debit-belastningsfullmakten som representerer kundeavtalen  
1. Skriv inn **Kunder** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Åpne kortet for kunden som du vil konfigurere SEPA direct debit for.  
3. Velg **Bankkonti**-handlingen.  
4. På siden **Kundebankkonto - oversikt** velger du kundebankkonto som skal bruke direct debit, og deretter velger du **Direct Debit-belastningsfullmakter** i **Prosess**-gruppen i kategorien **Hjem**.  
5. På siden **SEPA Direct Debit-belastningsfullmakter** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Bankkontokode for kunde**|Angir bankkontoen som avtale\-girobetalinger kreves inn fra. Dette feltet fylles ut automatisk.|  
    |**Gyldig fra**|Angi datoen direct debit\-belastningsfullmakten gjelder fra.|  
    |**Gyldig til**|Angi datoen da direct debit\-belastningsfullmakten utløper.|  
    |**Signeringsdato**|Angi datoen da kunden signert direct debit\-belastningsfullmakten.|  
    |**Type betaling**|Angi om avtalen dekker flere (**Gjentakende**) eller én enkelt (**Engangsforekomst**) direct debit-samlinger.|  
    |**Forventet antall debetbeløp**|Angi hvor mange direct debit-samlinger vil opprette. Dette feltet er bare relevant hvis du valgte **Gjentakende** i feltet **Type betaling**.|  
    |**Debetteller**|Angir hvor mange direct debit-samlinger som er utført ved hjelp av denne direct debit\-belastningsfullmakten. Dette feltet oppdateres automatisk.|  
    |**Sperret**|Angi om direct debit-samlinger ikke kan opprettes ved hjelp av denne direct debit\-belastningsfullmakten.|  

6.  Gjenta trinn 1 til 5 for alle kundene du vil konfigurere SEPA direct debit for.  

 Direct debitbelastningsfullmakten fylles automatisk ut i feltet **ID for Direct Debit-belastningsfullmakt** når du oppretter en salgsfaktura for kunden som du valgte i trinn 2. Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Se også  
[Innkreve betalinger med SEPA direct debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)
[Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md)
[Utveksle data elektronisk](across-data-exchange.md)
