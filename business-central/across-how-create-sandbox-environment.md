---
title: "Opprette et sandkassemiljø | Microsoft-dokumentasjon"
description: "Opprett et miljø for utforsking, læring, demoer, utvikling og testing."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 08/18/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: d31095d0fc67b342d74bff813fb2eff7e3f82262
ms.contentlocale: nb-no
ms.lasthandoff: 06/01/2018

---
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

# <a name="create-a-sandbox-environment"></a>Opprette et sandkassemiljø
Et sandkassemiljø (forhåndsvisning) er en ikke-produktiv forekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.

## <a name="to-create-a-sandbox-environment"></a>Slik oppretter du et sandkassemiljø
Du må ha et abonnement på [!INCLUDE[d365fin](includes/d365fin_md.md)] for å kunne opprette et sandkassemiljø. Det kan være bare ett sandkassemiljø per abonnement.

1. Logg deg på din produksjonsforekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten.
2. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.
![Oppsett av sandkassemiljø](./media/across-sandbox/sandbox-environment-setup.png)
3. Velg **Opprett**.  
  En annen kategori i webleseren åpnes for å fullføre oppsettet av sandkassemiljøet.
> [!NOTE]  
>  Hvis du har aktivert popup-blokkering i webleseren, endrer du den til å tillate URL-adresser fra adressen *.businesscentral.dynamics.com.   

4. Når sandkassemiljøet er klart, vil du bli videresendt til velkomstveiviseren i sandkassemiljøet.
![Velkomstveiviser i sandkasse](./media/across-sandbox/sandbox-wizard.png)

5. Velg **Finn ut mer** for å lese om scenarier som du kan prøve i et sandkassemiljø. Eller velg **Lukk** for å fortsette til rollesenteret i [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomsten.
6. Øverst i rollesenteret vises en melding som varsler deg at dette er et sandkassemiljø. Du kan også se typen miljø på tittellinjen i klienten.
![Varsling i sandkasserollesenteret](./media/across-sandbox/sandbox-rolecenter-notification.png)  
En helt ny leietaker er opprettet i sandkassemiljøet. Denne leietakeren har standard demonstrasjonsdata for CRONUS-selskapet. Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet under opprettelsen av sandkassen.
7.  Når som helst kan du gå tilbake til siden **Sandkassemiljø** og tilbakestille sandkassemiljøet.
> [!NOTE]  
>  Tilbakestilling av sandkassemiljøet fjerner det fullstendig, og deretter opprettes det på nytt med standard demonstrasjonsdata.  

8.  For å veksle mellom produksjons- og sandkassemiljøene kan du bruke Business Central-appstarteren.
![Sandkassemeny i Dynamics365](./media/across-sandbox/sandbox-dynamics365-menu.png)

9.  Det er mulig for en administrator eller en annen bruker å begrense eller blokkere tilgang for enkelte brukere til sandkassemiljøet. Dette kan gjøres ved hjelp av standard sikkerhetsfunksjoner i produktet, for eksempel brukerkort, brukergrupper og tillatelsessett.

![Tillatelsessett for sandkasse](./media/across-sandbox/sandbox-permission-sets.png)

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avanserte funksjoner i sandkassemiljøet
### <a name="the-in-client-designer"></a>Den interne designeren
I et sandkassemiljø er den interne designeren klar, og du kan aktivere den ved å velge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side.

![Intern designer](./media/across-sandbox/sandbox-inclient-designer.png)

### <a name="enable-the-advanced-user-experience"></a>Aktivere den avanserte brukeropplevelsen
Det er mulig å aktivere og prøve de avanserte (alle) funksjonene i [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasseleietaker ved å angi **Opplevelse**-feltet på **Selskapsopplysninger**-siden.

![Avansert sandkassemiljø](./media/across-sandbox/sandbox-advanced.png)

![Sandkasseproduksjon](./media/across-sandbox/sandbox-production.png)

Når du har aktivert de avanserte funksjonene i en sandkasseleietaker, får du tilgang til alle standardprofiler og rollesentre. Du kan også opprette et evalueringsselskap med et fullstendig oppsett, inkludert demonstrasjonsdata og tilgang til avanserte områder i produktet.

![Sandkasse, nytt selskap](./media/across-sandbox/sandbox-newcompany.png)


## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

