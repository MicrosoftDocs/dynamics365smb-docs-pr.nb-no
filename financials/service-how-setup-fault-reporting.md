---
title: "Definere feilrapportering i servicehåndtering | Microsoft-dokumentasjon"
description: Finn ut hvordan du definerer feilrapporteringsprosesser.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 19a377f9c4a41bee6aecc182774f884b1ead36ad
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-fault-reporting"></a>Definere feilrapportering
Feilrapportering lar deg opprette standarder for å registrere feilinformasjon for servicevarer. Du kan for eksempel angi hva problemet er, hvilke symptomene du ser, årsaken til problemet og hvordan du løse det.  

Feilkoder beskriver de vanligste servicevarefeilene eller handlingene som er utført på servicevarer. Avhengig av nivået på feilrapportering i selskapet, kan det også hende du må definere koder for feilområde og symptomkoder før du definerer feilkoder. Feilområdene beskriver områder for servicevarefeil. Feilårsakskoder beskriver årsaken til servicevarefeil og eventuelt å utelate garanti- og kontraktrabatter. Det kan for eksempel hende du vil utelate garanti- og kontraktrabatter hvis kunden på en eller annen måte var ansvarlig for feilen i servicevaren. Du tilordner feilårsakskoder til serviceordrer. Hvis du vil ha mer informasjon, kan du se [Arbeide med serviceoppgaver](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a>Angi det generelle nivået å bruke for feilrapportering
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Serviceoppsett**, og velg deretter den relaterte koblingen. 
2. I feltet **Feilrapporteringsnivå** velger du ett av alternativene som er beskrevet i tabellen nedenfor.  
  
    |**Feilnivå**|**Beskrivelse**|  
    |------------|-------------|  
    |Ingen | Ingen rapporteringskoder brukes.|  
    |Feil | Kodene er oppført i **Feilkoder**-tabellen. Disse kodene identifiserer servicevarefeil eller handlinger som skal utføres på servicevarer. Du kan samle relaterte koder i grupper med verdien **Feilområde - kode**.|  
    |Feil + Symptom | Du angir en kombinasjon av koder i tabellene **Feilkoder** og **Symptomkoder**. Typiske symptomkoder omfatter indikatorer som en kunde kan bruke til å beskrive et problem, for eksempel støy eller kvalitet.|  
    |Feil + Symptom + Område. | Du bruker koder for feil, symptomer og feilområde som en implementering av det internasjonale reparasjonskodingssystemet (IRIS).|  
  
Når du skal fullføre definisjonen av feilrapportering, kan du også angi hvilke reparasjoner eller løsninger som er tilknyttet en feil eller defekt. Du definerer på siden **Forhold ml. feil-/løsningskoder**, der du angir kombinasjoner av koder for servicevaregruppen til servicevaren som du åpnet vinduet, og antall forekomster av hver enkelt.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Opprette relasjoner mellom feilkode og løsningskode
<!--this needs to go in a working with topic-->
Hvis du vil kunne vise de vanligste reparasjonsmåtene for bestemte varefeil når du gir service til varene, må du samle opplysninger om forhold mellom feil-/løsningskoder. Bruk kjørselen **Sett inn forh. ml. feil/løsn.** til å finne alle kombinasjoner av feil- og løsningskoder i bokførte serviceordrer, og registrer dem på siden **Forhold ml. feil-/løsningskoder**. 
  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Sett inn forh. ml. feil/løsn.**, og velg deretter den relaterte koblingen.  
2. Angi datoer for å definere perioden som du vil skal være med i kjørselen.  
3. Merk av for **Forbindelse basert på servicevaregruppe** for å gruppere forbindelsene etter servicevaregruppe.  
4. Merk av for **Behold manuelt innsatte poster** hvis du vil beholde postene som allerede er satt inn manuelt på siden **Forhold ml. feil-/løsningskoder**.  

## <a name="see-also"></a>Se også
[Konfigurere servicehåndtering](service-setup-service.md)  
[Servicehåndtering](service-service.md)  

