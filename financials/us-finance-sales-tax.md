---
title: "Definere mva-grupper, områder og jurisdiksjoner i USA og Canada | Microsoft-dokumentasjon"
description: "Finn ut mer om hvordan salgsmva konfigureres, og hvordan mva-grupper, mva-områder (delstater, fylker, byer og lokasjoner), mva-jurisdiksjoner og mva-detaljer fungerer."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 763bb1b954b30734b0f81f121a6534c83442321a
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-in-the-us-and-canada"></a>Rapportere salgsmva i USA og Canada
Når du begynner å bruke [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du kjøre en assistert installasjonsveiledningen for hurtig og enkelt sette opp mva-informasjon for firmaet, kundene og leverandørene. I løpet av minutter er du klar til å opprette salgsdokumenter og kjøpsdokumenter med riktig beregnet merverdiavgift. Dette er beskrevet [i våre blogginnlegg](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Hvis du flytter til det tomme Mitt firma, anbefaler vi at du starter med å bruke hver av de assisterte installasjonsveiledningene, inkludert den for mva. Hvis du foretrekker å definere mva selv, vil denne artikkelen forklarer hva du må ta hensyn til.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Mva-grupper, mva-områder og mva-jurisdiksjoner
I [!INCLUDE[d365fin](includes/d365fin_md.md)] representerer en mva-gruppe en gruppe av lagervarer eller ressurser som det skal beregnes like mye mva. av. Ikke i Norge. Du kan for eksempel angi en mva-gruppe for avgiftspliktige varer og en annen for ikke-avgiftspliktige varer. Du må tilordne mva-gruppekoder til varer og finanskonti. Du må også tilordne mva-områdekoder til kunder, lokasjoner og til dine egne firmainnstillinger. Den assisterte installasjonsveiledningen hjelper deg med å gjøre dette.  

Hver enkelt mva-område er en gruppering av mva-jurisdiksjoner som er basert på en bestemt geografisk lokasjon. Mva-området for Miami i Florida, inneholder for eksempel tre mva-jurisdiksjoner: by (Miami), fylke (Dade), og delstat (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder et begrenset sett med mva-områder med en standardkonfigurasjon, men du kan endre dem og legge til nye mva-områder.  

Hvis du konfigurerer nye mva-områder og mva-jurisdiksjoner, må du forsikre deg om at du fyller ut feltene på riktig måte. I USA kan delstater, fylker, byer og lokasjoner kreve mva. I Canada kan føderale myndigheter og provinser kreve mva. Firmaer samler inn og remitterer mva til disse myndighetene for produkter som selges til sluttbrukere. Mva kan også kreves på eksisterende mva. Mva kan for eksempel beregnes for en salgsfaktura som allerede inkluderer mva fra andre jurisdiksjoner.  

I Canada må mva-beløp være angitt i dokumenter for hver mva-jurisdiksjon. Opptil fire jurisdiksjoner kan vises i et dokument, og jurisdiksjoner som har samme utskriftsrekkefølgen kombineres når de skrives ut.  

## <a name="tax-details"></a>Mva-detaljer
Vinduet **Mva-detaljer** viser forskjellige kombinasjoner av mva-jurisdiksjoner og mva-grupper for å opprette mva-satser. For hver mva-jurisdiksjon anbefaler vi at du definerer en mva-gruppe for vanlig mva, en annen mva-gruppe for varer eller tjenester som ikke er mva-belagt og en ekstra mva-gruppe for hver vare eller tjeneste som er behandlet med en annen mva-sats i denne jurisdiksjonen.  

I USA, når du selger til en kunde på en lokasjon der du ikke har en *situs*, eller en juridisk lokasjon i denne delstaten, krever du ikke inn mva. For lokasjoner der du ikke har en juridisk lokasjon må du sikre at feltene **Mva. under maksimum** og **Mva. over maksimum** er 0,00.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Mva og avgifter for varer og tjenester i USA og Canada](ca-finance-tax.md)  
[Enkelt oppsett av mva](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

