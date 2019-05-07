---
title: Opprette kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en kontakt for hvert nye selskap eller potensielle selskap du samhandler med eller har et forhold til.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 67945b8825ae94ff3a09a4072309c401abb41c6b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "920985"
---
# <a name="create-contacts"></a>Opprette kontakter
Du kan opprette en kontakt for hvert nytt selskap du utfører en samhandling med, for eksempel kunder, leverandører, prospektive kunder, banker, advokatfirmaer, konsulenter og så videre.

Det er to måter å opprette en kontakt på: fra grunnen av eller fra en eksisterende kunde, leverandør eller bankkonto.

## <a name="create-a-company-contact-from-scratch"></a>Opprette en selskapskontakt fra bunnen av
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Angi et nummer på kontakten i feltet **Nr.**.

    Hvis du har definert en nummerserie for kontakter på siden **Markedsføringsoppsett**, kan du eventuelt trykke Enter-tasten for å velge det neste tilgjengelige kontaktnummeret.  
4. Sett **Type** til **Selskap**.
5. Fyll ut de andre feltene etter behov:

## <a name="to-create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Opprette en selskapskontakt fra en kunde, leverandør eller bankkonto
Hvis du allerede har definert en rekke kunder, leverandører og bankkonti, kan du opprette kontakter på grunnlag av de eksisterende dataene. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen med informasjon om kunden, leverandøren eller bankkontoen.

> [!NOTE]  
>   Før du kan opprette kontaktselskaper på denne måten, må du angi en kode for forretningsforbindelse for kunder, leverandører og bankkonti, på siden **Markedsføringsoppsett**. Hvis du vil opprette kontakter fra en bankkonto, må du også angi nummerserie for bankkonti på siden **Finansoppsett**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi ett av følgende, alt etter hvor du vil opprette kontakter fra, og velg deretter den relaterte koblingen.
   * **Opprett kontakter fra kunder**
   * **Opprett kontakter fra leverandører**
   * **Opprett kontakter fra bankkonti**
2. Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** på siden for kjørselen som åpnes.
3. Velg **OK** for å starte oppretting av kontrakter.

    De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene. Forretningsforbindelsen for leverandører som er angitt på siden **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.

> [!TIP]  
>   Du kan også opprette en kunde, leverandør eller bankkonto fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Se også
[Synkronisere kontakter med kunder, leverandører og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Tilordne forretningsforbindelser til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Tilordne bransjegrupper til en kontakt](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Tilordne postgrupper til en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Opprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeide med Business Central](ui-work-product.md)
