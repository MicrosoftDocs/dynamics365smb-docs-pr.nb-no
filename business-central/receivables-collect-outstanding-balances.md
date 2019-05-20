---
title: Minne kunder på forfalte betalinger eller bøtelegge dem | Microsoft-dokumentasjon
description: Beskriver hvordan du sender en påminnelse til en kunde om en betaling som er forfalt, og legger gebyrer til betalingen på grunn av forsinkelsen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: a39e43a430720c0453ba5bd9bccf864237b8ae6f
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252760"
---
# <a name="collect-outstanding-balances"></a>Innkreve utestående saldi
Behandling av fordringer omfatter å kontrollere om forfalte beløp betales til riktig tid. Hvis kunder har forfalte betalinger, kan du først sende Kontoutdrag-rapporten som en påminnelse. Du kan eventuelt utstede purringer.

Du kan bruke purringer til å minne kunder på forfalte beløp. Du kan også bruke purringer til å beregne renter eller gebyrer og inkludere dem i purringen. Bruk rentenotaer hvis du vil debitere kunder for renter eller gebyrer uten å minne dem på forfalte beløp.

## <a name="reminders"></a>Purringer
Du må definere purrebetingelser og tilordne dem til kunder før du kan opprette purringer. Hver purrebetingelse har forhåndsdefinerte purregrader. Hver purregrad inkluderer en regel om når purringen skal utstedes, for eksempel hvor mange dager etter fakturaens forfallsdato eller etter datoen for forrige purring. Innholdet på siden **Rentenotabetingelser** fastsetter om det skal beregnes rente i purringen.  

Du kan jevnlig kjøre **Opprett purringer**-kjørselen for å opprette purringer for alle kunder med forfalte saldi, eller du kan opprette en purring manuelt for en spesifikk kunde og få linjene automatisk beregnet og utfylt.  

Du kan endre purringene etter at du har opprettet dem. Teksten som vises på starten og slutten av en purring, fastsettes av purregraden og vises i **Beskrivelse**-kolonnen. Hvis et beregnet beløp er satt inn automatisk i start- eller slutteksten, vil ikke teksten bli justert hvis du sletter linjer. Deretter må du bruker **Oppdater purring**-funksjonen.  

En kundepost med avmerking for **Avvent** vil ikke starte noen purreoppretting. Men hvis det opprettes en purring på grunnlag av en annen post, vil en forfalt post som er merket med Avvent, også bli inkludert i purringen. Rente beregnes ikke for linjer med disse postene.

Når du har opprettet purringer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede purringene, vanligvis via e-post.

## <a name="finance-charges"></a>Renter
Når en kunde ikke betaler innen forfallsdatoen, kan du beregne renter automatisk og legge dem til de forfalte beløpene på kundekontoen. Du kan informere kunder om tilleggsgebyr ved å sende rentenotaer.  

> [!NOTE]  
> Du bruker rentenotaer til å beregne renter samt informere kundene om renter uten å minne dem på forfalte betalinger. Du kan også beregne rente på forfalte betalinger når du oppretter purringer.  

Du kan opprette en rentenota for en individuell kunde manuelt og deretter fylle ut linjene automatisk. Du kan også bruke funksjonsjobben **Opprett rentenotaer** til å opprette rentenotaer for alle eller utvalgte kunder med forfalte saldi.  

Du kan endre rentenotaene etter at du har opprettet dem. Teksten som vises på starten og slutten av rentenotaen, fastsettes av rentebetingelsene og vises i **Beskrivelse**-kolonnen på linjene. Hvis et beregnet beløp er satt inn automatisk i start- eller slutteksten, vil ikke teksten bli justert hvis du sletter linjer. Deretter må du bruker funksjonen **Oppdater rentenotatekst**.  

Når du har opprettet rentenotaer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede rentenotaene, vanligvis via e-post.

## <a name="multiple-interest-rates"></a>Flere rentesatser
Når du definerer rentenotabetingelser og purrebetingelser for straff for forsinket betaling, kan du angi flere rentesatser slik at straffegebyret beregnes fra forskjellige renter i forskjellige perioder. Hvis flere rentesatser ikke er satt opp, brukes rentesatsen og perioden som er definert på sidene **Rentenotabetingelser** og **Purrebetingelser** for hele perioden i beregningen. Hvis du vil ha mer informasjon, kan du se [Angi flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="to-send-the-customer-statement-report"></a>Sende Kontoutdrag-rapporten
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoutdrag**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Under **Utdataalternativer** velger du hvordan du vil sende rapporten til kunden.

> [!NOTE]  
>   Hvis du bruker flere valutaer, skrives Kontoutdrag-rapporten alltid ut i kundens valuta. Den siste datoen i perioden brukes også som utdragsdato og datoen for aldersfordeling hvis aldersfordeling er inkludert.

## <a name="to-set-up-reminder-terms"></a>Slik definerer du purrebetingelser
Hvis kunder har forfalte betalinger, må du angi når og hvordan du vil sende purring. I tillegg vil du kanskje belaste kundekontiene med renter eller gebyr. Du kan opprette så mange purrebetingelser du vil. For hver purrebetingelseskode kan du definere et ubegrenset antall purregrader.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purrebetingelser**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.  
3. Hvis du vil bruke flere kombinasjoner av purrebetingelser, definerer du en kode for hver kombinasjon.

## <a name="to-set-up-reminder-levels"></a>Slik definerer du purregrader
Innstillingen fra grad 1 brukes første gang det opprettes en purring for en kunde. Når purringen utstedes, registreres gradnummeret i purrepostene som opprettes og kobles til de individuelle kundepostene. Hvis det er nødvendig å sende kunden en ny purring, kontrolleres alle purreposter som er koblet til åpne kundeposter, for å finne det høyeste gradnummeret. Betingelsene fra neste gradnummer vil deretter bli brukt i den nye purringen.

Hvis du oppretter flere purringer enn du har definert grader for, brukes betingelsene for den høyeste graden. Du kan opprette så mange purringer som er tillatt i henhold til feltet **Høyeste purregrad** i purrebetingelsene.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purrebetingelser**, og velg deretter den relaterte koblingen.  
2. På siden **Purrebetingelser** velger du linjen med betingelsene du vil definere grader for, og deretter velger du **Grader**.  
3. Fyll ut feltene etter behov.  

    For hver purregrad kan du spesifisere individuelle betingelser, som kan inkludere tilleggsgebyrer både i NOK og i utenlandsk valuta. Du kan definere mange tilleggsgebyr i fremmed valuta for hver kode på siden **Purregrad**.
4. Velg handlingen **Valutaer**.
5. På siden **Valutaer for purregrad** definerer du en valutakode og et tilleggsgebyr for hver purregradskode og tilhørende purregradsnummer.

    > [!NOTE]  
    > Når du oppretter purringer i en fremmed valuta, brukes betingelsene for den fremmede valutaen du definerer her, til å opprette purringer. Hvis det ikke er definert noen betingelser for purringer i fremmed valuta, brukes purrebetingelsene for NOK som er definert på siden **Purregrader**, og deretter konverteres de til den relevante valutaen.

    For hver purregrad kan du spesifisere tekst som skal skrives ut før (**Starttekst**) eller etter (**Sluttekst**), i postene i purringen.

6. Velg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og fyll ut **Purretekst**-siden.
7. Hvis du vil sette inn beslektede verdier automatisk i den resulterende purreteksten, angir du plassholderne nedenfor i **Tekst** feltet.  

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

Hvis du for eksempel skriver **Du skylder %9 %7, som forfaller den %2.**, vil den resulterende påminnelsen inneholde følgende tekst: **Du skylder 1 200,50 NOK, som forfaller 02-02-2014.**

> [!NOTE]
> Forfallsdatoen beregnes i henhold til datoformelen som du angir. Hvis du vil ha mer informasjon, kan du se [Bruke datoformler](ui-enter-date-ranges.md#using-date-formulas).

Når du har definert purrebetingelsene (med tilleggsgrader og tekst), registrerer du én av kodene på hvert kundekort. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).

## <a name="to-create-a-reminder-automatically"></a>Slik oppretter du en purring automatisk
En purring fungerer på samme måte som en faktura. Når du oppretter en purring, må du fylle ut et purrehode samt én eller flere purrelinjer. Du kan bruke en funksjon til å opprette purringer for alle kunder automatisk.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. På siden **Purring** velger du handlingen **Opprett purringer**.
3. På siden **Opprett purringer** fyller du ut feltene for å definere hvordan og for hvem purringene skal opprettes.
4. Velg **OK**.

## <a name="to-create-a-reminder-manually"></a>Slik oppretter du en purring manuelt
På siden **Purring** kan du fylle ut hurtigfanen **Generelt** manuelt og deretter fylle ut linjene automatisk.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
4. Velg handlingen **Foreslå purrelinjer**.
5. I vinduet **Opprett purringer** fyller du ut feltene for å definere hvordan og for hvem purringene skal opprettes.
6. Merk av for **Ta med avventende poster** hvis du vil at purringen skal bestå av forfalte åpne poster som er avventende.

    > [!Important]
    > Åpne poster som er på vent, settes inn, uavhengig av innstillingen i avmerkingsboksen Bare poster med forfalte beløp.

7. Velg **OK**.

## <a name="to-replace-reminder-texts"></a>Slik erstatter du purretekst  
Du kan angi teksten som vises i purringsutskrifter på flere måter. Av og til vil du kanskje erstatte start- og slutteksten som er angitt for den gjeldende purregraden, men tekst fra en annen grad.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. Åpne den aktuelle purringen, og velg deretter handlingen **Oppdater purretekst**.
3. Angi ønsket grad i feltet **Purregrad** på siden **Oppdater purretekst**.
3. Velg **OK** for å oppdatere start- og slutteksten.

## <a name="to-issue-a-reminder"></a>Utstede en purring
Når du har opprettet purringer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede purringene.

Når du utsteder en purring, overføres dataene til en separat side for utstedte purringer. Samtidig bokføres purrepostene. Hvis rente eller tilleggsgebyr er beregnet, bokføres poster til kundeposten og Finans.

Når en purring er utstedt, bokføres postene i henhold til dine spesifikasjoner på siden **Purrebetingelser**. Denne spesifikasjonen angir om renter og/eller tilleggsgebyrer skal bokføres på kundens konto og i Finans. Oppsettet på siden **Bokføringsgrupper - kunde** angir hvilke konti det skal bokføres på.

For hver kundepost i rentenotaen opprettes det en post på siden **Purre-/renteposter**.

Hvis det er merket av for **Bokfør rente** eller **Bokfør tilleggsgebyr** på siden **Purrebetingelser**, opprettes også følgende poster:

- Én post på siden **Avventende kundeposter**
- Én post for utestående på relevant finanskonto
- Én post for rente og/eller én post for tilleggsgebyr på relevant finanskonto

I tillegg kan utstedelsen av purringen resultere i mva-poster.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle purringen, og velg deretter handlingen **Utsted**.
3. På siden **Utsted purringer** fyller du ut feltene etter behov.
4. Velg **OK**.

Purringen blir enten skrevet ut eller sendt til en bestemt e-postadresse som et PDF-vedlegg.

## <a name="to-set-up-finance-charge-terms"></a>Definere rentenotabetingelser
Du definerer en kode som representerer de ulike måtene du vil at programmet skal beregne renter på. Deretter kan du angi denne koden i feltet **Rentenotabetingelseskode** på kunde- eller leverandørkort.

Renter kan beregnes ved hjelp av enten gjennomsnittlig dagssaldo eller forfalt beløp.

* Forfalt saldo-metode

    Rentegebyret er ganske enkelt en prosent av forfalt beløp:  
    *Forfalt saldo-metode* - *Rente* = *Forfalt beløp* x *(Rentesats / 100)*

*   Gjennomsnittlig daglig saldo-metode

    Det er tatt hensyn til hvor mange dager betalingen er forsinketl:  
    *Metoden Gjennomsnittlig daglig saldo* - *Rente* = *Forfalt beløp* x *(Dager forfalt / Renteperiode)* x *(Rentesats / 100)*

I tillegg er hver kode i tabellen Rentenotatekst knyttet til en undertabell, tabellen Rentenotatekst. For hver rentebetingelse kan du definere en start- og/eller slutt-tekst som kommer ut på rentenotaen.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotabetingelser**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.  
3. Hvis du vil bruke flere kombinasjoner av rentebetingelser, definerer du en kode for hver kombinasjon.

    For hver rentebetingelse kan du spesifisere individuelle betingelser, som kan inkludere tilleggsgebyrer både i NOK og i utenlandsk valuta. Du kan definere mange tilleggsgebyrer i fremmed valuta for hver kode på siden **Rentenotabetingelser**.
4. Velg handlingen **Valutaer**.
5. På siden **Valuta for rentenotabeting.** definerer du en valutakode og et tilleggsgebyr for hver betingelse.

    > [!NOTE]  
    > Når du oppretter renter i en utenlandsk valuta, brukes betingelsene for utenlandsk valuta du definerer her, til å opprette rentenotaer. Hvis det ikke er definert noen betingelser for rentenotaer i utenlandsk valuta, brukes rentenotabetingelsene for NOK som er definert på siden **Rentenotabetingelser**, og deretter konverteres de til den relevante valutaen.

    For hver rentenotabetingelse kan du angi tekst som skal skrives ut før (**Starttekst**) eller etter (**Sluttekst**), i postene i rentenotaen.  
6. Velg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og fyll ut siden **Rentenotatekst**.
7. Hvis du vil sette inn relaterte verdier automatisk i den resulterende rentenotateksten, angir du plassholderne nedenfor i **Tekst**-feltet.

|Plassholder|Verdi|  
|-----------------|-----------|  
|%1|Innholdet i **Bilagsdato**-feltet i rentenotahodet|  
|%2|Innholdet i **Forfallsdato**-feltet i rentenotahodet|  
|%3|Innholdet i feltet **Rentesats** på de relaterte rentenotabetingelsene|  
|%4|Innholdet i **Restbeløp**-feltet i rentenotahodet|  
|%5|Innholdet i **Rentebeløp**-feltet i rentenotahodet|  
|%6|Innholdet i **Tilleggsgebyr**-feltet i rentenotahodet|  
|%7|Purringens totalbeløp|  
|%8|Innholdet i **Valutakode**-feltet i rentenotahodet|  
|%9|Innholdet i **Bokføringsdato**-feltet i rentenotahodet|  

## <a name="to-create-a-finance-charge-memo-manually"></a>Slik oppretter du en rentenota manuelt  
Rentenotaer fungerer på samme måte som fakturaer. Du kan fylle ut hodet manuelt og angi at linjene skal fylles ut automatisk, eller du kan angi at det automatisk skal opprettes rentenotaer for alle kunder.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov.  
3. Velg handlingen **Foreslå rentenotalinjer**.
4. På siden **Foreslå rentenotalinjer** angir du et filter på hurtigfanen **Kundepost** hvis du vil opprette rentenotaer bare for bestemte poster.  
5.  Velg **OK** hvis du vil starte kjørselen.  

## <a name="to-update-finance-charge-memo-texts"></a>Slik oppdaterer du rentenotatekst  
Av og til vil du kanskje endre start- og slutteksten som du har definert for rentenotabetingelsene. Hvis du gjør dette etter at du har opprettet, men ikke utstedt rentenotaer, kan du angi at notaene skal oppdateres med den endrede teksten.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenota**, og velg deretter den relaterte koblingen.  
2. Åpne rentenotaen du vil endre teksten for, og velg deretter handlingen **Oppdater rentenotatekst**.
3. På siden **Oppdater rentenotatekst** kan du angi et filter hvis du vil oppdatere flere notaer.
4. Velg **OK** for å oppdatere start- og slutteksten.  

## <a name="to-issue-finance-charge-memos"></a>Utstede rentenotaer
Når du har opprettet rentenotaer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede rentenotaene.

Når en purring er utstedt, bokføres postene i henhold til dine spesifikasjoner på siden **Rentenotabetingelser**. Denne spesifikasjonen angir om renter og/eller tilleggsgebyrer skal bokføres på kundens konto og i Finans. Oppsettet på siden **Bokføringsgrupper - kunde** angir hvilke konti det skal bokføres på.

For hver kundepost i rentenotaen opprettes det en post på siden **Purre-/renteposter**.

Hvis det er merket av for **Bokfør rente** eller **Bokfør tilleggsgebyr** på siden **Rentenotabetingelser**, opprettes også følgende poster:

- Én post på siden **Avventende kundeposter**
- Én post for utestående på relevant finanskonto
- Én post for rente og/eller én post for tilleggsgebyr på relevant finanskonto

I tillegg kan utstedelsen av rentenotaen resultere i mva-poster.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotaer**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle notaen, og velg deretter handlingen **Utsted**.
3. På siden **Utsted rentenotaer** fyller du ut feltene etter behov.
4. Velg **OK**.

Rentenotaen blir enten skrevet ut eller sendt til en bestemt e-postadresse som et PDF-vedlegg.

## <a name="to-view-reminder-and-finance-charge-entries"></a>Slik viser du purre- og renteposter  
Når du utsteder en purring, opprettes en purrepost på siden **Purre-/renteposter** for hver purrelinje som inneholder en kundepost. Du kan deretter få en oversikt over hvilke purreposter som er opprettet for en bestemt kunde.    
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kunder**, og velg deretter den relaterte koblingen.  
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Poster**.
3. På siden **Kundeposter** velger du linjen med posten du vil se purrepostene for, og deretter velger du handlingen **Purre-/renteposter**.

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
