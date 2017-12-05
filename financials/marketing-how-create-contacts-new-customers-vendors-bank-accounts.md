---
title: "Opprette en kunde eller leverandør fra en kontakt | Microsoft-dokumentasjon"
description: "Du kan registrere en eksisterende kontakt som en kunde, leverandør eller bankkonto ved å bruke eksisterende data og angi en forretningsforbindelse."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 289213b9c44b07387fd0dcf315b9d08750bdd9f7
ms.contentlocale: nb-no
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-create-a-customer-vendor-or-bank-account-from-a-contact"></a>Opprette en kunde, leverandør eller bankkonto fra en kontakt
Du ønsker kanskje å registrere noen av de eksisterende kontaktene som kunder, leverandører eller bankkonti. Oppretting av en kunde, leverandør eller bankkonto fra en kontakt, lar deg bruke eksisterende data. Når du oppretter en kunde, leverandør eller bankkonto på denne måten, synkroniseres den med kontakten. Synkronisering gjør at informasjon som er felles mellom kontakter og kunder, leverandører eller bankkonto, er den samme.

Før du kan registrere kontakter på denne måten, må du angi en forretningsforbindelseskode for kunder, leverandører og bankkonti, i vinduet **Markedsføringsoppsett**. Hvis du vil registrere kontakter som bankkonti, må du også angi nummerserie for bankkonti i vinduet **Finansoppsett**.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>Slik oppretter du en kontakt som en kunde, leverandør eller bankkonto
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kontakter**, og velg deretter den relaterte koblingen.
2. Velg kontakten du vil opprette som en kunde, leverandør eller bankkonto.
3. Velg handlingen **Opprett som**, og velg deretter **Kunde**, **Leverandør** eller **Bank**.
4. Bekreft meldingen som vises.

Kontaktinformasjonen er overført fra **Kontakt**-kortet til **Bankkonto**-kortet, **Kunde**-kortet eller **Leverandør**-kortet. Noen ganger kan det være nødvendig å legge til spesifikke opplysninger på hvert kort, for eksempel fakturerings- og betalingsopplysninger.

## <a name="see-also"></a>Se også
[Opprette kontaktselskaper](marketing-create-contact-companies.md)  
[Opprette kontaktpersoner](marketing-create-contact-persons.md)  
[Sette opp forbindelser](marketing-setup-marketing.md)  
[Synkronisere kontakter med kunder, leverandører og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts.md)  
[Knytte kontakter til eksisterende kunder, leverandører og bankkonti](marketing-how-link-contact.md)  
[Tilordne forretningsforbindelser til en kontakt](marketing-business-relations.md#AssignBusRelContact)  
[Arbeide med Dynamics 365](ui-work-product.md)

