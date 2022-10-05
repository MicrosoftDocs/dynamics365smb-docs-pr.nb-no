---
title: Begrense og tillate bruk av en post
description: Hvis du vil hindre at en post brukes, kan du innlemme to arbeidsflytsvar i en arbeidsflyt som styrer bruken av posten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 09/08/2022
ms.author: edupont
ms.openlocfilehash: 2542dac4eba91d0d6d7dd3c773b19e1f6fd235a5
ms.sourcegitcommit: 9049f75c86dea374e5bfe297304caa32f579f6e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/23/2022
ms.locfileid: "9585976"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begrense og tillate bruk av en post

Hvis du vil hindre at en post brukes i bestemte aktiviteter, for eksempel før oppføringen er godkjent, kan du innlemme to arbeidsflytsvar i arbeidsflyten som styrer bruken av posten. Ett arbeidsflytsvar begrenser bruken av posten som definert av arbeidsflythendelsen og -betingelsene. Det andre arbeidsflytsvaret tillater bruken av posten som definert av arbeidsflythendelsen og -betingelsene. Det finnes to svar i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] for dette formålet: **Legg til postbegrensning** og **Fjern postbegrensning**.

> [!NOTE]  
> Standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] tilbyr støtte for å forhindre at en post posteres, eksporteres som en betaling og skrives ut som en sjekk. For å støtte andre begrensninger må Microsoft-partneren tilpasse programkoden.  

> [!NOTE]  
> Arbeidsflytfunksjonaliteten for å begrense poster fra å brukes, er ikke relatert til funksjonaliteten for å blokkere vare, kunde og leverandørposter fra å bli bokført.

Følgende fremgangsmåte beskriver hvordan du begrenser bestillinger fra å posteres før de er godkjent. Den nye arbeidsflyten skal baseres på den eksisterende malen for *arbeidsflyt for kjøpsfakturagodkjenning*.  

## <a name="create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Opprett et arbeidsflyttrinn som begrenser postering av ikke-godkjente bestillinger

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. På siden **Arbeidsflyter** velger du **Ny arbeidsflyt fra mal**-handlingen. Finn ut mer under [Opprett arbeidsflyter fra arbeidsflytmaler](across-how-to-create-workflows-from-workflow-templates.md).
3. På siden **Arbeidsflytmaler** velger du malen kalt *Arbeidsflyt for bestillingsfaktura*.  

   Legg merke til at de to første trinnene i arbeidsflyten er om å begrense og deretter tillate bruk av kjøpsfakturaer. Endre hendelsensbetingelsen på det første trinnet i den nye arbeidsflyten for å angi at den gjelder for bestillinger.  
4. I hurtigfanen **Arbeidsflyttrinn** velger du **Ved forutsetning av**-feltet for det første trinnet, og deretter velger du **Ordre** for **Dokumenttype**.  
5. Fortsette med å redigere, slette eller legge til andre trinn i arbeidsflyten for å gjenspeile en forretningsprosess som begynner ved å forhindre at ikke-godkjente bestillinger posteres.  

## <a name="see-also"></a>Se også

[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
