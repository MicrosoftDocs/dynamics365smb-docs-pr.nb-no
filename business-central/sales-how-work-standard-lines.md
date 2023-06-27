---
title: Standard gjentakende salgslinjer
description: Definere ofte brukte salgslinjer for å sette dem inn i salgsdokumenter og fylle ut linjene raskt med standardinformasjon.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, sell, replenishment'
ms.search.form: 172
ms.date: 07/06/2022
ms.author: edupont
---
# <a name="create-recurring-sales" />Opprett gjentakende salg

Hvis du ofte må opprette salgslinjer med lignende informasjon, kan du definere standardlinjer du deretter kan sette inn på gjentakende salgsdokumenter, for eksempel for gjentakende etterfyllingsordrer.  

## <a name="set-up-recurring-sales-lines" />Konfigurer gjentakende salgslinjer

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Gjentakende salgslinjer**, og velg deretter den relaterte koblingen.  
2. På siden **Gjentakende salgslinjer** velger du handlingen **Ny**.  
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I hurtigfanen **Linjer** angir du informasjon i feltene for å klargjøre salgslinjer som gjenspeiler standardlinjene du forventer å bruke som gjentakende linjer i salgsdokumenter.  

> [!NOTE]
> Du kan ikke definere priser på gjentakende salgslinjer, fordi priser, rabatter og så videre. beregnes på de faktiske salgsdokumentene etter at du setter inn de gjentakende salgslinjene.

[!INCLUDE [line-no-info](includes/line-no-info.md)]

## <a name="assign-recurring-sales-lines-to-a-customer" />Tildel gjentakende salgslinjer til kunder

Tilordne én eller flere gjentakende salgslinjer til en kunde, slik at de kan settes inn i salgsdokumenter for kunden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne kortet for den aktuelle kunden.
3. Velg handlingen **Gjentakende salgslinjer**.
4. På siden **Gjentakende salgslinjer** velger du kodene for de gjentakende salgslinjene som du vil sette inn i salgsdokumenter for kunden.
5. Fyll ut de andre feltene for å definere når, hvordan og hvor de gjentakende salgslinjene skal brukes.  

    Hvis du planlegger å bruke gjentakende salgslinjer sammen med kjørselen **Opprett gjentakende salgsfakturaer**, må du bruke feltene **Gyldig fra-dato** og **Gyldig til-dato** for å begrense når gjentakende salgslinjer brukes til oppretting av fakturaer. Hvis du vil ha mer informasjon, kan du se [Opprett flere salgsfakturaer basert på standard salgslinjer](sales-how-work-standard-lines.md#create-multiple-sales-invoices-based-on-recurring-sales-lines).

    Du kan også angi en betalingsmåte for direct-debit og en direct-debit-belastningsfullmakt. Salgsfakturaene som er opprettet med den satsvise jobben **Opprett gjentakende salgsfakturaer**, vil dermed inneholde informasjonen som kreves for å kreve inn betaling med SEPA direct debit. Hvis du vil ha mer informasjon, kan du se [Innkreve betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

6. I de fire feltene der du velger hvordan linjene settes inn på fire dokumenttyper, kan du velge ett av følgende alternativer:

|Alternativ|Beskrivelse|
|------|-----------|
|**Manuell**|Du må manuelt slå opp og sette inn en gjentakende salgslinje for kunden.|
|**Automatisk**|Hvis det finnes flere gjentakende salgslinjer for kunden, får du melding om hvor du kan velge en som kan settes inn. Hvis det bare finnes én gjentakende salgslinje, settes den inn automatisk.<br /><br />Dette bare fungerer hvis det nye dokumentet ble opprettet fra en dokumentliste, for eksempel ved å velge **Ny**-handlingen på **Ordrer**-siden. Den fungerer imidlertid ikke hvis dokumentet ble opprettet fra for eksempel et kundekort.|
|**Be alltid om bekreftelse**|Det vises en melding, og alle gjentakende salgslinjer vises slik at du kan velge én.

## <a name="insert-recurring-sales-lines-on-a-sales-invoice" />Sett inn gjentakende salgslinjer i en salgsfaktura

Hvis det finnes gjentakende salgslinjer for kunden, kan du sette dem inn eller få dem satt inn, på alle typer salgsdokumenter, for eksempel en salgsfaktura. Hvis du har aktivert alternativene for **Be alltid om bekreftelse** mens du tildeler gjentakende salgslinjer til kunder, blir du informert om det finnes gjentakende salgslinjer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Åpne salgsfakturaen du vil sette inn én eller flere standard salgslinjer på.
3. Velg handlingen **Hent gjentakende salgslinjer**.
4. På siden **Gjentakende salgslinjer** velger du oppslagsknappen i **Kode**-feltet, og deretter velger du et sett med standard salgslinjer.
5. Velg **OK** for å sette inn de standard salgslinjene på fakturaen, der du kan bruke informasjonen på nytt som den er eller redigere den.

## <a name="create-multiple-sales-invoices-based-on-recurring-sales-lines" />Opprett flere salgsfakturaer basert på gjentakende salgslinjer

Du kan bruke kjørselen **Opprett gjentakende salgsfakturaer** til å opprette salgsfakturaer i henhold til standard salgslinjer som er tilordnet til kundene, og med bokføringsdatoer innenfor gyldig-fra- og gyldig til-datoer du angir på standardsalgslinjene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Opprett gjentakende salgsfakturaer**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene på siden **Opprett gjentakende salgsfakturaer** etter behov.
3. I filterfeltet **Kode** angir du koden for standard salgslinjer som er tilordnet en kunde du vil opprette salgsfakturaer for.
4. Velg **OK**.

Salgsfakturaer blir opprettet for kunder med angitt standard kundesalgskode og eventuell angitt avtalegiroinformasjon, for bokføring på den angitte datoen.

## <a name="see-related-microsoft-training" />Se relatert [Microsoft-opplæring](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Salg](sales-manage-sales.md)  
[Definere salg](sales-setup-sales.md)  
[Opprett gjentakende kjøpslinjer](purchasing-how-work-recurring-purchase-lines.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
