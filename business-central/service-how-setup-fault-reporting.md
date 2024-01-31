---
title: Definere feilrapportering i servicehåndtering
description: Feilrapportering lar deg opprette standarder for å registrere feilinformasjon for servicevarer med feilkoder og mer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Konfigurere feilrapportering
Feilrapportering lar deg opprette standarder for å registrere feilinformasjon for servicevarer. Du kan for eksempel angi hva problemet er, hvilke symptomene du ser, årsaken til problemet og hvordan du løse det.  

Feilkoder beskriver de vanligste servicevarefeilene eller handlingene som er utført på servicevarer. Avhengig av nivået på feilrapportering i selskapet, kan det også hende du må definere koder for feilområde og symptomkoder før du definerer feilkoder. Feilområdene beskriver områder for servicevarefeil. Feilårsakskoder beskriver årsaken til servicevarefeil og eventuelt å utelate garanti- og kontraktrabatter. Det kan for eksempel hende du vil utelate garanti- og kontraktrabatter hvis kunden på en eller annen måte var ansvarlig for feilen i servicevaren. Du tilordner feilårsakskoder til serviceordrer. Hvis du vil ha mer informasjon, kan du se [Arbeide med serviceoppgaver](service-how-to-work-on-service-tasks.md).  

## Angi det generelle nivået for feilrapportering
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Serviceoppsett**, og velg deretter den relaterte koblingen.
2. I feltet **Feilrapporteringsnivå** velger du ett av alternativene som er beskrevet i tabellen nedenfor.  

    |**Feilnivå**|**Beskrivelse**|  
    |------------|-------------|  
    |Ingen | Ingen rapporteringskoder brukes.|  
    |Feil | Kodene er oppført i **Feilkoder**-tabellen. Disse kodene identifiserer servicevarefeil eller handlinger som skal utføres på servicevarer. Du kan samle relaterte koder i grupper med verdien **Feilområde - kode**.|  
    |Feil + Symptom | Du angir en kombinasjon av koder i tabellene **Feilkoder** og **Symptomkoder**. Typiske symptomkoder omfatter indikatorer som en kunde kan bruke til å beskrive et problem, for eksempel støy eller kvalitet.|  
    |Feil + Symptom + Område. | Du bruker koder for feil, symptomer og feilområde som en implementering av det internasjonale reparasjonskodingssystemet (IRIS).|  

Når du skal fullføre definisjonen av feilrapportering, kan du også angi hvilke reparasjoner eller løsninger som er tilknyttet en feil eller defekt. Du definerer på siden **Forhold ml. feil-/løsningskoder**, der du angir kombinasjoner av koder for servicevaregruppen til servicevaren som du åpnet vinduet, og antall forekomster av hver enkelt.

## Opprette relasjoner mellom feilkode og løsningskode
<!--this needs to go in a working with topic-->
Hvis du vil kunne vise de vanligste reparasjonsmåtene for bestemte varefeil når du gir service til varene, må du samle opplysninger om forhold mellom feilløsningskoder. Bruk kjørselen **Sett inn forh. ml. feil/løsn.** til å finne alle kombinasjoner av feil- og løsningskoder i bokførte serviceordrer, og registrer dem på siden **Forhold ml. feil-/løsningskoder**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Sett inn forh. ml. feilløsn.**, og velg deretter den relaterte koblingen.  
2. Angi datoer for å definere perioden som du vil skal være med i kjørselen.  
3. Merk av for **Forbindelse basert på servicevaregruppe** for å gruppere forbindelsene etter servicevaregruppe.  
4. Merk av for **Behold manuelt innsatte poster** hvis du vil beholde postene som allerede er satt inn manuelt på siden **Forhold ml. feil-/løsningskoder**.  

## Se også
[Konfigurere servicehåndtering](service-setup-service.md)  
[Servicebehandling](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]