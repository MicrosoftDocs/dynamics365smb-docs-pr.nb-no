---
title: Begrense og tillate bruk av en post | Microsoft-dokumentasjon
description: "Hvis du vil hindre at en post brukes i bestemte aktiviteter, for eksempel før oppføringen er godkjent, kan du innlemme to arbeidsflytsvar i en arbeidsflyt som styrer bruken av posten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begrense og tillate bruk av en post
Hvis du vil hindre at en post brukes i bestemte aktiviteter, for eksempel før oppføringen er godkjent, kan du innlemme to arbeidsflytsvar i en arbeidsflyt som styrer bruken av posten. Ett arbeidsflytsvar vil begrense bruken av posten som definert av arbeidsflythendelsen og -betingelsene. Et nytt arbeidsflytsvar vil tillate bruken av posten som definert av arbeidsflythendelsen og -betingelsene. Det finnes to svar i den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] for dette formålet: **Begrens bruk av en post.** og **Tillat bruk av en post.**.

> [!NOTE]  
>  Den generelle versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] tilbyr støtte for å forhindre at en post posteres, eksporteres som en betaling og skrives ut som en sjekk. For å støtte andre begrensninger må Microsoft-partneren tilpasse programkoden.  

> [!NOTE]  
>  Arbeidsflytfunksjonaliteten for å begrense poster fra å brukes, er ikke relatert til funksjonaliteten for å blokkere vare, kunde og leverandørposter fra å bli bokført.

Følgende fremgangsmåte beskriver hvordan du begrenser bestillinger fra å posteres før de er godkjent. Den nye arbeidsflyten skal baseres på den eksisterende arbeidsmalen for arbeidsflyt for kjøpsfakturagodkjenning.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Slik oppretter du et arbeidsflyttrinn som begrenser postering av ikke-godkjente bestillinger:  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.  
2. I **Arbeidsflyter**-vinduet oppretter du en ny arbeidsflyt kalt Arbeidsflyt for bestillingsgodkjenning. Hvis du vil ha mer informasjon, kan du se [Opprette arbeidsflyter](across-how-to-create-workflows.md).  
3. Velg handlingen **Kopier fra arbeidsflytmal**.  
4. Velg **Arbeidsflytkode for kilde**-feltet og velg deretter arbeidsmalen Arbeidsflyt for kjøpsfakturagodkjenning i **Arbeidsflytmaler**-vinduet.  

     Legg merke til at de to første trinnene i arbeidsflyten er om å begrense og deretter tillate bruk av kjøpsfakturaer. Fortsette å endre hendelsensbetingelsen på det første trinnet i den nye arbeidsflyten for å angi at den gjelder for bestillinger.  
5. I hurtigfanen **Arbeidsflyttrinn** velger du **Hendelsesvilkår**-feltet, og deretter velger du **Ordre** for **Dokumenttype**.  
6. Fortsette med å redigere, slette eller legge til andre trinn i arbeidsflyten for å tilpasse til en forretningsprosess som begynner ved å forhindre at ikke-godkjente bestillinger posteres.  

## <a name="see-also"></a>Se også  
[Opprette arbeidsflyter](across-how-to-create-workflows.md)   
[Arbeidsflyt](across-workflow.md)   

