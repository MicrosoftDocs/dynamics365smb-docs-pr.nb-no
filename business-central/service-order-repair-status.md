---
title: Definere statuser for serviceordrer og reparasjoner | Microsoft-dokumentasjon
description: Du må definere ni alternativer for reparasjonsstatus som identifiserer fremdriften av reparasjon og vedlikehold på servicevarer i serviceordrer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Definere statuser for serviceordrer og reparasjoner

Du må definere ni alternativer for reparasjonsstatus som identifiserer fremdriften av reparasjon og vedlikehold på servicevarer i serviceordrer. Du må definerer minst ni alternativer for reparasjonsstatus som identifiserer situasjoner eller handlinger som er iverksatt under vedlikehold av servicevarer.  

Du kan angi prioritetsnivå for alternativene for serviceordrestatus. De fire prioritetene er **Høy**, **Middels høy**, **Middels lav** og **Lav**.  

Når du endrer reparasjonsstatusen til en servicevare i en serviceordre, oppdateres serviceordrestatusen. Reparasjonsstatusen til hver enkelt servicevare er knyttet til serviceordrestatusen. Hvis servicevarene er koblet til to eller flere alternativer for serviceordrestatus, velges serviceordrestatusen med høyest prioritet.  

Før du kan definere en reparasjonsstatus, må du definere servicestatusprioritet.

## <a name="to-set-up-service-status-priorities"></a>Slik definerer du servicestatusprioritet

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceordrestatus**, og velg deretter den relaterte koblingen.  
2. Velg serviceordrestatusen du vil angi en prioritet for.  
3. I feltet **Prioritet** velger du prioriteten du vil ha for denne serviceordrestatusen.  

Gjenta trinnene 2 og 3 til du har angitt prioriteten for hvert enkelt av de fire statusalternativene: **Venter**, **I arbeid**, **Ferdig** og **Avvent**.  

## <a name="to-set-up-a-repair-status"></a>Slik definerer du reparasjonsstatus

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Reparasjonsstatus** og velg deretter den relaterte koblingen.
2. Opprett en ny reparasjonsstatus.  
3. Fyll ut feltene **Kode** og **Beskrivelse**.  
4. I **Serviceordrestatus**-feltet velger du ordrestatusen å knytte reparasjonsstatusen til. **Prioritet**-feltet viser prioriteten til serviceordrestatusen du har valgt.  
5. Velg en reparasjonsstatus. Du kan bare velge én. En reparasjonsstatus kan ikke kobles til mer enn ett reparasjonsstatusalternativ.  
6. Velg feltet **Bokføring tillatt** hvis du vil kunne bokføre serviceordrer som omfatter servicevarer, med reparasjonsstatusen.  
7. Merk av for **I kø-status tillatt** for å tillate manuell endring av alternativet for serviceordrestatusen til alternativet **I kø** i serviceordrer som omfatter servicevarer med denne reparasjonsstatusen.  
8. Merk av for **I arbeid-status tillatt**, **Ferdig-status tillatt** og **Avvent-status tillatt** på samme måte.

Gjenta disse trinnene for hvert enkelt alternativ for reparasjonsstatusen du vil opprette.

## <a name="see-also"></a>Se også

[Serviceordrestatus og reparasjonsstatus](service-service-order-status-and-repair-status.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
