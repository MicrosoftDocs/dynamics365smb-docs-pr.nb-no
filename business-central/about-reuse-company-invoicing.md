---
title: Bruke fakturering og Business Central | Microsoft-dokumentasjon
description: Løsning for å få tilgang til Microsoft Invoicing når du har registrert deg for Dynamics 365 Business Central.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Invoicing, Office 365
ms.date: 04/30/2020
ms.author: bholtorf
ms.openlocfilehash: 7776cd01218f5959734173226574bb4a0d043153
ms.sourcegitcommit: 866f0e6ed9df3397072b9df838e31c3a1f4b626d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2020
ms.locfileid: "3333863"
---
# <a name="using-the-same-office-365-account-in-d365fin-and-microsoft-invoicing"></a>Bruke samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Når du registrerer deg for en prøveversjon med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du flytte over til en 30 dager evalueringsfase, du kan du starte et abonnement eller du kan slutte å bruke [!INCLUDE[d365fin](includes/d365fin_md.md)]. I alle tilfeller kan du på et eller annet ha sett noe kalt **Microsoft Invoicing** og klikket på det. Dette var en app som var en del av det som nå er Microsoft 365 Business Standard, og ble tidligere kalt Office 365 Business Premium-abonnement, så det er ikke alle som har sett denne flisen i Office 365-opplevelsen.  

Microsoft Invoicing er ikke lenger tilgjengelig, men hvis du må logge deg på Invoicing for å hente dataene, kan du se en melding om at du ikke får tilgang til Microsoft Invoicing fordi kontoen din brukes i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Det vises en lignende melding hvis du installerer mobilappen for fakturering.  

## <a name="workaround"></a>Løsning
Fakturering og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delt plattform. Dette innebærer at du gjenkjennes som en eksisterende bruker av [!INCLUDE[d365fin](includes/d365fin_md.md)] når du klikker på fakturering i Microsoft 365-administrasjonssenteret. Årsaken er at fakturering ikke kan bruke det samme selskapet som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Så du må logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og gi nytt navn til det eksisterende selskapet ditt, og deretter opprette et nytt selskap som du deretter kan bruke i Fakturering. Ingen data flyttes eller overskrives i denne løsningen.

### <a name="to-rename-your-company"></a>Slik endrer du navn på selskapet
1. Logg på [!INCLUDE[d365fin](includes/d365fin_md.md)].
2. I øvre høyre hjørne velger du **Innstillinger**-ikonet ![Innstillinger](media/ui-experience/settings_icon_small.png "Innstillinger-ikon for rollesenter"), og deretter velger du **Mine innstillinger**.
3. I feltet **Selskap** velger du et annet selskap.
4. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskaper**, og velg deretter den relaterte koblingen.  
5. På **Selskaper**-siden velger du **Rediger oversikt**.  
6. Endre navnet i *Mitt selskap*-posten til et annet navn.  

    Vent noen minutter. Vi kan foreta flere endringer i den underliggende databasen, og det tar litt tid.
7.  Når systemet er klart igjen, velger du **Opprett et nytt selskap**-knappen.  
8.  I dialogboksen som vises, angir du navnet som *Mitt selskap*, og velger **Produksjon - Bare oppsettsdata**-alternativet.  

Dette tar også flere minutter. Når prosessen er fullført, får du tilgang til fakturering som en del av Microsoft 365 Business Standard-opplevelsen. men bare til å eksportere data ettersom Invoicing-programmet er avskrevet.  

### <a name="what-about-my-data"></a>Hva med dataene mine?
Når du endrer navn på det opprinnelige Mitt selskap, får databasetabellene som lagrer dine eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data nye navn, men selve dataene røres ikke.  

Hvis du bruker både fakturering og [!INCLUDE[d365fin](includes/d365fin_md.md)], lagres dataene i to forskjellige beholdere (de to selskapene). Ingenting deles, slik at du må administrere kunder og varer i begge selskapene.  

## <a name="see-also"></a>Se også
[Vanlige spørsmål](across-faq.md)  
[Administrasjon](admin-setup-and-administration.md)  
