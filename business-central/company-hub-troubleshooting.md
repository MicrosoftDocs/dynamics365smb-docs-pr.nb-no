---
title: Feilsøke selskapshuben
description: Finn ut hvordan du omgår eventuelle problemer som er knyttet til selskapetssenteret for Dynamics 365 Business Central for å styre arbeid på tvers av flere selskaper.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'accountant, accounting, troubleshoot'
ms.search.form: 1151
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="troubleshooting-your-company-hub"></a>Feilsøke selskapshuben

Det er lett nok å legge til selskaper i instrumentbordet for selskapshuben, men denne artikkelen tar opp problemer du kan møte underveis.  

## <a name="check-errors"></a>Sjekk feil

Bruk handlingen **Sjekk feil** til å vise en liste over nylige feil. Du kan vise flere detaljer for hver feil, og du kan rydde i loggen ved å slette eldre oppføringer.  

## <a name="connection-failed"></a>Tilkobling mislyktes

Det kan være et par årsaker til at du ikke kan koble til et selskap, inkludert følgende:

- URL-adressen i feltet **Miljøkobling** er ikke gyldig  

  Gå til siden **Miljøkoblinger**, åpne miljøet du ikke kan koble til, og velg deretter **Test tilkoblingen**-handlingen.  
- Klientens selskapet er frakoblet for øyeblikket, for eksempel hvis det blir oppgradert

  På instrumentpanelet velger du **Verktøy**-menyelementet, og deretter **Sjekk feil**. Dermed åpnes en liste med tekniske opplysninger, så du vil kanskje kontakte systemansvarlig hvis du ser feil. Feilmeldingen «*Serveren har avvist klientlegitimasjonen*» antyder at du ikke har tilgang.  
- Du har ikke tilgang til alle selskaper i miljøet du prøver å koble til

  I [!INCLUDE [prod_short](includes/prod_short.md)] kan en organisasjon ha flere forretningsenheter som kalles selskaper, og du har kanskje ikke tilgang til alle selskapene. Kontakt administratoren eller klienten for å sikre at du har tilgang til selskapene som du må arbeide i.  

## <a name="data-does-not-refresh"></a>Data blir ikke oppdatert

Når du legger til et selskap eller ber om en oppdatering av dataene, henter [!INCLUDE [prod_short](includes/prod_short.md)] dataene. Men du må oppdatere siden selv, for eksempel velge handlingen **Last inn alle selskaper på nytt**, oppdatere lesersiden, navigere fra instrumentbordet og deretter tilbake igjen, eller lignende.  

Hvis du har lagt til et selskap, men det vises ikke i oversikten, kan du også bruke handlingen **Last inn alle selskaper på nytt** for å oppdatere oversikten.

## <a name="see-also"></a>Se også

[Administrere arbeid på tvers av flere selskaper i selskapshuben](company-hub.md)  
[Legge til selskaper i selskapshuben](company-hub-add-company.md)  
[Regnskapsføreropplevelser i Business Central](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
