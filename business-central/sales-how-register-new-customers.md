---
title: Opprette et kundekort for å registrere nye kunder | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter et kundekort for å registrere informasjon om hver nye kunde eller klient du selger til.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 0bdc559f04064e2b4d49ef4ed7a8759c68be3579
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194046"
---
# <a name="register-new-customers"></a>Registrere nye kunder
Kunder er kilden til dine inntekter. Du må registrere gver kunde du selger til, som et kundekort. Kundekort inneholder informasjonen som er nødvendig for å selge produkter til kunden. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).  

Før du kan registrere nye kunder, må du definere forskjellige salgskoder som du kan velge fra når du fyller ut kundekort. Hvis du vil ha mer informasjon, kan du se [Sette opp salg](sales-setup-sales.md).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

> [!NOTE]  
> Hvis det finnes kundemaler for ulike kundetyper, vises en side når du oppretter et nytt kundekort der du kan velge en passende mal. Hvis det bare finnes én kundemal, brukes alltid denne malen i nye kundekort.  

## <a name="to-create-a-new-customer-card"></a>Opprette et nytt kundekort
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.  
2. På siden **Kunder** velger du handlingen **Ny**.

    Hvis det bare finnes én kundemal, åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.

    Hvis det finnes mer enn én kundemal, åpnes en side der du kan velge en kundemal. I det tilfellet følger du de to neste trinnene.
3. På siden **Velg en mal for en ny kunde** velger du malen som du vil bruke for det nye kundekortet.
4. Velg **OK**. Det åpnes et nytt kundekort med noen felt som er fylt ut med informasjon fra malen.  
5. Fortsette med å fylle ut eller endre feltet på kundekortet etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

I hurtigfanen **Salgspriser** kan du vise spesialpriser eller rabatter som skal gis til kunden hvis bestemte kriterier oppfylles, for eksempel vare, minimumsordreantall eller sluttdato. Hver rad representerer en spesialpris eller linjerabatt. Hver kolonne representerer et vilkår som må brukes for å garantere spesialprisen du angir i feltet **Enhetspris**, eller linjerabatten du angir i feltet **Linjerabatt-%**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md).

Kunden er nå registrert, og kundekortet er klart til å brukes på salgsdokumenter.

Hvis du vil bruke dette kundekortet som en mal når du oppretter nye kundekort, kan du lagre det som en mal. Hvis du vil ha mer informasjon, kan du se følgende avsnitt:

## <a name="to-save-the-customer-card-as-a-template"></a>Lagre kundekortet som en mal
1. På siden **Kundekort** velger du handlingen **Lagre som mal**. **Kundemal**-siden åpnes og viser kundekortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**. **Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for kunden.
4. Rediger eller angi dimensjonskoder som skal gjelde for nye kundekort som opprettes ved hjelp av malen.  
5. Når du har fullført den nye kundemalen, kan du velge **OK**-knappen.

Kundemalen legges til i listen over kundemaler, slik at du kan bruke den til å opprette nye kundekort.

## <a name="see-also"></a>Se også
[Definere betalingsmåter](finance-payment-methods.md)  
[Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md)  
[Opprette nummerserier](ui-create-number-series.md)  
[Salg](sales-manage-sales.md)    
[Sette opp salg](sales-setup-sales.md)    
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
