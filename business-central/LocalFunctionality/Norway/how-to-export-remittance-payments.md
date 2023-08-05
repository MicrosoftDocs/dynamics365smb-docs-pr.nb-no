---
title: 'Eksportere remitteringsoppdrag [NO]'
description: Dette emnet forklarer hvordan du kan bruke funksjonen for eksport av remitteringsoppdrag til å eksportere betalingsfilen til datamaskinen din i den norske versjonen av Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15000000, 15000002, 15000004, 15000006, 15000007, 15000010'
ms.date: 06/21/2021
ms.author: edupont
---
# Eksporter remitteringsoppdrag i den norske versjonen

Du kan bruke funksjonen for eksport av remitteringsoppdrag til å eksportere betalingsfilen til datamaskinen din. Deretter kan du overføre remitteringsoppdragene til banken.  

> [!IMPORTANT]  
>  Før du kan eksportere et remitteringsoppdrag, må du velge et betalingsformat i feltet **Betalingseksportformat** på **Bankkort**-siden.  

Du eksporterer betalinger til en bankfil ved å velge **Eksporter betalinger**-knappen på **Utbetalingskladd**-siden. Prosessen kan være forskjellig avhengig av eksportformatet du velger:  

- Betalinger ved hjelp av SEPA-betalingsstandarden eksporteres direkte til en fil når du velger **Eksporter betalinger**-knappen. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](../../payables-make-payments.md).  

- Betalinger ved hjelp av lokale betalingsstandarder som **Telepay**, eksporteres med enten **Remittering - les ut (bank)**- eller **Remittering - les ut (BBS)**-rapporten som åpnes automatisk når du velger **Eksporter betalinger**-knappen.  

Fremgangsmåten for å eksportere betalinger ved hjelp av **Eksporter remittering**-kjørselen beskrives i dette emnet.  

## Slik eksporterer du remitteringsoppdrag ved hjelp av Eksporter remittering-kjørsler:  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Utbetalingskladder** og velg den relaterte koblingen.  
2.  Klargjør for å eksportere betalingene fra kladden. Hvis du vil ha mer informasjon, kan du se [Eksportere betalinger til en bankfil](../../finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  
3.  Velg handlingen **Eksporter betalinger**.  
4.  Fyll ut feltene som beskrevet i tabellen nedenfor, ved å velge hurtigfanen **Alternativer** på rapportsiden som åpnes.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Remitteringsavtalekode**|Angi koden for avtalen.|  
    |**Operator**|Angi operatornummer.|  
    |**Passord**|Angi passordet for betalingene.|  
    |**Divisjon**|Angi divisjonen som betaler remittering.|  
    |**Oppdragsbemerkning**|Angi en bemerkning for betalingen.|  
    |**Filnavn**|Angi navnet og mappen for betalingsfilen.|  

5.  Velg **OK**.  

Betalingsinformasjonen eksporteres til filen som er angitt i remitteringsavtalen.  

Utbetalingskladden slettes og transaksjonene overføres til ventekladden.  

## Se også  
 [Elektroniske betalinger til leverandører i Norge](electronic-payments-to-vendors-in-norway.md)   
 [Sette opp remitteringsavtaler](how-to-set-up-remittance-agreements.md)   
 [Opprette remitteringskontoer](how-to-create-remittance-accounts.md)   
 [Angi leverandører for remittering](how-to-set-up-vendors-for-remittance.md)   
 [Mottakerreferansekoder](recipient-reference-codes.md)   
 [Opprette remitteringsforslag](how-to-create-remittance-suggestions.md)   
 [Opprette manuelle remitteringsoppdrag](how-to-create-manual-remittance-payments.md)   
 [Definere betalingslinjeinformasjon](how-to-set-up-payment-line-information.md)   
 [Kontrollere remitteringsoppdrag](how-to-test-remittance-payments.md)   
 [Typer betalingsreturfiler](types-of-payment-returns-files.md)   
 [Importere betalingsreturdata](how-to-import-payment-return-data.md)   
 [Slette remitteringsoppdrag](how-to-delete-remittance-payment-orders.md)   
 [Remitteringsfeil](remittance-errors.md)   
 [Vise remitteringsfeilkoder](how-to-view-remittance-error-codes.md)   
 [Annullere betalinger](how-to-cancel-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]