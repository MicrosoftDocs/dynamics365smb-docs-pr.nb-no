---
title: Angi en standardskriver
description: Finn ut de ulike måtene å konfigurere skrivere på som skal brukes som standard for utskriftsjobber.
author: jswymer
ms.topic: how-to
ms.reviewer: na
ms.service: dynamics365-business-central
ms.custom: bap-template
ms.search.keywords: 'online printing, email printing, cloud printing, Universal Print'
ms.search.form: '2650, 2750, 2752, 2753, 2754, 8900,'
ms.date: 02/09/2023
ms.author: jswymer
---
# <a name="specify-a-default-printer" /><a name="default"></a>Angi en standardskriver

Når skrivere er definert i Business Central, kan du angi hvilken skriver som skal brukes som standard. Det finnes noen andre måter å angi skrivere på som skal brukes som standard for rapporter og andre utskriftsjobber. En standardskriver er nyttig hvis du arbeider med forskjellige rapporter som krever ulike skrivere på grunn av sin plassering i firmaet eller utskriftsmulighetene.

> [!IMPORTANT]
> De eneste skriverne du kan angi som standard, er **Microsoft Print til PDF**- og skyskrivere som allerede er konfigurert for bruk i Business Central, for eksempel e-postskrivere og skrivere for Universell utskrift. Skybaserte skrivere konfigureres vanligvis av en administrator. Hvis du vil ha mer informasjon, kan du se [Skriveroppsett og -administrasjon](admin-printer-setup-overview.md).   

## <a name="set-a-printer-as-a-default-printer-for-all-print-jobs" />Angi en skriver som standardskriver for alle utskriftsjobber

Gjennom siden **Utskriftsbehandling** kan du konfigurere en skriver som standardskriver for alle utskriftsjobber. Du kan bare angi skriveren som standard for deg selv eller for alle brukere.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Utskriftsbehandling**, og velg deretter den relaterte koblingen.

    > [!TIP]
    > Du kan også åpne siden **Utskriftsbehandling** fra siden **Skrivertvalg** ved å velge **Utskriftsbehandling**.  
2. På siden **Utskriftsbehandling** velger du en skriver fra listen, velger **Behandle**, og velger deretter **Angi som min standardskriver** eller **Angi som standardskriver for alle brukere**.

> [!NOTE]
> Når du angir en standardskriver fra **Utskriftsbehandling**, legges det til en oppføring under **Skrivervalg**.

## <a name="set-a-default-printer-for-specific-reports" />Angi en standardskriver for bestemte rapporter

På siden **Skrivervalg** kan du angi hvilken skriver en rapport skal bruke som standard. Standardskriveren er angitt på brukerkontobasis. Du kan angi en standardskriver for bare deg selv, en annen bruker eller alle brukere.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Skrivervalg**, og velg deretter den relaterte koblingen. Alternativt kan du velge en skriver på siden **Utskriftsbehandling** og deretter velge handlingen **Skrivervalg**.
2. Velg handlingen **Ny** hvis du vil legge til et skrivervalg for en bestemt rapport.
3. Fyll ut feltene etter behov.

Den angitte rapporten er nå konfigurert slik at den skriver ut til den valgte skriveren som standard.

> [!NOTE]
> Når du skriver ut den aktuelle rapporten, kan du velge en annen skriver ved hjelp av feltet **Skriv ut** på rapportforespørselssiden.

> [!NOTE]
> Hvis du ikke definerer en rapport for en bestemt skriver på siden **Skrivervalg**, blir den skrevet ut på standardskriveren til selskapet, som definert på siden **Utskriftsbehandling**.

Du eller administratoren kan også bruke siden **Skrivervalg** til å definere andre variasjoner av utskrift for brukere og rapporter. Tabellen nedenfor beskriver kombinasjonen av verdier for å angi et annet utskriftsoppsett for en rapport.

|Til                                                 |Angi følgende verdier                                             |
|---------------------------------------------------|---------------------------------------------------------------------|
|Skrive ut en rapport på en bestemt skriver for alle brukere |Angi verdier i feltene **Rapport-ID** og **Skrivernavn**, og la feltet **Bruker-ID** stå tomt.|
|Skrive ut alle rapporter på en bestemt skriver til en bestemt bruker|Angi verdier i feltene **Bruker-ID** og **Skrivernavn**, og la feltet **Rapport-ID** stå tomt. Denne oppføringen gjør det samme som handlingen **Angi som min standardskriver** på siden **Utskriftsbehandling**.|
|Angi standardskriveren for alle rapporter for alle brukere|Angi en verdi i feltet **Skrivernavn**, og la feltene **Bruker-ID** og **Rapport-ID** stå tomme. Denne oppføringen gjør det samme som handlingen **Angi som standardskriver for alle brukere** på siden **Utskriftsbehandling**.|
|Skrive ut en bestemt rapport på brukerens standardskriver|Angi en verdi i feltet **Rapport-ID**, og la feltene **Skrivernavn** og **Bruker-ID** stå tomme.|
|Skrive ut en bestemt rapport på en bestemt skriver til en bestemt bruker|Angi verdier i alle tre feltene.|

> [!NOTE]
> Flere spesifikke skrivervalg har forrang over et mer generelt skrivervalg. Et skrivervalg som har verdier i feltene **Bruker-ID**, **Rapport-ID** og **Skrivernavn**, har for eksempel forrang over et skrivernavn som har tomme poster i feltene **Bruker-ID** eller **Rapport-ID**.

## <a name="choosing-the-printer-when-running-a-report" />Velg skriveren når du kjører en rapport

I stedet for å bruke standardskriveren når du kjører en rapport, kan du overstyre denne innstillingen fra forespørselssiden. Velg ganske enkelt hvilken skriver du vil bruke til denne rapportgenereringen, på rullegardinmenyen **Skriver**.

## <a name="sizing-print-jobs" />Endre størrelse på utskriftsjobber

Skyutskrifter er utformet for dokumenter med en fornuftig størrelse. De fleste skytjenester, inkludert PrintNode og HP ePrint, har en grense på 10 MB per jobb. Hvis du må skrive ut store rapporter, må du kanskje dele dem opp i flere utskrifter.

[Microsoft-opplæring](/training/modules/change-documents-dynamics-365-business-central/)

## <a name="see-also" />Se også

[Utskriftsbehandling](admin-printer-setup-overview.md)  
[Konfigurer skrivere for Universell utskrift](admin-printer-setup-universal-print.md)  
[Konfigurer e-postskrivere](admin-printer-setup-email.md)  
[Skrive ut en rapport](ui-work-report.md#PrintReport)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Kjøre kjørsler](ui-how-run-batch-jobs.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
