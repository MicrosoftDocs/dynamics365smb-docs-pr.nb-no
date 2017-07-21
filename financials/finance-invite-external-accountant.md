---
title: "Legge til den eksterne regnskapsføreren i Financials | Microsoft-dokumentasjon"
description: "Finn ut hvordan du kan invitere den eksterne regnskapsføreren til Dynamics 365 for Financials."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting
ms.date: 06/23/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 1b9f88f02b198ae8da0f3359a3ce7799b9535739
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="invite-your-external-accountant-to-your-included365finincludesd365finmdmd"></a>Invitere den eksterne regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)]
Hvis du bruker en ekstern regnskapsfører til å administrere regnskap og finansrapportering, kan du invitere regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at vedkommende kan arbeide med regnskapsdataene.

Når regnskapsføreren har fått tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], kan vedkommende bruke rollesenteret **Revisor**, som gir enkel tilgang til de mest relevante vinduene for arbeidet.  

> [!NOTE]  
>  Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, kan du se [Tilpasse Financials-opplevelsen](ui-experiences.md).  

## <a name="invite-your-accountant-to-your-included365finincludesd365finmdmd"></a>Invitere regnskapsføreren til [!INCLUDE[d365fin](includes/d365fin_md.md)]
I den nye versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] må en administrator legge til den eksterne regnskapsføreren i Active Directory-leieren for at du skal kunne invitere vedkommende. Fremgangsmåten for å gjøre dette er avhengig av kontotypen du brukte da du registrerte deg for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette emnet er basert på bruken av en Office 365-konto, som bruker Microsoft Azure Active Directory.  

> [!TIP]  
>  Vi anbefaler at du kontakter [!INCLUDE[d365fin](includes/d365fin_md.md)]-partneren din for å få hjelp.  

Hvis du har aktivert abonnementet på [!INCLUDE[d365fin](includes/d365fin_md.md)] og ikke lenger bruker evalueringsselskapet, har du en Azure Active Directory-leier. Administratoren eller [!INCLUDE[d365fin](includes/d365fin_md.md)]-partneren administrerer denne leieren i vinduet [Azure Portal](https://portal.azure.com). Det er her nye brukere legges til og lisenser brukes og fjernes. Hvis du vil ha mer informasjon, kan du se [Oversikt over Microsoft Azure Portal](https://docs.microsoft.com/en-us/azure/azure-portal-overview).  

### <a name="separate-license"></a>Egen lisens
En av lisenstypene for [!INCLUDE[d365fin](includes/d365fin_md.md)] er lisensen *Ekstern regnskapsfører*. Denne lisenstypen er beregnet på brukere som eksterne regnskapsførere. Dette betyr at du slipper å kjøpe en ekstra plass i Active Directory eller bruke en av de eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontiene på den eksterne regnskapsføreren. Hvis det gjeldende Office 365-abonnementet ditt omfatter ti brukere [!INCLUDE[d365fin](includes/d365fin_md.md)], og du bruker ti *Fullstendig bruker*-lisenser, kan systemansvarlig ganske enkelt legge til den eksterne regnskapsføreren som en gjestebruker i Azure Portal og tilordne denne brukeren til lisensen *Ekstern regnskapsfører* uten ekstra kostnad. Du kan imidlertid bare ha én bruker med lisensen *Ekstern regnskapsfører*. Hvis du vil legge til flere brukere, må du oppdatere Office 365-abonnementet tilsvarende.  

## <a name="see-also"></a>Se også
[Finans](finance.md)  
[Regnskapsføreropplevelser i Dynamics 365 for Financials](finance-accounting.md)  
[Financials for regnskapsførere på Microsoft.com](https://www.microsoft.com/en-us/dynamics365/financial-insights-for-accountants)  

