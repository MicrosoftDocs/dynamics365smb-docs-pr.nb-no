---
title: Opprette kontaktselskaper | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter kontaktselskaper i Financials.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 02/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: bd8dfb8abc9387ad6b9c500f25feb181878b6cfe
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017


---
# <a name="create-contact-companies"></a>Opprette kontaktselskaper
Du kan opprette en kontakt for hvert nytt selskap du utfører en samhandling med, for eksempel kunder, leverandører, prospektive kunder, banker, advokatfirmaer, konsulenter og så videre.

Det er to måter å opprette en kontakt på: fra grunnen av eller fra en eksisterende kunde, leverandør eller bankkonto.

Før du oppretter en kontakt, bør du kontrollere innstillingene i vinduet **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, se [Sette opp forbindelser](marketing-setup-marketing.md).

## <a name="create-a-company-contact-from-scratch"></a>Opprette en selskapskontakt fra bunnen av
1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi **Kontakter**, og deretter velger du den beslektede koblingen.
2. Velg handlingen **Ny**.
3. Angi et nummer på kontakten i feltet **Nr.**.

    Hvis du har definert en nummerserie for kontakter i vinduet **Markedsføringsoppsett**, kan du eventuelt trykke Enter-tasten for å velge det neste tilgjengelige kontaktnummeret.  
4. Sett **Type** til **Selskap**.
5. Fyll ut de andre feltene etter behov:

## <a name="create-a-company-contact-from-a-customer-vendor-or-bank-account"></a>Opprette en selskapskontakt fra en kunde, leverandør eller bankkonto
Hvis du allerede har definert en rekke kunder, leverandører og bankkonti, kan du opprette kontakter på grunnlag av de eksisterende dataene. Når du oppretter en kontakt på denne måten, synkroniseres kontaktinformasjonen med informasjon om kunden, leverandøren eller bankkontoen.

**Merk**: Før du kan opprette kontaktselskaper på denne måten, må du angi en forretningsforbindelseskode for kunder, leverandører og bankkonti, i vinduet **Markedsføringsoppsett**. Hvis du vil opprette kontakter fra en bankkonto, må du også angi nummerserie for bankkonti i vinduet **Finansoppsett**.

1. I øvre høyre hjørne, velger du ikonet **Søk etter side eller en rapport** ![Søk etter side eller rapport](media/ui-search/search_small.png "ikonet Søk etter side eller rapport"), angi ett av følgende, alt etter hvor du ønsker å opprette kontakter fra, og deretter velger du den beslektede koblingen.
   * **Opprett kontakter fra kunder**
   * **Opprett kontakter fra leverandører**
   * **Opprett kontakter fra bankkonti**
2. Hvis du bare vil opprette kontakter fra bestemte kunder, leverandører eller bankkonti, definerer du filtre i inndelingen **Kunde**, **Leverandør** eller **Bankkonto** i vinduet for kjørselen som åpnes.
3. Velg **OK**-knappen for å starte oppretting av kontrakter.

    De neste kontaktnumrene i nummerserien tilordnes de nye kontaktene. Forretningsforbindelsen for leverandører som er angitt i vinduet **Markedsføringsoppsett**, tilordnes til nyopprettede kontakter.

**Tips**: Du kan også opprette en kunde, leverandør eller bankkonto fra en kontakt. Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).

## <a name="see-also"></a>Se også
[Synkronisere kontakter med kunder, leverandører og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Tilordne forretningsforbindelser til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Tilordne bransjegrupper til en kontakt](marketing-industry-groups.md#AssignIndustryGroupContact)  
[Tilordne postgrupper til en kontakt](marketing-mailing-groups.md#AssignMailGroupContact)  
[Opprette kontaktpersoner](marketing-create-contact-persons.md)  
[Arbeide med Financials](ui-work-product.md)

