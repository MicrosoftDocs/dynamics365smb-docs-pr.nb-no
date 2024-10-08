---
title: Definere kontantkunder
description: Dette emnet beskriver trinnene som kreves for å definere fakturaen med et kundenummer for kunder som betaler kontant.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '21, 22'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-cash-customers"></a>Definere kontantkunder

Du kan ikke opprette en faktura uten å oppgi et kundenummer. Dette gjelder også ved kontantsalg og selv om ikke har noe å registrere på en kundekonto.  

## <a name="to-set-up-a-cash-customer"></a>Slik definerer du kontantkunder

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kunde** og velg den relaterte koblingen.  
2. Opprett et nytt **kundekort**. Hvis du vil ha mer informasjon, kan du se [Registrere nye kunder](sales-how-register-new-customers.md).
3. I feltet **Nr.** -feltet angir du for eksempel **Kontantsalg**.  
4. I feltet **Navn** angir du for eksempel **Kontantsalg**.  
5. På hurtigfanen **Fakturering** fyller du ut feltene **Bokføringsgruppe** og **Bokføringsgruppe - firma**.  

 Du har nå definert en kunde som har tilstrekkelig med opplysninger til å kunne faktureres.  

> [!NOTE]  
> Du valgte kanskje en bokføringsgruppe som også brukes ved innenlandsk kredittsalg. Hvis du vil oppdatere separate data for kontantsalg, for eksempel, med en spesiell salgskonto eller samlekonto for kunde, kan du opprette ytterligere en bokføringsgruppe for dette formålet.  
>
> Du må angi et nummer for bokføringsgruppens samlekonto for kunde, selv om saldoen på denne kontoen alltid vil være 0 etter at du bokfører en faktura.  

## <a name="see-also"></a>Se også

[Håndtere fordringer](receivables-manage-receivables.md)  
[Registrer nye kunder](sales-how-register-new-customers.md)
[Finans](finance.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
