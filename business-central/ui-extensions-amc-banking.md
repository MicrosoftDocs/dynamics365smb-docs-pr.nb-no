---
title: Bruke utvidelsen AMC Banking 365 Fundamentals | Microsoft Docs
description: Du kan enkelt utveksle data med banker ved å transformere data til det formatet de krever.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: bank, format, data
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 8eb45d8c65a09ac56617f84a41543c38a4518fa9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912399"
---
# <a name="using-the-amc-banking-365-fundamentals-extension"></a>Bruke utvidelsen AMC Banking 365 Fundamentals
Utvidelsen AMC Banking 365 Fundamentals gjør det enklere og mer nøyaktig å sende data til banker. Utvidelsen kobler [!INCLUDE[d365fin](includes/d365fin_md.md)] sammen med tjenesten AMC Banking 365 Fundamentals for Microsoft Dynamics 365 Business Central, som kan konvertere bankdata fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til formater som kreves av over 600 banker over hele verden. Dette gjør det for eksempel enklere å overføre betalinger og kreditter til leverandører ved å registrere innbetalingene i [!INCLUDE[d365fin](includes/d365fin_md.md)], og deretter laste dem opp til banken. Formatene kan også forenkle bankavstemmingsprosesser. Se [AMC Banking for Microsoft Dynamics 365 Business Central](https://amcbanking.com/landing365bc/help) mer informasjon.

> [!Note]
> AMC Banking har bygd flere utvidelser som fungerer sammen med [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette emnet beskriver bare den grunnleggende utvidelsen.

## <a name="using-our-demonstration-account"></a>Bruke vår demonstrasjonskonto
[!INCLUDE[d365fin](includes/d365fin_md.md)] leveres med en demonstrasjonskonto som lar deg prøve ut utvidelsen AMC Banking 365 Fundamentals. Vi gir standardinnstillinger for tilkobling til AMC Banking, med angivelse av bankkontoer som data skal hentes fra i [!INCLUDE[d365fin](includes/d365fin_md.md)], i tillegg til noen få datautvekslingsdefinisjoner. Du kan vise tilkoblingsinnstillingene på siden **AMC Banking-oppsett**. For bankkonto bruker utvidelsen verdier i feltene **Banknavn**, **Numre på kredittoverføringsmeldinger**, **Importformat for bankkontoutdrag** og **Betalingseksportformat**.

Vi tilbyr innstillingene, men hvis du vil prøve ut utvidelsen, må du kjøre veiledningen assistert oppsett for å bruke dem. På siden **AMC Banking-oppsett** velger du handlingen **Assistert oppsett** for å kjøre veiledningen.

> [!Note]
> Det finnes noen begrensninger på demonstrasjonskontoen. Når du for eksempel konverterer betalinger, vil ikke beløpet i den konverterte filen samsvare med det faktiske beløpet. I stedet vil beløpet alltid være fem enheter av valutaen du bruker for betalinger.  

## <a name="setting-up-the-extension"></a>Konfigurere utvidelsen
For å komme i gang med utvidelsen trenger du bare utføre noen enkle trinn, og en veiledning for assistert oppsett vil opprette tilkoblingen og aktivere utvidelsen. Veiviseren vil gjøre ting som å installere datautvekslingsdefinisjonene for eksport- og importoppsett for bankoppgaver og starte nummerseriene som brukes for kredittoverføringsmeldinger.  

### <a name="to-set-up-the-required-permission-sets"></a>Slik konfigurerer du de nødvendige tillatelsessettene
Før brukere kan bruke denne utvidelsen, må systemansvarlig kopiere følgende tillatelsessett, redigere dem og deretter tilordne de nye tillatelsessettene til brukere i stedet for originalen:

* **D365 Basic**
* **D365 Team Member**
* **D365 Read**
* **IntelligentCloudBC**

Hvis du vil ha mer informasjon, kan du se [Slik kopierer du et tillatelsessett](ui-define-granular-permissions.md#to-copy-a-permission-set).

For hvert nye tillatelsessett gir du bare **Lese**-tillatelsen for **AMC Banking-oppsettstabellen (20101)**. Hvis du vil ha mer informasjon, kan du se [Opprette eller endre tillatelser manuelt](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-connect-the-extension-to-amc-banking"></a>Slik kobler du utvidelsen til AMC Banking
1. Anskaff en modul og en serviceplan for AMC Banking. Dette gjør du ved å gå til siden [AMC-lisens](https://license.amcbanking.com/register).
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **AMC Banking-oppsett**, og velg deretter den relaterte koblingen.  
3. På siden **AMC Banking-oppsett** velger du handlingen **Assistert oppsett**.
4. Fullfør trinnene i den assisterte oppsettsveiledningen.

### <a name="to-connect-bank-accounts-to-the-extension"></a>Slik kobler du bankkonti til utvidelsen
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Åpne kortet for bankkontoen du vil koble til tjenesten.
3. I **Banknavn**-feltet velger du formatet som banken krever.  

   Formatene er filtrert slik at bare de som er relevante for landet/regionen som er angitt for bankkontoen, vises.
4. I feltet **Numre på kredittoverføringsmeldinger** velger du nummerserien som skal brukes for meldinger som følger med betalingene.
5. I feltene **Importformat for bankkontoutdrag** og **Betalingseksportformat** velger du datautvekslingsdefinisjonene som banken krever.

## <a name="using-the-extension"></a>Bruke utvidelsen
Bruk av denne utvidelsen er bare et spørsmål om å eksportere data på **Betalingskladder**-siden, og deretter laste dem opp til bankens webtjeneste. Hvis du vil ha mer informasjon, se [Betale med tjenesten for bankdatakonvertering eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

> [!Note]
> Du må fylle ut feltene **SWIFT-kode** og **IBAN** for hver bankkonto.

### <a name="to-export-data-and-submit-it-to-your-bank"></a>Slik eksporterer du data og sender dem til banken
> [!CAUTION]  
>  Når du eksporterer data ved hjelp av utvidelsen AMC Banking 365 Fundamentals, blir noen av forretningsdataene dine eksponert for leverandøren av tjenesten. Tjenesteleverandøren, AMC Consult A/S, er ansvarlig for personvernet vedrørende disse dataene. Hvis du vil ha mer informasjon, kan du se [personvernpolicyen for AMC](https://go.microsoft.com/fwlink/?LinkId=510158).

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.
2. Opprett kladdelinjene du vil eksportere.  

   > [!Note]
   > Husk å velge **Elektronisk betalingsprosess** i feltet **Bankbetalingstype** for hver linje.
3. Velg handlingen **Eksporter**.

### <a name="to-import-and-apply-the-converted-file"></a>Slik importerer og bruker du den konverterte filen
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Betalingsavstemmingskladd**, og velg deretter den relaterte koblingen.
2. Velg **Importer banktransaksjon**-handlingen, og velg deretter den konverterte filen.  

   [!INCLUDE[d365fin](includes/d365fin_md.md)] vil opprette en ny betalingsavstemmingskladd som inneholder dataene i filen. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Komme i gang](product-get-started.md)
