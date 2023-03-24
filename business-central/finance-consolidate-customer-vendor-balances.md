---
title: Konsolider saldoer for et selskap som er en kunde og en leverandør
description: Beskriver hvordan du konsoliderer saldoer for en kunde som også er en leverandør.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '5052, 21, 5050'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Konsolider saldoer for et selskap som er en kunde og en leverandør
Et selskap som du handler med, kan være både en kunde og en leverandør. Når dette er tilfellet, kan du unngå å ta unødvendige betalinger eller mottak og kanskje lagre transaksjonsgebyrer ved å konsolidere firmaets kunde- og leverandørsaldoer. Konsolideringen sammenligner selskapets saldoer som en leverandør og som en kunde, og deretter fylles beløpet ut slik at enten kunde- eller leverandørsaldoen beholdes, avhengig av hvilket beløp som var høyere. 

Hvis du vil konsolidere saldoene, må du først knytte kunde- og leverandørselskapene til en kontakt med typen **Selskap**. En kunde eller leverandør kan bare ha én kontakt av typen **Selskap**. Hvis du vil ha mer informasjon, kan du se [Opprett kontakter](marketing-create-contact-companies.md).

Når du har koblet sammen selskapene, tilbyr **Kundekort**-siden feltet **Saldo som leverandør**, og siden **Leverandørkort** inkluderer feltet **Saldo som kunde**.

Selv om det ikke er et krav, er kunde- og leverandørselskaper vanligvis samme juridiske enhet. 

## Før du begynner
Før du konsoliderer saldoer, må du angi noen innstillinger på siden **Markedsføringsoppsett**. 

* På hurtigfanen **Samhandlinger** må du angi koder for forretningsforbindelser i feltene **Kunder** og **Leverandører**. [!INCLUDE[prod_short](includes/prod_short.md)] bruker denne informasjonen til å bestemme hvilken type relasjon som skal vises for kontakter. 
* Valgfritt: På hurtigfanen **Duplikater** slår du duplikatsøk av eller på. Duplikatsøk er aktivert som standard. Hvis du vil ha mer informasjon, kan du se [Håndter duplikater](#handling-duplicates). 

## Knytt et eksisterende kunde- og leverandørselskap gjennom en kontakt
Trinnene nedenfor beskriver hvordan du kobler en kunde og en leverandør via en kontakt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunde** eller **Leverandør** og velg den relaterte koblingen.
2. Velg kunden eller leverandøren, og velg deretter handlingen **Kontakt**.
3. Hvis feltet **Kontaktens forretningsforbindelse** inneholder en annen verdi enn **Ingen**, må du fjerne relasjonen. Dette gjør du ved å bruke handlingen **Forretningsforbindelse** og deretter slette relasjonen. 
4. Avhengig av om du velger **Kunde** eller **Leverandør** i trinn 1, velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir deretter motparten. Det vil si at hvis du velger **Leverandør**, må du søke etter **Kunde**.
5. Velg kunden eller leverandøren, og velg deretter handlingen **Kontakter**.
6. Velg handlingen **Knytt til eksisterende**, og velg deretter alternativet **Kunde** eller **Leverandør**.
7. Velg kunden eller leverandøren.

## Opprett en leverandør fra en kunde eller omvendt
Du kan opprette en ny leverandør fra en eksisterende kunde eller en ny kunde fra en leverandør. Åpne **Kontakt**-siden fra sidene **Kunde** eller **Leverandør**. Velg handlingen **Opprett som**, og velg deretter alternativene **Kunde** eller **Leverandør**. 

## Opprett en ny kunde eller leverandør og knytt dem til via en leverandør- eller kundekontakt
1. Opprett en ny kunde eller leverandør. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md) eller [Registrer nye kunder](sales-how-register-new-customers.md).
2. Når du har definert kunden eller leverandøren, velger du **Opprett**-handlingen og velger enten **Kunde**- eller **Leverandør**-alternativene. 

## Slik konsoliderer du kunde- og leverandørsaldoer for et kontaktselskap
På siden **Utbetalingskladd** bruker du handlingen **Netto kunde-/leverandørsaldoer** til å konsolidere kunde- og leverandørsaldoen til ett enkelt nettobeløp. Handlingen oppretter, men bokfører ikke, utbetalingskladdelinjer som inneholder nettosaldoer.

> [!NOTE]
> Hvis kunde- eller leverandørsaldoen inneholder beløp som har forskjellige valutaer, opprettes en linje for beløpet i hver valuta.

## Håndter duplikater
Hvis du aktiverer duplikatsøk på hurtigfanen **Duplikater** på siden **Markedsføringsoppsett**, vises en advarsel når du endrer verdiene for felter som er en del av oppsettet for duplikatsøkestrenger. Når det blir funnet en duplikat, kan du gjøre følgende:

* Kombiner de like kontaktene til én enkelt kontakt som er lik både kunden og leverandøren, ved å bruke funksjonen **Slå sammen med** på siden **Kontaktkort**. Vanligvis utføres sammenslåing av kontakter når kunden og leverandøren er samme juridiske enhet. Hvis du vil ha mer informasjon, se [Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md). 
* Slett leverandørforretningsforbindelsen for leverandør- eller kundekontakten, og bruk deretter **Koble til eksisterende**-handling for å koble til en annen kontakt.    

## Se også
[Salg](sales-manage-sales.md)  
[Registrere nye kunder](sales-how-register-new-customers.md)  
