---
author: brentholtorf
ms.topic: include
ms.date: 04/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

## <a name="best-practices-for-working-with-column-definitions"></a>Anbefalte fremgangsmåter for arbeid med kolonnedefinisjoner

Kolonnedefinisjoner versjonskontrolleres ikke. Når du endrer en kolonnedefinisjon, erstattes den gamle versjonen når endringen lagres i databasen. Listen nedenfor inneholder noen anbefalte fremgangsmåter for å arbeide med kolonnedefinisjoner.

- Hvis du legger til en kolonnedefinisjon, velger du en god kode og fyller ut beskrivelsesfeltet med en meningsfull tekst mens du fortsatt vet hva du bruker kolonnedefinisjonen til. Denne informasjonen hjelper kollegene dine (og ditt fremtidige jeg) med å arbeide med finansrapportering og kanskje endre kolonnedefinisjonen.
- Før du endrer en kolonnedefinisjon, bør du vurdere å ta en kopi av den som en sikkerhetskopi, i tilfelle endringen ikke fungerer som forventet. Du kan enten bare kopiere definisjonen (gi den et bra navn), eller eksportere den. Hvis du vil finne ut mer, kan du gå til [Importer eller eksporter kolonnedefinisjoner](#import-or-export-financial-report-column-definitions).
- Hvis du trenger en ny kopi av en definisjon som [!INCLUDE [prod_short](prod_short.md)] gir, er det enkelt å opprette et nytt selskap som bare inneholder oppsettsdata. Deretter eksporterer du definisjonen og importerer den til selskapet der definisjonen trenger en oppdatering.
