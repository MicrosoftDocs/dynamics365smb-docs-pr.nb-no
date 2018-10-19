---
title: "Servicebokføring | Microsoft-dokumentasjon"
description: "Ved hjelp av funksjonaliteten for servicebokføring kan du behandle dokumenter effektivt og ha et vellykket kundeserviceopplegg. Du kan opprette og oppdatere bokførte dokumenter, og du kan opprette poster både i serviceområdet og i andre moduler for å sikre korrekt oppdatering."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 75f0fd760978b0efc4ab86b8d17a815280a09799
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="service-posting"></a>Servicebokføring
Ved hjelp av funksjonaliteten for servicebokføring kan du behandle dokumenter effektivt og ha et vellykket kundeserviceopplegg. Du kan opprette og oppdatere bokførte dokumenter, og du kan opprette poster både i serviceområdet og i andre moduler for å sikre korrekt oppdatering.  

> [!NOTE]  
>  Følgende beskriver servicebokføring, uavhengig av hvordan varer håndteres fysisk på lageret.  
>   
>  I en lokasjon som ikke er definert slik at lagerhåndtering kreves, kan du utføre bokføringshandlingene direkte fra **Servicelinjer**-vinduet. På lokasjoner som omfatter lagerhåndtering, utføres de nevnte bokføringshandlingene, unntatt Lever og Forbruk, indirekte gjennom ulike lagerleveringsfunksjoner, avhengig av oppsettet. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).  

## <a name="ship"></a>Levere  
Ved hjelp av leveringsalternativet kan du registrere relevante varer og tiden som er angitt i linjene i en serviceordre når du har fullført servicen. En bokført følgeseddel opprettes og oppdateringer forekommer i Lager-modulen og andre moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)] for å gjenspeile at varene er tatt ut av lageret og sendt til kunden. Nærmere bestemt opprettes vareposter, verdiposter, serviceposter og garantiposter.  

Hvis lokasjonen er definert slik at lagerhåndtering kreves, fungerer levering og flytting av servicelinjevarer på samme måte som for andre kildedokumenter. Den eneste forskjellen er at servicelinjevarer kan forbrukes eksternt eller internt, noe som krever to forskjellige frigivelsesfunksjoner.

## <a name="invoice"></a>Fakturere  
Du må bruke faktureringsalternativet til å utstede en faktura til kunden som skal betale for servicen. Vanligvis er det differansen mellom levert antall som er registrert med funksjonen **Bokfør levering**, og forbrukt antall som er registrert med funksjonen **Bokfør forbruk**, som skal faktureres. Du kan ikke fakturere det som ikke er levert. Når du kjører funksjonen **Bokfør faktura**, oppretter du en bokført servicefaktura og oppdaterer tidligere bokførte dokumenter slik at de samsvarer med antallene som inngår i den utstedte fakturaen. Som i andre bokføringsprosedyrer genereres relevante poster som inkluderer finansposter.  

## <a name="ship-and-invoice"></a>Lever og fakturer  
Leverings- og faktureringsalternativet lar deg utstede en servicefølgeseddel og en faktura samtidig.  

## <a name="ship-and-consume"></a>Lever og forbruk  
Ved hjelp av alternativet for levering og forbruk kan du registrere og bokføre varer, kost eller timer som er brukt til service, men som ikke kan inkluderes i fakturaen til kunden. En faktura utstedes ikke, men du kan utstede både servicefølgeseddel og serviceforbruk samtidig for å gjenspeile at noen varer eller timer er gitt til kunden kostnadsfritt. Tilhørende poster opprettes også for å registrere forbruk.  

> [!NOTE]  
>  Ved hjelp av prosedyren for servicebokføring kan du foreta delvis bokføring. Du kan opprette en dellevering eller en delfaktura ved å fylle ut feltene **Levere (antall)** og **Fakturer (antall)** på hver enkelt servicelinje i serviceordrene før du bokfører. Merk at du ikke kan opprette en faktura for noe som ikke er levert. Det vil si at for å kunne fakturere, er det nødvendig at du på forhånd har registrert en levering, eller at du velger å levere og fakturere samtidig.  

Når bokføringen er fullført, kan du vise de bokførte servicedokumentene i de tilsvarende vinduene **Bokført servicefølgeseddel** og **Bokført servicefaktura**. De bokførte postene som er opprettet, kan vises i ulike vinduer som inneholder bokførte poster, for eksempel **Finansposter**, **Vareposter**, **Lagerposter**, **Serviceposter**, **Prosjektposter**, **Garantiposter** og så videre.  

## <a name="to-view-information-about-a-posted-service-document"></a>Slik viser du informasjon om bokførte servicedokumenter  
Når du bokfører en servicefaktura, servicefølgeseddel eller servicekreditnota, overføres opplysningene i dokumentet henholdsvis til vinduene **Bokført servicefaktura**, **Bokført servicefølgeseddel** eller **Bokført salgskreditnota (service)**. Du kan ikke angi, endre eller slette noe i disse vinduene. Du kan imidlertid skrive følgesedler, fakturaer eller kreditnotaer fra disse vinduene.  

Følgende fremgangsmåte tar utgangspunkt i en bokført servicefaktura, men du kan bruke samme fremgangsmåte for bokførte servicefølgesedler og bokførte kreditnotaer.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokført servicefaktura**, og velg deretter den relaterte koblingen.  
2. Åpne den bokførte servicefakturaen du vil vise.  
3. Hvis du vil ha en oversikt over den bokførte fakturaen, velger du handlingen **Statistikk**.  

    Vinduet **Serviceordrestatistikk** åpnes. I vinduet vises informasjon som antall, beløp, mva, kost, fortjeneste og kundens kredittgrense for det bokførte dokumentet.

## <a name="see-also"></a>Se også  
[Postere serviceordrer](service-how-to-post-service-orders.md)   
[Opprette serviceordrer](service-how-to-create-service-orders.md)

