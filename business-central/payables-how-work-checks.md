---
title: Utstede, skrive ut og kansellere sjekker | Microsoft-dokumentasjon
description: Beskriver hvordan du utsteder sjekker ved hjelp av utbetalingskladden, skriver ut sjekker og kansellerer eller viser sjekkposter i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e73c2dd0533aade4aa6225c9d2f385baaea3cfd1
ms.openlocfilehash: bcd0e21bc40b63c99f37618ae3406395b3c31b10
ms.contentlocale: nb-no
ms.lasthandoff: 06/11/2018

---
# <a name="make-check-payments"></a>Foreta sjekkbetalinger
Du kan utstede elektroniske og manuelle sjekker i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Begge metodene bruker utbetalingskladden til å utstede sjekker til leverandører. Du kan også kansellere sjekker og vise sjekkposter.

Følgende fremgangsmåte viser hvordan du betaler en leverandør med maskinelle sjekker ved å utligne betalingen mot den aktuelle leverandørfakturaen, skrive ut sjekken og deretter bokføre betalingen som betalt. Dette fører til positive leverandørposter, utlignet mot negative bankposter og fysiske sjekker for behandling i banken.

Du kan betale med to typer sjekker. For begge disse typene må feltet **Motkontotype** eller **Kontotype** inneholde **Bankkonto**.

- **Maskinell sjekk**: Velg dette alternativet hvis du vil at programmet skal opprette og senere skrive ut en sjekk på beløpet på betalingskladdelinjen. Du må skrive ut sjekkene før du kan bokføre kladdelinjene. Du kan bare velge **Maskinell sjekk** hvis
- **Manuell sjekk**: Velg dette alternativet hvis du manuelt har skrevet en sjekk og vil at programmet skal opprette en tilhørende sjekkpost på dette beløpet. Når du bruker dette alternativet, kan du ikke skrive ut sjekken.

> [!NOTE]  
> For å være sikker på at banken bare innfrir validerte sjekker og beløp, kan du sende dem en fil som inneholder informasjon om leverandør, sjekk og betaling. Hvis du vil ha mer informasjon, kan du se [Eksportere en Positive Pay-fil](finance-how-positive-pay.md).

Skriveren må være riktig konfigurert for sjekkskjemaene, og du må definere hvilke sjekkoppsett som skal brukes. Hvis du vil ha mer informasjon, kan du se [Definere sjekkoppsett](finance-how-define-check-layouts.md)

Du kan skrive ut opptil 10 fakturaer på en side for en blankett. Hvis en sjekk gjelder for flere enn 10 fakturaer, kansellerer vi sjekken på den første siden og skrive ut ordet KANSELLER på sjekken når du skriver ut blanketten. Vi skriver deretter ut resten av fakturaene og det totale sjekkbeløpet på den andre siden. 

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Slik betaler du en leverandørfaktura med en maskinell sjekk
Nedenfor beskrives hvordan du betaler en leverandør med sjekk. Fremgangsmåten er lik refusjon til kunde med sjekk.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Betalingskladder**, og velg deretter den relaterte koblingen.
2. Fyll ut utbetalingskladdelinjene. Hvis du vil ha mer informasjon, kan du se [Registrere betalinger og refusjoner](payables-how-post-payments-refunds.md).
3. I feltet **Betalingsmåte - kode** velger du **Sjekk**.
4. I feltet **Bankbetalingstype** velger du **Maskinell sjekk**.
5. Velg **Skriv ut sjekk**-handlingen.
6. Fyll ut feltene etter behov i vinduet **Sjekk**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Velg **Send til**-knappen, velg **PDF-dokument**, og velg deretter **OK**-knappen.

    De fysiske sjekkene kan nå flyttes til banken for behandling. Fortsett med å bokføre betalingen som utlignet til leverandøren, og dermed betalt i systemet.
8. Velg handlingen **Bokfør**.

Fullstendig utlignede leverandørposter og bankposter opprettes.

> [!NOTE]  
> Hvis du vil skrive ut og betale sjekker i flere valutaer fra forskjellige bankkonti, må du utføre kjørselen **Skriv ut sjekk** separat for hver enkelt valuta og angi riktig bankkonto.

## <a name="to-cancel-printed-checks-that-are-not-posted"></a>Kansellere utskrevne sjekker som ikke er bokført
Du kan kansellere ikke-bokførte sjekker etter at de er skrevet ut, ved hjelp av handlingen **Kanseller sjekk** i vinduet **Betalingskladd**.

1. I vinduet **Betalingskladd** velger du **Kanseller sjekk**, og deretter velger du hvilke sjekker som skal kanselleres.

## <a name="to-void-checks"></a>Kansellere sjekker
Når sjekkbetaliner er bokført, kan du bare kansellere (void) sjekker fra de resulterende bankpostene.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkonti**, og velg deretter den relaterte koblingen.
2. Velg relevant bankkonto, velg handlingene **Rediger** og **Sjekkposter**.
3. I vinduet **Sjekkposter** velger du handlingen **Kanseller sjekk**.
4. Merk av for **Kanseller sjekk**.
5. Velg **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Slik viser du et sammendrag av bokførte sjekker
Hvis du vil gå gjennom bokførte sjekker, for eksempel for å kontrollere flere sjekker som er betalt til én leverandør, kan du bruke rapporten **Bankkonto - sjekkopplysninger**.
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bankkonto - sjekkopplysninger**, og velg deretter den relaterte koblingen.
2. Angi filtre som er relevante, og velg deretter **Forhåndsvisning**-knappen.

## <a name="see-also"></a>Se også
[Utføre betalinger](payables-make-payments.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Konfigurere banktjenester](bank-setup-banking.md)  
[Eksportere en Positive Pay-fil](finance-how-positive-pay.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

