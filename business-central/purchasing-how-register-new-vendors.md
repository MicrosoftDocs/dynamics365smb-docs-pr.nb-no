---
title: Opprette et leverandørkort for å registrere en ny leverandør | Microsoft-dokumentasjon
description: Finn ut hvordan du oppretter et leverandørkort for å registrere en ny leverandør.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8efd74c3ae6962a383e5b127056d744dd7c1892f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748796"
---
# <a name="register-new-vendors"></a>Registrere nye leverandører

Leverandører tilbyr produktene du selger. Hver leverandør du kjøper fra, må være registrert som et leverandørkort.

Før du kan registrere nye leverandører, må du definere forskjellige kjøpskoder som du kan velge fra når du fyller ut leverandørkort. Når du har angitt alle nødvendige hoveddata, kan du konfigurere leverandøren ytterligere, for eksempel angi betalingsprioritet og vise en oversikt over varer som leverandøren og andre leverandører kan levere. En annen gruppe med oppsettsoppgaver for leverandører er å registrere avtaler om rabatter, priser og betalingsmåter. Hvis du vil ha mer informasjon, kan du se [Definere kjøp](purchasing-setup-purchasing.md).

Leverandørkort inneholder informasjon som er nødvendig for å kjøpe produkter fra leverandøren. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
> Hvis det finnes leverandørmaler for ulike leverandørtyper, vises en side når du oppretter et nytt leverandørkort, der du kan velge en passende mal. Hvis det bare finnes én leverandørmal, brukes alltid denne malen i nye leverandørkort.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="to-create-a-new-vendor-card"></a>Opprette et nytt leverandørkort

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.  
2. På **Leverandører**-siden velger du **Ny**.

    Hvis det finnes mer enn én leverandørmal, åpnes en side der du kan velge en leverandørmal. I det tilfellet følger du de to neste trinnene.
3. På siden **Velg en mal for en ny leverandør** velger du malen som du vil bruke for det nye leverandørkortet.
4. Velg **OK**. Det åpnes et nytt leverandørkort med noen felt som er fylt ut med informasjon fra malen.
5. Fortsette med å fylle ut eller endre feltet på leverandørkortet etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Hvis du ikke vet fakturaadressen som skal brukes for hver eneste faktura fra en leverandør, lar du være å fylle ut feltet **Leverandørnr.** på leverandørkortet. I stedet velger du betal til-leverandørnummeret når du har definert en forespørsel, bestilling eller et fakturahode.

Leverandøren er nå registrert, og leverandørkortet er klart til å brukes på kjøpsdokumenter.

Hvis du vil bruke dette leverandørkortet som en mal når du oppretter nye leverandørkort, kan du lagre det som en leverandørmal. Hvis du vil ha mer informasjon, kan du se følgende avsnitt:

### <a name="deleting-vendor-cards"></a>Slette leverandørkort
Hvis du har bokført en transaksjon for en leverandør, kan du ikke slette kortet, fordi postene kan være nødvendige for revisjon. Hvis du vil slette leverandørkort med poster, kontakter du Microsoft-partneren for å gjøre det gjennom kode.

## <a name="to-save-the-vendor-card-as-a-template"></a>Lagre leverandørkortet som en mal
1. På siden **Leverandørkort** velger du handlingen **Lagre som mal**. **Leverandørmal**-siden åpnes og viser leverandørkortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**. **Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for leverandøren.
4. Rediger eller angi dimensjonskoder som skal gjelde for nye leverandørkort som opprettes ved hjelp av malen.
5. Når du har fullført den nye leverandørmalen, kan du velge **OK**-knappen.  
   Leverandørmalen legges til i listen over leverandørmaler, slik at du kan bruke den til å opprette nye leverandørkort.

## <a name="see-also"></a>Se også
[Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md)  
[Opprette nummerserier](ui-create-number-series.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)   
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
