---
title: Sandkassemiljøer
description: Finn ut hvordan et eget miljø kan hjelpe deg med å utforske, lære, prøve, utvikle, feilsøke og teste Business Central på en sikker måte.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 12/20/2021
ms.author: solsen
ms.openlocfilehash: 1a80e5ba3fb54d618334f65de452984dc3c1c356
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8142474"
---
# <a name="sandbox-environments-in-prod_short"></a>Sandkassemiljøer i [!INCLUDE[prod_short](includes/prod_short.md)]

Med [!INCLUDE[prod_short](includes/prod_short.md)] online kan du enkelt få et sikkert miljø der du kan teste, lære opp eller feilsøke uten å forstyrre firmaets arbeidsprosesser eller forretningsdata. Et slikt ikke-produksjonsmiljø kalles en *sandkasse*. Isolert fra produksjon er et sandkassemiljø stedet der du trygt kan utforske, lære, demonstrere, utvikle og teste tjenesten uten risikoen ved å påvirke data og innstillinger i produksjonsmiljøet.  

> [!TIP]
> Kom du til denne artikkelen etter at du valgte navnet på [!INCLUDE [prod_short](includes/prod_short.md)]-miljøet på den øverste linjen? Du kan for øyeblikket ikke endre navnet eller miljøet på den måten. Du må i stedet be administratoren om å endre navnet eller dele koblingen med et annet miljø.

Administratoren administrerer sandkassemiljøer i [administrasjonssenteret](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Hvis du for eksempel vil opprette en sandkasse for ytelsestest, kan systemansvarlig opprette et eget miljø i administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Produksjons- og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types) i utvikler- og administrasjonsinnholdet.  

Du kan også trygt bruke sandkasser til opplæring, for eksempel for å følge en læringsbane fra [Microsoft Learn](/learn/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), fordi det er et sikkert miljø du kan eksperimentere med. Hvis noe går galt, sletter du sandkassen og begynner på nytt.  

Når du er ferdig, kan du fjerne sandkassen ved å bruke administrasjonssenteret.  

> [!NOTE]
> Teknisk sett er sandkassemiljøer svært forskjellige fra produksjonsmiljøer. Administratoren kan opprette en sandkasse med produksjonsdata, men det er fortsatt en sandkasse, og du kan for eksempel ikke be om databaseeksport. Hvis du vil ha mer informasjon, kan du se [Sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) i utvikler- og administrasjonsinnholdet.

Sandkassemiljøet er ikke minst nyttig fordi det inneholder et par nyttige funksjoner:

* [Avansert brukeropplevelse](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Utforming](#designer)  

## <a name="advanced-user-experience"></a>Avansert brukeropplevelse

Det er mulig å aktivere og prøve alle funksjonene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] i en sandkasseleietaker ved å sette **Opplevelse**-feltet på **Selskapsopplysninger**-siden til *Premium*. Finn **Selskapsopplysninger**-siden på ikonmenyen for :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="Innstillinger-ikon."::: meny.  

Når du har aktivert *Premium*-brukeropplevelsen, får du tilgang til alle standardprofilene (rollene) og rollesentrene i standardversjonen. Alternativt kan du kontakte en videresalgspartner for en demonstrasjon av funksjonene. Hvis du vil ha mer informasjon, kan du se [Hvordan finner jeg en partner for videresalg?](across-faq.yml#how-do-i-find-a-reselling-partner).  

### <a name="complete-sample-data"></a>Fullstendige eksempeldata

I situasjoner der du trenger flere eksempeldata, kontakter du partneren for videresalg.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Designer

I et sandkassemiljø finner du **Designer** aktivert. Du kan aktivere Designer ved å velge designikonet ![Designer.](./media/across-sandbox/sandbox-inclient-design-icon.png) på en side, eller ved å velge **Designer**-menyelementet på ![Innstillinger](media/ui-experience/settings_icon_small.png) menyen Innstillinger.  

Hvis du vil ha mer informasjon, kan du se [Bruk av utformingen](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) i innholdet for utviklere og administratorer (bare på engelsk).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Se også

[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)] Prøveversjoner og abonnementer](across-preview.md)  
[Behandle miljøer i administrasjonssenteret for Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Produksjons- og sandkassemiljøer](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
