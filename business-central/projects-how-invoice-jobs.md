---
title: Opprette en salgsfaktura for prosjekt for å fakturere et prosjekt | Microsoft Docs
description: Beskriver hvordan du kan fakturere kunder for prosjektutgifter etter hvert som et prosjekt skrider frem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 873135d2fa6053b7101a999981fb3117ee8689ab
ms.sourcegitcommit: 93c8681054b059cec38cb29b86de20be37980676
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938149"
---
# <a name="invoice-jobs"></a>Fakturere prosjekter
I løpet av prosjektet kan det akkumuleres prosjektkostnader fra ressursforbruk, materiale og prosjektrelaterte kjøp. Under fremdriften til prosjektet blir disse transaksjonene bokført til prosjektkladden. Det er viktig at alle kostnader blir registrert i prosjektkladden før du fakturerer kunden.

> [!NOTE]
> Du kan også kjøpe eksterne ressurser som ikke er knyttet til et prosjekt, for eksempel for å fakturere en leverandør for arbeid som er levert. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).

Du kan fakturere hele prosjektet fra siden **Prosjektoppgavelinjer** eller bare fakturere utvalgte fakturerbare linjer fra siden **Planleggingslinjer**. Fakturering kan utføres etter at prosjektet er fullført, eller ved bestemte intervaller under fremdriften til prosjektet, basert på en faktureringsplan.

> [!NOTE]  
> Hvis du velger **Fakturerbar** i feltet **Prosjektlinjetype** i kjøpsdokumentene for prosjektrelaterte kjøp, opprettes prosjektplanleggingslinjer som er klare til å bli fakturert til kunden. Hvis du vil ha mer informasjon, kan du se [Administrere prosjektforsyninger](projects-how-manage-project-supplies.md).

## <a name="to-create-multiple-job-sales-invoices"></a>Opprette flere salgsfakturaer for prosjekt
Du kan opprette en faktura for et prosjekt eller for én eller flere prosjektoppgaver for en kunde enten når arbeidet som skal faktureres, er fullført, eller når faktureringsdatoen som er basert på et faktureringsestimat, er nådd.

Følgende fremgangsmåte viser hvordan du bruker en satsvis jobb til å fakturere flere prosjekter.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett salgsfaktura for prosjekt**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Angi filtre hvis du vil begrense prosjektene som kjørselen skal behandle.
4. Velg **OK** for å opprette fakturaene.  

Du kan gå gjennom og bokføre opprettede fakturaer i **Salgsfakturaer**-vinduet.

> [!NOTE]
> Du kan også fakturere en kunde ved å velge prosjektet, og deretter velge handlingen **Opprett salgsfaktura for prosjekt**. 

## <a name="to-create-and-post-job-sales-invoice-from-job-planning-lines"></a>Slik oppretter og bokfører du prosjektsalgsfaktura fra prosjektplanleggingslinjer
Du kan opprette en faktura fra en prosjektplanleggingslinje og samtidig angi antallet for varen, ressursen eller finanskontoen som du vil fakturere.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.
2. Åpne et relevant prosjekt.
3. Velg en prosjektoppgave der feltet **Prosjektoppgavetype** inneholder **Bokføring**, og velg deretter handlingen **Prosjektplanleggingslinjer**.  
4. På en prosjektplanleggingslinjer, i feltet **Ant. som skal overføres til faktura** angir du antallet av varen, ressursen, finanskontotypen du vil fakturere.  
5. Velg handlingen **Opprett salgsfaktura**.
6. På siden **Opprett salgsfaktura for prosjekt** skriver du inn bokføringsdatoen og om du vil opprette en ny faktura eller føye til denne fakturaen til en eksisterende.
7. Velg **OK**-knappen.  
8. På siden **Prosjektplanleggingslinjer** velger du handlingen **Salgsfakturaer/kreditnotaer**.

    Siden **Salgsfaktura** åpnes og viser antallet du har overført til fakturaen.
9. Gjør flere endringer, og velg deretter handlingen **Bokfør**.

> [!NOTE]  
>   Fremgangsmåten ovenfor er identisk for å opprette, gå gjennom og bokføre en prosjektrelatert salgskreditnota.


## <a name="see-also"></a>Se også
[Administrere prosjekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
