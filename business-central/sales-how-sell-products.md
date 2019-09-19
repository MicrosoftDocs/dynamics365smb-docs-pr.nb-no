---
title: Opprette en ordre og selge varer | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en ordre for å registrere avtalen med en kunde om å selge eller handle med produkter i samsvar med bestemte betingelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 08/19/2019
ms.author: sgroespe
ms.openlocfilehash: 4eb0a35f29b9eb6022b2517a1568a9fe80fdfc07
ms.sourcegitcommit: 81b6062194bf04d8052a3cd394cc0b41e3f53e6d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/20/2019
ms.locfileid: "1887648"
---
# <a name="sell-products"></a>Selge produkter
Du kan opprette en ordre eller salgsfaktura for å registrere avtalen med en kunde om å selge bestemte produkter på bestemte leverings- og betalingsbetingelser.

> [!NOTE]  
>   Du bruker ordrer hvis salgsprosessen krever at du kan sende deler av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke er tilgjengelig samtidig. Hvis du selger varer ved å levere direkte fra leverandøren til kunden, som en direkte levering, må du også å bruke ordrer. Hvis du vil ha mer informasjon, kan du se [Foreta direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer ordrer på samme måte som salgsfakturaer. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).

Du kan forhandle med kunden ved først å opprette et tilbud, som du kan konvertere til en ordre når dere blir enige om salget. Hvis du vil ha mer informasjon, kan du se [Gi salgstilbud](sales-how-make-offers.md).

Etter at kunden har bekreftet avtalen, for eksempel etter en tilbudsprosess, kan du sende en ordrebekreftelse for å registrere din forpliktelse til å levere produktene som avtalt.

Når du leverer produkter, helt eller delvis, kan du bokføre ordren som levert eller som levert og fakturert for å opprette de beslektede vare- og kundepostene i systemet. Når du bokfører ordren, kan du også sende dokumentet som et PDF-vedlegg i e-post. Du kan få brødteksten i e-posten forhåndsutfylt med et sammendrag av ordren og betalingsinformasjonen, for eksempel en kobling til PayPal. Hvis du vil ha mer informasjon, kan du se [Sende dokumenter i e-post](ui-how-send-documents-email.md).

I forretningsmiljøer der kunden betaler en stund etter levering, i henhold til betalingsbetingelsene, blir en bokført salgsfaktura værende åpen (ubetalt) til regnskapsavdelingen bekrefter at betalingen er mottatt, og utligner betalingen mot den bokførte salgsfakturaen, Hvis du vil ha mer informasjon, kan du se [Avstemme betalinger ved hjelp av automatisk utligning](receivables-how-reconcile-payments-auto-application.md).

I forretningsmiljøer der kunden betaler umiddelbart, for eksempel ved PayPal eller kontant, registreres betalingen umiddelbart når du bokfører salgsfakturaen som fakturert, det vil si at den bokførte salgsfakturaen lukkes som fullstendig utlignet. Du velger den relevante metoden i **Betalingsmåte - kode**-feltet i ordren. Se under trinn 8. For elektroniske betalinger, for eksempel PayPal, må du også fylle ut feltet **Betalingstjeneste**. Hvis du vil ha mer informasjon, kan du se [Aktivere kundebetalinger gjennom betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan opprette direkte betalte ordrer for kunder som ikke er registrert ved å definere et kontant kundekort, som du velger på ordren. Du finner mer informasjon under [Definere kontantkunder](finance-how-to-set-up-cash-customers.md).

Du kan enkelt å løse eller annullere en bokført salgsfaktura som resultat av en ordre før den er betalt. Dette er praktisk hvis du vil rette en skrivefeil, eller hvis kunden ber om en endring tidlig i ordreprosessen. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bokførte salgsfakturaen er betalt, må du opprette en salgskreditnota for å reversere salget. Hvis du vil ha mer informasjon, kan du se [Behandle ordrereturer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Varekortet kan være av typen **Lager**, **Service** eller **Ikke-lagervarer** for å angi om varen er en fysisk lagerenhet, en arbeidstidsenhet eller en fysisk enhet som ikke beholdes i lagerbeholdningen. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md). Ordreprosessen er den samme for alle de tre varetypene.

Du kan fylle kundefelt i ordren på to måter, avhengig av om kunden allerede er registrert. Se trinn 2 og 3 i fremgangsmåten nedenfor.

## <a name="to-create-a-sales-order"></a>Opprette en ordre
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Ordrer**, og velg deretter den relaterte koblingen.
2. I feltet **Kunde** angir du navnet på en eksisterende kunde.

    Andre felt på siden **Ordre** fylles nå med standardinformasjon for den valgte kunden. Hvis kunden ikke er registrert, følger du denne fremgangsmåten:
3. I feltet **Kunde** angir du navnet på den nye kunden.
4. Klikk **Ja**-knappen i dialogboksen for å registrere den nye kunden.
5. På siden **Velg en mal for en ny kunde** velger du en mal som du vil basere det nye kundekortet på, og deretter velger du **OK**-knappen.

    Det åpnes et nytt kundekort som er forhåndsutfylt med informasjon om den valgte kundemalen. **Navn**-feltet er forhåndsutfylt med det nye kundenavnet du skrev inn i salgsfakturaen i ordren.
6. Fortsette med å fylle ut resten av feltene på kundekortet. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).  
7. Når du har fullført kundekortet, velger du **OK**-knappen for å gå tilbake til siden **Ordre**.

    Flere felt i ordren er nå fylt ut med informasjon du har angitt på det nye kundekortet.
8. Fyll ut resten av feltene på siden **Ordre** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du vil at kunden betaler umiddelbart, for eksempel ved kredittkort eller PayPal, fyller du ut feltet **Betalingsmåte - kode**. Betalingen registreres deretter når du bokfører ordren som fakturert. Hvis du velger KONTANT, registreres betalingen på en bestemt motkonto.

    Du kan nå begynne å fylle ut ordrelinjene med lagervarer eller tjenester du vil selge til kunden.

    Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.
9. Angi nummeret på en vare eller tjeneste i **Vare**-feltet i hurtigfanen **Linjer**.  
10. I feltet **Antall** angir du hvor mange varer som skal selges.

    > [!NOTE]  
    >   For varer av typen Tjeneste er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Salgspris** multiplisert med verdien i feltet **Antall**.

    Prisen og linjebeløpene vises med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.
11. I feltet **Linjerabatt-%** angir du en prosent hvis du vil gi kunden en rabatt på produktet. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.

    Hvis du har konfigurert varepriser i hurtigfanen **Salgspriser og salgslinjerabatter** i kunde- eller varekortet, oppdateres prisen og beløpet på tilbudslinjen automatisk hvis de avtalte priskriteriene er oppfylt. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).
12. Hvis du vil legge til en kommentar om tilbudslinjen som kunden kan se på tilbudsutskriften, skriver du en tekst i **Beskrivelse**-feltet på en tom linje.  
13. Gjenta trinn 9 til 12 for hver vare som du vil selge til kunden.

    Totaler under linjene beregnes automatisk når du oppretter eller endrer linjer.
14. Det åpnes et nytt kundekort som viser informasjon om den valgte kundemalen. Fyll ut feltene som gjenstår. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).  
15. Når du har fullført kundekortet, velger du **OK**-knappen for å gå tilbake til siden **Ordre**.

    Flere felt i ordren er nå fylt ut med informasjon du har angitt på det nye kundekortet.
16. Fyll ut resten av feltene på siden **Ordre** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du er nå klar til å fylle ut ordrelinjene for produktene du selger til kunden eller for noen transaksjon med kunden som du vil registrere i en finanskonto.   

    Hvis du har definert gjentakende salgslinjer for kunden, for eksempel en månedlig etterfyllingsordre, kan du sette inn disse linjene på ordren ved å velge handlingen **Hent gjentakende salgslinjer**.  
17. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden med salgslinjen.

18. I **Nr.** velger du en post skal bokføres, i henhold til verdien i **Type**-feltet.

    La feltet **Nr.** stå tomt i følgende tilfeller:

    * Hvis linjen er for en kommentar. Skriv inn kommentaren i **Beskrivelse**-feltet.
    * Hvis linjen er for en katalogvare. Velg handlingen **Velg katalogvarer**. Hvis du vil ha mer informasjon, kan du se [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).

19. I **Antall**-feltet angir du hvor mange enheter av produktet, gebyret eller transaksjonen som linjen skal registrere for kunden.  

    > [!NOTE]  
    >   Hvis varen er av typen **Vare - tjeneste** eller **Ressurs**, er antallet en tidsenhet, for eksempel timer, som angitt i feltet **Enhetskode** på linjen. Hvis du vil ha mer informasjon, kan du se [Definere vareenheter](inventory-how-setup-units-of-measure.md).

    Verdien i **Linjebeløp**-feltet beregnes som *salgspris* x *antall*.  

    Prisen og linjebeløpene er med eller uten mva, avhengig av hva du valgte i feltet **Priser inkludert merverdiavgift** på kundekortet.  
20. Hvis du vil gi en rabatt, skriver du inn en prosentandel i feltet **Linjerabatt-%**. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.  

    Hvis du har konfigurert varepriser i hurtigfanen **Salgspriser og salgslinjerabatter** i kunde- eller varekortet, oppdateres prisen og beløpet på salgslinjen automatisk hvis de avtalte priskriteriene er oppfylt. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Gjenta trinn 9 til 12 for hver hvert produkt eller gebyr som du vil selge til kunden.  

    Totaler-feltene under linjene oppdateres automatisk når du oppretter eller endrer linjer for å vise beløpene som skal bokføres i postene.

    > [!NOTE]
    > I svært sjeldne tilfeller kan de bokførte beløpene avvike fra det som vises i totalfeltene. Dette skyldes vanligvis avrundingsberegninger i forbindelse med mva eller salgsmva.<br /><br />Når du skal kontrollere beløpene som faktisk skal bokføres, kan du bruke siden **Statistikk**, som tar hensyn til avrundingsberegningene. Hvis du velger **Frigi**-handlingen, oppdateres totaler-feltene slik at de omfatter avrundingsberegninger.  
22. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

    Hvis du har definert fakturarabatter for kunden, settes den angitte prosentverdien automatisk inn i feltet **Fakturarabatt %** hvis kriteriene er oppfylt, og det relaterte beløpet settes inn i feltet **Fakturarabattbeløp før mva.**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).
23. Hvis du vi sende bare en del av ordreantallet, kan du angi antallet i den feltet **Levere (antall)**. Verdien kopieres til feltet **Fakturer (antall)**.
24. Hvis du vi fakturere bare en del av det sendte antallet, kan du angi antallet i den feltet **Fakturer (antall)**. Antallet må være lavere enn verdien i feltet **Levere (antall)**.   
25. Når ordrelinjene er fullført, kan du velge handlingen **Bokfør og send**.

Dialogboksen **Bokfør og send bekreftelse** viser kundens foretrukne metode for mottak av dokumenter. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).

Beslektet element og kundeposter opprettes nå i systemet, og ordren skrives ut som et PDF-dokument. Når ordren er fullstendig bokført, fjernes fra listen over ordrer og erstattes med nye dokumenter i listen over bokførte salgsfakturaer og oversikten over bokførte følgesedler.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Lager](inventory-manage-inventory.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
