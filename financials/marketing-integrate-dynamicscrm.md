---
title: Administrere kunderelasjoner ved hjelp av Dynamics 365 for Sales fra Dynamics 365 for Financials | Microsoft-dokumentasjon
description: "Hvis du bruker Dynamics 365 for Sales til kundeengasjement, kan du bruke Dynamics 365 for Financials for ordrebehandling og økonomi og få sømløs integrasjon i kundeemne-til-kontanter-prosessen"
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map
ms.date: 03/05/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: c0291cc316b49e1f1f4f2196745914daca158f61
ms.contentlocale: nb-no
ms.lasthandoff: 05/04/2017

---
# <a name="managing-your-customer-relationships-using-dynamics-365-for-sales-from-inside-dynamics-365-for-financials"></a>Administrere kunderelasjoner ved hjelp av Dynamics 365 for Sales fra Dynamics 365 for Financials
Hvis du bruker Dynamics 365 for Sales til kundeengasjement, kan du bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] for ordrebehandling og økonomi og få sømløs integrasjon i kundeemne-til-kontanter-prosessen.

Når programmet er konfigurert til å integrere med Dynamics 365 for Sales, har du tilgang til salgstall fra [!INCLUDE[d365fin](includes/d365fin_md.md)] og motsatt vei i noen tilfeller. Denne integrasjonen gjør at du kan arbeide med og synkronisere datatyper som er felles for begge tjenester, for eksempel kunder, kontakter og salgsinformasjon, og hold dataene oppdaterte på begge lokasjoner.  

**Merk**: I den gjeldende versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)], kalles Dynamics 365 for Sales for Dynamics CRM. For enkelhet, skal resten av denne artikkelen bruke terminologien som brukes i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Selgeren i Dynamics CRM kan for eksempel bruke prislister fra [!INCLUDE[d365fin](includes/d365fin_md.md)] når de oppretter en salgsordre. Når de legger til varen på salgsordrelinjen i Dynamics CRM, kan de også se lagernivået (tilgjengelighet) av varen fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse dataene er publisert som en del av assistert installasjonsveiledningen **Tilkoblingsoppsett for Dynamics CRM**.  

**Merk**: Denne funksjonen krever at opplevelsen er satt til **Løsning**. Hvis du vil ha mer informasjon, se [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelse](ui-experiences.md).  

## <a name="setting-up-the-connection"></a>Definere tilkoblingen
Fra startsiden kan du få tilgang til **Tilkoblingsoppsett for Dynamics CRM** assistert oppsettguide som hjelper deg med å konfigurere tilkoblingen. Når dette er gjort, vil du ha en sømløs kobling i Dynamics CRM-oppføringer med [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster.  

**Merk**: Følgende forklarer det assisterte oppsettet, men du kan utføre de samme oppgavene manuelt i vinduet **Tilkoblingsoppsett for Dynamics CRM**.

Du kan velge hvilke data som skal synkroniseres mellom de to tjenestene i den assisterte oppsettguiden. Du kan også angi at du vil importere din eksisterende Dynamics CRM-løsning. I så fall må du angi en administrativ brukerkonto.

### <a name="setting-up-the-user-account-for-importing-the-solution"></a>Konfigurere kontoen for import av løsning
Hvis du vil importere en eksisterende Dynamics CRM-løsning, bruker oppsettguiden en administrativ konto. Angi kontoen som må være en gyldig bruker i Dynamics CRM med følgende sikkerhetsroller:

* Systemansvarlig  
* Løsningstilpasser  

Hvis du vil ha mer informasjon, se [Opprette brukere og tilordne sikkerhetsroller for Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) på techNet og [Administrere brukere og tillatelser](ui-how-users-permissions.md).  

Denne kontoen brukes bare under oppsettet. Når løsningen er importert til [!INCLUDE[d365fin](includes/d365fin_md.md)], er kontoen ikke lenger nødvendig.

### <a name="setting-up-the-user-account-for-synchronization"></a>Konfigurere kontoen for synkronisering
Integreringen er avhengig av en delt brukerkonto. Så i Office 365-abonnementet, må du opprette et engasjert personell som skal brukes for synkronisering mellom de to tjenestene. Denne kontoen må være en gyldig bruker i Dynamics CRM allerede, men du trenger ikke å tilordne sikkerhetsroller til kontoen fordi installasjonsprogrammet for TV-guiden gjør dette for deg. Du må angi denne kontoen én eller flere ganger i installasjonsveiledningen, avhengig av hvor mye synkroniseringen du vil aktivere. Hvis du vil ha mer informasjon, se [Opprette brukere og tilordne sikkerhetsroller for Microsoft Dynamics 365 (online)](https://technet.microsoft.com/library/jj191623.aspx) på techNet.

Hvis du velger å aktivere *Varedisposisjon*, må integrasjonsbrukerkontoen ha en tilgangstast for webtjenester. Dette er en totrinns ting på siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for denne brukerkontoen, må du velge knappen **Endre webtjenestenøkkel**, og i oppsettguiden for tilkobling av CRM må du angi brukeren som OData-webtjenestebrukeren.

Hvis du velger å aktivere *ordrerintegrering*, må du angi en bruker som kan håndtere denne synkroniseringen - integreringsbrukeren eller en annen brukerkonto.

### <a name="coupling-records"></a>Koblingsposter
Du kan velge å synkronisere mellom de to tjenestene i den assisterte oppsettguiden. Men senere kan du også definere synkronisering av bestemte typer data. Dette kalles *kobling*, og denne delen inneholder anbefalinger om hva du må ta i betraktning.

Hvis du vil vise Dynamics CRM-kontoer som kunder i for eksempel [!INCLUDE[d365fin](includes/d365fin_md.md)], må du koble to typer poster. Det er ikke veldig komplisert - du åpner **Kundeoversikt**-vinduet i [!INCLUDE[d365fin](includes/d365fin_md.md)], og det er en handling i båndet for å koble disse dataene med Dynamics CRM. Vil du angi hvilke [!INCLUDE[d365fin](includes/d365fin_md.md)]-kunder som samsvarer med hvilke konti i Dynamics CRM.

I enkelte områder avhenger funksjonaliteten av at du kobler noen bestemte sett med data før andre sett med data, som vist i følgende liste:

* Kunder og konti  
  * Koble selgere med Dynamics CRM-brukere først  
* Varer og ressurser  
  * Koble målenheter med Dynamics CRM-enhetsgrupper først  
* Varer og ressurspriser  
  * Koble kundeprisgrupper med Dynamics CRM-priser først  

**Merk**: Hvis du bruker priser i fremmed valuta, må du kontrollere at du kobler valutaer til Dynamics CRM-transaksjonsvalutaer.

Dynamics CRM-salgsordrer avhenger av ekstra informasjon, for eksempel kunder, målenheter, valutaer, kundeprisgrupper, varer og/eller ressurser. For at Dynamics CRM-salgsordrer skal fungere sømløst sammen, må du koble kunder, målenheter, valutaer, kundeprisgrupper, varer og/eller ressurser først.

### <a name="synchronizing-records-fully"></a>Fullstendig synkronisering av oppføringer
Til slutten av den assisterte oppsettguiden, kan du velge **Kjør full synkronisering** for å starte synkronisering av alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-poster med alle relaterte poster i den tilkoblede Dynamics CRM-løsningen. I vinduet **Gjennomgang av full synkronisering for CRM** velger du **Start**-handlingen. Deretter synkroniseringen begynner å utføre jobber i henhold til avhengighetene. Hvis du for eksempel synkroniseres valuta poster før kundeoppføringer. Fullstendig synkronisering kan ta lang tid, og derfor kjører i bakgrunnen, slik at du kan fortsette å arbeide [!INCLUDE[d365fin](includes/d365fin_md.md)].

Hvis du vil kontrollere fremdriften for individuelle prosjekter i en fullstendig synkronisering, detaljer for den **Status for jobben køen**, **til Int. tabellen Jobbstatus**, eller **fra Int. tabellen Jobbstatus** i den **CRM Full synkronisering. Se gjennom** vindu.

Fra den **CRM Tilkoblingsoppsett** -vinduet kan du få detaljer om fullstendig synkronisering når som helst. Herfra kan du også åpne **Tilordninger for integreringstabell**-vinduet for å se detaljer om tabellene i Financials og i Dynamics CRM-løsningen som må synkroniseres.

## <a name="see-also"></a>Se også
[Forbindelser](marketing-relationship-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)]-opplevelsen](ui-experiences.md)  
[Behandle brukere og tillatelser](ui-how-users-permissions.md)    
[Introduser organisasjonen og brukerne forl Dynamics 365 (tilkoblet)](https://www.microsoft.com/en-US/Dynamics/crm-customer-center/onboard-your-organization-and-users-to-dynamics-365-online.aspx)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
