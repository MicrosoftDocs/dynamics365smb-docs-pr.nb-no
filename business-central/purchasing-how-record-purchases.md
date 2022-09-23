---
title: Registrere kjøp med kjøpsfakturaer (inneholder video)
description: Beskriver hvordan du kan kjøpe beholdning, ikke-lagervarer eller ressurser ved å opprette og bokføre kjøpsfakturaer eller ordrer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.search.form: 50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310
ms.date: 09/01/2022
ms.author: edupont
ms.openlocfilehash: daedfacb3e496fa668095916b07caa7488765a83
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9535481"
---
# <a name="record-purchases-with-purchase-invoices"></a>Registrere kjøp med kjøpsfakturaer

Du kan opprette en kjøpsfaktura eller bestilling for å registrere kjøpskostnader og spore leverandørgjeld. Kjøpsfakturaer og bestillinger brukes også til å oppdatere lagernivåer dynamisk, noe som betyr at du kan redusere lagerkostnadene og gi bedre kundeservice. Kjøpskostnadene, inkludert tjenesteutgifter samt lagerverdier som er resultat av bokføring av kjøpsfakturaer eller ordrer, bidrar til fortjenestetall og andre økonomiske ytelsesindikatorer i rollesenteret.

## <a name="create-purchase-invoices"></a>Opprette kjøpsfakturaer

I tillegg til å kjøpe fysiske varer (varetypen **Beholdning**), som påvirker lagerverdisettingen, kan du kjøpe tjenester som representeres av tidsenheter. Dette kan du gjøre varetypen **Service** eller med linjetypen **Ressurs**.

Når du mottar lagervarene eller den kjøpte tjenesten er fullført, kan du bokføre kjøpsfakturaen eller bestillingen for å oppdatere lager- og økonomiposter og aktivere betaling til leverandøren i samsvar med betalingsbetingelsene. Finn ut mer under [Bokføring av kjøp](ui-post-purchases.md), [Motta varer](warehouse-how-receive-items.md) og [Utføring av betalinger](payables-make-payments.md).

> [!CAUTION]  
> Ikke bokfør fysiske varer for en kjøpsfaktura før du mottar varene og kjenner de endelige kostnadene for kjøpet, herunder eventuelle tilleggskostnader. Hvis ikke, kan det hende at lagerverdien og fortjenestebeløpet er skjevt.

### <a name="create-a-purchase-invoice"></a>Opprett en kjøpsfaktura

Nedenfor ser du en beskrivelse av hvordan du oppretter en kjøpsfaktura. Trinnene er de samme for en bestilling. Hovedforskjellen er at bestillinger har flere felt og handlinger for fysisk håndtering av varer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.

    Andre felt på siden **Kjøpsfaktura** fylles nå med standardinformasjon for den valgte leverandøren. Hvis leverandøren ikke er registrert, følger du denne fremgangsmåten:

    1. I feltet **Leverandør** angir du navnet på den nye leverandøren.
    2. Velg **Ja** i dialogboksen for å registrere den nye leverandøren.
    3. Hvis du vil vite mer om hvordan du fyller ut leverandørkortet, kan du gå til [Registrer nye leverandører](purchasing-how-register-new-vendors.md).  
    4. Når du har fylt ut leverandørkortet, velger du **OK** for å gå tilbake til **Kjøpsfaktura**-siden.

3. Fyll ut resten av feltene på siden **Kjøpsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du kan nå begynn å fylle ut kjøpsfakturalinjene med varer eller ressurser du har kjøpt fra leverandøren.

    > [!NOTE]  
    > Hvis du har definert gjentakende bestillingslinjer for leverandøren, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på fakturaen ved å velge handlingen **Hent gjentakende bestillingslinjer**.
4. Angi nummeret på en vare eller en tjeneste i **Varenr.**-feltet i hurtigfanen **Linjer**.
5. I feltet **Antall** angir du hvor mange varer som skal kjøpes.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Direkte enhetskost** multiplisert med verdien i feltet **Antall**.

    Prisen og linjebeløpet vises med eller uten mva., avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på leverandørkortet.

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene som skal bokføres i postene.

6. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.** nederst på fakturaen.

    > [!NOTE]  
    > Hvis du har definert fakturarabatter for leverandøren, settes den angitte prosentverdien automatisk inn i feltet **Leverandørfakturarabatt-%** hvis kriteriene er oppfylt. Det relaterte beløpet settes inn i feltet **Fakturarabattbeløp**.
7. Velg **Bokfør** når du mottar innkjøpte varer eller tjenester.

Kjøpet gjenspeiles nå i beholdningen, ressursposter og økonomiposter, og leverandørbetalingen aktiveres. Kjøpsfakturaen fjernes fra listen over kjøpsfakturaer og erstattes med et nytt dokument i listen over bokførte kjøpsfakturaer.  

> [!NOTE]
> I sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva. eller salgsmva.
>
> Når du skal kontrollere beløpene som faktisk skal bokføres, kan du gå til siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.

## <a name="when-to-use-purchase-orders"></a>Når du bør bruke bestillinger

Du må bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke er tilgjengelig hos leverandøren. Hvis du leverer solgte varer direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke bestillinger. Finn ut mer under [Lag direkte leveringer](sales-how-drop-shipment.md).

I alle andre henseender fungerer bestillinger på samme måte som kjøpsfakturaer. Følgende fremgangsmåte er basert på en kjøpsfaktura. Trinnene er de samme for en bestilling.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## <a name="purchasing-non-inventory-items"></a>Kjøp av ikke-lagervarer

Linjene på en kjøpsfaktura kan være av typen **Ressurs** eller **Vare**. Varekort kan også klassifiseres av typen **Lager**, **Service** eller **Ikke-lagervarer** som angir om varen er en fysisk lagerenhet, en arbeidstidsenhet (gjelder også ressurser) eller en fysisk enhet som ikke holdes i lagerbeholdningen. Finn ut mer under [Registrer nye varer](inventory-how-register-new-items.md). Kjøpsfakturaprosessen er den samme for alle typene nevnt ovenfor.

> [!NOTE]
> Med kjøpslinjetypen **Ressurs** kan du også kjøpe eksterne ressurser, for eksempel for å fakturere en leverandør for arbeid som er levert. Finn ut mer under [Definer ressurser](projects-how-setup-resources.md).
>
> Hvis du vil bruke en kjøpt ressurs, må du kanskje angi ressursens kapasitet og tilordne den manuelt til et prosjekt. Kjøp av en ressurs oppretter en ressurspost, men ressursposter spores imidlertid ikke for antall og verdi, for eksempel varer. Hvis antalls- og verdisporing er nødvendig, kan du vurdere å bruke andre linjeelementtyper.

## <a name="posted-invoices"></a>Bokførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan enkelt korrigere eller annullere en bokført kjøpsfaktura før du betaler leverandøren. Dette er praktisk hvis du må rette en skrivefeil eller endre kjøpet tidlig i bestillingsprosessen. Finn ut mer under [Korriger eller annuller ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md). Hvis du allerede har betalt for varer eller tjenester i den bokførte kjøpsfakturaen, må du opprette en kjøpskreditnota for å reversere innkjøpet. Finn ut mer under [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).

[Åpne listen **Bokførte kjøpsfakturaer**](https://businesscentral.dynamics.com/?page=146) i [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="external-document-number"></a>Eksternt dokumentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/processing-invoices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Bokføre kjøp](ui-post-purchases.md)  
[Motta varer](warehouse-how-receive-items.md)  
[Be om tilbud](purchasing-how-request-quotes.md)  
[Kjøpe varer for salg](purchasing-how-purchase-products-sale.md)  
[Klargjøre direkte leveringer](sales-how-drop-shipment.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Definere kjøp](purchasing-setup-purchasing.md)  
[Definere ressurser](projects-how-setup-resources.md)  
[Registrere nye leverandører](purchasing-how-register-new-vendors.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
