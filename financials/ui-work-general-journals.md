---
title: "Bruke finanskladder til å bokføre direkte i Finans | Microsoft-dokumentasjon"
description: "Finn ut hvordan du bruker finanskladder til å bokføre finanstransaksjoner på finanskonti og andre konti, for eksempel bank-, kunde- og leverandørkonti."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2aac957fc253f6c7d2f621ea2e5e039733081a19
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="working-with-general-journals"></a>Arbeide med finanskladder
De fleste finanstransaksjoner bokføres i Finans via dedikerte forretningsdokumenter, for eksempel kjøpsfakturaer eller ordrer. Når det gjelder forretningsaktiviteter som ikke representeres av et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], for eksempel mindre utgifter eller innbetalinger, kan du opprette de relaterte transaksjonene ved å bokføre kladdelinjer i **Finanskladd**-vinduet. Hvis du vil ha mer informasjon, kan du se [Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md).

Du kan for eksempel bokføre ansattes utlegg for firmarelaterte utgifter for senere refusjon. Hvis du vil ha mer informasjon, kan du se [Registrere og refundere ansattes utgifter](finance-how-record-reimburse-employee-expenses.md).

Du bruker finanskladder til å bokføre finanstransaksjoner direkte på finanskonti og andre konti, for eksempel bank-, kunde-, leverandør- og ansattkonti. Bokføring med en finanskladd oppretter alltid poster på finanskonti. Dette gjelder selv om en kladdelinje for eksempel bokføres på en kundekonto, ettersom en post bokføres til en finanssamlekonto via en bokføringsgruppe.

Opplysningene du angir i en kladd, er midlertidige og kan endres mens de fortsatt befinner seg i kladden. Når du bokfører kladden, overføres opplysningene til poster i individuelle konti, der de ikke kan endres. Du kan imidlertid oppheve utligningen av bokførte poster, og du kan bokføre tilbakeførings- eller korrigeringsposter. Hvis du vil ha mer informasjon, kan du se [Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Bruke kladder og kladdemaler
Det finnes flere finanskladdemaler. Hver kladdemal er representert av et eget vindu med bestemte funksjoner og feltene som er nødvendige for å støtte disse funksjonene, for eksempel vinduet **Betalingsavstemmingskladd** for å behandle betalinger og **Betalingskladd** for å betale leverandører eller gi ansatte refusjon. Hvis du vil ha mer informasjon, kan du se [Foreta betalinger](payables-make-payments.md) og [Avstemme kundebetalinger manuelt](receivables-how-apply-sales-transactions-manually.md).

Du kan definere dine egne personlige kladder som en kladd for hver enkelt kladdemal. Du kan for eksempel definere din egen kladd for betalingskladden som har personlig oppsett og innstillinger. Tipset nedenfor er et eksempel på hvordan du kan tilpasse en kladd.

> [!TIP]  
> Hvis du merker av for **Foreslå motkontobeløp** på linjen for den kladden i vinduet **Finanskladder**, vil deretter for eksempel **Beløp**-feltet på finanskladdelinjer for samme dokumentnummer, automatisk forhåndsutfylles med verdien som kreves for balansere dokumentet. Hvis du vil ha mer informasjon, kan du se [La [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå verdier](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Forstå hovedkonti og motkonti
Hvis du har definert standard motkonti for kladdene, vil motkontoen på siden **Finanskladder** bli fylt ut automatisk når du fyller ut **Kontonr.**-feltet. Hvis ikke, fyller du ut feltene **Kontonr.** og **Motkontonr.** manuelt. Et positivt beløp i **Beløp**-feltet debiteres hovedkontoen og krediteres motkontoen. Et negativt beløp krediteres hovedkontoen og debiteres motkontoen.

> [!NOTE]  
>   Mva beregnes separat for hovedkontoen og motkontoen, så de kan bruke ulike mva-prosentsatser.

## <a name="working-with-recurring-journals"></a>Arbeide med gjentakelseskladder
En gjentakende kladd er en finanskladd med bestemte felt for håndtering av transaksjoner du bokfører ofte, med få eller ingen endringer. Hvis du bruker disse feltene for gjentatte transaksjoner, kan du bokføre både faste og variable beløp. Du kan også angi automatiske tilbakeføringsposter for dagen etter bokføringsdatoen, og bruke fordelingsnøkler med de gjentakende postene.

## <a name="working-with-standard-journals"></a>Arbeide med standardkladder
Når du har opprettet kladdelinjer som du vet at du sannsynligvis vil opprette igjen senere, kan du lagre dem som en standardkladd før du bokfører kladden. Denne funksjonen gjelder varekladder og finanskladder.

> [!NOTE]  
>   Den følgende fremgangsmåten dreier seg om varekladden, men informasjonen gjelder også finanskladden.

### <a name="to-save-a-standard-journal"></a>Slik lagrer du som standardkladd
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varekladder**, og velg deretter den relaterte koblingen.
2. Legg inn én eller flere kladdelinjer.
3. Velg kladdelinjene du vil bruke på nytt.
4. Velg handlingen **Lagre som standardkladd**.
5. I forespørselsvinduet **Lagre som standard varekladd** definerer du en ny eller eksisterende standard varekladd som linjene skal lagres i.

    Hvis du allerede har opprettet én eller flere standard varekladder og vil erstatte en av disse med det nye settet med varekladdelinjer, velger du ønsket kode i feltet Kode.
6. Velg **OK** for å bekrefte at du vil overskrive den eksisterende standardvarekladden og erstatte alt innholdet i den.
7. Velg feltet **Lagre enhetsbeløp** hvis du vil lagre verdiene i standardvarekladdens **Enhetsbeløp**-felt.
8. Velg feltet **Lagre mengde** hvis du vil at programmet skal lagre verdiene i **Antall**-feltet.
9. Velg **OK** for å lagre standardvarekladden.

Når du har lagret standardvarekladden, vises Varekladd-vinduet slik at du kan fortsette med å bokføre den – i forvisning om at den enkelt kan gjenopprettes neste gang du har behov for å bokføre de samme eller lignende linjer.

### <a name="to-reuse-a-standard-journal"></a>Bruke en standardkladd på nytt
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Varekladder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Hent standardkladder**.

    Vinduet Standard varekladder åpnes med koder og beskrivelser for alle eksisterende standard varekladder.
3. Hvis du vil se nærmere på en standard varekladd før du velger å bruke den på nytt, velger du handlingen **Vis kladd**.

    Eventuelle endringer du gjør i en standard varekladd, implementeres umiddelbart. De vil være der neste gang du åpner eller gjenbruker den aktuelle standardvarekladden. Du må derfor være sikker på at endringen er viktig nok til å gjelde generelt. I motsatt fall gjør du den ønskede endringen i varekladden etter at linjene fra standardvarekladden er satt inn. Se trinn 4 nedenfor.
4. I vinduet **Standard varekladder** velger du den standard varekladden du vil bruke på nytt, og deretter velger du **OK**.

    Nå er varekladden fylt med linjene som var lagret som standard varekladd. Hvis det allerede finnes kladdelinjer i varekladden, plasseres de innsatte linjene under de eksisterende kladdelinjene.

    Hvis du ikke merket av for **Lagre enhetsbeløp** da du brukte funksjonsjobben **Lagre som standard varekladd**, blir **Enhetsbeløp**-feltet på linjer du satte inn fra standardkladden, fylt ut automatisk med varens gjeldende verdi, som er kopiert fra **Enhetskost**-feltet på varekortet.

    > [!NOTE]  
>   Hvis du har valgt feltet **Lagre enhetsbeløp** eller **Lagre mengde**, må du kontrollere at de innsatte verdiene er riktige for den aktuelle lagerjusteringen før du bokfører varekladden.

    Hvis de innsatte varekladdelinjene inneholder lagrede enhetsbeløp du ikke vil bokføre, kan du raskt justere verdien til gjeldende verdi for varen, som i det følgende.

6. Velg varekladdelinjene du vil justere, og velg deretter handlingen **Beregn enhetsbeløp på nytt**. Deretter oppdateres Enhetsbeløp-feltet med gjeldende enhetskost for varen.
7. Velg handlingen **Bokfør**.

## <a name="to-renumber-document-numbers-in-journals"></a>Nummerere bilagsnumre i kladder på nytt
Hvis du vil sikre at det ikke oppstår posteringsfeil på grunn av rekkefølgen på bilagsnumrene, kan du bruke funksjonen **Nummerere bilagsnumre på nytt** før du bokfører en kladd.

I alle kladdene som er basert på finanskladden, kan feltet **Bilagsnr.** redigeres, slik at du kan angi forskjellige bilagsnumre for ulike kladdelinjer eller det samme bilagsnummeret for relaterte kladdelinjer.

Hvis feltet **Nummerserie** i den satsvise jobben for kladden er fylt ut, vil deretter posteringsfunksjonen i finanskladder kreve at bilagsnummeret på individuelle eller grupperte kladdelinjene er i sekvensiell rekkefølge. Hvis du vil sikre at det ikke oppstår posteringsfeil på grunn av rekkefølgen på bilagsnumrene, kan du bruke funksjonen **Nummerere bilagsnumre på nytt** før du bokfører kladden. Hvis relaterte linjer ble gruppert etter bilagsnummer før du brukte funksjonen, forblir de gruppert, men kan tilordnes til et annet bilagsnummer.

Denne funksjonen fungerer også for filtrerte visninger.

Eventuell ny nummerering av dokumenter vil respektere relaterte programmer, for eksempel en betalingsutligning som er utført fra dokumentet på kladdelinjen til en leverandørkonto. Dette betyr at feltet **Utlignings-ID** og **Utligningsbilagsnr.** i de berørte postene kan oppdateres.

Følgende fremgangsmåte er basert på vinduet **Finanskladd**, men gjelder for alle andre kladder som er basert på finanskladden, for eksempel vinduet **Utbetalingskladd**.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.
2. Når du er klar til å bokføre kladden, velger du handlingen **Nummerer dokumentnumre på nytt**.

Verdier i feltet **Bilagsnr.** endres der det er nødvendig, slik at bilagsnummeret på individuelle eller grupperte kladdelinjer er i sekvensiell rekkefølge. Når dokumenter er nummerert på nytt, kan du fortsette å bokføre kladden.

## <a name="see-also"></a>Se også
[Bokføre transaksjoner direkte i Finans](finance-how-post-transactions-directly.md)  
[Tilbakeføre bokføringer](finance-how-reverse-journal-posting.md)  
[Fordele kostnader og inntekter](year-allocate-costs-income.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

