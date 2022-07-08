---
title: Opprette et leverandørkort for å registrere en ny leverandør (inneholder video)
description: I dette emnet lærer du hvordan du oppretter et leverandørkort for å registrere en ny leverandør og lagre leverandørkort som en mal.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.search.form: 26, 27, 34, 461, 786, 1379, 1385, 1386, 1628
ms.date: 09/29/2021
ms.author: edupont
ms.openlocfilehash: 2c6b1b37398d0121c5c79bb0c9d9786abe14120f
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9074617"
---
# <a name="register-new-vendors"></a>Registrere nye leverandører

Leverandører tilbyr produktene du selger. Hver leverandør du kjøper fra, må være registrert som et leverandørkort.

Før du kan registrere nye leverandører, må du definere forskjellige kjøpskoder som du kan velge fra når du fyller ut leverandørkort. Når du har angitt alle nødvendige hoveddata, kan du konfigurere leverandøren ytterligere, for eksempel angi betalingsprioritet og vise en oversikt over varer som leverandøren og andre leverandører kan levere. En annen gruppe med oppsettsoppgaver for leverandører er å registrere avtaler om rabatter, priser og betalingsmåter. Hvis du vil ha mer informasjon, kan du se [Definere kjøp](purchasing-setup-purchasing.md).

Leverandørkort inneholder informasjon som er nødvendig for å kjøpe produkter fra leverandøren. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).

> [!NOTE]  
> Hvis det finnes leverandørmaler for ulike leverandørtyper, vises en side når du oppretter et nytt leverandørkort, der du kan velge en passende mal. Hvis det bare finnes én leverandørmal, brukes alltid denne malen i nye leverandørkort.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a>Legge til nye leverandører

Du kan legge til nye leverandører manuelt ved å fylle ut feltene på siden **Leverandørkort**, eller du kan bruke maler som inneholder forhåndsdefinert informasjon. Du kan for eksempel opprette maler for ulike typer leverandørprofiler. Når du bruker maler, sparer du tid når du legger til nye leverandører og bidrar til å sikre at informasjonen er riktig hver gang. Hvis du oppretter maler for mer enn én leverandørtype, kan du velge hvilken mal du vil bruke når du legger til en leverandør. Hvis du oppretter bare én mal, brukes den for alle nye leverandører. Når du har opprettet en mal, kan du bruke handlingen **Bruk mal** til å bruke den på en eller flere utvalgte leverandører. Når du skal opprette en mal, fyller du ut informasjonen du vil bruke på nytt på siden Leverandørkort, og deretter lagrer du den som en mal. Hvis du vil ha mer informasjon, kan du se delen [Slik lagrer du siden Leverandørkort som en mal](purchasing-how-register-new-vendors.md#to-save-the-vendor-card-as-a-template).

> [!TIP]
> Det kan være nyttig å tilpasse siden **Leverandørmal** når du oppretter en mal. Det kan for eksempel hende at du vil legge til et felt som ikke allerede vises på siden. Hvis du vil ha mer informasjon, kan du se [Tilpass arbeidsområdet](/dynamics365/business-central/ui-personalization-user#to-start-personalizing-a-page-through-the-personalizing-banner).

Du kan også opprette en leverandør fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du en kontakt, leverandør, ansatt eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact). 

### <a name="to-create-a-new-vendor"></a>Slik oppretter du en ny leverandør

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

> [!TIP]  
> Hvis du ikke vet fakturaadressen som skal brukes for hver eneste faktura fra en leverandør, lar du være å fylle ut feltet **Leverandørnr.** på leverandørkortet. I stedet velger du betal til-leverandørnummeret når du har definert en forespørsel, bestilling eller et fakturahode.

Leverandøren er nå registrert, og leverandørkortet er klart til å brukes på kjøpsdokumenter.

Hvis du vil bruke dette leverandørkortet som en mal når du oppretter nye leverandørkort, kan du lagre det som en leverandørmal. Hvis du vil ha mer informasjon, kan du se delen [Slik lagrer du leverandørkortet som en mal](#to-save-the-vendor-card-as-a-template).

### <a name="deleting-and-editing-vendor-information"></a>Slette og redigere leverandøropplysninger

Du kan når som helst redigere informasjonen på leverandørkort. Hvis du imidlertid har bokført en transaksjon for en leverandør, kan du ikke slette kortet, fordi postene kan være nødvendige for revisjon. Hvis du vil slette leverandørkort med poster, kontakter du Microsoft-partneren for å gjøre det via kode.

> [!TIP]
> Du kan endre IBAN-nummer på en leverandørbankkonto uten at endringen påvirker historiske registeroppføringer for kredittoverføring. Registreringsoppføringer for kreditoverføring lagrer mottakerens IBAN-nummer, mottakerens bankkontonummer som er angitt i feltene Leverandørbankkonto og Mottakernavn på siden Leverandørkort når postene ble opprettet.

## <a name="to-save-the-vendor-card-as-a-template"></a>Lagre leverandørkortet som en mal

1. På siden **Leverandørkort** velger du handlingen **Lagre som mal**. **Leverandørmal**-siden åpnes og viser leverandørkortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**. **Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for leverandøren.
4. Rediger eller angi dimensjonskoder som skal gjelde for nye leverandørkort som opprettes ved hjelp av malen.
5. Når du har fullført den nye leverandørmalen, kan du velge **OK**-knappen.  
   Leverandørmalen legges til i listen over leverandørmaler, slik at du kan bruke den til å opprette nye leverandørkort.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/trade-master-data-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Slå sammen dupliserte poster](sales-how-merge-duplicate-records.md)  
[Opprette nummerserier](ui-create-number-series.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]