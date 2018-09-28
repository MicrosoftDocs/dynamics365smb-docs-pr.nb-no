---
title: Tildelingsstatus og reparasjonsstatus | Microsoft-dokumentasjon
description: Finn ut mer om forholdet mellom reparasjonsstatusen til servicevarer og tildelingsstatusen til tildelingspostene for dem.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resources, allocation, status, repairs
ms.date: 10/01/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 014ede5232017bb090fa6cd33816064a6c4b99b8
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="allocation-status-and-repair-status-of-service-items"></a>Tildelingsstatusen og reparasjonsstatusen til servicevarene
Reparasjonsstatusen til servicevarer og tildelingsstatusen til tildelingsposter for servicevarene har en bestemt forbindelse i Service. Tildelingsstatusen endres når du endrer reparasjonsstatusen til servicevaren til **Ferdig** eller **Delvis vedlikeholdt**, og når du konverterer et servicetilbud til en serviceordre. Reparasjonsstatusen til servicevaren endres når du avbryter servicevaretildelingen eller tildeler servicevaren på nytt til en annen ressurs. Du kan vise reparasjonsstatusen til servicevarer i vinduet **Serviceoppgaver**, og du kan oppdatere reparasjonsstatusen i feltet **Reparasjonsstatuskode** i vinduet **Arbeidsordre**. Du kan vise tildelingsstatus i **Status**-feltet i vinduet **Ressurstildelinger**.  
  
## <a name="changing-repair-status"></a>Endre reparasjonsstatus  
Når du endrer reparasjonsstatusen til en servicevare på en servicevarelinje, søkes det etter en tilhørende tildelingspost for denne servicevaren med statusen **Aktiv**. Hvis det blir funnet en slik tildelingspost, oppdateres statusen på én av følgende måter:  
  
* Hvis du endrer reparasjonsstatusen til **Ferdig**, endres tildelingsstatusen fra **Aktiv** til **Ferdig**.  
* Hvis du endrer reparasjonsstatusen til **Delvis vedlikeholdt**, det vil si at deler av servicen er fullført, eller **Henvist**, det vil si at det er ikke utført service, endres tildelingsstatusen fra **Aktiv** til **Ny tildeling nødvendig**.  
* Når en serviceordretildelingspost opprettes som angir at ingen ressurs er fordelt, settes **Status**-feltet i vinduet **Ressursfordelinger** til **Ikke aktiv**.  
* Statusen for tildelingsposten settes til **Kansellert** når du tildeler den refererte servicevaren i serviceordretildelingsposten på nytt, noe som angir at den tildelte ressursen eller ressursgruppen ikke har forsøkt serviceoppgaven.  
  
Tildelingsstatusen gjenspeiler når vedlikeholdsprosessen er ferdig, eller når det er nødvendig med en annen ressurs for å fullføre servicen av servicevaren.  
  
## <a name="converting-service-quotes-to-service-orders"></a>Konvertere servicetilbud til serviceordrer  
Når du konverterer et servicetilbud til en serviceordre, oppdateres serviceordren, servicevarene i ordren samt tilhørende tildelingsposter på følgende måter:  
  
* Reparasjonsstatusen til servicevarene endres til **Første**.  
* Serviceordrestatusen endres til **I kø**.  
* Det søkes etter tildelingsposter for alle servicevarene i serviceordren, med status **Aktiv**. Hvis det blir funnet slike tildelingsposter, endres tildelingsstatusen fra **Aktiv** til **Ny tildeling nødvendig**.  
  
## <a name="canceling-allocations"></a>Avbryte tildelinger  
Når du avbryter en tildeling for en servicevare, oppdaterer [!INCLUDE[d365fin](includes/d365fin_md.md)] tildelingsstatusen til den tilhørende tildelingsposten fra **Aktiv** til **Ny tildeling nødvendig**.

Reparasjonsstatusen til servicevaren i tildelingsposten oppdateres på følgende måter:  
  
* Hvis reparasjonsstatusen er **Første**, endres reparasjonsstatusen til **Henvist** (ingen service er påbegynt).  
* Hvis reparasjonsstatusen er **I arbeid**, endres reparasjonsstatusen til **Delvis vedlikeholdt** (deler av servicen er fullført).  
  
## <a name="reallocating-an-active-allocation-entry"></a>Tildele en aktiv tildelingspost på nytt  
Når du tildeler en servicevare på nytt i en tildelingspost som er **Aktiv**, oppdateres tildelingsposten på følgende måter:  
  
* Hvis servicen ble startet mens tildelingen var **Aktiv** (det vil si hvis reparasjonsstatusen til servicevaren i posten var endret til **I arbeid**), endres tildelingsstatusen fra **Aktiv** til **Ferdig**.  
* Hvis servicen ikke ble startet da tildelingen var **Aktiv**, endres tildelingsstatusen fra **Aktiv** til **Avbrutt**.  
  
Reparasjonsstatusen til servicevaren i tildelingsposten oppdateres på samme måte som om du hadde avbrutt tildelingen:  
  
* Hvis reparasjonsstatusen er **Første**, endres reparasjonsstatusen til **Henvist** (ingen service er påbegynt).  
* Hvis reparasjonsstatusen er **I arbeid**, endres reparasjonsstatusen til **Delvis vedlikeholdt** (deler av servicen er fullført).  
  
Det opprettes en ny tildelingspost som inneholder den nye ressursen, og som har statusen **Aktiv**.  
  
## <a name="reallocating-a-service-item"></a>Tildele en servicevare på nytt  
Når du tildeler en servicevare på nytt i en tildelingspost med statusen **Ny tildeling nødvendig**, oppdateres tildelingsposten på følgende måter:  
  
* Hvis servicen ble startet mens tildelingen var **Aktiv** (det vil si hvis reparasjonsstatusen til servicevaren i posten var endret til **I arbeid**), endres tildelingsstatusen fra **Ny tildeling nødvendig** til **Ferdig**.  
* Hvis servicen ikke ble startet da tildelingen var **Aktiv**, endres tildelingsstatusen fra **Ny tildeling nødvendig** til **Avbrutt**.  
  
Det opprettes en ny tildelingspost som inneholder den nye ressursen, og som har statusen **Aktiv**.  
  
## <a name="see-also"></a>Se også  
[Definere ressurstildelinger](service-how-setup-resource-allocation.md)  
[Tildele ressurser](service-how-to-allocate-resources.md)  


