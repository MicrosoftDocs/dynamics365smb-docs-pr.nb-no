---
title: Kjøpe varer eller tjenester for et prosjekt og administrere forsyninger | Microsoft-dokumentasjon
description: Beskriver hvordan du administrerer forsyninger og innkjøp av materialer og tjenester for prosjekter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 676658e869d0310fac71dda592c892994dac0edc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312847"
---
# <a name="manage-job-supplies"></a>Administrere prosjektforsyninger
Behandling av prosjektforsyninger som varer, tjenester og utgifter inngår i og er en viktig del av alle prosjektutførelser. Du kan bruke lagerantallene eller foreta prosjektspesifikke kjøp ved hjelp av bestillinger eller kjøpsfakturaer. En servicejobb på en datamaskin krever for eksempel en ny disk. Du oppretter en kjøpsfaktura for å kjøpe en ny disk, og registrerer prosjektet den skal brukes på.

Hvis kjøpsprosessen ikke krever at den fysiske transaksjonen registreres separat, kan et kjøp behandles på siden **Finanskladd for prosjekt**. Hvis du vil ha mer informasjon, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Slik kjøper du varer eller tjenester for et prosjekt
Følgende fremgangsmåte viser hvordan du bruker en kjøpsfaktura til å kjøpe produkter for et prosjekt. Bruk samme fremgangsmåte når du bruker en bestilling.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** og fyll ut feltene etter behov. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
3. I feltene **Prosjektnr.** og **Prosjektoppgavenr.** velger du informasjonen på prosjektet som du vil kjøpe varer eller tjenester for. Bruk funksjonen **Velg kolonner** hvis feltet ikke er synlig. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

    Verdien du velger i feltet **Prosjektlinjetype**, definerer om en planleggingslinje blir opprettet når du bokfører forbruket for varen. Hvis feltet inneholder **Fakturerbar**, opprettes det prosjektplanleggingslinjer som er klare for å faktureres kunden. Hvis du vil ha mer informasjon, kan du se [Fakturere prosjekter](projects-how-invoice-jobs.md).
4. Velg handlingen **Bokfør**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>Slik viser du verdien av kjøp for et prosjekt
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Jobber**, og velg deretter den relaterte koblingen.
2. Åpne et aktuelt prosjektkort.

    På hurtigfanen **Oppgaver** viser feltet **Utestående bestillinger** det totale utestående beløpet, i lokal valuta, for lagervarer og tjenester i kjøpsdokumenter for prosjektoppgavelinjen.  

    Feltet **Mottatt, ikke fakturert (beløp)** viser verdien for varer som er levert i kjøpsdokumenter, men som ennå ikke er fakturert.  
3. Velg enten feltene for å åpne siden **Bestillingslinjer**, der du kan gå gjennom informasjon om de relaterte kjøpsdokumentlinjene, inkludert hvilke varer eller tjenester som er mottatt.

## <a name="to-post-a-job-related-expense"></a>Slik bokfører du en prosjektrelatert utgift
Hvis du pådrar deg ekstraordinære eller enkeltstående prosjektutgifter, kan du bruke siden **Finanskladd for prosjekt** til å bokføre dem direkte til den aktuelle prosjektkontoen.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder for prosjekt**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje, og skriv inn informasjon om utgiften, inkludert informasjon i feltene **Prosjektnr.** og **Prosjektoppgavenr.**  
3. Når kladden er fullført, kan du velge handlingen **Bokfør**.

## <a name="see-also"></a>Se også
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
