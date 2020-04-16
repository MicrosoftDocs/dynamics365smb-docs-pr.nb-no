---
title: Definere kontantkunder | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du definerer kunder som betaler kontant.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ebef3cd903472a22a9e2676d0856107da3be9c0a
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183311"
---
# <a name="set-up-cash-customers"></a>Definere kontantkunder
Du kan ikke opprette en faktura uten å oppgi et kundenummer. Dette gjelder også ved kontantsalg og selv om ikke har noe å registrere på en kundekonto.  

## <a name="to-set-up-a-cash-customer"></a>Slik definerer du kontantkunder  
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunde**, og velg deretter den relaterte koblingen.  
2.  Opprett et nytt **kundekort**. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).
3.  I feltet **Nr.** -feltet angir du for eksempel **Kontantsalg**.  
4.  I feltet **Navn** angir du for eksempel **Kontantsalg**.  
5.  På hurtigfanen **Fakturering** fyller du ut feltene **Bokføringsgruppe** og **Bokføringsgruppe - firma**.  

 Du har nå definert en kunde som har tilstrekkelig med opplysninger til å kunne faktureres.  

> [!NOTE]  
>  Du valgte kanskje en bokføringsgruppe som også brukes ved innenlandsk kredittsalg. Hvis du vil oppdatere separate data for kontantsalg, for eksempel, med en spesiell salgskonto eller samlekonto for kunde, kan du opprette ytterligere en bokføringsgruppe for dette formålet.  
>   
>  Du må angi et nummer for bokføringsgruppens samlekonto for kunde, selv om saldoen på denne kontoen alltid vil være 0 etter at du bokfører en faktura.  

## <a name="see-also"></a>Se også
[Håndtere fordringer](receivables-manage-receivables.md)  
[Registrere nye kunder](sales-how-register-new-customers.md)    
[Finans](finance.md)  

