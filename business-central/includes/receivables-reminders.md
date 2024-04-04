---
author: brentholtorf
ms.topic: include
ms.date: 02/09/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
Du kan bruke purringer til å minne kunder på forfalte beløp. Du kan også bruke purringer til å beregne renter eller gebyrer og inkludere dem i purringen.

Du må definere purrebetingelser og tilordne dem til kunder før du kan opprette purringer. Hvis du vil ha mer informasjon, kan du se [Definer betingelser og grader for purringer](../finance-setup-reminders.md). [!INCLUDE [reminder-terms](reminder-terms.md)] Innholdet på siden **Rentenotabetingelser** fastsetter om det skal beregnes rente i purringen.  

Du kan jevnlig kjøre **Opprett purringer**-kjørselen for å opprette purringer for alle kunder med forfalte saldi, eller du kan opprette en purring manuelt for en spesifikk kunde og få linjene automatisk beregnet og utfylt.  

Du kan endre purringene etter at du har opprettet dem. Teksten som vises på starten og slutten av en purring, fastsettes av purregraden og vises i **Beskrivelse**-kolonnen. Hvis et beregnet beløp er satt inn automatisk i start- eller slutteksten, vil ikke teksten bli justert hvis du sletter linjer. Deretter må du bruker **Oppdater purring**-funksjonen.  

En kundepost med avmerking for **Avvent** vil ikke starte noen purreoppretting. Men hvis det opprettes en purring på grunnlag av en annen post, vil en forfalt post som er merket med Avvent, også bli inkludert i purringen. Rente beregnes ikke for linjer med disse postene.

Når du har opprettet purringer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede purringene, vanligvis via e-post.

### Slik oppretter du en purring automatisk

En purring fungerer på samme måte som en faktura. Når du oppretter en purring, må du fylle ut et purrehode samt én eller flere purrelinjer. Du kan bruke en funksjon til å opprette purringer for alle kunder automatisk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 0.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Purringer**, og velg deretter den relaterte koblingen.
2. På siden **Purring** velger du handlingen **Opprett purringer**.
3. På siden **Opprett purringer** fyller du ut feltene for å definere hvordan og for hvem purringene skal opprettes.
4. Velg **OK**.

### Slik oppretter du en purring manuelt

På siden **Purring** kan du fylle ut hurtigfanen **Generelt** manuelt og deretter fylle ut linjene automatisk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg igjen 2.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Purringer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
4. Velg handlingen **Foreslå purrelinjer**.
5. I vinduet **Opprett purringer** fyller du ut feltene for å definere hvordan og for hvem purringene skal opprettes.
6. Merk av for **Ta med avventende poster** hvis du vil at purringen skal bestå av forfalte åpne poster som er avventende.
7. Merk av for **Bare poster med forfalte beløp** hvis du vil at purringen skal bestå av bare forfalte åpne poster. Bare fakturaer og betalinger vil vises siden dette er postene som kundenes betalinger kan forfalt til.

    > [!Important]
    > Åpne poster som er på vent, settes inn, uavhengig av innstillingen i avmerkingsboksen **Bare poster med forfalte beløp**.

8. Velg **OK**.

### Slik erstatter du purretekst

Du kan angi teksten som vises i purringsutskrifter på flere måter. Av og til vil du kanskje erstatte start- og slutteksten som er angitt for den gjeldende purregraden, men tekst fra en annen grad.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg igjen 3.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Purringer**, og velg deretter den relaterte koblingen.
2. Åpne den aktuelle purringen, og velg deretter handlingen **Oppdater purretekst**.
3. Angi ønsket grad i feltet **Purregrad** på siden **Oppdater purretekst**.
4. Velg **OK** for å oppdatere start- og slutteksten.

### Utstede en purring

Når du har opprettet purringer og foretatt eventuelle nødvendige endringer, kan du skrive ut kontrollrapportene eller utstede purringene.

Når du utsteder en purring, overføres dataene til en separat side for utstedte purringer. Samtidig bokføres purrepostene. Hvis rente eller tilleggsgebyr er beregnet, bokføres poster til kundeposten og Finans.

Når en purring er utstedt, bokføres postene i henhold til dine spesifikasjoner på siden **Purrebetingelser**. Denne spesifikasjonen angir om renter og/eller tilleggsgebyrer skal bokføres på kundens konto og i Finans. Oppsettet på siden **Bokføringsgrupper - kunde** angir hvilke konti det skal bokføres på.

For hver kundepost i rentenotaen opprettes det en post på siden **Purre-/renteposter**.

Hvis det er merket av for **Bokfør rente** eller **Bokfør tilleggsgebyr** på siden **Purrebetingelser**, opprettes også følgende poster:

- Én post på siden **Kundeposter**
- Én post for utestående på relevant finanskonto
- Én post for rente og/eller én post for tilleggsgebyr på relevant finanskonto

I tillegg kan utstedelsen av purringen resultere i mva-poster.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg også her 4.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Purringer**, og velg deretter den relaterte koblingen.
2. Velg den aktuelle purringen, og velg deretter handlingen **Utsted**.
3. På siden **Utsted purringer** fyller du ut feltene etter behov.
4. Velg **OK**.

Purringen blir enten skrevet ut eller sendt til en bestemt e-postadresse som et PDF-vedlegg.

### Avbryte den utstedte purringen

Hvis påminnelser ble utstedt med en feil, kan du annullere dem før de sendes ut. Du kan gjøre dette enten én om gangen eller som en bunke.

1. På siden **Utstedte purringer** velger du én eller flere linjer for de utstedte purringene du vil avbryte, og deretter velger du handlingen **Avbryt**.
2. På siden **Avbryt utstedte purringer** fyller du ut feltene etter behov, og deretter velger du **OK**.


