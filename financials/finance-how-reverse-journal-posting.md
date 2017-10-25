---
title: "Angre en bokføring ved å bokføre en tilbakeføringspost | Microsoft-dokumentasjon"
description: "Hvis du har foretatt en feilaktig bokføring i finanskladden, kan du bruke funksjonen Tilbakefør transaksjon til å angre bokføringen med et riktig revisjonsspor."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reimbursement
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 802171d4f421270cb7e9b4f9dfedec9b9fe5ddc6
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reverse-postings"></a>Tilbakeføre bokføringer
Hvis du vil angre en feilaktig kladdebokføring, velger du posten og oppretter en tilbakeføringspost (poster som er identiske med den opprinnelige posten, men med motsatt fortegn i beløpsfeltet) med samme bilagsnummer og bokføringsdato som den opprinnelige posten. Når du har tilbakeført en post, må du lage den riktige posten.

Du kan bare tilbakeføre poster som er bokført fra en finanskladdelinje. En post kan bare tilbakeføres én gang.

Hvis du vil ha mer informasjon om bokføring fra en finanskladd, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).

Hvis du har utført en ukorrekt nagativ antallsbokføring, for eksempel en bestilling med galt vareantall, og bokført denne som mottatt (men ikke fakturert), kan du angre bokføringen.

Hvis du har utført en ukorrekt positiv antallsbokføring, for eksempel en bestillingsretur med galt vareantall, og bokført denne som sendt (men ikke fakturert), kan du angre bokføringen.   

## <a name="to-reverse-the-journal-posting-of-a-general-ledger-entry"></a>Tilbakeføre kladdebokføring av en finanspost
Du kan tilbakeføre poster i alle **Poster**-vinduer. Fremgangsmåten nedenfor er basert på vinduet **Finansposter**.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finansposter**, og velg deretter den relaterte koblingen.
2. Velg posten du vil tilbakeføre, og velg deretter handlingen **Tilbakefør transaksjon**. Vær oppmerksom på at den må stamme fra en kladdebokføring.
3. I vinduet **Tilbakefør transaksjonsposter** velger du den relevante posten og deretter handlingen **Tilbakefør**.
4. Velg **Ja** i bekreftelsesmeldingen.

## <a name="to-undo-a-quantity-posting-on-a-posted-purchase-receipt"></a>Slik angrer du antallsbokføring på bokførte kjøpsmottak  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokførte kjøpsmottak**, og velg deretter den relaterte koblingen.  
2.  Åpne det bokførte mottaket som du vil angre.  
3.  Velg linjen(e) du vil angre.  
4.  Velg **Angre mottak**-handlingen.

    Det settes inn en korreksjonslinje under den valgte mottakslinjen.  

    Hvis antallet ble mottatt i et lagermottak, settes en korreksjonslinje inn i det bokførte lagermottaket.  

    Feltene **Mottatt (antall)** og **Mott. antall (ufakt.)** på den tilknyttede bestillingen blir satt til null.

## <a name="to-undo-and-then-redo-a-quantity-posting-on-a-posted-return-shipment"></a>Slik angrer du og gjør om en antallsbokføring på en bokført returforsendelse

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bokførte returforsendelser**, og velg deretter den relaterte koblingen.  
2.  Åpne den bokførte returforsendelsen som du vil angre.
3. Velg linjen(e) du vil angre.  

4.  Velg handlingen **Angre returforsendelse**.  

    En korreksjonslinje er satt inn i det bokførte dokumentet, og feltene **Returant. levert** og **Returfors., ikke fakt.** på ordrereturen settes til null.  

    Gå deretter tilbake til bestillingsreturen for å gjøre om bokføringen.  

5.  Noter nummeret i feltet **Ordrereturnr.** i vinduet **Bokført bestillingsreturseddel** .  
6.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.  
7.  Åpne den aktuelle bestillingsreturen, og velg deretter **Åpne på nytt**.  
8.  Korriger posten i feltet **Antall** og bokfør bestillingsreturen på nytt.  

## <a name="see-also"></a>Se også
[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

