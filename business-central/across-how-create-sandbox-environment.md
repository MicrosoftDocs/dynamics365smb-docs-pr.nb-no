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
ms.date: 04/01/2020
ms.author: solsen
ms.openlocfilehash: 59b659ca458e6cfe7c13ef5094dbbf80a144c369
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188567"
---
# <a name="creating-a-sandbox-environment-in-prodshort"></a>Opprette et sandkassemiljø i [!INCLUDE [prodshort](includes/prodshort.md)]

Med [!INCLUDE [prodshort](includes/prodshort.md)] kan du enkelt opprette et sikkert miljø der du kan teste, lære opp eller feilsøke uten å forstyrre firmaets arbeidsprosesser eller forretningsdata. Et slikt ikke-produksjonsmiljø kalles en *sandkasse*. Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.  

Systemansvarlig kan opprette sandkassemiljøer i [administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du raskt vil teste noe, kan du opprette et sandkassemiljø fra innsiden [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Teknisk sett er sandkassemiljøer svært forskjellige fra produksjonsmiljøer, selv om systemansvarlig oppretter en sandkasse som inkluderer produksjonsdata. Du kan ikke bruke en sandkasse for ytelsestester, og du kan for eksempel ikke be om databaseeksport. Hvis du vil opprette en sandkasse for ytelsestest, kan systemansvarlig opprette et eget produksjonsmiljø i administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Typer miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments).

## <a name="to-create-a-sandbox-environment-in-your-prodshort"></a>Slik oppretter du et sandkassemiljø i [!INCLUDE [prodshort](includes/prodshort.md)]

1. Logg deg på din produksjonsforekomst av [!INCLUDE[d365fin](includes/d365fin_md.md)].

2. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Velg **Opprett**-knappen.  

    Det åpnes en annen fane med [!INCLUDE[d365fin](includes/d365fin_md.md)], der du kan fullføre oppsettet av sandkassemiljøet.

    > [!NOTE]  
    >  Hvis du har aktivert popup-blokkering i webleseren, endrer du den til å tillate URL-adresser fra adressen *.businesscentral.dynamics.com.

Når sandkassemiljøet er klart, vil du bli videresendt til velkomstveiviseren i sandkassemiljøet.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Du kan velge **Finn ut mer**-knappen for å lese om utviklerscenarioer som du kan prøve i et sandkassemiljø, eller velg **Lukk**-knappen for å fortsette til Rollesenteret for [!INCLUDE[d365fin](includes/d365fin_md.md)]-sandkasseforekomsten din.

Øverst i rollesenteret vises en melding som varsler deg at dette er et sandkassemiljø. Du kan også se typen miljø på tittellinjen i klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Et sandkassemiljø som er opprettet på denne måten, inneholder bare standard demonstrasjonsdata for CRONUS-selskapet. Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet.<br /><br />
> Du kan også opprette et sandkassemiljø som inneholder produksjonsdataene. Du må gjøre dette ved hjelp av administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i hjelpen for utviklere og IT-eksperter.

Når som helst kan du gå tilbake til siden **Sandkassemiljø** og tilbakestille sandkassemiljøet.

> [!NOTE]  
> Tilbakestilling av sandkassemiljøet fjerner det fullstendig, og deretter opprettes det på nytt med standard demonstrasjonsdata.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

En administrator kan begrense eller blokkere tilgang for enkelte brukere til sandkassemiljøet. Dette kan gjøres ved hjelp av produktets standard sikkerhetsfunksjoner, for eksempel brukerkort, brukergrupper og tillatelsessett. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avanserte funksjoner i sandkassemiljøet

Sandkassemiljøet er ikke minst nyttig fordi det inneholder et par nyttige funksjoner.

### <a name="designer"></a>Designer

I et sandkassemiljø finner du **Designer** aktivert. Du kan aktivere Designer ved å velge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side, eller ved å velge **Utforming**-menyen på menyen ![Innstillinger](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

### <a name="to-enable-the-advanced-user-experience"></a>Slik aktiverer du den avanserte brukeropplevelsen
Det er mulig å aktivere og prøve alle funksjonene i standardversjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)] i en sandkasseleietaker ved å angi **Opplevelse**-feltet på **Selskapsopplysninger**-siden.

<!-- ![Sandbox Environment Advanced](./media/across-sandbox/sandbox-advanced.png) -->

<!-- ![Sandbox Production](./media/across-sandbox/sandbox-production.png) -->

Når du har aktivert *Premium*-brukeropplevelsen, får du tilgang til alle standardprofilene (rollene) og rollesentrene i standardversjonen. Du kan også opprette et evalueringsselskap med et fullstendig oppsett, inkludert demonstrasjonsdata og tilgang til avanserte områder i produktet. Alternativt kan du kontakte en videresalgspartner for en demonstrasjon av funksjonene. Hvis du vil ha mer informasjon, se [Hvordan finner jeg en partner for videresalg?](across-faq.md#findpartner).  

<!-- ![Sandbox New Company](./media/across-sandbox/sandbox-newcompany.png) -->

## <a name="see-also"></a>Se også

[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] Prøveversjoner og abonnementer](across-preview.md)  
[Behandle miljøer i administrasjonssenteret for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
