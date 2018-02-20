---
title: "Definere SEPA-kredittoverføring | Microsoft-dokumentasjon"
description: "Finn ut hvordan du definerer SEPA-kredittoverføring i Finance and Operations, Business edition."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sepa, credit, transfer, payment,
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 66f24ea238eed97ffe7f76f3c979cc2843875860
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-sepa-credit-transfer"></a>Definere SEPA-kredittoverføring
Fra vinduet **Utbetalingskladd** kan du eksportere betalinger til en fil for opplasting til den elektroniske banken for behandling av relaterte pengeoverføringer. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter formatet for SEPA-kreidttoverføring, men andre formater for elektroniske betalinger kan være tilgjengelige i ditt land/region.  

Du kan gjøre det mulig å eksportere et bankfilformat som ikke støttes som standard i [!INCLUDE[d365fin](includes/d365fin_md.md)], ved å definere en datautvekslingsdefinisjon ved hjelp av rammeverket for datautveksling. Hvis du vil ha mer informasjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  

Før du kan behandle betalingen elektronisk ved å eksportere betalingsfiler i formatet for SEPA-kredittoverføring, må du utføre følgende konfigureringstrinn:  

* Definer den aktuelle bankkontoen slik at den kan håndtere SEPA-kredittoverføringsformatet.  
* Definer leverandørkort slik at betalinger behandles ved å eksportere filer i SEPA-kredittoverføringsformatet.  
* Definer den tilknyttede finanskladden slik at betalingseksport kan utføres fra vinduet **Utbetalingskladd**.  
* Knytt datautvekslingsdefinisjon for én eller flere betalingstyper til de(n) aktuelle betalingsmåten(e):  

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Slik oppretter du en bankkonto for SEPA-kredittoverføring:  
1. Skriv inn **Bankkontoer** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Åpne kortet for bankkontoen som du vil eksportere betalingsfiler fra, i formatet for SEPA-kredittoverføring.  
3. På hurtigfanen **Overfør** i feltet **Betalingseksportformat** velger du **SEPADD**.  
4. I feltet **SEPA CT-mld., ID-nr-serie** velger du en nummerserie med numre som tilordnes til bokføringer av SEPA-kredittoverføringer.  
5. Kontroller at **IBAN**-feltet er utfylt.  

    > [!NOTE]  
    >  **EUR** må angis i **Valutakode**-feltet fordi SEPA-kredittoverføringer bare kan foretas i euro.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Slik oppretter du et leverandørkort for SEPA-kredittoverføring:  
1. Skriv inn **Leverandører** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Åpne kortet for leverandøren som du vil betale elektronisk, ved å eksportere betalingsfiler i formatet for SEPA-kredittoverføring.  
3. Velg **BANK** i hurtigfanen **Betaling** i feltet **Betalingsmåte - kode**.  
4. I feltet **Foretrukket bankkonto** velger du banken som pengene skal overføres til når den behandles av den elektroniske banken.  

     Verdien i feltet **Foretrukket bankkonto** overføres til feltet **Mottakerbankkonto** i vinduet **Utbetalingskladd** vinduet.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Slik definerer du utbetalingskladden for eksport av betalingsfiler:  
1. Skriv inn **Utbetalingskladder** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. Åpne utbetalingskladden du bruker til å behandle betalinger med, ved å eksportere filer i formatet for SEPA-kredittoverføring.  
3. Velg rulle\-gardinknappen i **Bunkenavn**-feltet.  
4. Velg **Rediger oversikt** under **Behandle** på fanebladet **Hjem** i vinduet **Finanskladder**.  
5. På linjen for utbetalingskladden du vil bruke til å eksportere betalinger, merker du av for **Tillat betalingseksport**.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>Slik knytter du datautvekslingsdefinisjon for én eller flere betalingstyper til de(n) aktuelle betalingsmåten(e):  
1. Skriv inn **Betalingsmåter** i **Søk**-boksen, og velg deretter den relaterte koblingen.  
2. I vinduet **Betalingsmåter** velger du betalingsmåten som brukes til å eksportere betalinger fra, og deretter velger du feltet **Definisjon av betalingseksportlinje**.  
3. I vinduet **Definisjoner av betalingseksportlinje** velger du koden du angav i **Kode**-feltet på hurtigfanen **Linjedefinisjoner** i trinn 4 i delen "Slik beskriver du formateringen av linjer og kolonner i filen" i fremgangsmåten [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).  

    Direct debitbelastningsfullmakten fylles automatisk ut i feltet **ID for Direct Debit-belastningsfullmakt** når du oppretter en salgsfaktura for kunden som du valgte i trinn 2. Hvis du vil ha mer informasjon, kan du se [Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md).  

## <a name="see-also"></a>Se også  
[Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md)  
[Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md)  
[Opprette gjentakende salgs- og kjøpslinjer](sales-how-work-standard-lines.md)  
[Utveksle data elektronisk](across-data-exchange.md)  

