---
title: Opprette fakturaer eller kreditnotaer for servicer | Microsoft-dokumentasjon
description: Finn ut hvordan du oppretter fakturaer, slik at du kan få betalt for servicen.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 62fd9e94b810887ecb152bba5a58c2f724b4025b
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252116"
---
# <a name="create-service-invoices-or-credit-memos"></a>Opprette servicefakturaer eller kreditnotaer
Enkel fakturering av serviceordrene er en viktig funksjon i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan sende fakturaer til kundene når du måtte ønske, eller opprette fakturaer periodisk.  
  
Hvis du vil opprette en faktura direkte, kan du bruke **Servicekontrakt**-siden. Du kan også sette opp systemet slik at en servicetekniker ute hos kunden kan opprette en faktura for service som ikke er knyttet til en kontrakt eller ordre.  

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Fakturere en servicekontrakt fra siden Servicekontrakt   
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Opprett servicekontraktfakturaer**, og velg deretter den relaterte koblingen.  
2. Angi hvilke filtre du vil bruke.  
3. I feltet **Bokføringsdato** angir du datoen som du vil bruke som bokføringsdato på servicefakturaene.  
4. I feltet **Fakturer t.o.m. dato** angir du datoen som du vil fakturere kontrakter frem til. Kjørselen inkluderer kontraktene med neste fakturadato frem til denne datoen.  
5. I feltet **Handling** velger du **Opprett fakturaer**.  
6. Velg **OK** for å opprette servicefakturaene.  
  
  > [!NOTE]  
  >  Du kan ikke opprette servicefakturaer for servicekontrakten nåe feltverdien i **Endringsstatus** satt til **Åpen**.  
  
## <a name="to-post-an-invoice-from-a-service-order"></a>Slik bokfører du en faktura fra en serviceordre  
Følgende fremgangsmåte beskriver hvordan du definerer delen av service som kunden skal betale for.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Serviceordrer**, og velg deretter den relaterte koblingen.  
2. Velg serviceordren du vil fakturere, og åpne ordrekortet.  
3. Velg handlingen **Servicelinjer**.  
4. Finn de nødvendige postene, og angi deretter antallene som kunden skal betale for i feltet **Fakturer (antall)**.  
  
   > [!NOTE]  
   >  Du kan fakturere kunden for den registrerte servicen enten fullstendig eller delvis. Hvis du velger å fakturere kunden fullstendig, må verdien i feltet **Fakturer (antall)** være lik verdien i **Antall**-feltet. Du kan bokføre en fullstendig faktura sammen med en fullstendig levering, og du kan bokføre en fullstendig faktura for en allerede bokført fullstendig levering som verken er fakturert eller forbrukt tidligere.  
   >   
   >  Når du bokfører en delfaktura, har du to måter å angi fakturaantall på. Hvis du skal bokføre service med alternativet **Levere og fakturere**, må verdien i feltet **Fakturer (antall)** være lik verdien i feltet **Levere (antall)**. Hvis du vil fakturere en allerede bokført følgeseddel, må fakturaantallet ikke være større enn verdien i feltet **Levert (antall)**.  
  
5. Velg **Bokfør**, og deretter **Fakturer** eller **Lever og fakturer**. Hvis du vil ha mer informasjon om disse alternativene, kan du se [Bokføring i Servicehåndtering](service-service-posting.md).  
  
 Den valgte servicelinjen bokføres. Du kan bokføre flere servicelinjer samtidig ved å merke alle linjene og velge **Bokfør**. Hvis du gjør dette, må du kontrollere at alle nødvendige opplysninger er angitt på linjene du vil bokføre.  
  
 Når du bokfører ordren med alternativet **Fakturer**, opprettes en bokført servicefaktura sammen med tilhørende poster og oppdateringer til relevante felt i servicelinjene i ordren. I tillegg oppdateres tidligere bokført(e) leveringsdokument(er) med antallene som er fakturert. Hvis du velger bokføringsalternativet **Lever og fakturer**, opprettes også en bokført følgeseddel.

## <a name="to-create-a-service-invoice-manually"></a>Opprette en servicefaktura manuelt  
Når du bokfører en serviceordre med alternativet **Fakturer** eller **Lever og fakturer**, bokføres vanligvis en servicefaktura automatisk. Du kan likevel få behov for å utstede en faktura som ikke er koblet til verken en servicekontrakt eller en serviceordre. Denne fremgangsmåten beskriver hvordan du utsteder en faktura samtidig som kunden mottar service.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefakturaer**, og velg deretter den relaterte koblingen.  
2. Opprett en ny servicefaktura.  
3. Fyll ut feltet **Nr.** .  
  
    > [!NOTE]  
    >  Hvis du har definert en nummerserie for servicefakturaer på siden **Serviceoppsett**, kan du trykke Enter for å velge det neste tilgjengelige servicefakturanummeret.  
  
4. I feltet **Kundenr.** -feltet angir du kundenummeret. Velg den aktuelle kunden fra listen .  
  
    Kundefeltene fylles ut med informasjonen fra **Kunde**-kortet.  
  
5. Angi en dato i feltet **Bokføringsdato** . Denne datoen vises i de bokførte postene. Dette feltet fylles automatisk ut med gjeldende arbeidsdato, men du kan endre den manuelt.  
6. Fyll ut feltet **Bilagsdato**. Datoen som angis her, vises på fakturautskriften, og brukes til å beregne forfallsdatoen.  
7. Fyll ut servicelinjene i fakturaen. Fyll ut feltene **Type**, **Nr.** og **Antall** for å registrere varer, ressurser og kost som er brukt ved service. 

## <a name="to-invoice-posted-shipment-lines"></a>Slik fakturerer du bokførte følgeseddellinjer  
Du må kanskje opprette en servicefaktura for service som allerede er levert, enten fra én eller flere serviceordrer, men ennå ikke fakturert eller forbrukt. Du kan fylle ut fakturalinjene automatisk med de valgte bokførte følgeseddellinjene for en bestemt kunde.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefakturaer**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Opprett fakturalinjer for service som er levert, men ikke fakturert. Du kan også bruke handlingen **Hent følgeseddellinjer** for å legge til bokførte leveringslinjer i fakturaen.  
4. Bokfør servicefakturaen.  
  
 Den bokførte servicefakturaen og tilhørende poster blir opprettet. De tidligere bokførte leveringsdokumentene oppdateres med fakturerte antall og relevante antall i servicelinjene i kildeordrene.  

## <a name="to-create-a-combined-invoice"></a>Slik oppretter du en samlefaktura  
Du kan fakturere kunden for servicer som er utført i forskjellige serviceordrer. Fakturalinjer opprettes for varer, ressurstimer eller kost som allerede er levert fra forskjellige serviceordrer, men som ennå ikke er fakturert.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicefakturaer**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Velg handlingen **Hent følgeseddellinjer**. På siden **Hent servicefølgeseddellinjer** vises alle linjer som er leverte, men ikke fakturerte for kunden.  
4. Velg linjene for servicen du vil fakturere, og velg **OK** for å legge til servicefølgeseddellinjene i fakturaen.  

## <a name="to-create-a-service-credit-memo"></a>Slik oppretter du en servicekreditnota  
Et servicekreditnotadokument brukes vanligvis når en kunde returnerer varer, men kan også brukes til å kompensere en kunde eller til å korrigere feilaktige fakturaer.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekreditnotaer**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Feltene **Bokføringsdato** og **Bilagsdato** viser arbeidsdatoen. Du kan endre dette ved behov.    
4. På kreditnotalinjene angir du opplysninger om varene som er returnert eller fjernet, eller kompensasjonen som skal gis til kunden.  

## <a name="see-also"></a>Se også
[Bokføre servicefakturaer](service-how-to-post-service-orders.md)  
[Konfigurere servicehåndtering](service-setup-service.md)  
[Servicebokføring](service-service-posting.md)  
