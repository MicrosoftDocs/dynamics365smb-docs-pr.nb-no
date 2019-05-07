---
title: Felttilordning ved import av SEPA CAMT-filer | Microsoft-dokumentasjon
description: I europeiske markeder kan du importere bankkontoutdragsfiler i de regionale SEPA-standardene (Single Euro Payments Area).
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a474a760d5b3ef485468e9752f4ffb97610bfc55
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "930038"
---
# <a name="field-mapping-when-importing-sepa-camt-files"></a>Felttilordning ved import av SEPA CAMT-filer
[!INCLUDE[d365fin](includes/d365fin_md.md)] støtter de regionale SEPA-standardene (Single Euro Payments Area) for import av SEPA-bankkontoutdrag (CAMT-format). Hvis du vil ha mer informasjon, kan du se [Konfigurere konverteringstjenesten for bankdata](bank-how-setup-bank-data-conversion-service.md).  

 SEPA CAMT-standarden har også lokale variasjoner. Derfor må du kanskje endre den generiske datautvekslingsdefinisjonen (angitt med **SEPA CAMT**-koden på siden **Definisjoner av bokføringsutveksling**) for å tilpasse det til en lokal variant av standarden. Tabellene nedenfor viser til element-til-felt-tilordningen for tabell 81, 273 og 274 i implementeringen av SEPA CAMT i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Hvis du vil ha informasjon om oppretting eller justering av en datautvekslingsdefinisjon, kan du se [Definere datautvekslingsdefinisjoner](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>Tilordning av CAMT-data til felt i tabellen Finanskladd (81)  

|Elementbane|Meldingselement|Datatype|Beskrivelse|Identifikator for minustegn|Feltnr.|Feltnavn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Beløp|Desimaltall|Pengebeløpet i kontantposten||13|Beløp|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Tekst|Angir om posten er en kredit- eller en debetpost|DBET|13|Beløp|  
|Stmt/Ntry/BookgDt/Dt|Dato|Dato|Datoen når en post bokføres på en konto i kontotjenestebehandlerens bøker||5|Bokføringsdato|  
|Stmt/Ntry/BookgDt/DtTm|Dato/klokkeslett|Dato/klokkeslett|Datoen og klokkeslettet når en post bokføres på en konto i kontotjenestebehandlerens bøker||5|Bokføringsdato|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Navn|Tekst|Navnet på parten som skylder (den endelige) kreditoren et pengebeløp||1221|Informasjon om betaler|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ustrukturert|Tekst|Informasjon for å aktivere tilsvarende/avstemming av en post med varene som betalingen skal utlignes mot, for eksempel kommersielle fakturaer i et kundefordringsystem i et ustrukturert skjema||8|Beskrivelse|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Tekst|Mer informasjon om posten||1222|Transaksjonsinformasjon|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>Tilordning av CAMT-data til felt i tabellen Bankkontoavstemming (273)  

|Elementbane|Meldingselement|Datatype|Beskrivelse|Identifikator for minustegn|Feltnr.|Feltnavn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Dato|Datoen og klokkeslettet da meldingen ble opprettet.||3|Utdragsdato|  
|Stmt/Bal/Amt|Beløp|Desimaltall|Beløpet som er resultat av de innbrakte beløpene for alle debet- og kreditposter||4|Utdrag - sluttsaldo|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>Tilordning av CAMT-data til felt i tabellen Bankkontoavstemmingslinje (274)  

|Elementbane|Meldingselement|Datatype|Beskrivelse|Identifikator for minustegn|Feltnr.|Feltnavn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Beløp|Desimaltall|Pengebeløpet i kontantposten||7|Utdragsbeløp|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Tekst|Angir om posten er en kredit- eller en debetpost|DBET|7|Utdragsbeløp|  
|Stmt/Ntry/BookgDt/Dt|Dato|Dato|Datoen når en post bokføres på en konto i kontotjenestebehandlerens bøker||5|Transaksjonsdato|  
|Stmt/Ntry/BookgDt/DtTm|Dato/klokkeslett|Dato/klokkeslett|Datoen og klokkeslettet når en post bokføres på en konto i kontotjenestebehandlerens bøker||5|Transaksjonsdato|  
|Stmt/Ntry/ValDt/Dt|Dato|Dato|Datoen når aktiva blir tilgjengelige for kontoeieren hvis det opprettes en kreditpost, eller slutter å være tilgjengelig for kontoeieren hvis det opprettes en debetpost||12|Valuteringsdato|  
|Stmt/Ntry/ValDt/DtTm|Dato/klokkeslett|Dato/klokkeslett|Datoen og klokkeslettet når aktiva blir tilgjengelige for kontoeieren hvis det opprettes en kreditpost, eller slutter å være tilgjengelig for kontoeieren hvis det opprettes en debetpost||12|Valuteringsdato|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Navn|Tekst|Navnet på parten som skylder (den endelige) kreditoren et pengebeløp||15|Informasjon om betaler|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ustrukturert|Tekst|Informasjon for å aktivere tilsvarende/avstemming av en post med varene som betalingen skal utlignes mot, for eksempel kommersielle fakturaer i et kundefordringsystem i et ustrukturert skjema||6|Beskrivelse|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Tekst|Mer informasjon om posten||16|Transaksjonsinformasjon|  

 Elementer i **Ntry**-noden som importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)], men som ikke tilordnes til felt som er lagret i tabellen **Kolonnedefinisjon for bokføringsutveksl.**. Brukere kan vise disse elementene fra sidene **Betalingsavstemmingskladd**, **Betalingsutligning** og **Bankkontoavstemming** ved å velge handlingen **Detaljer om bankkontoutdragslinje**. Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).  
## <a name="see-also"></a>Se også  
[Definere datautveksling](across-set-up-data-exchange.md)  
[Utveksle data elektronisk](across-data-exchange.md)  
[Konfigurere tjeneste for konvertering av bankdata](bank-how-setup-bank-data-conversion-service.md)   
[Bruke XML-skjemaer til å klargjøre datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md)  
