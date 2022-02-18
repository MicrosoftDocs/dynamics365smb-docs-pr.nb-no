---
title: Registrere nye kunder ved å opprette et kundekort (inneholder video)
description: Beskriver hvordan du oppretter et kundekort for å registrere informasjon om hver nye kunde eller klient du selger til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client, customer, credit
ms.search.form: 7, 21, 22, 33, 42, 43, 367, 368, 369, 461, 512, 785, 1330, 1380, 1381, 1382, 1627, 2107, 7177, 9080, 9081, 9084, 9301, 9305
ms.date: 09/24/2021
ms.author: edupont
ms.openlocfilehash: 0e3745351039db7b4e24b8dfa1e31d920878aed0
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115261"
---
# <a name="register-new-customers"></a>Registrere nye kunder

Kunder er kilden til dine inntekter. Du må registrere gver kunde du selger til, som et kundekort. Kundekort inneholder informasjonen som er nødvendig for å selge produkter til kunden. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).  

Før du kan registrere nye kunder, må du definere forskjellige salgskoder som du kan velge fra når du fyller ut kundekort. Hvis du vil ha mer informasjon, kan du se [Sette opp salg](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a>Legge til nye kunder
Du kan legge til nye kunder manuelt ved å fylle ut feltene på siden **Kundekort**, eller du kan bruke maler som inneholder forhåndsdefinert informasjon. Du kan for eksempel opprette maler for ulike typer kundeprofiler. Når du bruker maler, sparer du tid når du legger til nye kunder og bidrar til å sikre at informasjonen er riktig hver gang. Hvis du oppretter maler for mer enn én kundetype, kan du velge hvilken mal du vil bruke når du legger til en kunde. Hvis du oppretter bare én mal, brukes den for alle nye kunder. Når du har opprettet en mal, kan du bruke handlingen **Bruk mal** til å bruke den på en eller flere utvalgte kunder. Når du skal opprette en mal, fyller du ut informasjonen du vil bruke på nytt på siden Kundekort, og deretter lagrer du den som en mal. Hvis du vil ha mer informasjon, kan du se delen [Slik lagrer du kundekortet som en mal](sales-how-register-new-customers.md#to-save-the-customer-card-as-a-template)

> [!TIP]
> Det kan være nyttig å tilpasse siden **Kundemal** når du oppretter en mal. Det kan for eksempel hende at du vil legge til feltet **Kredittgrense** i en mal. Hvis du vil ha mer informasjon, kan du se [Tilpass arbeidsområdet](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan også opprette en kunde fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du en kontakt, leverandør, ansatt eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  

### <a name="to-create-a-new-customer-card"></a>Opprette et nytt kundekort

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Handlingen **Priser og rabatter** gir alternativer for å administrere spesialpriser eller rabatter for kunden når en bestilling oppfyller bestemte kriterier. Kriteriene kan for eksempel være når de kjøper en bestemt vare, bestiller et minimumsantall eller kjøper før en dato, for eksempel når en kampanje avsluttes. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).

Kunden er nå registrert, og kundekortet er klart til å brukes på salgsdokumenter.

Hvis du vil bruke dette kundekortet som en mal når du oppretter nye kundekort, kan du lagre det som en mal. Hvis du vil ha mer informasjon, kan du se følgende avsnitt:  

### <a name="to-save-the-customer-card-as-a-template"></a>Lagre kundekortet som en mal

1. På siden **Kundekort** velger du handlingen **Lagre som mal**. **Kundemal**-siden åpnes og viser kundekortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**. **Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for kunden.
4. Rediger eller angi dimensjonskoder som skal gjelde for nye kundekort som opprettes ved hjelp av malen.  
5. Når du har fullført den nye kundemalen, kan du velge **OK**-knappen.

Kundemalen legges til i listen over kundemaler, slik at du kan bruke den til å opprette nye kundekort.

## <a name="deleting-customer-cards"></a>Slette kundekort

Hvis du har bokført en transaksjon for en kunde, kan du ikke slette kortet, fordi postene kan være nødvendige for revisjon. Hvis du vil slette kundekort med poster, kontakter du Microsoft-partneren for å gjøre det gjennom kode.  

## <a name="managing-credit-limits"></a>Håndtering av kredittgrenser

Kredittgrenser, saldobeløp og betalingsbetingelser gjør det mulig for [!INCLUDE [prod_short](includes/prod_short.md)] å utstede kreditt og gi en advarsel om forfalte beløp når du oppretter en ordre.  Funksjoner for purre- og rentebetingelser gir deg dessuten mulighet til å fakturere renter og/eller tilleggsgebyr.  

Feltet **Kredittgrense** på et kundekort angir maksimumsbeløpet som du tillater kunden å overskride betalingssaldoen med, før det utstedes advarsler. Når du deretter angir opplysninger i kladder, tilbud, ordrer og fakturaer, tester [!INCLUDE [prod_short](includes/prod_short.md)] salgshodet og de enkelte salgslinjene for å se om kredittgrensen er overskredet.

Du kan bokføre selv om kredittgrensen er blitt overskredet. Hvis du lar feltet være tomt, betyr det at kunden ikke har noen kredittgrense.  

Du kan velge å ikke motta advarsler om at kundens kredittgrense er overskredet, og du kan angi hvilke typer advarsel du vil vise.

### <a name="to-specify-credit-limit-warnings"></a>Slik angir du advarsler om kredittgrense

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salgsoppsett**, og velg deretter den relaterte koblingen.

2. På hurtigfanen **Generelt** i feltet **Kredittvarsler** velger du det relevante alternativet som er beskrevet i følgende tabell:

    |Alternativ| Beskrivelse|
    |------|------------|
    |**Begge advarslene**| Både feltet **Kredittgrense** og feltet **Forfalt beløp** på kundekortet merkes av, og en advarsel vises hvis kunden har oversteget sin kredittgrense, eller hvis kunden har et forfalt beløp.|
    |**Kredittgrense**|Verdien i feltet **Kredittgrense** på kundekortet sammenlignes med kundens saldo, og det vises en advarsel hvis kundens saldo overskrider dette beløpet.|
    |**Forfalt beløp**|Feltet **Forfalt beløp** er merket av på kundekortet, og det vises en advarsel hvis kunden har en forfalt saldo.|
    |**Ingen advarsel**|Det vises ingen advarsler om kundens status.|

## <a name="see-also"></a>Se også

[Definere betalingsmåter](finance-payment-methods.md)  
[Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md)  
[Opprette nummerserier](ui-create-number-series.md)  
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
