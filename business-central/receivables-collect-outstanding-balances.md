---
title: Innkrev utestående saldoer
description: 'Finn ut hvordan du kan minne kundene på utestående betalinger. Send et kundeutdrag, utstede en purring eller send en rentenota.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'payment due, debt, overdue, fee, charge, reminder'
ms.search.form: '6, 25, 440, 443, 448, 452'
ms.date: 07/01/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="collect-outstanding-balances"></a>Innkrev utestående saldoer

Behandling av fordringer omfatter å kontrollere om forfalte beløp betales til riktig tid. Hvis kunder har forfalte betalinger, kan du først sende **Kontoutdrag**-rapporten som en påminnelse. Du kan eventuelt utstede purringer.

Bruk purringer til å varsle kunder om forfalte beløp. Du kan også bruke purringer til å beregne renter eller gebyrer og inkludere dem i purringen. Bruk rentenotaer hvis du vil debitere kunder for renter eller gebyrer uten å minne dem på forfalte beløp.

## <a name="statements"></a>Utdag

Fra kundekortet kan du opprette et utdrag over kundens transaksjoner med deg. Deretter kan du generere en PDF-fil og sende den til kunden. Du kan også bruke **Kontoutdrag**-rapporten til å sende kundene en oversikt over forretningene med deg. 

> [!TIP]
> Om nødvendig kan du sende utdraget til Excel for å gjøre endringer.  

### <a name="to-send-the-customer-statement-report"></a>Sende Kontoutdrag-rapporten

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 10.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontoutdrag** og velg den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Under **Utdataalternativer** velger du hvordan du vil sende rapporten til kunden.

> [!NOTE]
> Hvis du bruker flere valutaer, skrives Kontoutdrag-rapporten alltid ut i kundens valuta. Den siste datoen i perioden brukes også som utdragsdato og datoen for aldersfordeling hvis aldersfordeling er inkludert.

## <a name="reminders"></a>Purringer

[!INCLUDE [receivables-reminders](includes/receivables-reminders.md)]

## <a name="finance-charges"></a>Renter

Når en kunde ikke betaler innen forfallsdatoen, kan du beregne renter automatisk og legge dem til de forfalte beløpene på kundens konto. Du kan informere kunder om tilleggsgebyr ved å sende rentenotaer.  

> [!NOTE]  
> Du bruker rentenotaer til å beregne renter samt informere kundene om renter uten å minne dem på forfalte betalinger. Du kan også beregne rente på forfalte betalinger når du oppretter purringer.  

Før du kan opprette rentenotaer, må du definere betingelser. Hvis du vil ha mer informasjon, kan du se [Definer rentenotabetingelser](finance-setup-finance-charges.md).  

Du kan opprette en rentenota for en individuell kunde manuelt og deretter fylle ut linjene automatisk. Du kan også bruke funksjonen **Opprett rentenotaer** til å opprette rentenotaer for alle eller utvalgte kunder med forfalte saldi.  

Du kan endre rentenotaene etter at du har opprettet dem. Teksten som vises på starten og slutten av rentenotaen, fastsettes av rentebetingelsene og vises i **Beskrivelse**-kolonnen på linjene. Hvis et beregnet beløp er satt inn automatisk i start- eller sluttteksten, justeres ikke teksten hvis du sletter linjer. Deretter må du bruker funksjonen **Oppdater rentenotatekst**.  

Når du har opprettet rentenotaer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede rentenotaene, vanligvis via e-post.

### <a name="to-create-a-finance-charge-memo-manually"></a>Slik oppretter du en rentenota manuelt

Rentenotaer fungerer på samme måte som fakturaer. Du kan fylle ut hodet manuelt og angi at linjene skal fylles ut automatisk, eller du kan angi at det automatisk skal opprettes rentenotaer for alle kunder.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rentenotaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**, og fyll deretter ut feltene etter behov.  
3. Velg handlingen **Foreslå rentenotalinjer**.
4. På siden **Foreslå rentenotalinjer** angir du et filter på hurtigfanen **Kundepost** hvis du vil opprette rentenotaer bare for bestemte poster.

    > [!NOTE]
    > Selv om de er oppført, vil valg av **Betaling** og **Kreditnota** som **Dokumenttype**-filtre ikke ha noen virkning fordi funksjonen **Foreslå rentenotalinjer** bare behandler positive beløp.
5. Velg **OK** for å starte kjørselen.  

### <a name="to-update-finance-charge-memo-texts"></a>Slik oppdaterer du rentenotatekst

I noen tilfeller vil du kanskje endre start- og slutteksten som du har definert for rentenotabetingelsene. Hvis du gjør dette etter at du har opprettet, men ikke utstedt rentenotaer, kan du angi at notaene skal oppdateres med den endrede teksten.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rentenota**, og velg deretter den relaterte koblingen.  
2. Åpne rentenotaen du vil endre teksten for, og velg deretter handlingen **Oppdater rentenotatekst**.
3. På siden **Oppdater rentenotatekst** kan du angi et filter hvis du vil oppdatere flere notaer.
4. Velg **OK** for å oppdatere start- og slutteksten.  

### <a name="to-issue-finance-charge-memos"></a>Utstede rentenotaer

Når du har opprettet rentenotaer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede rentenotaene.

Når du utsteder en purring, bokføres postene i henhold til dine spesifikasjoner på siden **Rentenotabetingelser**. Denne spesifikasjonen angir om renter og/eller tilleggsgebyrer skal bokføres på kundens konto og i Finans. Innstillingene på siden **Bokføringsgrupper – kunde** bestemmer hvilke konti renter eller gebyrer bokføres på.

For hver kundepost i rentenotaen opprettes det en post på siden **Purre-/renteposter**.

Hvis det er merket av for **Bokfør rente** eller **Bokfør tilleggsgebyr** på siden **Rentenotabetingelser**, opprettes også følgende poster:

- Én post på siden **Avventende kundeposter**
- Én post for utestående på relevant finanskonto
- Én post for rente og/eller én post for tilleggsgebyr på relevant finanskonto

I tillegg kan utstedelsen av rentenotaen resultere i mva-poster.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rentenotaer**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle notaen, og velg deretter handlingen **Utsted**.
3. På siden **Utsted rentenotaer** fyller du ut feltene etter behov.
4. Velg **OK**.

Rentenotaen skrives ut for sendt til en angitt e-post som PDF-vedlegg.

### <a name="to-cancel-an-issued-finance-charge-memo"></a>Avbryte den utstedte rentenotaen.

Hvis rentenotaer ble utstedt ved en feiltakelse, kan du annullere dem før de sendes ut på nytt. Du kan gjøre dette enten en etter en eller som en batch.

1. På siden **Utstedte rentenotaer** velger du én eller flere linjer for de utstedte rentenotaene du vil avbryte, og deretter velger du handlingen **Avbryt**.
2. På siden **Avbryt utstedte rentenotaer** fyller du ut feltene etter behov, og deretter velger du **OK**.

### <a name="to-view-reminder-and-finance-charge-entries"></a>Slik viser du purre- og renteposter

Når du utsteder en purring, opprettes en purrepost på siden **Purre-/renteposter** for hver purrelinje som inneholder en kundepost. Du kan deretter få en oversikt over hvilke purreposter som er opprettet for en bestemt kunde.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 5.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.  
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Poster**.
3. På siden **Kundeposter** velger du linjen med posten du vil se purrepostene for, og deretter velger du handlingen **Purre-/renteposter**.

## <a name="multiple-interest-rates"></a>Flere rentesatser

[!INCLUDE [multiple-interest-rates-def](includes/multiple-interest-rates-def.md)] Hvis du vil ha mer informasjon, kan du se [Angi flere rentesatser](finance-how-to-set-up-multiple-interest-rates.md).  

## <a name="see-also"></a>Se også

[Konfigurer påminnelsesbetingelser og -nivåer](finance-setup-reminders.md)  
[Konfigurer rentenotabetingelser](finance-setup-finance-charges.md)  
[Håndtere fordringer](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
