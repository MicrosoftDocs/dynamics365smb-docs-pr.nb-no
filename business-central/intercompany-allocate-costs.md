---
title: Fordel kost til konserninterne partnere| Microsoft Docs
description: Finn ut hvordan mva-innstillinger for kunder og leverandører kontrollerer om og hvordan mva. beregnes.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocate-costs-to-intercompany-partners" />Fordel kost til konserninterne partnere
Når du bruker konserninterne bokføringer til å overføre dokumenter mellom partnerselskaper, kontrollerer mva-relaterte innstillinger (primært mva-bokføringsgruppen for firma) som er tilordnet kunde- eller leverandørkontiene (tilknyttet den konserninterne partneren) om og hvordan mva. beregnes og registreres. Du kan også utføre kostnadsdistribusjoner direkte fra en bestilling til partnerselskaper. Hvis du for eksempel registrerer en kjøpsfaktura fra en ekstern leverandør og vil distribuere noen av eller alle kostnadene til én eller flere konserninterne partnere.

Du kan fordele kost til én eller flere konserninterne partnere ved å bruke følgende:

* **Konserninterne finanskladder** – disse kladdene er nyttige når en tjeneste kjøpes. Når et morselskap for eksempel leier inn en tjeneste for å konfigurere datasystemer i to datterselskaper. Fakturaen sendes til morselskapet, men kostnadene fordeles til de konserninterne partnerne. Hvis du vil ha mer informasjon, kan du se [Arbeide med konserninterne dokumenter og kladder](intercompany-how-work-documents-journals.md).
* Bestillinger og fakturaer – det er nyttig å bruke kjøpsdokumenter når kjøpsfunksjonene i for eksempel driftsutgifter, desentraliseres i ett selskap og deretter tildeles de konserninterne partnerne.

## <a name="to-allocate-costs-using-an-intercompany-general-journal" />Slik fordeles kost ved hjelp av en konsernintern finanskladd
Følg denne fremgangsmåten for å angi en linje i en konsernintern finanskladd. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsernintern finans**, og velg deretter den relaterte koblingen.
2. Hvis det er nødvendig, angir du angir du dokumentnummeret på fakturaen fra leverandøren i feltet **Eksternt dokumentnr.**.
3. I feltet **Dokumenttype** velger du **Faktura**.
4. Velg **Leverandør** i **Kontotype**-feltet.
5. Velg leverandøren i **Kontonr.**-feltet.
6. I **Beløp**-feltet angir du et negativt beløp som er likt beløpet på fakturaen.
7. Angi **Finanskonto** i **Motkontotype**-feltet.
8. Velg motkontoen i **Motkontonr.**-feltet.
9. Følg denne fremgangsmåten for å fordele kost til konserninterne partnere:
   1. Opprett en ny linje.
   2. La feltet **Dokumenttype** være tomt, og velg deretter alternativet som lar feltet stå tomt.
   3. I feltet **Dokumentnr.** angir du et tall som er forskjellig fra nummeret i feltet **Eksternt dokumentnr.**. Kostnadsfordelingen anses som en annen transaksjon.
   4. Velg **KI-partner** i **Kontotype**-feltet.
   5. I **Kontonr.**-feltet velger du den konserninterne partneren kostnaden skal fordeles til.
   6. Angi **Finanskonto** i **Motkontotype**-feltet.
   7. I feltet **Motkontonr.** velger du finanskontoen der du vil bokføre beløpet du mottar fra den konserninterne partneren.
   1. I feltet **Beløp** angir du beløpet på fakturaen som skal fordeles til den konserninterne partneren.
   1. I feltet **Finanskontonr. for KI-partner** velger du finanskontoen som du vil bokføre beløpet til for den konserninterne partneren. 
   1. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Gjenta denne fremgangsmåten for hver konserninterne partner som skal ta del i kostnaden.
1. Hvis du vil bokføre dokumentet og fordele kostnadene, velger du **Bokfør**.  

## <a name="to-allocate-costs-using-a-purchase-document" />Slik fordeles kostnader ved hjelp av et kjøpsdokument
Følgende fremgangsmåte viser hvordan du fordeler kostnader ved hjelp av en kjøpsfaktura. Trinnene er de samme for bestillinger.

> [!NOTE]
> Du må tilpasse siden **Kjøpsfaktura** ved å legge til feltene **KI-partnerkode**, **Referansetype for KI-partner** og **KI-partner**. Hvis du vil ha mer informasjon, kan du se [Slik tilpasser du en side med Tilpasse-banneret](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfaktura**, og velg deretter den relaterte koblingen.
2. Velg **Finankonto** i **Type**-feltet.
   
   Finanskonto er det eneste alternativet du kan bruke til å fordele kostnader.  
1. I feltet **Nr.** velger du finanskontoen det skal bokføres til.
1. I **KI-partnerkode**-feltet velger du den konserninterne partneren kostnaden skal fordeles til.
1. I feltet **Referansetype for KI-partner** velger du finanskontoen som skal brukes til fordelingen. Denne kontoen tilordner utgiften til en konto i den konserninterne partnerens kontoplan.
1. I feltet **Antall** angir du hvor mange enheter som skal belastes den konserninterne partneren.
1. I feltet **Direkte enhetskost eks. mva.** angir du kostnaden per vare som skal belastes til den konserninterne partneren.
1. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
1. Du bokfører bestillingen ved å velge **Bokfør**.

## <a name="to-send-the-allocated-costs-to-intercompany-partners" />Slik sender du fordelte kostnader til konserninterne partnere
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **KI-utbokstransaksjoner**, og velg deretter den relaterte koblingen.
2. Velg linjer som skal sendes, og velg deretter handling **Send til KI-partner**. 
3. Du fordeler kostnadene ved å velge handlingen **Fullfør linjehandlinger**.

## <a name="calculating-vat-for-cost-distributions" />Beregne mva. for kostnadsdistribusjoner
Når du bruker et dokument til å distribuere kostnader til konserninterne partnere, må du være oppmerksom på to mva-innstillinger: 
* Innstillingene på finanskontoen for utgifter:
   * Hvis de generelle forretningsgruppene eller mva-bokføringsgruppene for firma er definert i finanskontoen, avhenger beregningen av gruppene og produktgruppene fra dokumentlinjen.
   * Hvis de generelle forretningsgruppene eller mva-bokføringsgruppene for firma ikke er definert i finanskontoen, er beregningen avhengig av følgende:
* Bokføringsgruppeinnstillingene for den konserninterne partneren
   * Om den konserninterne partneren er tilordnet et kundenummer som det ikke er angitt en generell forretningsgruppe eller mva-bokføringsgrupper for firma fir.
   * Det finnes ikke noe kundenummer tilknyttet den konserninterne partneren. Firmabokføringsgruppene eller mva-bokføringsgruppene for firma er tomme, og linjen i mva-bokføringsoppsettet brukes, som vanligvis er en gruppe der 0 % mva. er angitt.

> [!NOTE]
> Det er viktig å validere både det konserninterne partneroppsettet og finanskontooppsettet (for utgiftskontoen som brukes i kostnadsfordelingen) før du fordeler kostnader til konserninterne partnere.

## <a name="see-also" />Se også
[Oppsett av konserninternt](intercompany-how-setup.md)  
[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeid med finanskladder](ui-work-general-journals.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
