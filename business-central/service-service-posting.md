---
title: Servicebokføring | Microsoft-dokumentasjon
description: Ved hjelp av funksjonaliteten for servicebokføring kan du behandle dokumenter effektivt og ha et vellykket kundeserviceopplegg. Du kan opprette og oppdatere bokførte dokumenter, og du kan opprette poster både i serviceområdet og i andre moduler for å sikre korrekt oppdatering.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fb95895588211d35122b94cf3888179c570945e3
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388227"
---
# <a name="service-posting"></a>Servicebokføring
Ved hjelp av funksjonaliteten for servicebokføring kan du behandle dokumenter effektivt og ha et vellykket kundeserviceopplegg. Du kan opprette og oppdatere bokførte dokumenter, og du kan opprette poster både i serviceområdet og i andre moduler for å sikre korrekt oppdatering.  

> [!NOTE]  
>  Følgende beskriver servicebokføring, uavhengig av hvordan varer håndteres fysisk på lageret.  
>   
>  I en lokasjon som ikke er definert slik at lagerhåndtering kreves, kan du utføre bokføringshandlingene direkte fra **Servicelinjer**-siden. På lokasjoner som omfatter lagerhåndtering, utføres de nevnte bokføringshandlingene, unntatt Lever og Forbruk, indirekte gjennom ulike lagerleveringsfunksjoner, avhengig av oppsettet. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Levere  
Ved hjelp av leveringsalternativet kan du registrere relevante varer og tiden som er angitt i linjene i en serviceordre når du har fullført servicen. En bokført følgeseddel opprettes og oppdateringer forekommer i Lager-modulen og andre moduler i [!INCLUDE[prod_short](includes/prod_short.md)] for å gjenspeile at varene er tatt ut av lageret og sendt til kunden. Nærmere bestemt opprettes vareposter, verdiposter, serviceposter og garantiposter.  

Hvis lokasjonen er definert slik at lagerhåndtering kreves, fungerer levering og flytting av servicelinjevarer på samme måte som for andre kildedokumenter. Den eneste forskjellen er at servicelinjevarer kan forbrukes eksternt eller internt, noe som krever to forskjellige frigivelsesfunksjoner.

## <a name="invoice"></a>Fakturere  
Du må bruke faktureringsalternativet til å utstede en faktura til kunden som skal betale for servicen. Vanligvis er det differansen mellom levert antall som er registrert med funksjonen **Bokfør levering**, og forbrukt antall som er registrert med funksjonen **Bokfør forbruk**, som skal faktureres. Du kan ikke fakturere det som ikke er levert. Når du kjører funksjonen **Bokfør faktura**, oppretter du en bokført servicefaktura og oppdaterer tidligere bokførte dokumenter slik at de samsvarer med antallene som inngår i den utstedte fakturaen. Som i andre bokføringsprosedyrer genereres relevante poster som inkluderer finansposter.  

## <a name="ship-and-invoice"></a>Lever og fakturer  
Leverings- og faktureringsalternativet lar deg utstede en servicefølgeseddel og en faktura samtidig.  

## <a name="ship-and-consume"></a>Lever og forbruk  
Ved hjelp av alternativet for levering og forbruk kan du registrere og bokføre varer, kost eller timer som er brukt til service, men som ikke kan inkluderes i fakturaen til kunden. En faktura utstedes ikke, men du kan utstede både servicefølgeseddel og serviceforbruk samtidig for å gjenspeile at noen varer eller timer er gitt til kunden kostnadsfritt. Tilhørende poster opprettes også for å registrere forbruk.  

> [!NOTE]  
>  Ved hjelp av prosedyren for servicebokføring kan du foreta delvis bokføring. Du kan opprette en dellevering eller en delfaktura ved å fylle ut feltene **Levere (antall)** og **Fakturer (antall)** på hver enkelt servicelinje i serviceordrene før du bokfører. Merk at du ikke kan opprette en faktura for noe som ikke er levert. Det vil si at for å kunne fakturere, er det nødvendig at du på forhånd har registrert en levering, eller at du velger å levere og fakturere samtidig.  

Når bokføringen er fullført, kan du vise de bokførte servicedokumentene på de tilsvarende sidene **Bokført servicefølgeseddel** og **Bokført servicefaktura**. De bokførte postene som er opprettet, kan vises på ulike sider som inneholder bokførte poster, for eksempel **Finansposter**, **Vareposter**, **Lagerposter**, **Serviceposter**, **Prosjektposter**, **Garantiposter** og så videre.  

## <a name="to-view-information-about-a-posted-service-document"></a>Slik viser du informasjon om bokførte servicedokumenter  
Når du bokfører en servicefaktura, servicefølgeseddel eller servicekreditnota, overføres opplysningene i dokumentet henholdsvis til sidene **Bokført servicefaktura**, **Bokført servicefølgeseddel** eller **Bokført salgskreditnota (service)**. Du kan ikke angi, endre eller slette noe på disse sidene. Du kan imidlertid skrive følgesedler, fakturaer eller kreditnotaer fra disse sidene.  

Følgende fremgangsmåte tar utgangspunkt i en bokført servicefaktura, men du kan bruke samme fremgangsmåte for bokførte servicefølgesedler og bokførte kreditnotaer.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokført servicefaktura**, og velg deretter den relaterte koblingen.  
2. Åpne den bokførte servicefakturaen du vil vise.  
3. Hvis du vil ha en oversikt over den bokførte fakturaen, velger du handlingen **Statistikk**.  

    Siden **Serviceordrestatistikk** åpnes. Siden viser informasjon som antall, beløp, mva, kost, fortjeneste og kundens kredittgrense for det bokførte dokumentet.

## <a name="see-also"></a>Se også  
[Postere serviceordrer](service-how-to-post-service-orders.md)   
[Opprette serviceordrer](service-how-to-create-service-orders.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]