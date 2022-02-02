---
title: Registrere kjøp med kjøpsfakturaer (inneholder video)
description: Beskriver hvordan du kan kjøpe beholdning, ikke-lagervarer eller ressurser ved å opprette og bokføre kjøpsfakturaer eller ordrer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146
ms.date: 09/07/2021
ms.author: edupont
ms.openlocfilehash: 3d634e1ffb34cfdc0e4e7f6fc5e6ad4805cdabb5
ms.sourcegitcommit: e008b3d7003c256475d6c606e5f7c9866a6bbb72
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/10/2022
ms.locfileid: "7953037"
---
# <a name="record-purchases-with-purchase-invoices"></a>Registrere kjøp med kjøpsfakturaer

Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Hvis du vil kontrollere et lager, brukes kjøpsfakturaer og bestillinger også til å oppdatere lagernivåer dynamisk, slik at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer eller ordrer, bidrar til fortjenestetall og andre økonomiske KPIer i rollesenteret.

## <a name="create-purchase-invoices"></a>Opprette kjøpsfakturaer

I tillegg til å kjøpe fysiske varer (varetypen **Beholdning**), som påvirker lagerverdisettingen, kan du kjøpe tjenester som representeres av tidsenheter. Dette kan du gjøre varetypen **Service** eller med linjetypen **Ressurs**.

Når du mottar lagervarene, eller når den kjøpte tjenesten er fullført, kan du bokføre kjøpsfakturaen eller bestillingen for å oppdatere lager- og økonomiposter og aktivere betaling til leverandøren i samsvar med betalingsbetingelsene. Hvis du vil ha mer informasjon, kan du se [Bokføre kjøp](ui-post-purchases.md) og [Utføre betalinger](payables-make-payments.md).

> [!CAUTION]  
> Ikke bokfør fysiske varer for en kjøpsfaktura før du mottar varene og kjenner de endelige kostnadene for kjøpet, herunder eventuelle tilleggskostnader. Hvis ikke, kan det hende at lagerverdien og fortjenestebeløpet er skjevt.

### <a name="to-create-a-purchase-invoice"></a>Slik oppretter du en kjøpsfaktura:

Nedenfor ser du en beskrivelse av hvordan du oppretter en kjøpsfaktura. Trinnene er de samme for en bestilling. Hovedforskjellen er at bestillinger har flere felt og handlinger for fysisk håndtering av varer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.

    Andre felt på siden **Kjøpsfaktura** fylles nå med standardinformasjon for den valgte leverandøren. Hvis leverandøren ikke er registrert, følger du denne fremgangsmåten:

    1. I feltet **Leverandør** angir du navnet på den nye leverandøren.
    2. Klikk **Ja**-knappen i dialogboksen for å registrere den nye leverandøren.
    3. Hvis du vil ha mer informasjon om hvordan du fyller ut leverandørkortet, kan du se [Registrer nye leverandører](purchasing-how-register-new-vendors.md).  
    4. Når du har fylt ut leverandørkortet, velger du **OK**-knappen for å gå tilbake til **Kjøpsfaktura**-siden.

3. Fyll ut resten av feltene på siden **Kjøpsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du kan nå begynn å fylle ut kjøpsfakturalinjene med varer eller ressurser du har kjøpt fra leverandøren.

    > [!NOTE]  
    > Hvis du har definert gjentakende bestillingslinjer for leverandøren, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på fakturaen ved å velge handlingen **Hent gjentakende bestillingslinjer**.
4. Angi nummeret på en vare eller tjeneste i **Varenr.**-feltet i hurtigfanen **Linjer**.
5. I feltet **Antall** angir du hvor mange varer som skal kjøpes.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Direkte enhetskost** multiplisert med verdien i feltet **Antall**.

    Prisen og linjebeløpet vises med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på leverandørkortet.

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene som skal bokføres i postene.

6. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.** nederst på fakturaen.

    > [!NOTE]  
    > Hvis du har definert fakturarabatter for leverandøren, settes den angitte prosentverdien automatisk inn i feltet **Leverandørfakturarabatt-%** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp**.
7. Velg **Bokfør** når du mottar innkjøpte varer eller tjenester.

Kjøpet gjenspeiles nå i beholdningen, ressursposter og økonomiposter, og leverandørbetalingen aktiveres. Kjøpsfakturaen fjernes fra listen over kjøpsfakturaer og erstattes med et nytt dokument i listen over bokførte kjøpsfakturaer.  

> [!NOTE]
> I sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva eller salgsmva.
>
> Når du skal kontrollere beløpene som faktisk skal bokføres, kan du bruke siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.

## <a name="when-to-use-purchase-orders"></a>Når du bør bruke bestillinger

Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke var tilgjengelig hos leverandøren. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer. Følgende fremgangsmåte er basert på en kjøpsfaktura. Trinnene er de samme for en bestilling.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="selling-non-inventory-items"></a>Salg av ikke-lagervarer

Varene på en bestilling kan være av typen **Lager**, **Tjeneste**, **Ressurs** eller **Ikke-lagervarer** for å angi om varen er en fysisk lagerenhet, en arbeidstidsenhet eller en fysisk enhet som ikke beholdes i lagerbeholdningen. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md). Kjøpsfakturaprosessen er den samme for alle de tre varetypene.

> [!NOTE]
> Med kjøpslinjetypen **Ressurs** kan du også kjøpe eksterne ressurser, for eksempel for å fakturere en leverandør for arbeid som er levert. Hvis du vil ha mer informasjon, kan du se [Definere ressurser](projects-how-setup-resources.md).
>
> Hvis du vil bruke en kjøpt ressurs, må du kanskje angi ressursens kapasitet og tilordne den manuelt til et prosjekt. Kjøp av en ressurs vil opprette en ressurspost, men ressursposter spores imidlertid ikke for antall og verdi, for eksempel varer. Hvis antalls- og verdisporing er nødvendig, kan du vurdere å bruke andre linjeelementtyper.

## <a name="posted-invoices"></a>Bokførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan enkelt korrigere eller annullere en bokført kjøpsfaktura før du betaler leverandøren. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis du vil endre kjøpet tidlig i bestillingsprosessen. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du allerede har betalt for varer eller tjenester i den bokførte kjøpsfakturaen, må du opprette en kjøpskreditnota for å reversere innkjøpet. Hvis du vil ha mer informasjon, kan du se [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

[Åpne listen **Bokførte kjøpsfakturaer**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Innkjøp](purchasing-manage-purchasing.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Definere ressurser](projects-how-setup-resources.md)  
[Bokføre kjøp](ui-post-purchases.md)  
[Be om tilbud](purchasing-how-request-quotes.md)  
[Kjøpe varer for salg](purchasing-how-purchase-products-sale.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Klargjøre direkte leveringer](sales-how-drop-shipment.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]