---
title: Konfigurere arbeidstimer og servicetimer | Microsoft-dokumentasjon
description: "Du kan angi de vanlige servicearbeidstimene i selskapet. Disse servicetimene brukes til å beregne responsdatoen og -klokkeslettet for serviceordrer og -tilbud, og til å sende advarsler om responstid."
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
ms.openlocfilehash: 630875f80f4107522962c79734284569cbc2b6f7
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-work-hours-and-service-hours"></a>Konfigurere arbeidstimer og servicetimer
Med et servicesystem kan du vanligvis spore ressurstimer og serviceordrestatus for å prognostisere arbeidsmengder og servicebehov. [!INCLUDE[d365fin](includes/d365fin_md.md)] har innebygde verktøy du kan tilpasse for å registrere denne typen informasjon.  
  
Etter at du har angitt selskapets standard servicetimer, kan du beregne responstiden for serviceordrer eller sende advarsler eller varsler når det kommer serviceanrop. Varslingsfunksjonen implementeres sammen med jobbskjemaet.   
  
Når du arbeider med en serviceordre, vil du oppdaterer statusen slik at du kan overvåke fremdriften. Serviceordrestatusen gjenspeiler reparasjonsstatusen til alle servicevarene i serviceordren. Hvis du vil ha mer informasjon, kan du se [Forstå serviceordre- og reparasjonsstatus](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>Slik definerer du Standard servicetimer  
Du bruker vinduet **Standard servicetimer** til å definere selskapets normale antall servicearbeidstimer. Disse servicetimene brukes til å beregne responsdatoen og -klokkeslettet for serviceordrer og -tilbud, og til å sende advarsler om responstid. Standard servicetimer brukes for servicekontrakter hvis du ikke angir spesifikke servicetimer for en kontrakt.  
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Standard servicetimer**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Hvis du lar linjene i vinduet **Standard servicetimer** stå tomme, bruker programmet 24 timer som standardverdi, som bare er gjelder for arbeidsdager fra kalenderen.  
  
## <a name="to-set-up-work-hour-templates"></a>Definere arbeidstidsmaler
Du kan bruke vinduet **Arbeidstidsmal** til å definere maler som inneholder vanlige arbeidstider i selskapet. Du kan for eksempel opprette maler for heltidsteknikere og deltidsteknikere. Du kan bruke arbeidstidsmaler når du legger til kapasitet i ressurser.  
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Arbeidstidsmaler**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Når du har angitt arbeidstimer for hver dag, beregnes verdien i feltet **Sum per uke** automatisk.  

## <a name="to-set-up-contract-specific-service-hours"></a>Slik definerer du kontraktsspesifikke servicetimer  
Du kan bruke vinduet **Servicetimer** til å definere spesifikke servicetimer timer for kunden som eier servicekontrakten. Servicetimer brukes til å beregne responsdatoen og -tiden for serviceordrer og -tilbud som hører til servicekontrakten.  
  
Hvis du ikke definerer spesifikke servicetimer for servicekontrakten, brukes standard servicetimer for servicekontraktene.  
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Servicekontrakter**, og velg deretter den relaterte koblingen.  
2. Åpne servicekontrakten du vil definere spesifikke servicetimer for, og velg **Servicetimer**.  
4. Hvis du vil definere servicetimer basert på standard servicetimer, velger du handlingen **Kopier std. servicetimer**.  
5. Rediger feltene i servicetimepostene. Sett inn eller slett poster for å definere servicetimer for kontrakten. Merk at feltene **Dag**, **Starttidspunkt** og **Sluttidspunkt** kreves for hver linje.  
6. Hvis du vil at servicetimene skal gjelde fra en bestemt dato, fyller du ut feltet **Startdato**.  
7. Hvis du vil at servicetimene skal gjelde i ferier, setter du en hake i avmerkingsboksen i feltet **Gyldig i ferier**.  

## <a name="see-also"></a>Se også  
[Forstå tildelingsstatus og reparasjonsstatus](service-allocation-status-and-repair-status.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  
[Forstå serviceordre- og reparasjonsstatus](service-order-repair-status.md)  

