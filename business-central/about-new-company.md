---
title: Opprette nye selskaper med en automatisk oppsettguide | Microsoft-dokumentasjon
description: Det er enkelt å opprette et nytt, tomt selskap i Business Central. En guide for assistert oppsett hjelper deg gjennom trinnene, og du kan importere forretningsdataene eksisterende.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fc318d3de70cb56e722bd02c868fc570fb62692b
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385052"
---
# <a name="creating-new-companies-in-prod_short"></a>Opprette nye seleskaper i [!INCLUDE[prod_short](includes/prod_short.md)]

I [!INCLUDE[prod_short](includes/prod_short.md)] kalles beholderen for forretningsdataene som hører til en konsern eller juridisk enhet et *selskap*. Når du registrerer deg for [!INCLUDE[prod_short](includes/prod_short.md)], får du et demoselskap og et tomt selskap, *Mitt selskap*. Bytte mellom selskaper er enkelt: simpelthen gå til **Mine innstillinger**, og bytt til det andre selskapet. Du kan også opprette nye selskaper i [!INCLUDE[prod_short](includes/prod_short.md)], avhengig av forretningsbehovene. Når du oppretter et nytt selskap, gir en guide for assistert oppsett deg det grunnleggende. Deretter kan du importere aktuelle data fra det gamle systemet eller et annet selskap i [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="creating-a-new-company"></a>Opprette et nytt selskap

Hvis du vil legge til et selskap til din [!INCLUDE[prod_short](includes/prod_short.md)], kan du bruke den assisterte oppsettsveiledningen **Opprett nytt selskap** for å komme i gang. Oppsettsveiviseren er tilgjengelig fra **Selskaper**-siden og fra oppslaget i **Selskap**-feltet på siden **Mine innstillinger**.  

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
> Når du oppretter et nytt selskap, tar litt tid før du kan bruke det i [!INCLUDE[prod_short](includes/prod_short.md)]. Statusen for oppsettet på siden **Selskaper** viser når det nye selskapet er klart. Deretter du kan bytte til et nytt selskap ved hjelp av **Mine innstillinger**.  

Du kan opprette så mange nye selskaper under 30 dagers prøveperioden, men de er bare tilgjengelige under prøveperioden. Ta kontakt med din [!INCLUDE[prod_short](includes/prod_short.md)]-partner for mer informasjon.  

## <a name="copying-a-company"></a>Kopiere et selskap

På siden **Selskaper** kan du bruke **Kopier**-handlingen til å opprette et annet selskap basert på innholdet i et eksisterende selskap. Dette er for eksempel nyttig når du vil teste et selskap uten å forstyrre produksjonsdata.

> [!Important]
> Denne funksjonen kan ikke brukes til å ta en sikkerhetskopi av et selskap. Å ta en sikkerhetskopi av selskapet begynner ved å eksportere databasen som en bacpac-fil. Hvis du vil ha mer informasjon, kan du se [Eksportere databaser](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-database-export) i hjelpen for utvikling og administrasjon.

## <a name="company-setup"></a>Selskapsoppsett

Når du logger deg på et nytt selskap, kjøres veiviseren **Selskapsoppsett** automatisk og hjelper deg med å komme i gang. Du blir bedt om informasjon om selskapet, for eksempel adressen, bankdetaljer og lagerkostmetoden. Vi ber om opplysningene fordi de brukes som grunnlag for mange områder i [!INCLUDE[prod_short](includes/prod_short.md)], som du ikke kan definere senere manuelt.  

For eksempel firmaadressen er inkludert i fakturaer og andre dokumenter, bankinformasjonen brukes i betalinger og kostmetoden brukes til å beregne priser og lagerverdisetting.  

Når du har det grunnleggende på plass, kan du definere gjenstående kjerneområder. Deretter er du klar til å legge til forretningsdataene, for eksempel kunder og leverandører. Hvis du vil ha mer informasjon, kan du se [Definere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md).  

## <a name="companies-and-environments"></a>Selskaper og miljøer

[!INCLUDE [company_environment](includes/company_environment.md)]

Hvis du vil ha mer informasjon, kan du se [Bytte til et annet selskap eller miljø](ui-organization-switch.md). 

## <a name="changing-a-companys-name"></a>Endre et selskaps navn

Når et selskap er opprettet, kan du ikke endre navnet på det. Du kan imidlertid endre **visningsnavnet**, som er tekst som skal vises for selskapet i programmet.  

> [!TIP]
> Du kan gi et selskap nytt navn hvis du bruker [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.

## <a name="see-also"></a>Se også

[Tilpasse Business Central](ui-customizing-overview.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Komme i gang](product-get-started.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]