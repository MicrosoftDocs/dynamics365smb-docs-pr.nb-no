---
title: Opprette et sandkassemiljø | Microsoft-dokumentasjon
description: Opprett et miljø for utforsking, læring, demoer, utvikling og testing.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 02/15/2019
ms.author: solsen
ms.openlocfilehash: 91db02673c1e408927d9863af9ec6751bc33e480
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803218"
---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="creating-a-sandbox-environment"></a>Opprette et sandkassemiljø
Et sandkassemiljø (forhåndsvisning) er en ikke-produktiv forekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.

## <a name="to-create-a-sandbox-environment"></a>Slik oppretter du et sandkassemiljø
Du må ha et abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] for å kunne opprette et sandkassemiljø. Det kan være bare ett sandkassemiljø per abonnement.

1. Logg deg på din produksjonsforekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten.
2. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre") ikonet, angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.
<!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Velg **Opprett**.  
  En annen kategori i webleseren åpnes for å fullføre oppsettet av sandkassemiljøet.
> [!NOTE]  
>  Hvis du har aktivert popup-blokkering i webleseren, endrer du den til å tillate URL-adresser fra adressen *.businesscentral.dynamics.com.   

4. Når sandkassemiljøet er klart, vil du bli videresendt til velkomstveiviseren i sandkassemiljøet.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

5. Velg **Finn ut mer** for å lese om scenarier som du kan prøve i et sandkassemiljø. Eller velg **Lukk** for å fortsette til rollesenteret i [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomsten.
6. Øverst i rollesenteret vises en melding som varsler deg at dette er et sandkassemiljø. Du kan også se typen miljø på tittellinjen i klienten.
<!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) --> 
En ny leietaker er opprettet i sandkassemiljøet. Denne leietakeren har standard demonstrasjonsdata for CRONUS-selskapet. Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet under opprettelsen av sandkassen.

7. Når som helst kan du gå tilbake til siden **Sandkassemiljø** og tilbakestille sandkassemiljøet.
> [!NOTE]  
>  Tilbakestilling av sandkassemiljøet fjerner det fullstendig, og deretter opprettes det på nytt med standard demonstrasjonsdata.  

8. For å veksle mellom produksjons- og sandkassemiljøene kan du bruke Business Central-appstarteren.
<!-- ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

9. Det er mulig for en administrator eller en annen bruker å begrense eller blokkere tilgang for enkelte brukere til sandkassemiljøet. Dette kan gjøres ved hjelp av standard sikkerhetsfunksjoner i produktet, for eksempel brukerkort, brukergrupper og tillatelsessett.

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avanserte funksjoner i sandkassemiljøet
### <a name="designer"></a>Designer
I et sandkassemiljø er den interne **designeren** klar, og du kan aktivere den ved å velge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side.

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="enable-the-advanced-user-experience"></a>Aktivere den avanserte brukeropplevelsen
Det er mulig å aktivere og prøve de avanserte (alle) funksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasseleietaker ved å angi **Opplevelse**-feltet på **Selskapsopplysninger**-siden.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Når du har aktivert de avanserte funksjonene i en sandkasseleietaker, får du tilgang til alle standardprofiler og rollesentre. Du kan også opprette et evalueringsselskap med et fullstendig oppsett, inkludert demonstrasjonsdata og tilgang til avanserte områder i produktet.

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->


## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
