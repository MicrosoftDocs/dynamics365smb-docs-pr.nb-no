---
title: Opprette en salgsfaktura for prosjekt for å fakturere et prosjekt | Microsoft-dokumentasjon
description: Beskriver hvordan du kan fakturere kunder for prosjektutgifter etter hvert som et prosjekt skrider frem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project invoice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 368b0b1edf1105045a365d8d5ac523c88955ad8a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758745"
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

## <a name="to-calculate-and-post-job-completion-entries"></a>Slik beregner og bokfører du prosjektferdiggjørelsesposter
Når du har fullført alle aktiviteter for et prosjekt, inkludert bokføring og fakturering, må du oppdatere prosjektet for å sette **Status** til **Ferdig**. Deretter må du reversere alle VIA-er som er bokført i finans.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Prosjekter**, og velg deretter den relaterte koblingen.  
2. Merk et åpent prosjekt, og velg handlingen **Rediger**.
3. I feltet **Status** velger du **Fullført**.
4. Følg hjelpetrinnene for å beregne og bokføre VIA. Alternativt følger du trinn 5 og 6 hvis du vil gjøre dette manuelt.  
5. Velg handlingen **Beregn VIA**.
6. På siden **Beregn VIA for prosjekt** fyller du ut feltene etter behov.  

     VIA-postene for prosjekt du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.  
7. Velg handlingen **Bokfør VIA i Finans for prosjekt**.
8. Fyll ut feltene etter behov på siden **Bokfør VIA i Finans for prosjekt**.  

     VIA-finanspostene for prosjekt som du oppretter ved å kjøre kjørselen, vil ha en avmerking i **Prosjekt ferdig**-boksen for å angi at de er ferdiggjørelsesposter.

## <a name="see-also"></a>Se også
[Administrere prosjekter](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
