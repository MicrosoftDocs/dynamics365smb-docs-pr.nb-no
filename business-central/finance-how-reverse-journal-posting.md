---
title: "Angre en bokføring ved å bokføre en tilbakeføringspost | Microsoft-dokumentasjon"
description: "Hvis du har foretatt en feilaktig bokføring i finanskladden, kan du bruke funksjonen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9a4a7001ab5a752bf2e2acdd273d2a584a1e0b8a
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="reverse-postings"></a>Tilbakeføre bokføringer
Hvis du vil angre en feilaktig kladdebokføring, velger du posten og oppretter en tilbakeføringspost (poster som er identiske med den opprinnelige posten, men med motsatt fortegn i beløpsfeltet) med samme bilagsnummer og bokføringsdato som den opprinnelige posten. Når du har tilbakeført en post, må du lage den riktige posten.

Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje. En post kan bare tilbakeføres én gang.

Hvis du vil ha mer informasjon om bokføring fra en finanskladd, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).

Hvis du har utført en ukorrekt nagativ antallsbokføring, for eksempel en bestilling med galt vareantall, og bokført denne som mottatt (men ikke fakturert), kan du angre bokføringen.

Hvis du har utført en ukorrekt positiv antallsbokføring, for eksempel en bestillingsretur med galt vareantall, og bokført denne som sendt (men ikke fakturert), kan du angre bokføringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Tilbakeføre kladdebokføring av en finanspost
Du kan tilbakeføre poster i alle **Poster**-vinduer. Fremgangsmåten nedenfor er basert på vinduet **Finansposter**.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finansposter**, og velg deretter den relaterte koblingen.
2. Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**. Vær oppmerksom på at den må stamme fra en kladdebokføring.
3. I vinduet **Tilbakefør transaksjonsposter** velger du den relevante posten og deretter handlingen **Tilbakefør**.
4. Velg **Ja** i bekreftelsesmeldingen.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Slik angrer du antallsbokføring på bokførte kjøpsmottak  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte kjøpsmottak**, og velg deretter den relaterte koblingen.  
2.  Åpne det bokførte mottaket som du vil angre.  
3.  Velg linjen(e) du vil angre.  
4.  Velg **Angre mottak**-handlingen.

    Det settes inn en korreksjonslinje under den valgte mottakslinjen.  

    Hvis antallet ble mottatt i et lagermottak, settes en korreksjonslinje inn i det bokførte lagermottaket.  

    Feltene **Mottatt (antall)** og **Mott. antall (ufakt.)** på den tilknyttede bestillingen blir satt til null.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Slik angrer du og gjør om en antallsbokføring på en bokført returforsendelse

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte returforsendelser**, og velg deretter den relaterte koblingen.  
2.  Åpne den bokførte returforsendelsen som du vil angre.
3. Velg linjen(e) du vil angre.  

4.  Velg handlingen **Angre returforsendelse**.  

    En korreksjonslinje er satt inn i det bokførte dokumentet, og feltene **Returant. levert** og **Returfors., ikke fakt.** på ordrereturen settes til null.  

    Gå deretter tilbake til bestillingsreturen for å gjøre om bokføringen.  

5.  Noter nummeret i feltet **Ordrereturnr.** i vinduet **Bokført bestillingsreturseddel** .  
6.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.  
7.  Åpne den aktuelle bestillingsreturen, og velg deretter **Åpne på nytt**.  
8.  Korriger posten i feltet **Antall** og bokfør bestillingsreturen på nytt.  

## <a name="to-post-a-negative-entry"></a>Bokføre en negativ post  
Du kan bruke **Korreksjon**-feltet til å bokføre en negativ debet i stedet for en kredit, eller til å bokfører en negativ kredit i stedet for en debet på kontoen. For å dekke juridiske krav vises dette feltet som standard i alle kladder. Feltet **Debetbeløp** og **Kreditbeløp** omfatter den opprinnelige posten og den korrigert posten. Disse feltene har ingen innvirkning på kontoens saldo.  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen  
2.  Velg ønsket kladdenavn i **Bunkenavn**-feltet.  
3.  Angi informasjon i de aktuelle feltene.  
4.  På kladdelinjen som du vil aktivere for negative poster merker du av for **Korreksjon**.  
5.  Hvis du vil bokføre kladden, velger du **Bokfør** og deretter **Ja**.

## <a name="see-also"></a>Se også
[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
