---
title: Konfigurer påminnelsesbetingelser og -nivåer
description: Konfigurere Business Central slik at du kan sende påminnelser om forfalte betalinger og legge til gebyrer eller gebyrer på grunn av forsinkelsen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '431, 432, 436, 478'
ms.date: 03/12/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-reminder-terms-and-levels"></a>Konfigurer påminnelsesbetingelser og -nivåer

Du kan bruke purringer til å informere kunder om forfalte beløp og be om betaling. [!INCLUDE [reminder-terms](includes/reminder-terms.md)]

> [!TIP]
> Når du har definert betingelser og nivåer for purringer, kan du inkludere dem i automatiserte prosesser for oppretting, utstedelse og sending av purringer. Hvis du vil vite mer om den automatiserte prosessen, kan du gå til [Automatiser purringer i innkrevinger](finance-automate-reminders.md).

## <a name="reminder-terms"></a>Purrebetingelser

Hvis kunder har forfalte betalinger, må du angi når og hvordan du vil sende purring. I tillegg vil du kanskje belaste kundekontiene med renter eller gebyr. Du kan opprette så mange purrebetingelser du vil.  

> [!NOTE]
> Hvis du vil beregne rente på forfalte betalinger, kan du gjøre det når du oppretter purringer. Hvis du imidlertid bare vil beregne rente og informere kundene om dette uten å sende purringer, kan du bruke en [rentenota](finance-setup-finance-charges.md). Du finner mer informasjon under [Purringer](receivables-collect-outstanding-balances.md#reminders) eller [Rentenotaer](receivables-collect-outstanding-balances.md#finance-charges).

### <a name="set-up-attachment-and-email-body-texts-for-communications"></a>Konfigurer tekst for vedlegg og brødtekst i e-post for kommunikasjon

På siden **Oppsett av purrebetingelser** kan du definere vedleggstekst og standard e-postmeldinger som skal brukes enten for alle purrenivåer, eller opprette bestemte meldinger for hvert nivå. Meldingen du sender for første purrenivå, kan for eksempel ha en annen tone eller et annet innhold enn den andre eller tredje. Hvis du vil opprette tekster for vedlegg og e-postmeldinger for alle nivåer, velger du **Kundekommunikasjon** øverst på siden. Hvis du vil opprette meldinger for bestemte linjer, velger du en linje på hurtigfanen **Purregrad**, og deretter velger du handlingen **Kundekommunikasjon** på hurtigfanen.

Som standard bruker vedleggstekster og e-posttekster språkinnstillingen din. Hvis du utsteder purringer til kunder i andre land, kan det imidlertid hende at du vil kommunisere på et annet språk. Du kan opprette tekster for hvert språk som [!INCLUDE [prod_short](includes/prod_short.md)] støtter, ved å bruke handlingen **Legg til tekst for språk**. Hvis du gjør det, må du sørge for at språket er det samme for vedleggstekster og e-posttekster. Hvis de ikke samsvarer, og purreperioden har mer enn ett nivå, kan det hende at automatiseringen ikke kan tilpasse meldingen for ett eller flere nivåer. Hvis du vil kontrollere at språkene samsvarer, bruker du handlingen **Oversikt kommunikasjon** og sammenligner kommunikasjonen for tekstene.

Når du sender en e-post, er purringen en rapport du legger ved e-posten. Du definerer rapporten som genererer purringen, på siden **Purring/rentenota for rapportvalg**, der du også velger rapporten som inneholder brødteksten i e-posten i feltet **Navn på oppsett for brødtekst i e-post**. Når du sender e-post til kundene, settes tekstene på hurtigfanen **E-posttekst** inn i rapporten som er valgt i feltet **Navn på oppsett for brødtekst i e-post**. Standardrapporten har et tekstfelt for denne teksten. Hvis du vil, kan du redigere denne rapporten, for eksempel legge til eller fjerne innhold. Rediger oppsettet for disse rapportene på **Rapportoppsett**-siden. Hvis du vil lære mer om rapportoppsett, kan du gå til [Kom i gang med å opprette rapportoppsett](ui-get-started-layouts.md).

> [!NOTE]
> Kommunikasjon via e-post direkte fra [!INCLUDE [prod_short](includes/prod_short.md)] krever at du er konfigurert til å gjøre det. Hvis du vil ha mer informasjon om hvordan du kobler sammen e-postkontoer med [!INCLUDE [prod_short](includes/prod_short.md)], går du til [Konfigurer e-post](admin-how-setup-email.md).

### <a name="set-up-reminder-terms"></a>Definer purrebetingelser

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Purrebetingelser**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  
3. Hvis du vil bruke flere kombinasjoner av purrebetingelser, definerer du en kode for hver kombinasjon.

## <a name="reminder-levels"></a>Purregrader

For hver purreperiode kan du definere et ubegrenset antall purrenivåer, selv om de fleste selskaper bare bruker to eller tre nivåer. Innstillingen fra grad 1 brukes første gang det opprettes en purring for en kunde. Når purringen utstedes, registreres gradnummeret i purrepostene som opprettes og kobles til de individuelle kundepostene. Hvis det er nødvendig å sende kunden en ny purring, kontrolleres alle purreposter som er koblet til åpne kundeposter, for å finne det høyeste gradnummeret. Betingelsene fra neste gradnummer vil deretter bli brukt i den nye purringen.

Hvis du oppretter flere purringer enn du har definert grader for, brukes betingelsene for den høyeste graden. Du kan opprette så mange purringer som er tillatt i henhold til feltet **Høyeste purregrad** i purrebetingelsene.

### <a name="to-set-up-reminder-levels"></a>Slik definerer du purregrader

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Purrebetingelser**, og velg deretter den relaterte koblingen.  
2. På siden **Purrebetingelser** velger du linjen med betingelsene du vil definere grader for, og deretter velger du **Grader**.  
3. Fyll ut feltene etter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    > [!TIP]
    > Innstillingen for feltet **Beregn renter** bestemmer om renter skal vises på purringen når purringen utstedes. Feltet **Bokfør rente** på siden **Purrebetingelsene** bestemmer imidlertid om den beregnede renten skal bokføres til finans- og kundekonti.
    >
    > Hvis du vil angi at renter skal beregnes, velger du feletet **Beregn renter**.

    For hver purregrad kan du også angi tilleggsgebyr både i lokal og utenlandsk valuta. Du kan definere mange tilleggsgebyr i fremmed valuta for hver kode på siden **Purregrad**.  

    Tilleggsgebyrene kan beregnes på tre ulike måter, som er definert av verdien i feltet **Tilleggsgebyr beregningstype**.  

    - **Fast**

        Gebyr beregnes basert på verdiene i feltene **Tilleggsgebyr** på linjen for selve purregraden.  
    - **Enkel dynamisk**

        Gebyr beregnes basert på verdiene i feltene på den relevante linjen på siden **Oppsett av tilleggsgebyr** for purregraden.
    - **Akkumulert dynamisk**

        Gebyr beregnes basert på verdiene i feltene på de kombinerte linjene på siden **Oppsett av tilleggsgebyr** for purregraden.

4. Velg handlingen **Valutaer**.
5. På siden **Valutaer for purregrad** definerer du en valutakode og et tilleggsgebyr for hver purregradskode og tilhørende purregradsnummer.

    > [!NOTE]  
    > Når du oppretter purringer i en fremmed valuta, brukes betingelsene for den fremmede valutaen du definerer her, til å opprette purringer. Hvis det ikke er definert noen betingelser for purringer i fremmed valuta, brukes purrebetingelsene for LV som er definert på siden **Purregrader**, og deretter konverteres de til den relevante valutaen.

    For hver purregrad kan du spesifisere tekst som skal skrives ut før (**Starttekst**) eller etter (**Sluttekst**), i postene i purringen.

6. Velg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og fyll ut **Purretekst**-siden.
7. Hvis du vil sette inn beslektede verdier automatisk i purreteksten, kan du angi plassholderne nedenfor i **Tekst**-feltet.  

    |Plassholder|Verdi|  
    |-----------------|-----------|  
    |%1|Innholdet i **Bilagsdato**-feltet i purrehodet|  
    |%2|Innholdet i **Forfallsdato**-feltet i purrehodet|  
    |%3|Innholdet i feltet **Rentesats** på de relaterte rentenotabetingelsene|  
    |%4|Innholdet i **Restbeløp**-feltet i purrehodet|  
    |%5|Innholdet i **Rentebeløp**-feltet i purrehodet|  
    |%6|Innholdet i **Tilleggsgebyr**-feltet i purrehodet|  
    |%7|Purringens totalbeløp.|  
    |%8|Innholdet i **Purregrad**-feltet i purrehodet|  
    |%9|Innholdet i **Valutakode**-feltet i purrehodet|  
    |%10|Innholdet i **Bokføringsdato**-feltet i purrehodet|  
    |%11|Selskapsnavnet|  
    |%12|Innholdet i **Tilleggsgebyr per linje**-feltet i purrehodet|  

    Hvis du for eksempel skriver **Du skylder %9 %7, som forfaller den %2.**, vil purringen inneholde følgende tekst: **Du skylder 1200,50 USD, som forfaller 02-02-2024.**.

    > [!NOTE]
    > [!INCLUDE [prod_short](includes/prod_short.md)] beregner forfallsdatoen i henhold til datoformelen som du angir. Hvis du vil ha mer informasjon, kan du se [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).

8. Hvis du vil angi språket for en e-postmelding, velger du handlingen **Legg til tekst for språk**. **Språkkode-feltet** oppdateres slik at det viser valget ditt. På hurtigfanen **E-posttekst** skriver du inn innholdet i meldingen på det valgte språket.

Når du har definert purrebetingelsene, kan du tilordne dem til kunder på Kundekort-sider. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).  

## <a name="see-also"></a>Se også

[Innkreve utestående saldi](receivables-collect-outstanding-balances.md)  
[Send purringer om utestående saldoer](receivables-send-reminders.md)  
[Definer rentenotabetingelser](finance-setup-finance-charges.md)  
[Konfigurere finans](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
