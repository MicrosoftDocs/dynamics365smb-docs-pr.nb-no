---
title: "Synkronisere kontakter med kunder og leverandører | Microsoft-dokumentasjon"
description: "Du kan koble eller synkronisere kontaktinformasjon for kontakter som også er kunder, leverandører eller bankkonti, så du oppdaterer informasjon bare på ett sted."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f377236158ae1035fd40dd15342d76822aa91ac8
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synkronisere kontakter med kunder, leverandører og bankkonti
Hvis en del av kontaktene også er kunder, leverandører eller bankkonti, kan du synkronisere kontaktinformasjonen med relatert kunde, leverandør eller bankkonto. Synkronisering gjør at informasjon som er felles mellom kontakter og kunder, leverandører eller bankkonto, er den samme.  

Før du kan synkronisere kontaktene med kunder, leverandører eller bankkonti, må du angi en kode for forretningsforbindelse for kunder, leverandører og bankkonti i vinduet **Markedsføringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Sette opp forbindelser](marketing-setup-marketing.md).

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a>Ulike metoder for å synkronisere kontakter med kunder, leverandører og bankkonti
Du kan synkronisere kontaktene med kunder, leverandører eller bankkonti ved hjelp av tre metoder:

* Koble kontakter til eksisterende kunder, leverandører og/eller bankkonti fra kontaktkortet. Hvis du vil ha mer informasjon, kan du se [Knytte kontakter til kunder, leverandører og bankkonti](marketing-how-link-contact.md).
* Opprett kunder, leverandører eller bankkonti fra kontakten. Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).
* Opprett kontakter fra kunder, leverandører eller bankkonti. Hvis du vil ha mer informasjon, kan du se [Opprette en selskapskontakt fra kunde, leverandør eller bankkonto](marketing-how-create-contact-companies.md).

## <a name="consequences-of-synchronization"></a>Konsekvensene av synkronisering
Når kontakten synkroniseres med kunde, leverandør, bankkonto:

* Du trenger du bare å oppdatere opplysninger på ett sted. Hvis du for eksempel endrer telefonnummeret på kontakten, blir telefonnummeret automatisk oppdatert med de samme endringene på kunden, leverandøren eller bankkontoen.
* Hvis du har angitt en nummerserie for kontakter, opprettes det automatisk et kontaktkort for kunden, leverandøren eller bankkontoen når du oppretter et kundekort, leverandørkort eller bankkontokort.
* Du kan du opprette tilbud og ordrer og forespørsler og bestillinger fra kontakten.
* Du kan angi at samhandlinger registreres når du utfører handlinger, for eksempel når du skriver ut ordrer, rammeordrer, oppretter serviceordrer, sender e-post og så videre.
* Hvis du sletter en kontakt som er koblet til en kunde, leverandør eller bankkonto, er det bare kontakten som fjernes. Kunden, leverandøren eller bankkontoen beholdes.
* Hvis du sletter en kunde, leverandør eller bankkonto som er koblet til en kontakt, beholdes kontakten.

> [!NOTE]  
>   Noen detaljer, for eksempel fakturerings- og bokføringsopplysninger, vises ikke på kontaktkortet. Du vil derfor kanskje legge dem til manuelt på kundekortet, leverandørkortet eller bankkontokortet når du oppretter kontakter som kunder, leverandører eller bankkonti.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

