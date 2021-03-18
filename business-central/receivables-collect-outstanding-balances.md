---
title: Innkreve utestående saldi
description: Lær hvordan du sender en påminnelse til en kunde om en betaling som er forfalt, og legger gebyrer til betalingen på grunn av forsinkelsen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge, reminder
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8de49351f6fa81363f624c39c73d4360be440083
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5392228"
---
# <a name="collect-outstanding-balances"></a>Innkreve utestående saldi

Behandling av fordringer omfatter å kontrollere om forfalte beløp betales til riktig tid. Hvis kunder har forfalte betalinger, kan du først sende **Kontoutdrag**-rapporten som en påminnelse. Du kan eventuelt utstede purringer.

Du kan bruke purringer til å minne kunder på forfalte beløp. Du kan også bruke purringer til å beregne renter eller gebyrer og inkludere dem i purringen. Bruk rentenotaer hvis du vil debitere kunder for renter eller gebyrer uten å minne dem på forfalte beløp.

## <a name="statements"></a>Utdrag

Fra kundekortet kan du opprette et utdrag med kundens transaksjoner med deg. Deretter sender du kunden den genererte PDF-filen. Du kan også bruke **Kontoutdrag**-rapporten til å sende kundene en oversikt over forretningene med deg. Kontoutdraget kan sendes til Excel for videre behandling.  

### <a name="to-send-the-customer-statement-report"></a>Sende Kontoutdrag-rapporten

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoutdrag**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Under **Utdataalternativer** velger du hvordan du vil sende rapporten til kunden.

> [!NOTE]
> Hvis du bruker flere valutaer, skrives Kontoutdrag-rapporten alltid ut i kundens valuta. Den siste datoen i perioden brukes også som utdragsdato og datoen for aldersfordeling hvis aldersfordeling er inkludert.

## <a name="reminders"></a>Purringer

Du må definere purrebetingelser og tilordne dem til kunder før du kan opprette purringer. Hvis du vil ha mer informasjon, kan du se [Definer betingelser og grader for purringer](finance-setup-reminders.md). [!INCLUDE [reminder-terms](includes/reminder-terms.md)] Innholdet på siden **Rentenotabetingelser** fastsetter om det skal beregnes rente i purringen.  

Du kan jevnlig kjøre **Opprett purringer**-kjørselen for å opprette purringer for alle kunder med forfalte saldi, eller du kan opprette en purring manuelt for en spesifikk kunde og få linjene automatisk beregnet og utfylt.  

Du kan endre purringene etter at du har opprettet dem. Teksten som vises på starten og slutten av en purring, fastsettes av purregraden og vises i **Beskrivelse**-kolonnen. Hvis et beregnet beløp er satt inn automatisk i start- eller slutteksten, vil ikke teksten bli justert hvis du sletter linjer. Deretter må du bruker **Oppdater purring**-funksjonen.  

En kundepost med avmerking for **Avvent** vil ikke starte noen purreoppretting. Men hvis det opprettes en purring på grunnlag av en annen post, vil en forfalt post som er merket med Avvent, også bli inkludert i purringen. Rente beregnes ikke for linjer med disse postene.

Når du har opprettet purringer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede purringene, vanligvis via e-post.

### <a name="to-create-a-reminder-automatically"></a>Slik oppretter du en purring automatisk

En purring fungerer på samme måte som en faktura. Når du oppretter en purring, må du fylle ut et purrehode samt én eller flere purrelinjer. Du kan bruke en funksjon til å opprette purringer for alle kunder automatisk.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. På siden **Purring** velger du handlingen **Opprett purringer**.
3. På siden **Opprett purringer** fyller du ut feltene for å definere hvordan og for hvem purringene skal opprettes.
4. Velg **OK**.

### <a name="to-create-a-reminder-manually"></a>Slik oppretter du en purring manuelt

På siden **Purring** kan du fylle ut hurtigfanen **Generelt** manuelt og deretter fylle ut linjene automatisk.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
4. Velg handlingen **Foreslå purrelinjer**.
5. I vinduet **Opprett purringer** fyller du ut feltene for å definere hvordan og for hvem purringene skal opprettes.
6. Merk av for **Ta med avventende poster** hvis du vil at purringen skal bestå av forfalte åpne poster som er avventende.
7. Merk av for **Bare poster med forfalte beløp** hvis du vil at purringen skal bestå av bare forfalte åpne poster. Bare fakturaer og betalinger vil vises siden dette er postene som kundenes betalinger kan forfalt til.

    > [!Important]
    > Åpne poster som er på vent, settes inn, uavhengig av innstillingen i avmerkingsboksen **Bare poster med forfalte beløp**.

8. Velg **OK**.

### <a name="to-replace-reminder-texts"></a>Slik erstatter du purretekst

Du kan angi teksten som vises i purringsutskrifter på flere måter. Av og til vil du kanskje erstatte start- og slutteksten som er angitt for den gjeldende purregraden, men tekst fra en annen grad.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. Åpne den aktuelle purringen, og velg deretter handlingen **Oppdater purretekst**.
3. Angi ønsket grad i feltet **Purregrad** på siden **Oppdater purretekst**.
4. Velg **OK** for å oppdatere start- og slutteksten.

### <a name="to-issue-a-reminder"></a>Utstede en purring

Når du har opprettet purringer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede purringene.

Når du utsteder en purring, overføres dataene til en separat side for utstedte purringer. Samtidig bokføres purrepostene. Hvis rente eller tilleggsgebyr er beregnet, bokføres poster til kundeposten og Finans.

Når en purring er utstedt, bokføres postene i henhold til dine spesifikasjoner på siden **Purrebetingelser**. Denne spesifikasjonen angir om renter og/eller tilleggsgebyrer skal bokføres på kundens konto og i Finans. Oppsettet på siden **Bokføringsgrupper - kunde** angir hvilke konti det skal bokføres på.

For hver kundepost i rentenotaen opprettes det en post på siden **Purre-/renteposter**.

Hvis det er merket av for **Bokfør rente** eller **Bokfør tilleggsgebyr** på siden **Purrebetingelser**, opprettes også følgende poster:

- Én post på siden **Kundeposter**
- Én post for utestående på relevant finanskonto
- Én post for rente og/eller én post for tilleggsgebyr på relevant finanskonto

I tillegg kan utstedelsen av purringen resultere i mva-poster.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Purringer**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle purringen, og velg deretter handlingen **Utsted**.
3. På siden **Utsted purringer** fyller du ut feltene etter behov.
4. Velg **OK**.

Purringen blir enten skrevet ut eller sendt til en bestemt e-postadresse som et PDF-vedlegg.

### <a name="to-cancel-an-issued-reminder"></a>Avbryte den utstedte purringen

Hvis påminnelser ble utstedt med en feil, kan du annullere dem før de sendes ut. Du kan gjøre dette enten én om gangen eller som en bunke.

1. På siden **Utstedte purringer** velger du én eller flere linjer for de utstedte purringene du vil avbryte, og deretter velger du handlingen **Avbryt**.
2. På siden **Avbryt utstedte purringer** fyller du ut feltene etter behov, og deretter velger du **OK**.

## <a name="finance-charges"></a>Renter

Når en kunde ikke betaler innen forfallsdatoen, kan du beregne renter automatisk og legge dem til de forfalte beløpene på kundekontoen. Du kan informere kunder om tilleggsgebyr ved å sende rentenotaer.  

> [!NOTE]  
> Du bruker rentenotaer til å beregne renter samt informere kundene om renter uten å minne dem på forfalte betalinger. Du kan også beregne rente på forfalte betalinger når du oppretter purringer.  

Før du kan opprette rentenotaer, må du definere betingelser. Hvis du vil ha mer informasjon, kan du se [Definer rentenotabetingelser](finance-setup-finance-charges.md).  

Du kan opprette en rentenota for en individuell kunde manuelt og deretter fylle ut linjene automatisk. Du kan også bruke funksjonsjobben **Opprett rentenotaer** til å opprette rentenotaer for alle eller utvalgte kunder med forfalte saldi.  

Du kan endre rentenotaene etter at du har opprettet dem. Teksten som vises på starten og slutten av rentenotaen, fastsettes av rentebetingelsene og vises i **Beskrivelse**-kolonnen på linjene. Hvis et beregnet beløp er satt inn automatisk i start- eller slutteksten, vil ikke teksten bli justert hvis du sletter linjer. Deretter må du bruker funksjonen **Oppdater rentenotatekst**.  

Når du har opprettet rentenotaer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede rentenotaene, vanligvis via e-post.

### <a name="to-create-a-finance-charge-memo-manually"></a>Slik oppretter du en rentenota manuelt

Rentenotaer fungerer på samme måte som fakturaer. Du kan fylle ut hodet manuelt og angi at linjene skal fylles ut automatisk, eller du kan angi at det automatisk skal opprettes rentenotaer for alle kunder.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov.  
3. Velg handlingen **Foreslå rentenotalinjer**.
4. På siden **Foreslå rentenotalinjer** angir du et filter på hurtigfanen **Kundepost** hvis du vil opprette rentenotaer bare for bestemte poster.

    > [!NOTE]
    > Selv om de er oppført, vil valg av **Betaling** og **Kreditnota** som **Dokumenttype**-filtre ikke ha noen virkning fordi funksjonen **Foreslå rentenotalinjer** bare behandler positive beløp.
5.  Velg **OK** for å starte kjørselen.  

### <a name="to-update-finance-charge-memo-texts"></a>Slik oppdaterer du rentenotatekst  
Av og til vil du kanskje endre start- og slutteksten som du har definert for rentenotabetingelsene. Hvis du gjør dette etter at du har opprettet, men ikke utstedt rentenotaer, kan du angi at notaene skal oppdateres med den endrede teksten.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenota**, og velg deretter den relaterte koblingen.  
2. Åpne rentenotaen du vil endre teksten for, og velg deretter handlingen **Oppdater rentenotatekst**.
3. På siden **Oppdater rentenotatekst** kan du angi et filter hvis du vil oppdatere flere notaer.
4. Velg **OK** for å oppdatere start- og slutteksten.  

### <a name="to-issue-finance-charge-memos"></a>Utstede rentenotaer
Når du har opprettet rentenotaer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede rentenotaene.

Når en purring er utstedt, bokføres postene i henhold til dine spesifikasjoner på siden **Rentenotabetingelser**. Denne spesifikasjonen angir om renter og/eller tilleggsgebyrer skal bokføres på kundens konto og i Finans. Oppsettet på siden **Bokføringsgrupper - kunde** angir hvilke konti det skal bokføres på.

For hver kundepost i rentenotaen opprettes det en post på siden **Purre-/renteposter**.

Hvis det er merket av for **Bokfør rente** eller **Bokfør tilleggsgebyr** på siden **Rentenotabetingelser**, opprettes også følgende poster:

- Én post på siden **Avventende kundeposter**
- Én post for utestående på relevant finanskonto
- Én post for rente og/eller én post for tilleggsgebyr på relevant finanskonto

I tillegg kan utstedelsen av rentenotaen resultere i mva-poster.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rentenotaer**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle notaen, og velg deretter handlingen **Utsted**.
3. På siden **Utsted rentenotaer** fyller du ut feltene etter behov.
4. Velg **OK**.

Rentenotaen blir enten skrevet ut eller sendt til en bestemt e-postadresse som et PDF-vedlegg.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Avbryte den utstedte rentenotaen.
Hvis rentenotaer ble utstedt med en feil, kan du annullere dem før de sendes ut. Du kan gjøre dette enten én om gangen eller som en bunke.
1. På siden **Utstedte rentenotaer** velger du én eller flere linjer for de utstedte rentenotaene du vil avbryte, og deretter velger du handlingen **Avbryt**.
2. På siden **Avbryt utstedte rentenotaer** fyller du ut feltene etter behov, og deretter velger du **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Slik viser du purre- og renteposter  
Når du utsteder en purring, opprettes en purrepost på siden **Purre-/renteposter** for hver purrelinje som inneholder en kundepost. Du kan deretter få en oversikt over hvilke purreposter som er opprettet for en bestemt kunde.    
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.  
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Poster**.
3. På siden **Kundeposter** velger du linjen med posten du vil se purrepostene for, og deretter velger du handlingen **Purre-/renteposter**.

## <a name="multiple-interest-rates"></a>Flere rentesatser

Når du definerer rentenotabetingelser og purrebetingelser for straff for forsinket betaling, kan du angi flere rentesatser slik at straffegebyret beregnes fra forskjellige renter i forskjellige perioder. Hvis flere rentesatser ikke er satt opp, brukes rentesatsen og perioden som er definert på sidene **Rentenotabetingelser** og **Purrebetingelser** for hele perioden i beregningen. Hvis du vil ha mer informasjon, kan du se [Angi flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/process-financial-periodic-activities-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Definer betingelser og grader for purringer](finance-setup-reminders.md)  
[Definer rentenotabetingelser](finance-setup-finance-charges.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]