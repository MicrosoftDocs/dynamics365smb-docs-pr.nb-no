---
title: "Definere foretrukne metoder for å sende salgsdokumenter | Microsoft-dokumentasjon"
description: "Beskriver hvordan du konfigurerer kundens foretrukne sendemetode for salgsdokumenter, for eksempel e-post, PDF-fil, elektronisk dokument og så videre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 974e0567b1207eb3dd2204f1d90e9b65061cbc54
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-document-sending-profiles"></a>Definere en profil for dokumentsending
Du kan definere hver kunde med en foretrukket metode for sending av salgsdokumenter, slik at du ikke trenger å velge et alternativ for sending hver gang du velger handlingen **Bokfør og send**.

I vinduet **Profiler for dokumentsending** definerer du ulike sendingsprofiler som du kan velge fra feltet **Profil for dokumentsending** på et kundekort. Du kan merke av for **Standard** for å angi at profilen for dokumentsending er standardprofilen for alle kunder, bortsett fra kunder der feltet **Profil for dokumentsending** er fylt ut med en annen sendingsprofil.

Når du velger handlingen **Bokfør og send** i et salgsdokument, viser dialogboksen **Bokfør og send bekreftelse** sendingsprofilen som brukes, enten den som er satt opp for kunden, eller standarden for alle kunder. I dialogboksen kan du endre sendingsprofilen for salgsdokumentet. Hvis du vil ha mer informasjon, kan du se [Fakturere salg](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Slik definerer du en profil for dokumentsending:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Profiler for dokumentsending**, og velg deretter den relaterte koblingen.
2. I vinduet **Profiler for dokumentsending** velger du handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Slik angir du en sendingsprofil på et kundekort:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kortet til kunden som du vil definere en sendingsprofil for.
3. Velg en profil i feltet i feltet **Profiler for dokumentsending**, som du har satt opp som beskrevet i forrige fremgangsmåte.

## <a name="see-also"></a>Se også
[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

