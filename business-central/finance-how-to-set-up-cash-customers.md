---
title: Definere kontantkunder | Microsoft-dokumentasjon
description: Dette emnet beskriver hvordan du definerer kunder som betaler kontant.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/11/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 93c28879417b12bc142c84c38c054828b380cc53
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-cash-customers"></a>Definere kontantkunder
Du kan ikke opprette en faktura uten å oppgi et kundenummer. Dette gjelder også ved kontantsalg og selv om ikke har noe å registrere på en kundekonto.  

## <a name="to-set-up-a-cash-customer"></a>Slik definerer du kontantkunder  
1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunde**, og velg deretter den relaterte koblingen.  
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


