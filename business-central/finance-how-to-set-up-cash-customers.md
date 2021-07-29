---
title: Definere kontantkunder
description: Dette emnet beskriver trinnene som kreves for å definere fakturaen med et kundenummer for kunder som betaler kontant.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 9462b7bb887b5c4d2dcc0f602d5cd0fe57ccc1fb
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6442088"
---
# <a name="set-up-cash-customers"></a>Definere kontantkunder
Du kan ikke opprette en faktura uten å oppgi et kundenummer. Dette gjelder også ved kontantsalg og selv om ikke har noe å registrere på en kundekonto.  

## <a name="to-set-up-a-cash-customer"></a>Slik definerer du kontantkunder  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunde** og velg den relaterte koblingen.  
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



[!INCLUDE[footer-include](includes/footer-banner.md)]