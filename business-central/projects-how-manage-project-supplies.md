---
title: Administrere prosjektforsyninger
description: Beskriver de ulike måtene for å administrere forsyninger og innkjøp av materialer og tjenester på for prosjekter.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: 'project management, material, purchase'
ms.search.form: '98, 1020'
ms.date: 02/22/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Administrere prosjektforsyninger

Du bør behandle prosjektforsyninger av varer, tjenester og utgifter som en integrert og viktig del av alle prosjekter. Du kan bruke lagerantallene eller foreta prosjektspesifikke kjøp via bestillinger eller kjøpsfakturaer. Et serviceprosjekt på en datamaskin krever for eksempel en ny disk. Du oppretter en kjøpsfaktura for å kjøpe en ny disk, og registrerer prosjektet som bruker den.

Hvis kjøpsprosessen ikke krever at du registrerer den fysiske transaksjonen separat, kan du behandle et kjøp på siden **Finanskladd for prosjekt**. Hvis du vil ha mer informasjon, kan du se [Slik bokfører du en prosjektrelatert utgift](projects-how-manage-project-supplies.md#to-post-a-project-related-expense).

## Slik kjøper du varer eller tjenester for et prosjekt

Følgende fremgangsmåte viser hvordan du bruker en kjøpsfaktura til å kjøpe produkter for et prosjekt. Bruk samme fremgangsmåte når du bruker en bestilling.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** og fyll ut feltene etter behov. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
3. I feltet **Prosjektnr.** og **Prosjektoppgavenr.** velger du informasjonen på prosjektet som du vil kjøpe varer eller tjenester for. Bruk verktøyene for tilpassing hvis et felt ikke er synlig. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

    Verdien du velger i feltet **Prosjektlinjetype**, definerer om en planleggingslinje blir opprettet når du bokfører forbruket for varen. Hvis feltet inneholder **Fakturerbar**, opprettes det prosjektplanleggingslinjer som er klare for å faktureres kunden. Hvis du vil ha mer informasjon, kan du se [Fakturer prosjekter](projects-how-invoice-jobs.md).
4. Velg handlingen **Bokfør**.

## Slik viser du verdien av kjøp for et prosjekt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Prosjekter**, og velg deretter den relaterte koblingen.
2. Åpne et aktuelt prosjektkort.

    På hurtigfanen **Oppgaver** viser feltet **Utestående bestillinger** det totale utestående beløpet, i lokal valuta, for lagervarer og tjenester i kjøpsdokumenter for prosjektoppgavelinjen.  

    Feltet **Mottatt, ikke fakturert (beløp)** viser verdien for varer som er levert i kjøpsdokumenter, men som ennå ikke er fakturert.  
3. Velg enten feltene for å åpne siden **Bestillingslinjer**, der du kan gå gjennom informasjon om de relaterte kjøpsdokumentlinjene, inkludert hvilke varer eller tjenester som er mottatt.

## Slik bokfører du en prosjektrelatert utgift

Hvis du pådrar deg ekstraordinære eller enkeltstående prosjektutgifter, kan du bruke siden **Finanskladd for prosjekt** til å bokføre dem direkte til den aktuelle prosjektkontoen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finanskladder for prosjekt**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje, og skriv inn informasjon om utgiften, inkludert informasjon i feltene **Prosjektnr.** og **Prosjektoppgavenr**.  
3. Når kladden er fullført, kan du velge handlingen **Bokfør**.

## Se også

[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med Business Central](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
