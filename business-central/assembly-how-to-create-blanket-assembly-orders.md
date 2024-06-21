---
title: Opprette rammemonteringsordrer
description: Opprett rammeordrer for tilpassede monteringsvarer før du med jevne mellomrom oppretter de faktiske ordrene i henhold til rammeordreavtalen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'kit, kitting'
ms.search.form: '900, 901, 902, 903, 904, 907, 910, 916, 920, 921, 922, 923, 940, 941, 942, 930, 931, 932, 914, 915, 905'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="create-blanket-assembly-orders"></a>Opprette rammemonteringsordrer

Du kan bruke monteringsstyring for å tilpasse en monteringsvare i henhold til en kundeforespørsel under salgsprosessen. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).  

 Som med alle andre typer varer kan du også opprette rammeordrer for tilpassede monteringsvarer før du med jevne mellomrom lager de faktiske ordrene i henhold til rammeordreavtalen. Denne prosessen omfatter flere ekstra trinn når du sammenligner den med å opprette en vanlig rammeordre, og den bruker en variant av en koblet monteringsordre, som er en rammemonteringsordre.

> [!NOTE]  
>  I likhet med alle rammebestillinger er antallene på monteringsrammebestillinger bare prognoser og ikke operative før de konverteres til faktiske monteringsordrer. Derfor er ordrefunksjonalitet som beregning av tilgjengelighet, reservasjon og varesporing ikke aktiv for rammemonteringsordrer.  

## <a name="to-create-a-blanket-assembly-order-for-an-assemble-to-order-item"></a>Slik oppretter du en rammemonteringsordre for en montere\-til\-ordre-vare

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Rammeordrer**, og velg deretter den relaterte koblingen.  
2. Opprette en ny rammeordre med én linje for en monteringsvare. Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md).  
3. Angi hele antallet i feltet **Ant. som skal monteres til ordre** på linjen for rammemonteringsordre.

    > [!NOTE]  
    >  Du bør ikke opprette rammebestillingsavtaler for et delvist antall. Du må derfor angi samme antall som du skrev inn i feltet **Antall** på rammeordrelinjen.  

4. Velg handingen **Monter til ordre**, og velg deretter handlingen **Montere til ordre – linjer**. Du kan også merke feltet **Ant. som skal monteres til ordre** på linjen.  
5. Gå gjennom eller endre monteringsordrelinjene i henhold til rammeordreavtalen du har med kunden, på siden **Montere til ordre – linjer**. Hvis du vil vise mer informasjon, velger du **Vis dokument** for å åpne hele rammemonteringsordren. Du kan ikke endre innholdet i de fleste av feltene, og du kan ikke bokføre.  
6. Når du har justert monteringsordrelinjene i henhold til rammeordreavtalen, lukker du siden **Montere til ordre – linjer** for å gå tilbake til siden **Rammeordre**.  
7. Når kunden ber om å få opprettet en ordre basert på den avtalte rammeordren, oppretter du en ordre for den/de avtalte monteringsvaren(e). Hvis du vil ha mer informasjon, kan du se [Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md).

Den koblede rammemonteringsordren og eventuelle tilpasninger knyttes til denne nye salgsordren for å klargjøre for montering av varen(e) som skal selges.  

## <a name="see-also"></a>Se også

[Opprette rammeordrer](sales-how-to-create-blanket-sales-orders.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Lager](inventory-manage-inventory.md)  
[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
