---
title: Kjøpvarer for et salg
description: Du kan opprette en faktura for en leverandør fra en salgsfaktura for å kjøpe produkter.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'supply planning, sales demand, replenish'
ms.search.form: '50, 51, 56, 9308'
ms.date: 03/14/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="purchase-items-for-a-sale-by-creating-purchase-invoices"></a>Kjøpe varer som er på salg ved å opprette kjøpsfakturaer

I ordrer og på salgsfakturaer kan du bruke funksjoner til raskt å opprette kjøpsdokumenter for manglende vareantall som kreves av salget. Du kan bruke to ulike funksjoner, avhengig av dokumenttypen.

> [!Note]
> Denne funksjonen er for påfyll av salgsvarer i ditt eget lager. Hvis du vil kjøpe varer for direkte levering fra leverandøren til kunden, må du opprette en direkte levering. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md).   

|Funksjon|Description|
|--------|-----------|
|**Opprett bestillinger**|I en ordre oppretter denne funksjonen en bestilling for hver enkelt leverandør av varene i ordren. Du kan redigere kjøpsantallet før du oppretter bestillingene. Det er bare utilgjengelige salgsantall som foreslås.
|**Opprett kjøpsfaktura**|I en ordre og på en salgsfaktura oppretter denne funksjonen en kjøpsfaktura for en valgt leverandør for alle linjene eller valgte linjer i salgsdokumentet. Hele salgsantallet foreslås.|

## <a name="to-create-one-or-more-purchase-orders-from-a-sales-order"></a>Opprette én eller flere bestillinger fra en ordre
Hvis du vil opprette en bestilling for hvert utilgjengelige vareantall i ordren, bruker du funksjonen **Opprett bestillinger**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Åpne en ordre du vil kjøpe varer for.
3. Velg handlingen **Opprett bestillinger**.

    Siden **Opprett bestillinger** åpnes med en linje for hver unike vare i ordren. Som standard vises linjer for både helt tilgjengelige salgsantall og utilgjengelige salgsantall (nedtonet). Du kan velge handlingen **Vis utilgjengelige** hvis du bare vil se linjer for utilgjengelige salgsantall.

    Feltet **Antall å kjøpe** inneholder som standard det utilgjengelige salgsantallet.
4. Hvis du vil kjøpe et annet antall enn det utilgjengelige salgsantallet, endrer du verdien i feltet **Antall å kjøpe**.

    > [!NOTE]  
    >   Du kan også endre feltet **Antall å kjøpe** på nedtonede linjer selv om de representerer helt tilgjengelige salgsantall.
5. Velg **OK**.

    En bestilling opprettes for hver enkelt leverandør av varene i ordren, inkludert eventuelle antallsendringer du har foretatt på siden **Opprett bestillinger**.
7. Fortsett behandlingen av for eksempel bestillingen eller bestillingene ved å redigere eller legge til bestillingslinjer. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).


## <a name="to-create-a-purchase-invoice-from-a-sales-order-or-sales-invoice"></a>Opprette en kjøpsfaktura fra en ordre eller salgsfaktura
Hvis du vil opprette én kjøpsfaktura for én eller flere linjer i et salgsdokument ved først å velge leverandøren du vil kjøpe fra, bruker du funksjonen **Opprett kjøpsfaktura**.

> [!NOTE]  
>   Denne funksjonen oppretter en kjøpsfaktura for det nøyaktige vareantallet i det valgte salgsdokumentet. Hvis du vil endre kjøpsantallet, må du redigere kjøpsfakturaen etter at den er opprettet.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Åpne en salgsfaktura du vil kjøpe varer for.
3. Velg én eller flere salgsfakturalinjer du vil bruke på kjøpsfakturaen. Hvis du vil bruke alle salgsfakturalinjene, merker du dem alle eller ingen av dem.
4. Velg handlingen **Opprett kjøpsfaktura**.
5. Velg **Alle linjer** eller **Valgte linjer**, og velg deretter **OK**-knappen.  
6. I listen over leverandører som vises, velger du leverandøren du vil kjøpe alle varene fra, og deretter velger du **OK**.

    Det opprettes en kjøpsfaktura som inneholder én, flere enn én eller alle linjene på salgsfakturaen.
7. Fortsette med å behandle kjøpsfakturaen, for eksempel ved å redigere eller legge til kjøpsfakturalinjene. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrer kjøp](purchasing-how-record-purchases.md)  
[Fakturer salg](sales-how-invoice-sales.md)  
[Registrer nye leverandører](purchasing-how-register-new-vendors.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
