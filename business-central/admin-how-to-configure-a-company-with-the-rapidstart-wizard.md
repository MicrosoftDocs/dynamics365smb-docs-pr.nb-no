---
title: Konfigurere et selskap med RapidStart-veiviseren | Microsoft-dokumentasjon
description: Du kan raskt konfigurere et nytt selskap du har opprettet, ved hjelp av konfigurasjonsveiviseren for RapidStart Services.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1b29412d166bd5b2225d780a0b0cee476874dcd0
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130855"
---
# <a name="configure-a-company-with-the-rapidstart-wizard"></a>Konfigurere et selskap med RapidStart-veiviseren
Du kan raskt konfigurere et nytt selskap du har opprettet, ved hjelp av konfigurasjonsveiviseren for RapidStart Services.

I fremgangsmåten nedenfor har du gitt kunden konfigurasjonspakken, som deretter installeres på datamaskinen. Kunden åpner det nye selskapet, som ikke inneholder noen kundedata. Du eller kunden følger deretter trinnene i RapidStart Services-veiviseren, som er beskrevet i denne fremgangsmåten, for å angi grunnleggende informasjon om selskapet. Veiviseren importerer konfigurasjonspakken og bruker deretter pakken på selskapet.  

## <a name="to-configure-a-new-company"></a>Slik konfigurerer du et nytt selskap:  
1. I rollesenteret for RapidStart Services-implementerer velger du handlingen **RapidStart-veiviser**.  
2. Utvid hurtigfanen **Trinn 1**, som inneholder generelle opplysninger om det nye firmaet. Angi den aktuelle informasjonen om det nye selskapet i feltene. Ett felt er obligatorisk: **Navn**. Resten av feltene er valgfrie.  
3. Utvid hurtigfanen **Trinn 2**, som inneholder kommunikasjons- og kontaktopplysninger for det nye firmaet. Angi den aktuelle informasjonen om det nye selskapet i feltene.
4. Utvid hurtigfanen **Trinn 3**, som inneholder bankkonto- og betalingsopplysninger for det nye firmaet. Angi den aktuelle informasjonen om det nye selskapet i feltene.  
5. Vis hurtigfanen **Trinn 4**. Velg **AssistEdit**-knappen for å velge konfigurasjonspakken du vil bruke. Navnet på konfigurasjonspakken vises. Deretter kan du utføre følgende handlinger, i oppført rekkefølge:  

    1. Bruk konfigurasjonen ved å velge handlingen **Bruk pakke**. Dette importerer konfigurasjonspakken og bruker alle databasedata i pakken samtidig.  

    2. Se gjennom konfigurasjonen etter at den er tatt i bruk. Med dette alternativet kan du se gjennom konfiguasjonsdetaljer og spørreskjemaer som er levert av partneren, og importere noen hoveddata som kreves for firmaet. Velg handlingen **Konfigurasjonsforslag**. Hvis du vil ha mer informasjon, kan du se [Fullføre konfigurasjonsspørreskjemaet](admin-gather-customer-setup-values.md#to-complete-the-configuration-questionnaire).  

6. Vis hurtigfanen **Trinn 5**. Angi hvilket rollesenter som skal være standard for det nye selskapet.  

    > [!IMPORTANT]  
    >  Ikke endre rollesenteret ditt før du har fullført konfigurasjonen av selskapet. Hvis du har flere oppsettdetaljer å vurdere og endre, bruker du først konfigurasjonsforslaget til å fortsette arbeidet. Gå deretter tilbake til veiviseren for å oppdatere rollesenterprofilen din, eller velg handlingen **Fullfør konfigurasjon**.

7. Velg **OK**-knappen.  
8. Du kan kontrollere at konfigurasjonsinformasjonen er brukt på det nye selskapet ved å velge ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.

Siden **Informasjon om selskapet** inneholder informasjon som du har angitt.   

Du har nå konfigurert selskapet og brukt data i det.  

## <a name="see-also"></a>Se også  
[Bruke konfigurasjoner for nye selskaper](admin-apply-configuration-to-new-companies.md)  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]