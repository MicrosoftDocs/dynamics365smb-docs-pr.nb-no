---
title: Angre en bokføring ved å bokføre en tilbakeføringspost
description: Hvis du har foretatt en feilaktig bokføring i finanskladden, kan du bruke funksjonen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.search.form: 20, 25, 29, 38, 202, 5912,
ms.date: 07/22/2021
ms.author: edupont
ms.openlocfilehash: 2a9689db234280c2bcca5e32ade2a82488c15de5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8147729"
---
# <a name="reverse-journal-postings-and-undo-receiptsshipments"></a>Tilbakeføre kladdebokføringer og angre mottak/leveringer

Tilbakeførte kladdebokføringer brukes ikke bare til å korrigere feil, men de brukes også for eksempel til å tømme en gammel avsetningspost før du skriver inn en ny. Du velger posten og oppretter en tilbakeføringspost (poster som er identiske med den opprinnelige posten, men med motsatt fortegn i beløpsfeltet) med samme bilagsnummer og bokføringsdato som den opprinnelige posten. Når du har tilbakeført en post, må du lage den riktige posten.

Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje. En post kan bare tilbakeføres én gang.

Hvis du vil angre en mottaks- eller leveringsbokføring, kan du bruke funksjonen **Angre** på det bokførte bilaget før de bokføres som fakturert. Du kan angre mengder av typen **Vare** og **Ressurs**.

Hvis du har utført en ukorrekt negativ antallsbokføring, for eksempel en bestilling med galt vareantall, og bokført denne som mottatt (men ikke fakturert), kan du angre bokføringen.

Hvis du har utført en ukorrekt positiv antallsbokføring, for eksempel en følgeseddelen eller bestillingsreturforsendelse med galt vareantall, og bokført denne som sendt, men ikke fakturert, kan du angre bokføringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Tilbakeføre kladdebokføring av en finanspost
Du kan tilbakeføre poster fra alle **Poster**-sider. Fremgangsmåten nedenfor er basert på siden **Finansposter**.
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Finansposter**, og velg deretter den relaterte koblingen.
2. Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**. Vær oppmerksom på at den må stamme fra en kladdebokføring.
3. Velg handlingen **Tilbakeføre** på siden **Tilbakefør transaksjonsposter**.
4. Velg **Ja** i bekreftelsesmeldingen.

> [!NOTE]
> Du kan ikke tilbakeføre poster som er bokført med informasjon fra en jobb, eller som har realisert agio og disagio i den samme transaksjonen.

## <a name="to-post-a-negative-entry"></a>Bokføre en negativ post  
Du kan bruke **Korreksjon**-feltet til å bokføre en negativ debet i stedet for en kredit, eller til å bokfører en negativ kredit i stedet for en debet på kontoen. For å dekke juridiske krav vises dette feltet som standard i alle kladder. Feltet **Debetbeløp** og **Kreditbeløp** omfatter den opprinnelige posten og den korrigert posten. Disse feltene har ingen innvirkning på kontoens saldo.  

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder**, og velg deretter den relaterte koblingen  
2.  Velg ønsket kladdenavn i **Bunkenavn**-feltet.  
3.  Angi informasjon i de aktuelle feltene.  
4.  På kladdelinjen som du vil aktivere for negative poster merker du av for **Korreksjon**.  
5.  Hvis du vil bokføre kladden, velger du **Bokfør** og deretter **Ja**.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Slik angrer du antallsbokføring på bokførte kjøpsmottak  
Nedenfor beskrives hvordan du angrer et bokført mottak av varer eller ressurser. Trinnene er de samme for bokførte leveringer.

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte kjøpsmottak**, og velg deretter den relaterte koblingen.  
2.  Åpne det bokførte mottaket som du vil angre.  
3.  Velg linjen(e) du vil angre.  
4.  Velg **Angre mottak**-handlingen.

Det settes inn en korreksjonslinje under den valgte mottakslinjen. Hvis antallet ble mottatt i et lagermottak, settes en korreksjonslinje inn i det bokførte lagermottaket.  

Feltene **Mottatt (antall)** og **Mott. antall (ufakt.)** på den tilknyttede bestillingen blir satt til null.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Slik angrer du og gjør om en antallsbokføring på en bokført returforsendelse
Følgende beskriver hvordan du angrer en bokført returforsendelse av varer eller ressurser og deretter bokfører bestillingsreturen med et nytt antall. Trinnene er de samme for bokførte retursedler.

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bokførte returforsendelser**, og velg deretter den relaterte koblingen.  
2.  Åpne den bokførte returforsendelsen som du vil angre.
3. Velg linjen(e) du vil angre.  

4.  Velg handlingen **Angre returforsendelse**.  

    En korreksjonslinje er satt inn i det bokførte dokumentet, og feltene **Returant. levert** og **Returfors., ikke fakt.** på ordrereturen settes til null.  

    Gå deretter tilbake til bestillingsreturen for å gjøre om bokføringen.  

5.  Noter nummeret i feltet **Ordrereturnr.** på siden **Bokført bestillingsreturseddel**. -feltet.  
6.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.  
7.  Åpne den aktuelle bestillingsreturen, og velg deretter **Åpne på nytt**.  
8.  Korriger posten i feltet **Antall** og bokfør bestillingsreturen på nytt.  

## <a name="see-also"></a>Se også

[Angre monteringsbokføring](assembly-how-to-undo-assembly-posting.md)  
[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]