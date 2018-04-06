---
title: Konfigurere bankfeeder for Yodlee| Microsoft-dokumentasjon
description: "Du kan konvertere betalingsinformasjon til et hvilket som helst dataformat som banken krever, og gjøre det mulig å eksportere eller importere bankfiler."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream, payment process
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: fa5c0c39dbbce40b59d639f810522c66da1a09ab
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Konfigurere bankfeedservicen Envestnet Yodlee
Du kan importere elektroniske bankkontoutdrag fra banken slik at du raskt kan fylle ut vinduet **Betalingsavstemmingskladd**. Dermed kan du utligne betalinger og avstemme bankkontoen. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

Bankfeedservicen Envestnet Yodlee er installert som en utvidelse til [!INCLUDE[d365fin](includes/d365fin_md.md)] og er klar til å bli aktivert. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md).

> [!NOTE]
> Bankfeeder for Envestnet Yodlee-tjenesten støttes bare i USA, Canada og Storbritannia.

Når du har aktivert bankfeedservicen, må du koble en bankkonto til nettbankkontoen som feeden vil komme fra. Du kobler bankkonti til nettbankbankkonti i følgende ulike scenarier:

* En bankkonto finnes ikke i [!INCLUDE[d365fin](includes/d365fin_md.md)] for nettbankkontoen. Du kan derfor opprette bankkontoen ved å koble fra nettbankkontoen.
* Det finnes en bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vil koble til en nettbankkonto.
* Tilkoblingen for en koblet bankkonto må være fjernet fordi du vil slutte å bruke bankfeedservice for kontoen.
* Nettbankkontoer er endret, og du vil oppdatere informasjon om bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)].

Når bankfeedservicen er aktivert, kan du angi en bankkonto til automatisk å importere nye bankkontoutdrag til vinduet **Betalingsavstemmingskladd** hver annen timer. Transaksjoner for betalinger som allerede er bokført som utlignet og/eller avstemt i vinduet **Betalingsavstemmingskladd** vil ikke bli importert. Hvis du vil ha mer informasjon, kan du se avsnittet “Aktivere automatisk import av bankkontoutdrag”.

> [!NOTE]  
>   Hvis du bruker det assisterte oppsettet Konfigurer selskap, vil noen av trinnene i fremgangsmåtene nedenfor utføres automatisk når du kommer til oppsettet for bankkontoen til selskapet. Hvis du vil ha mer informasjon, kan du se [Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

## <a name="to-enable-the-bank-feed-service"></a>Aktivere bankfeedservicen
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Åpne bankkontoen som du vil bruke for bankfeedservicen.
3. I vinduet **Bankkonto**, i feltet **Importformat for bankkontoutdrag**, velger du YODLEEBANKFEED.  

Bankfeedservicen vil bli aktivert når du kobler en bankkonto til den relaterte nettbankkontoen. Se den neste fremgangsmåten.  

## <a name="to-create-a-new-linked-bank-account"></a>Opprette ny tilknyttet bankkonto
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg den relevante bankkontoen, og velg deretter **Opprett ny tilknyttet bankkonto**. Vinduet **Bankkontotilknytning** åpnes etter en liten stund.

    > [!NOTE]  
>   Dette vinduet viser den faktiske nettsiden for bankfeedservicen Envestnet Yodlee. Terminologi og funksjonene i vinduet samsvarer kanskje ikke med instruksjonene i dette emnet.  
3. I vinduet **Tilknytning til nettbankkonto**, i ruten **Bankkontotilknytning**, bruker du søkefunksjonen til å finne banken der du har en eller flere nettbankkontoer.
4. Velg banknavn. Ruten **Logg på** åpnes.
5. Skriv inn brukernavnet og passordet du bruker til å logge på nettbanken, og velg deretter **Neste**.  
6. Bankfeedservicen klargjør å koble den første nettbankkontoen i den angitte banken, til en ny bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)].

    > [!NOTE]  
>   Hvis du har mer enn én nettbankkonto i banken, må du opprette flere bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] for disse ekstra nettbankkontoene. Se trinn 8 til 10.  

    Når prosessen er fullført, vises banknavnet i ruten **Mine konter** på **Tilknyttet**-fanen. Tallet i parentes angir hvor mange nettbankkontoer som ble tilknyttet.  
7. Velg **OK**.

    Hvis du bare kobler én online bankkonto, den **Bankkort**-vinduet åpnes, og viser navnet på den elektroniske bankkontoen. I dette tilfellet er tilknytningen av bankkontoen fullført. Det eneste som gjenstår er å opprette en bankkonto. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-how-setup-bank-accounts.md).

    Hvis mer enn én nettbankkonto ble tilknyttet, åpnes vinduet **Bankkontotilknytning** som viser alle nettbankkontoene som ikke er knyttet til bankkontoene i [!INCLUDE[d365fin](includes/d365fin_md.md)] ennå. I det tilfellet følger du det neste trinnet.  
8. I vinduet **Bankkontotilknytning** velger du linjen for en nettbankkonto, og deretter velger du handlingen **Tilknytt ny bankkonto**.  

    Vinduet **Bankkort** åpnes for det en ny bankkonto og viser navnet på nettbankkontoen.

    Hvis det allerede finnes en bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)] som du vil tilknytte nettbankkontoen, følger du fremgangsmåten nedenfor.  
9. I vinduet **Bankkontotilknytning** velger du linjen for en nettbankkonto, og deretter velger du handlingen **Tilknytt eksisterende bankkonto**.
10. I vinduet **Bankkontooversikt** velger du bankkontoen du vil knytte til, og deretter velger du **OK**-knappen.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Knytte en bankkonto til en nettbankkonto
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg linjen for en bankkonto som ikke er tilknyttet en nettbankkonto, og velg deretter handlingen **Tilknytt nettbankkonto**. Vinduet **Tilknytning til nettbankkonto** åpnes med navnet til banken forhåndsutfylt i ruten **Bankkontotilknytning**.
3. Velg banknavn. Ruten **Logg på** åpnes.
4. Skriv inn brukernavnet og passordet du bruker til å logge på nettbanken, og velg deretter **Neste**.  

    Bankfeedservicen klargjør å koble bankkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)] til den relaterte nettbankkontoen.  

    Når prosessen er fullført, vises banknavnet i ruten **Mine konter** på **Tilknyttet**-fanen. Hvis banken har mer enn én bankkonto, tilknyttes bare bankkontoen du valgte i trinn 2.  
5. Velg **OK**.

I vinduet **Bankkontooversikt** er det merket av for **Tilknyttet**.

## <a name="to-unlink-a-bank-account"></a>Fjerne tilknytning for en bankkonto
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.  
2. Velg linjen for en tilknyttet bankkonto som du vil fjerne tilknytningen for en relatert nettbankkonto, og velg deretter handlingen **Fjern tilknytning for nettbankkonto**.

> [!NOTE]  
>   Hvis du velger **Ja** i bekreftelsesdialogboksen, fjernes tilknytningen til nettbankkontoen og påloggingsdetaljene nullstilles. Hvis du vil tilknytte bankkontoen til nettbankkontoen på nytt, må du logge på banken. Hvis du vil ha mer informasjon, kan du se avsnittet “Knytte en bankkonto til en nettbankkonto“.

## <a name="to-update-bank-account-linking"></a>Oppdatere bankkontotilknytning
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg den relevante bankkontoen, og velg deretter handlingen **Oppdater bankkontotilknytning**.

Hvis det finnes problemer for noen av de tilknyttede bankkontoene i vinduet **Bankkontooversikt**, åpnes vinduet **Bankkontotilknytning** som viser hvilke bankkontoer som har problemer. Problemer kan løses best ved å fjern tilkoblingen til nettbankkontoen og opprette tilknytningen på nytt. Hvis du vil ha mer informasjon, kan du se avsnittet «Knytte en bankkonto til en nettbankkonto».

## <a name="to-enable-automatic-import-of-bank-statements"></a>Aktivere automatisk import av bankkontoutdrag
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg linjen for en tilknyttet bankkonto, og velg deretter handlingen **Oppsett for automatisk bankkontoutdragsimport**.
3. I vinduet **Oppsett for automatisk bankkontoutdragsimport**, i feltet **Antall dager inkludert**, angir du hvor langt tilbake i tid nye banktransaksjonene skal hentes.

    > [!NOTE]  
>   Det anbefales at du setter denne verdien til 7 dager eller mer.  
4. Merk av for **Aktivert**.  

Hver time viser vinduet **Betalingsavstemmingskladd** nye betalinger som er gjort i nettbankkontoen.

> [!NOTE]  
>   Transaksjoner for betalinger som allerede er bokført som utlignet og/eller avstemt i vinduet **Betalingsavstemmingskladd** vil ikke bli importert.

## <a name="see-also"></a>Se også
[Konfigurere banktjenester](bank-setup-banking.md)  
[Håndtere bankkonti](bank-manage-bank-accounts.md)  
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

