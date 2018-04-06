---
title: "Opprette en kjøpsfaktura og registrere kjøp | Microsoft-dokumentasjon"
description: "Beskriver hvordan du kjøper lager- og servicevarer ved å opprette og bokføre kjøpsfakturaer eller bestillinger."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c977747432a2fd919d74aae8f70b151e62da0fab
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="record-purchases"></a>Registrere kjøp
Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Hvis du vil kontrollere en beholdning, brukes kjøpsfakturaer og bestillinger også til å oppdatere lagernivåer dynamisk, slik at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer eller ordrer, bidrar til fortjenestetall og andre økonomiske KPIer i rollesenteret.

> [!NOTE]  
>   Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke var tilgjengelig hos leverandøren. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer. Følgende fremgangsmåte er basert på en kjøpsfaktura. Trinnene er de samme for en bestilling.

Når du mottar lagervarene, eller når den kjøpte tjenesten er fullført, kan du bokføre kjøpsfakturaen eller bestillingen for å oppdatere lager- og økonomiposter og aktivere betaling til leverandøren i samsvar med betalingsbetingelsene. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).

> [!CAUTION]  
>   Ikke bokfør en kjøpsfaktura før du mottar varene og kjenner de endelige kostnadene for kjøpet, herunder eventuelle tilleggskostnader. Hvis ikke, kan det hende at lagerverdien og fortjenestebeløpet er skjevt.

Du kan enkelt korrigere eller annullere en bokført kjøpsfaktura før du betaler leverandøren. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du allerede har betalt for varene i den bokførte kjøpsfakturaen, må du opprette en kjøpskreditnota for å reversere innkjøpet. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

Varer kan være av typen **Lager** eller **Tjeneste**. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md). Kjøpsfakturaprosessen er den samme for begge varetyper.

Du kan fylle leverandørfelt i kjøpsfakturaen på to måter, avhengig av om leverandøren allerede er registrert.

## <a name="to-create-a-purchase-invoice"></a>Slik oppretter du en kjøpsfaktura:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.

    Andre felt i **Kjøpsfaktura**-vinduet fylles nå med standardinformasjon for den valgte leverandøren. Hvis leverandøren ikke er registrert, følger du denne fremgangsmåten:
3. I feltet **Leverandør** angir du navnet på den nye leverandøren.
4. Klikk **Ja**-knappen i dialogboksen for å registrere den nye leverandøren.
5. I vinduet **Velg en mal for en ny leverandør** velger du en mal som du vil basere det nye leverandørkortet på, og deretter velger du **OK**-knappen.
6. Det åpnes et nytt leverandørkort som er forhåndsutfylt med informasjon om den valgte leverandørmalen. **Navn**-feltet er forhåndsutfylt med det nye leverandørnavnet du skrev inn i kjøpsfakturaen.
7. Fortsette med å fylle ut resten av feltene på leverandørkortet. Hvis du vil ha mer informasjon, kan du se [Registrere nye leverandører](purchasing-how-register-new-vendors.md).  
8. Når du har fylt ut leverandørkortet, velger du **OK**-knappen for å gå tilbake til **Kjøpsfaktura**-vinduet.

    Flere felt i **Kjøpsfaktura**-vinduet er fylt ut med informasjon du har angitt på det nye leverandørkortet.
9. Fyll ut resten av feltene vinduet **Kjøpsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du kan nå begynn å fylle ut kjøpsfakturalinjene med lagervarer eller tjenester du har kjøpt fra leverandøren.

    > [!NOTE]  
    >   Hvis du har definert gjentakende bestillingslinjer for leverandøren, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på fakturaen ved å velge handlingen **Hent gjentakende bestillingslinjer**.
10. Angi nummeret på en vare eller tjeneste i **Varenr.**-feltet i hurtigfanen **Linjer**.
11. I feltet **Antall** angir du hvor mange varer som skal kjøpes.

    > [!NOTE]  
    >   For varer av typen **Tjeneste** er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Direkte enhetskost** multiplisert med verdien i feltet **Antall**.

    Prisen og linjebeløpet vises med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på leverandørkortet.
12. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.** nederst på fakturaen.

    > [!NOTE]  
    >   Hvis du har definert fakturarabatter for leverandøren, settes den angitte prosentverdien automatisk inn i feltet **Leverandørfakturarabatt-%** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp**.
13. Velg **Bokfør** når du mottar innkjøpte varer eller tjenester.

Kjøpet gjenspeiles nå i lager- og økonomiposter, og leverandørbetalingen aktiveres. Kjøpsfakturaen fjernes fra listen over kjøpsfakturaer og erstattes med et nytt dokument i listen over bokførte kjøpsfakturaer.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Be om tilbud](purchasing-how-request-quotes.md)  
[Kjøpe varer for salg](purchasing-how-purchase-products-sale.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Klargjøre direkte leveringer](sales-how-drop-shipment.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

