---
title: Bokføre konserninterne dokumenter og kladder
description: Dette emnet forklarer hvordan du bruker konserninterne dokumenter eller kladder til å bokføre transaksjoner med de konserninterne partnerne.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '600, 610'
---
# <a name="work-with-intercompany-documents-and-journals" />Arbeide med konserninterne dokumenter og kladder

Bruk konserninterne dokumenter eller kladder til å bokføre transaksjoner med de konserninterne partnerne. Når du bokfører et konserninternt dokument eller en kladdelinje i selskapet, opprettes det et tilsvarende dokument eller kladdelinje i den konserninterne utboksen. Du overfører linjen fra utboksen til partneren. Partneren kan deretter bokføre den tilsvarende transaksjonen i selskapet sitt, uten å måtte registrere dataene på nytt.

For salgs-og kjøpsdokumenter sikrer den konserninterne partnerkoden på kunden eller leverandøren at alle ordrer og fakturaer for transaksjoner mellom partnerne, produserer tilhørende bilag i partnerselskapene. Selskapskontoene er i balanse.

Det samme gjelder for konserninterne finanskladdelinjer. Du trenger ikke å angi kontoer, men du velger bare partnerselskapet. Tilsvarende konserninterne finanskladdelinjer opprettes deretter i partnerselskapet.

## <a name="fill-in-and-send-an-intercompany-sales-order" />Fyll ut og send en konsernintern ordre

Du kan sende ordrer, bestillinger og returordrer før bokføring. Fakturaer og kreditnotaer kan ikke sendes før de bokført.

Fremgangsmåten nedenfor beskriver hvordan du fyller ut og sender en konsernintern ordre. Den samme fremgangsmåten gjelder for konserninterne bestillinger og returordrer og for bokførte konserninterne fakturaer og kreditnotaer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2. Velg **Ny** for å opprette en ny ordre. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).  
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kointroller at kunden er en konsernintern partner.
5. Hvis du vil sende ordren før du bokfører den, kan du velge **Send KI-ordre**.

> [!NOTE]
> Hvis du gjør trinn 5, går ordren til den konserninterne utboksen der du kan sende den senere. Hvis du vil lære mer om den konserninterne innboksen og utboksen, går du til [Administrer den konserninterne innboksen og utboksen](intercompany-how-manage-intercompany-inbox.md).

## <a name="fill-in-and-post-an-intercompany-journal" />Fyll ut og bokfør en konsernintern kladd

Når du bokfører en konsernintern kladdelinje i selskapet, opprettes det en tilsvarende kladdelinje i den konserninterne utboksen som du kan overføre til partneren. Med lanseringsbølge 1 for 2022 kan du også definere selskapet for å opprette mottatte konserninterne transaksjoner automatisk som partnere bokførte i konserninterne finanskladder. Partneren kan deretter bokføre den tilsvarende transaksjonen i selskapet sitt, uten å måtte registrere dataene på nytt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsernintern finanskladder**, og velg deretter den relaterte koblingen.  
2. Åpne kladden. Hvis du vil ha mer informasjon, kan du se [Arbeide med finanskladder](ui-work-general-journals.md).
3. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/invoicing/includes/tooltip-inline-tip_md.md)]
4. I feltet **Finanskontonr. for KI-partner** angir du nummeret til den konserninterne finanskontoen der beløpet skal bokføres i partnerens selskap.

    > [!NOTE]
    > Dette Feltet må fylles ut på en linje med en bankkonto eller finanskonto i feltet **Kontonr.** eller **Motkontonr.**.  
5. Velg handlingen **Bokfør**.

Postene bokføres i selskapet ditt, og en kladd med tilhørende poster opprettes i den konserninterne utboksen slik at du kan sende dem til partnerselskapet.

## <a name="see-also" />Se også

[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
