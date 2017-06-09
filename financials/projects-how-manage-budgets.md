---
title: Administrere prosjektbudsjetter| Microsoft-dokumentasjon
description: Beskriver hvordan du budsjetterer for prosjekter.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project budget, forecast
ms.date: 03/28/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 9a351b581e0312d21b04db43a85243b8a5afb0e3
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-manage-job-budgets"></a>Administrere prosjektbudsjetter
Du kan opprette et budsjett for hvert prosjekt. Budsjettet brukes til å planlegge ressursene du tildeler til et prosjekt. Budsjettet kan enten være generelt med få poster, eller det kan inneholde mange poster som er oppdelt i aktivitetsnivåer. Deretter kan du sammenligne de budsjetterte beløpene med det faktiske forbruket slik det er registrert i prosjektkladden. Ved å overvåke forskjeller mellom faktisk bruk og budsjettert bruk kan du kontrollere et pågående prosjekt og forbedre kvaliteten på fremtidige prosjekter ved å redusere risikoen for å underestimere kostnader.

Følgende fremgangsmåte beskriver hvordan du kan beregne budsjetterte kostnader under planleggingen. Hvis du vil ha informasjon om registrering av budsjetterte sammenlignet med faktiske prosjektpriser og kostnader, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).  

## <a name="JobBudgetCosts"></a> Slik estimerer du budsjetterte kostnader for et prosjekt
Når en kunde vil vite prisen på et prosjekt som faktureres basert på forbruk, må du fastsette de budsjetterte kostbeløpene for prosjektet. Du bruker vinduet **Prosjektoppgavelinjer** til å gjøre dette.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Prosjekter**, og deretter velger du den beslektede koblingen.  
2. Åpne et relevant prosjekt.
3. Merk en oppgavelinje for bokføring, og velg deretter handlingen **Prosjektplanleggingslinjer**.
4. Fyll ut feltene etter behov på en ny linje. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]   

Se følgende informasjon for feltet **Linjetype**.  

| Linjetype | Beskrivelse |
| --- | --- |
| **Både Budsjett og Fakturerbar** |Kost- og prisbeløpene som er angitt på planleggingslinjen, er budsjettert kost for den bestemte planleggingslinjen. Prisbeløpet vil bli fakturert. |
| **Budsjett** |Kunden belastes ikke for forbruk. Forbruk overføres ikke til en faktura, men brukes likevel i VIA-beregningen. |
| **Fakturerbar** |Kunden belastes for forbruk. Forbruk overføres til fakturaen basert på antallet som er angitt i feltet Ant. som skal overføres til faktura. |

**Merk**: Feltet **Planleggingsdato** for planleggingslinjen inneholder datoen da forbruk som er knyttet til planleggingslinjen, er forventet å fullføres. Det er også datoen da planleggingslinjen kan overføres til en salgsfaktura og bokføres.  

**Merk**: Når du fyller ut feltet **Antall**, blir all informasjon om totalpris og totalkostnad beregnet og fylt ut for den planleggingslinjen. Du kan redigere dem når som helst.

I vinduet **Prosjektkort** kan du nå se en oversikt over totalt budsjetterte kostnader, budsjettert pris, fakturerbar kostnad og fakturerbar pris for hver oppgave.

Hvis du vil ha informasjon om registrering av budsjetterte sammenlignet med faktiske prosjektpriser og kostnader, kan du se [Registrere forbruk for prosjekter](projects-how-record-job-usage.md).

## <a name="see-also"></a>Se også
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

