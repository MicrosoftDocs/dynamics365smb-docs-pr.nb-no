---
title: Opprett et sandkassemiljø
description: Opprett et miljø for utforsking, læring, demoer, utvikling og testing innenfra Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: a76ae33815b8e9368f45b72fd8703bfc47cbd079
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215631"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Opprette et sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du enkelt opprette et sikkert miljø der du kan teste, lære opp eller feilsøke uten å forstyrre firmaets arbeidsprosesser eller forretningsdata. Et slikt ikke-produksjonsmiljø kalles en *sandkasse*. Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.  

Administratoren administrerer sandkassemiljøer i [administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), men hvis du raskt vil teste noe, kan du opprette et sandkassemiljø innenfra [!INCLUDE[prod_short](includes/prod_short.md)]. Når du er ferdig, kan du fjerne sandkassen ved å bruke administrasjonssenteret.  

> [!NOTE]
> Teknisk sett er sandkassemiljøer svært forskjellige fra produksjonsmiljøer, selv om systemansvarlig oppretter en sandkasse som inkluderer produksjonsdata. Du kan ikke bruke en sandkasse for ytelsestester, og du kan for eksempel ikke be om databaseeksport. Hvis du vil opprette en sandkasse for ytelsestest, kan systemansvarlig opprette et eget miljø i administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Produksjons- og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Slik oppretter du et sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)]

1. Logg deg på din produksjonsforekomst av [!INCLUDE[prod_short](includes/prod_short.md)].

2. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Sandkassemiljø**, og velg deretter den relaterte koblingen.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Velg **Opprett**-knappen.  

    Det åpnes en annen fane med [!INCLUDE[prod_short](includes/prod_short.md)], der du kan fullføre oppsettet av sandkassemiljøet.

    > [!NOTE]  
    >  Hvis du har aktivert popup-blokkering i webleseren, endrer du den til å tillate URL-adresser fra adressen *.businesscentral.dynamics.com.

Når sandkassemiljøet er klart, vil du bli videresendt til velkomstveiviseren i sandkassemiljøet.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

Du kan velge **Finn ut mer**-knappen for å lese om utviklerscenarioer som du kan prøve i et sandkassemiljø, eller velg **Lukk**-knappen for å fortsette til Rollesenteret for [!INCLUDE[prod_short](includes/prod_short.md)]-sandkasseforekomsten din.

Øverst i rollesenteret vises en melding som varsler deg at dette er et sandkassemiljø. Du kan også se typen miljø på tittellinjen i klienten.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Et sandkassemiljø som er opprettet på denne måten, inneholder bare standard demonstrasjonsdata for CRONUS-selskapet. Ingen data kopieres eller blir ellers overført fra produksjonsmiljøet.
>
> Du kan eventuelt opprette et sandkassemiljø basert på produksjonsdata. Du må gjøre dette ved hjelp av administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Administrere miljøer](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) i utvikler- og administrasjonsinnholdet.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

En administrator kan begrense eller blokkere tilgang for enkelte brukere til sandkassemiljøet. Dette kan gjøres ved hjelp av produktets standard sikkerhetsfunksjoner, for eksempel brukerkort, brukergrupper og tillatelsessett. Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md).  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Avanserte funksjoner i sandkassemiljøet

Sandkassemiljøet er ikke minst nyttig fordi det inneholder et par nyttige funksjoner:

* [Avansert brukeropplevelse](#advanced-user-experience)  
* [Fullstendige eksempeldata](#complete-sample-data)  
* [Utforming](#designer)  

### <a name="advanced-user-experience"></a>Avansert brukeropplevelse

Det er mulig å aktivere og prøve alle funksjonene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] i en sandkasseleietaker ved å sette **Opplevelse**-feltet på **Selskapsopplysninger**-siden til *Premium*. Finn **Selskapsopplysninger**-siden på ikonmenyen for :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Innstillinger":::.  

Når du har aktivert *Premium*-brukeropplevelsen, får du tilgang til alle standardprofilene (rollene) og rollesentrene i standardversjonen. Du kan også opprette et evalueringsselskap med et fullstendig oppsett, inkludert demonstrasjonsdata og tilgang til avanserte områder i produktet. Alternativt kan du kontakte en videresalgspartner for en demonstrasjon av funksjonene. Hvis du vil ha mer informasjon, kan du se [Hvordan finner jeg en partner for videresalg?](/dynamics365/business-central/across-faq.yml#findpartner).  

### <a name="complete-sample-data"></a>Fullstendige eksempeldata

I situasjoner der du trenger flere eksempeldata, kontakter du partneren for videresalg.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Slik oppretter du et selskap med fullstendige eksempeldata i en sandkasse

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskaper**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**, og velg deretter **Opprett nytt selskap**.  
3. Velg **Neste** på siden for **assistert oppsett av oppretting av et selskap**.  
4. Angi et navn for det nye selskapet, og velg deretter **Avansert evaluering - Fullfør eksempeldata** i feltet **Velg dataene og oppsettet for å komme i gang**.  
5. Fullfør resten av den assisterte oppsettsveiledningen.  

Når veiledningen for assistert oppsett er fullført, kan du begynne å utforske det nye selskapet med de fullstendige eksempeldataene. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  

### <a name="designer"></a>Designer

I et sandkassemiljø finner du **Designer** aktivert. Du kan aktivere Designer ved å velge designikonet ![Designer](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side, eller ved å velge **Utforming**-menyen på menyen ![Innstillinger](media/ui-experience/settings_icon_small.png).  

Hvis du vil ha mer informasjon, kan du se [Bruk av utformingen](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i innholdet for utviklere og administratorer (bare på engelsk).  

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Se også

[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Prøveversjoner og abonnementer](across-preview.md)  
[Behandle miljøer i administrasjonssenteret for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
