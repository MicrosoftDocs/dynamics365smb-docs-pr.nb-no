---
title: Konfigurere bankfeeder for Envestnet Yodlee
description: 'Du kan konvertere betalingsinformasjon til et hvilket som helst dataformat som banken krever, og gjøre det mulig å eksportere eller importere bankfiler.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'Yodlee, feed, stream, payment process'
ms.search.form: '1280, 1290'
ms.date: 03/20/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="set-up-the-envestnet-yodlee-bank-feeds-service"></a>Konfigurer Envestnet Yodlee Bank Feeds-tjenesten

Du kan importere elektroniske bankkontoutdrag fra banken slik at du raskt kan fylle ut på siden **Betalingsavstemmingskladd**. Dermed kan du utligne betalinger og avstemme bankkontoen. Hvis du vil ha mer informasjon, kan du se [Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!IMPORTANT]
> På grunn av direktivet for betalingstjenester i Europa (PSD2), vil du ikke lenger kunne importere bankkontoutdrag fra banker i Stobritannia i [!INCLUDE[prod_short](includes/prod_short.md)] etter 14. september 2019. Vi undersøker muligheten for å tilby denne funksjonen igjen senere.

> [!NOTE]
> Envestnet Yodlee Bank Feeds-tjenesten støttes bare i den elektroniske versjonen av Business Central. Denne funksjonaliteten støttes ikke for lokale versjoner av [!INCLUDE [prod_short](includes/prod_short.md)] eller for [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer som driftes på programtjenester for å bygge inn ISV. Hvis du vil bruke denne funksjonaliteten lokalt, må du skaffe en cobrand-konto fra Envestnet, og du må legge til kode som skal integreres med Yodlee-API-en.
>
> Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.
> Det er bare banker som befinner seg i disse landene/områdene, som støttes, selv om banker fra andre land/områder kan vises i vinduet for valg av bank Envestnet Yodlee Bank Feeds i [!INCLUDE[prod_short](includes/prod_short.md)].

> [!IMPORTANT]
> Kontakt Microsofts kundestøtte for teknisk assistanse med Envestnet Yodlee-funksjonaliteten. Ikke kontakt Envestnet Yodlee. Hvis du vil ha mer informasjon, kan du se [Konfigurere teknisk støtte for Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/technical-support).

Envestnet Yodlee Bank Feeds-tjenesten er installert som en utvidelse til den elektroniske versjonen av [!INCLUDE[prod_short](includes/prod_short.md)] og er klar til å bli aktivert i de støttede landene/områdene. Hvis du vil ha mer informasjon, kan du se [Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md).

Når du har aktivert bankfeedservicen, må du koble en bankkonto til nettbankkontoen som feeden vil komme fra. Du kobler bankkonti til nettbankbankkonti i følgende ulike scenarier:

* En bankkonto finnes ikke i [!INCLUDE[prod_short](includes/prod_short.md)] for nettbankkontoen. Du kan derfor opprette bankkontoen ved å koble fra nettbankkontoen.
* Det finnes en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] som du vil koble til en nettbankkonto.
* Tilkoblingen for en koblet bankkonto må være fjernet fordi du vil slutte å bruke bankfeedservice for kontoen.
* Nettbankkontoer er endret, og du vil oppdatere informasjon om bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)].

Når bankfeedservicen er aktivert, kan du angi en bankkonto til automatisk å importere nye bankkontoutdrag til siden **Betalingsavstemmingskladd** annenhver time. Transaksjoner for betalinger som allerede er bokført som utlignet eller avstemt på siden **Betalingsavstemmingskladd**, blir ikke importert. Hvis du vil ha mer informasjon, kan du se avsnittet “Aktivere automatisk import av bankkontoutdrag”.

> [!NOTE]  
> Hvis du bruker den assisterte oppsettsveiledning Konfigurer selskap, vil noen av trinnene i fremgangsmåtene nedenfor utføres automatisk når du kommer til oppsettet for bankkontoen til selskapet. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md).

## <a name="to-enable-the-bank-feed-service"></a>Aktivere bankfeedservicen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.
2. Åpne bankkontoen som du vil bruke for bankfeedservicen.
3. På kortet **Bankkonto**, i feltet **Importformat for bankkontoutdrag**, velger du YODLEEBANKFEED.  

Bankfeedservicen er aktivert når du kobler en bankkonto til den relaterte nettbankkontoen. Se den neste fremgangsmåten.  

> [!NOTE]
> Hvis du bruker det assisterte oppsettet **Selskapsoppsett**, aktiverer du tjenesten ved å merke av for **Bruk en bankfeedservice**. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i Business Central](about-new-company.md).

## <a name="to-create-a-new-linked-bank-account"></a>Opprette ny tilknyttet bankkonto

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg den relevante bankkontoen, og velg deretter **Opprett ny tilknyttet bankkonto**. Siden **Bankkontotilknytning** åpnes etter en liten stund.

    > [!NOTE]  
    > Denne siden viser den faktiske nettsiden for Envestnet Yodlee Bank Feeds-tjenesten. Terminologi og funksjonene på siden samsvarer kanskje ikke med instruksjonene i dette emnet.  
3. På siden **Tilknytning til nettbankkonto**, i ruten **Bankkontotilknytning**, bruker du søkefunksjonen til å finne banken der du har en eller flere nettbankkontoer.
4. Velg banknavn. Ruten **Logg på** åpnes.
5. Skriv inn brukernavnet og passordet du bruker til å logge deg på nettbanken, og velg deretter **Neste**.  
6. Bankfeedservicen klargjør å koble den første nettbankkontoen i den angitte banken, til en ny bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)].

    > [!NOTE]  
    > Hvis du har mer enn én nettbankkonto i banken, må du opprette flere bankkonti i [!INCLUDE[prod_short](includes/prod_short.md)] for disse ekstra nettbankkontoene. Se trinn 8 til 10.  

    Når prosessen er fullført, vises banknavnet i ruten **Mine konter** på **Tilknyttet**-fanen. Tallet i parentes angir hvor mange nettbankkontoer som ble tilknyttet.  
7. Velg **OK**-knappen.

    Hvis du bare kobler én online bankkonto, åpnes **Bankkort**-siden og viser navnet på den nettbaserte bankkontoen. I dette tilfellet er tilknytningen av bankkontoen fullført. Det eneste som gjenstår er å opprette en bankkonto. Hvis du vil ha mer informasjon, kan du se [Opprette bankkonti](bank-how-setup-bank-accounts.md).

    Hvis mer enn én nettbankkonto ble tilknyttet, åpnes siden **Bankkontotilknytning** som viser alle nettbankkontoene som ikke er knyttet til bankkontoene i [!INCLUDE[prod_short](includes/prod_short.md)] ennå. I det tilfellet følger du det neste trinnet.  
8. På siden **Bankkontotilknytning** velger du linjen for en nettbankkonto, og deretter velger du handlingen **Tilknytt ny bankkonto**.  

    Siden **Bankkort** åpnes for en ny bankkonto og viser navnet på nettbankkontoen.

    Hvis det allerede finnes en bankkonto i [!INCLUDE[prod_short](includes/prod_short.md)] som du vil tilknytte nettbankkontoen, følger du fremgangsmåten nedenfor.  
9. På siden **Bankkontotilknytning** velger du linjen for en nettbankkonto, og deretter velger du handlingen **Tilknytt eksisterende bankkonto**.
10. På siden **Bankkontooversikt** velger du bankkontoen du vil knytte til, og deretter velger du **OK**-knappen.

## <a name="to-link-a-bank-account-to-an-online-bank-account"></a>Knytte en bankkonto til en nettbankkonto

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkontoer**, og velg deretter den relaterte koblingen.
2. Velg linjen for en bankkonto som ikke er tilknyttet en nettbankkonto, og velg deretter handlingen **Tilknytt nettbankkonto**. Siden **Tilknytning til nettbankkonto** åpnes med navnet til banken forhåndsutfylt i ruten **Bankkontotilknytning**.
3. Velg banknavn. Ruten **Logg på** åpnes.
4. Skriv inn brukernavnet og passordet du bruker til å logge deg på nettbanken, og velg deretter **Neste**.  

    Bankfeedservicen klargjør å koble bankkontoen i [!INCLUDE[prod_short](includes/prod_short.md)] til den relaterte nettbankkontoen.  

    Når prosessen er fullført, vises banknavnet i ruten **Mine konter** på **Tilknyttet**-fanen. Hvis banken har mer enn én bankkonto, tilknyttes bare bankkontoen du valgte i trinn 2.  
5. Velg **OK**.

På siden **Bankkontooversikt** er det merket av for **Tilknyttet**.

## <a name="to-edit-the-credentials-for-an-online-bank-account"></a>Slik redigerer du legitimasjon for en bankkonto på nettet

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.  
2. Velg linjen for en bankkonto som ikke er tilknyttet en nettbankkonto, og velg deretter handlingen **Rediger informasjon om nettbankkonto**.
3. Oppdater legitimasjonen.

## <a name="to-unlink-a-bank-account"></a>Fjerne tilknytning for en bankkonto

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.  
2. Velg linjen for en tilknyttet bankkonto som du vil fjerne tilknytningen for en relatert nettbankkonto, og velg deretter handlingen **Fjern tilknytning for nettbankkonto**.

> [!NOTE]  
> Hvis du velger **Ja** i bekreftelsesdialogboksen, fjernes tilknytningen til nettbankkontoen og påloggingsdetaljene nullstilles. Hvis du vil tilknytte bankkontoen til nettbankkontoen på nytt, må du logge på banken. Hvis du vil ha mer informasjon, kan du se avsnittet «Knytte en bankkonto til en nettbankkonto».

## <a name="to-update-bank-account-linking"></a>Oppdatere bankkontotilknytning

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg den relevante bankkontoen, og velg deretter handlingen **Oppdater bankkontotilknytning**.

Hvis det finnes problemer for noen av de tilknyttede bankkontoene på siden **Bankkontooversikt**, åpnes siden **Bankkontotilknytning** som viser hvilke bankkontoer som har problemer. Problemer kan løses best ved å fjern tilkoblingen til nettbankkontoen og opprette tilknytningen på nytt. Hvis du vil ha mer informasjon, kan du se avsnittet «Knytte en bankkonto til en nettbankkonto».

## <a name="to-enable-automatic-import-of-bank-statements"></a>Aktivere automatisk import av bankkontoutdrag

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg linjen for en tilknyttet bankkonto, og velg deretter handlingen **Oppsett for automatisk bankkontoutdragsimport**.
3. På siden **Oppsett for automatisk bankkontoutdragsimport**, i feltet **Antall dager inkludert**, angir du hvor langt tilbake i tid nye banktransaksjonene skal hentes.

    > [!NOTE]  
    > Det anbefales at du setter denne verdien til 7 dager eller mer.  
4. Merk av for **Aktivert**.  

Hver time viser siden **Betalingsavstemmingskladd** nye betalinger som er gjort i nettbankkontoen.

> [!NOTE]  
> Transaksjoner for betalinger som allerede er bokført som utlignet og/eller avstemt på siden **Betalingsavstemmingskladd** vil ikke bli importert.

## <a name="see-also"></a>Se også

[Konfigurere banktjenester](bank-setup-banking.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Tilpass [!INCLUDE[prod_short](includes/prod_short.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
