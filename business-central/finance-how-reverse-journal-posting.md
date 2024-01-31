---
title: Angre en bokføring ved å bokføre en tilbakeføringspost
description: 'Hvis du finner en feil i en bokført finanskladd, kan du bruke handlingen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Tilbakeføre kladdebokføringer og angre mottak/leveringer

Tilbakeførte kladdebokføringer er nyttige for eksempel for å korrigere feil og for å tømme en gammel avsetningspost før du skriver inn en ny. En tilbakeføringspost er det samme som originalposen, men med motsatt rekkefølge i **Beløp**-feltet. Tilbakeføringsposten må ha samme dokumentnummer og bokføringsdato som originalposten. Når du har tilbakeført en post, må du lage den riktige posten.

Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje. En post kan bare tilbakeføres én gang.

Hvis du vil angre en mottaks- eller leveringsbokføring, kan du bruke funksjonen **Angre** på det bokførte bilaget før de bokføres som fakturert. Du kan angre mengder av typen **Vare** og **Ressurs**.

Hvis du har bokfør feil negativt antall, for eksempel en bestilling med galt vareantall, som mottatt, men ikke fakturert, kan du angre bokføringen.

Hvis du har bokført feil positivt antall, for eksempel en følgeseddelen eller bestillingsreturforsendelse med galt vareantall, som sendt, men ikke fakturert, kan du angre bokføringen.

## Tilbakeføre kladdebokføring av en finanspost

Du kan tilbakeføre poster fra alle **Poster**-sider. Fremgangsmåten nedenfor er basert på siden **Finansposter**.

> [!NOTE]
> Posten må stamme fra en kladdebokføring.
>
> Du kan heller ikke tilbakeføre poster som er bokført med informasjon fra en jobb, eller som har realisert agio og disagio i den samme transaksjonen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Finansposter**, og velg deretter den relaterte koblingen.
2. Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**.
3. Velg handlingen **Tilbakeføre** på siden **Tilbakefør transaksjonsposter**.
4. Velg **Ja** for å bekrefte tilbakeføringen.

## Bokføre en negativ post  

Bruk **Korreksjon**-feltet til å bokføre en negativ debet i stedet for en kredit, eller til å bokfører en negativ kredit i stedet for en debet på kontoen. Feltet er som standard tilgjengelig i alle kladder. Feltet **Debetbeløp** og **Kreditbeløp** omfatter den opprinnelige posten og den korrigert posten. Disse feltene har ingen innvirkning på kontoens saldo.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen  
2. Velg ønsket kladdenavn i **Bunkenavn**-feltet.  
3. Angi informasjon i de aktuelle feltene.  
4. På kladdelinjen som du vil aktivere for negative poster merker du av for **Korreksjon**.  
5. Hvis du vil bokføre kladden, velger du **Bokfør** og deretter **Ja**.

## Slik angrer du et antall på bokførte kjøpsmottak  

Nedenfor beskrives hvordan du angrer et bokført mottak av varer eller ressurser. Trinnene er de samme for bokførte leveringer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte kjøpsmottak**, og velg deretter den relaterte koblingen.  
2. Åpne det bokførte mottaket som du vil angre.  
3. Velg linjen(e) du vil angre.  
4. Velg **Angre mottak**-handlingen.

Det legges til en korrigeringslinje under den valgte mottakslinjen. Hvis antallet ble mottatt i et lagermottak, legges en korreksjonslinje til i det bokførte lagermottaket.  

Feltene **Mottatt (antall)** og **Mott. antall (ufakt.)** på den tilknyttede bestillingen blir satt til null.

## Slik angrer du og gjør om en antallsbokføring på en bokført returforsendelse

Følgende trinn beskriver hvordan du kan:

* Angre en bokført returforsendelse for varer eller ressurser.
* Bokføre bestillingsreturen på nytt med et nytt antall.

Trinnene er de samme for bokførte retursedler.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte returforsendelser**, og velg deretter den relaterte koblingen.  
2. Åpne bokført returforsendelse for å angre.
3. Velg linjen(e) du vil angre.  

4. Velg handlingen **Angre returforsendelse**.  

    En korreksjonslinje er satt inn i det bokførte dokumentet, og feltene **Returant. levert** og **Returfors., ikke fakt.** på ordrereturen settes til null.  

    Gå deretter tilbake til bestillingsreturen for å gjøre om bokføringen.  

5. Noter nummeret i feltet **Ordrereturnr.** på siden **Bokført bestillingsreturseddel**. -feltet.  
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.  
7. Åpne den aktuelle bestillingsreturen, og velg deretter **Åpne på nytt**.  
8. Korriger posten i feltet **Antall** og bokfør bestillingsreturen på nytt.  

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

## Se også

[Angre monteringsbokføring](assembly-how-to-undo-assembly-posting.md)  
[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]