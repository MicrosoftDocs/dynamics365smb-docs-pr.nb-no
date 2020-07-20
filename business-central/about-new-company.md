---
title: Opprette nye selskaper med en automatisk oppsettguide | Microsoft-dokumentasjon
description: Det er enkelt å opprette et nytt, tomt selskap i Business Central. En guide for assistert oppsett hjelper deg gjennom trinnene, og du kan importere forretningsdataene eksisterende.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/03/2020
ms.author: edupont
ms.openlocfilehash: 4247b6c34fd086d22291408d1058cf8718841888
ms.sourcegitcommit: ca5bf1d934997ef8c0bc9f8ab0e5568f0ed42fa4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2020
ms.locfileid: "3535287"
---
# <a name="creating-new-companies-in-d365fin"></a>Opprette nye seleskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)]

I [!INCLUDE[d365fin](includes/d365fin_md.md)] kalles beholderen for forretningsdataene som hører til en konsern eller juridisk enhet et *selskap*. Når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)], får du et demoselskap og et tomt selskap, *Mitt selskap*. Bytte mellom selskaper er enkelt: simpelthen gå til **Mine innstillinger**, og bytt til det andre selskapet. Du kan også opprette nye selskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)], avhengig av forretningsbehovene. Når du oppretter et nytt selskap, gir en guide for assistert oppsett deg det grunnleggende. Deretter kan du importere aktuelle data fra det gamle systemet eller et annet selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="creating-a-new-company"></a>Opprette et nytt selskap

Hvis du vil legge til et selskap til din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruke den assisterte oppsettsveiledningen **Opprett nytt selskap** for å komme i gang. Oppsettsveiviseren er tilgjengelig fra **Selskaper**-siden og fra oppslaget i **Selskap**-feltet på siden **Mine innstillinger**.  

Veiviseren for oppsett har tre maler og et tomt alternativ:

- **Evaluering - eksempeldata**  
    Dette oppretter et selskap som ligner på demoselskapet, med eksempeldata og oppsettsdata.  
- **Produksjon - bare oppsettsdata**  
    Dette oppretter et selskap som ligner på **Mitt selskap**, med oppsettsdata, men uten eksempeldata.
- **Avansert evaluering - fullført eksempeldata** - dette oppretter et selskap med oppsettdata og fullfør eksempeldata for alle funksjoner, inkludert produksjons- og servicehåndtering
- **Opprett nytt- ingen data**  
    Dette oppretter et tomt selskap uten oppsettsdata.  

Hvis du ønsker å begynne med et nytt selskap, må du velge **Produksjon - Bare oppsettsdata** og deretter importere egne forretningsdata, for eksempel kunder, varer og leverandører. Velg **Ny**-malen hvis du vil definere alt fra begynnelsen. I så fall kan du bruke veiviseren **Selskapsoppsett** med assistert oppsettsveiledning for å komme i gang med grunnleggende oppsettsdata.  

> [!NOTE]  
> Når du oppretter et nytt selskap, tar litt tid før du kan bruke det i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Statusen for oppsettet på siden **Selskaper** viser når det nye selskapet er klart. Deretter du kan bytte til et nytt selskap ved hjelp av **Mine innstillinger**.  

Du kan opprette så mange nye selskaper under 30 dagers prøveperioden, men de er bare tilgjengelige under prøveperioden. Ta kontakt med din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner for mer informasjon.  

## <a name="copying-a-company"></a>Kopiere et selskap

På siden **Selskaper** kan du bruke **Kopier**-handlingen til å opprette et annet selskap basert på innholdet i et eksisterende selskap. Dette er for eksempel nyttig når du vil teste et selskap uten å forstyrre produksjonsdata.

> [!Important]
> Denne funksjonen kan ikke brukes til å ta en sikkerhetskopi av et selskap. Å ta en sikkerhetskopi av selskapet begynner ved å eksportere databasen som en bacpac-fil. Hvis du vil ha mer informasjon, kan du se [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjelpen for utvikling og administrasjon.

## <a name="company-setup"></a>Selskapsoppsett

Når du logger deg på et nytt selskap, kjøres veiviseren **Selskapsoppsett** automatisk og hjelper deg med å komme i gang. Du blir bedt om informasjon om selskapet, for eksempel adressen, bankdetaljer og lagerkostmetoden. Vi ber om opplysningene fordi de brukes som grunnlag for mange områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du ikke kan definere senere manuelt.  

For eksempel firmaadressen er inkludert i fakturaer og andre dokumenter, bankinformasjonen brukes i betalinger og kostmetoden brukes til å beregne priser og lagerverdisetting.  

Når du har det grunnleggende på plass, kan du definere gjenstående kjerneområder. Deretter er du klar til å legge til forretningsdataene, for eksempel kunder og leverandører. Hvis du vil ha mer informasjon, kan du se [Definere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md).  

## <a name="companies-and-environments"></a>Selskaper og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

Hvis du vil ha mer informasjon, kan du se [Bytte til et annet selskap eller miljø](ui-organization-switch.md).  

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Komme i gang](product-get-started.md)  
