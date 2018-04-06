---
title: Arbeide med serviceoppgaver | Microsoft-dokumentasjon
description: "Når du har opprettet en serviceordre eller -tilbud, registrert servicevarelinjer og tildelt ressurser til servicevarene i ordren eller tilbudet, kan du begynne å reparere og vedlikeholde servicevarene."
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
ms.openlocfilehash: 1e6db49370a1fc2d9a2bb99e55d00ed69908d703
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="work-on-service-tasks"></a>Arbeide med serviceoppgaver
Når du har opprettet en serviceordre eller -tilbud, registrert servicevarelinjer og tildelt ressurser til servicevarene i ordren eller tilbudet, kan du begynne å reparere og vedlikeholde servicevarene.  

Ved hjelp av **Serviceoppgave**-vinduet i [!INCLUDE[d365fin](includes/d365fin_md.md)] får du en oversikt over alle servicevarene som trenger tilsyn. Tenk på vinduet som et servicekontrollpanel der du kan se hvilke ordrer som venter, finne og registrere reservedeler og holde lageret oppdatert.  
  
Hvis du vil spore endringer og få en grafisk fremstilling av servicevirksomheten, kan du bruke statistikkverktøyene i [!INCLUDE[d365fin](includes/d365fin_md.md)] til å generere diagrammer og analyse raskt og automatisk.  
  
## <a name="to-work-on-a-service-task"></a>Slik arbeider du med en serviceoppgave  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceoppgaver**, og velg deretter den relaterte koblingen. 
2. Hvis du ønsker en oversikt over serviceoppgaver en bestemt ressurs eller ressursgruppe er tildelt til, fyller du ut feltet **Ressursfilter** eller **Ressursgruppefilter** og trykker Enter.  
3. Hvis du ønsker en oversikt over serviceoppgaver med en bestemt responsdato, eller responsdato innen en bestemt tidsperiode, fyller du ut feltet **Responsdatofilter** og trykker Enter.  
4. Hvis du ønsker en oversikt over serviceoppgaver med en bestemt tildelingsstatus eller reparasjonsstatus, fyller du ut feltet **Filter for tildelingsstatus** eller **Filter for repar.statuskode** og trykker Enter.  
5. Velg serviceoppgaven du vil arbeide med. I fanebladet **Naviger**, under **Serviceoppgaver**, velger du **Arbeidsordre**. Vinduet **Arbeidsordre** åpnes.  
6. Registrer standardtekst, reservedeler, ressurstimer og kostnader etter behov med de tilsvarende alternativene i **Type**-feltet: <Blank>, **Vare**, **Ressurs** og **Kostnad**.  
7. Velg den aktuelle statusen i **Reparasjonsstatus**-feltet.  
  
   > [!NOTE]  
   >  Fyll ut feltet **Reparasjonsstatus** med statusen **Ferdig** eller **Delvis vedlikeholdt** hvis vedlikeholdet av servicevaren er ferdig eller en annen ressurs fortsetter vedlikeholdet. Statusen **Ferdig** eller **Ny tildeling nødvendig** angis automatisk for tildelingsposten som tilsvarer servicevaren.  

## <a name="to-register-service-operations"></a>Slik registrerer du serviceoperasjoner  
Når du utfører en service i en serviceordre, kan du spesifisere detaljer om brukte varer, påløpt kost og tidsbruk. Dataene du angir, lagres i vinduet **Servicevareskjema**. Du kan oppdatere dataene etter behov. 
   
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne serviceordren du vil registrere service for, og velg varelinjen.  
3. Velg **Handlinger**, **Linje** og **Arbeidsordre**.  
4. På linjene spesifiserer du brukte varer, påløpt kost og tidsbruk for service.  
  
   > [!NOTE]  
   >  Du kan også registrere service direkte i servicelinjene som er koblet til serviceordren.  
  
## <a name="to-register-spare-parts"></a>Slik registrerer du reservedeler  
Når du arbeider med servicevarer i serviceordrer, kan det hende du må bruke reservedeler for servicen. Følgende fremgangsmåte viser hvordan du registrerer reservedelene du bruker i vinduet **Servicevareskjema**.  
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceoppgaver**, og velg deretter den relaterte koblingen. 
2. Velg linjen som inneholder den aktuelle servicevaren, og velg deretter handlingen **Arbeidsordre**.  
3. Angi en ny servicelinje.  
4. I feltet **Type** velger du **Vare**.  
5. I feltet **Nr.** velger du den aktuelle reservedelen.  
6. I feltet **Antall** angir du hvor mange varer du skal bruke.  
  
 Du kan bruke en lignende fremgangsmåte til å registrere reservedeler på siden **Servicelinjer**, som du kan åpne på siden **Serviceordre**.  
  
## <a name="to-register-spare-parts-from-a-service-order"></a>Registrere reservedeler fra en serviceordre  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Åpne serviceordren du vil registrere reservedeler for.  
3. Velg linjen som inneholder den aktuelle servicevaren. Velg **Handlinger**, **Ordre** og deretter **Servicelinjer**.  
4. angi en ny servicelinje.  
  
## <a name="to-replace-a-service-item-or-a-service-item-component"></a>Erstatte en servicevare eller servicevarekomponent  
Når du gir service til en servicevare som består av komponenter, kan det hende du må erstatte en defekt komponent med en ny. Hver gang du angir en reservedel for en servicevare med komponenter, kan du velge mellom å erstatte en komponent eller å opprette en ny. Den nye varen registreres ikke som en komponent i servicevaren før du bokfører denne servicelinjen eller serviceordren. 
    
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceoppgaver**, og velg deretter den relaterte koblingen. 
2. Velg linjen som inneholder servicevaren, og velg deretter handlingen **Arbeidsordre**.  
3. Angi en ny servicelinje.  
4. I feltet **Type** velger du **Vare**.  
5. I feltet **Nr.** velger du komponenten du vil erstatte.  
6. Trykk **Enter**. Det vises en dialogboks med tre alternativer: **Erstatt komponent**, **Ny komponent** og **Ignorer**. Tabellen nedenfor beskriver alternativene.  
  
    |Alternativ | Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Erstatt komponent**|Endrer statusen til komponenten du erstatter, til ikke aktiv, og den vises på oversikten over erstattede komponenter for servicevaren.|  
    |**Ny komponent**|Angir den nye komponenten på oversikten over komponenter til servicevaren.|  
    |**Ignorer**|Endrer ingenting i oversikten over komponenter til servicevaren.|  
  
7. Velg **Erstatt komponent**.  
8. Velg komponenten du erstatter, og velg deretter **OK**.  

## <a name="to-change-the-response-time-for-a-service-item-line"></a>Slik endrer du responstiden for en servicevarelinje  
Når du registrerer en servicevarelinje i en serviceordre eller et tilbud, avhengig av om servicevaren er i en servicekontrakt, angis automatisk responstid i timer, og responsdatoen og -tiden beregnes i henhold til denne. Du kan endre responstiden i timer, og responsdatoen og -tiden hvis du har behov for det.  

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceordrer** eller **Servicekontrakttilbud**, og velg deretter den relaterte koblingen.  
2. Velg serviceordren eller tilbudet for å åpne kortet.  
3. Angi nye responstimer eller ny responsdato og responstid i feltet **Responstid (timer)** eller i feltene **Responsdato** og **Responstid** på servicevarelinjen du vil endre responstid for.  

## <a name="to-register-faultresolution-codes"></a>Slik registrerer du feil-/løsningskoder  
Når du har reparert en servicevare, kan du registrere både feilkoden og løsningskoden for varen ved å velge en kombinasjon fra eksisterende forhold mellom feil-/løsningskoder. Feil- og løsningskoder vises nå i tilhørende felt i vinduet **Servicevareskjema**. Du kan også registrere kodene direkte i dette vinduet.  
    
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Serviceoppgaver**, og velg deretter den relaterte koblingen. 
2. Velg linjen som inneholder den aktuelle servicevaren, og velg deretter handlingen **Arbeidsordre**.  
3. På siden **Arbeidsordre** velger du **Forhold ml. feil-/løsningskoder**. Vinduet **Forhold ml. feil-/løsningskoder** åpnes.  
  
  >  [!Note]
  >  Du angir filtre i relasjonene som vises i vinduet, ved å kopiere servicevaregruppen og feilkodene fra vinduet **Servicevareskjema**.  
  
4. Fyll ut linjen. Velg riktig kombinasjon av feil- og løsningskoder, og velg deretter **OK** for å kopiere den til servicevaren. Hvis det ikke finnes en rett kombinasjon, kan du opprette en ny kombinasjon i vinduet.  

## <a name="see-also"></a>Se også  
[Definere feilrapportering](service-how-setup-fault-reporting.md)
[Tildelingsstatus og reparasjonsstatus](service-allocation-status-and-repair-status.md)  
[Servicebokføring](service-service-posting.md)  


