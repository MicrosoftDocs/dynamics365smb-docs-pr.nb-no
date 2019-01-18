---
title: Bruke fakturering og Business Central | Microsoft-dokumentasjon
description: "Løsning for å få tilgang til Microsoft Invoicing når du har registrert deg for Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 3e2357766d514f30e42869a4f10ede1e66a6fec1
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Bruke samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing
Når du registrerer deg for en prøveversjon med [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du flytte over til en 30 dager evalueringsfase, du kan du starte et abonnement eller du kan slutte å bruke [!INCLUDE[d365fin](includes/d365fin_md.md)]. I alle tilfellene, hvis du logger på Office-portalen, kan du se en rute som kalles **Business Center** og klikke den. Dette er en del av Office 365 Business Premium-abonnementet, så ikke alle ser denne ruten i Office-portalen.  

Hvis du ikke har tilgang til forretningssenteret, ser du en del kalt **Fakturering**. Hvis du åpner denne delen, vises en melding om at du ikke har tilgang til Microsoft Invoicing fordi kontoen brukes i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Det vises en lignende melding hvis du installerer mobilappen for fakturering.  

## <a name="workaround"></a>Løsning
Fakturering og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en delt plattform. Dette innebærer at du gjenkjennes som en eksisterende bruker av [!INCLUDE[d365fin](includes/d365fin_md.md)] når du klikker på fakturering i forretningssenteret. Årsaken er at fakturering ikke kan bruke det samme selskapet som [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Så du må logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og gi nytt navn til det eksisterende selskapet ditt, og deretter opprette et nytt selskap som du deretter kan bruke i fakturering. Ingen data flyttes eller overskrives i denne løsningen.

### <a name="to-rename-your-company"></a>Slik endrer du navn på selskapet
1.  Logg på [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Selskaper**, og velg deretter den relaterte koblingen.  
3.  På **Selskaper**-siden velger du **Rediger oversikt**-knappen.  
4.  Endre navnet i *Mitt selskap*-posten til et annet navn.  

    Vent noen minutter. Vi kan foreta flere endringer i den underliggende databasen, og det tar litt tid.
5.  Når systemet er klart igjen, velger du **Opprett et nytt selskap**-knappen.  
6.  I dialogboksen som vises, angir du navnet som *Mitt selskap*, og velger **Produksjon - Bare oppsettsdata**-alternativet.  

Dette tar også flere minutter. Når prosessen er fullført, får du tilgang til fakturering som en del av Office 365 Business Premium-opplevelsen.  

### <a name="what-about-my-data"></a>Hva med dataene mine?
Når du endrer navn på det opprinnelige Mitt selskap, får databasetabellene som lagrer dine eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data nye navn, men selve dataene røres ikke.  

Hvis du bruker både fakturering og [!INCLUDE[d365fin](includes/d365fin_md.md)], lagres dataene i to forskjellige beholdere (de to selskapene). Ingenting deles, slik at du må administrere kunder og varer i begge selskapene.  

## <a name="see-also"></a>Se også
[Vanlige spørsmål](across-faq.md)  
[Administrasjon](admin-setup-and-administration.md)  

