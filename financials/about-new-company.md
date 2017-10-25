---
title: Opprette nye selskaper med en automatisk oppsettguide | Microsoft-dokumentasjon
description: "Det er enkelt å opprette et nytt, tomt selskap i Dynamics 365 for Financials. En guide for assistert oppsett hjelper deg gjennom trinnene, og du kan importere forretningsdataene eksisterende."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: company, setup wizard
ms.date: 07/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: 3ff3c7af87033595d64e583b62b0e0242b22d2f1
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="creating-new-companies-in-included365finlongincludesd365finlongmdmd"></a>Opprette nye seleskaper i [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]
I [!INCLUDE[d365fin](includes/d365fin_md.md)], beholdere for forretningsdataene som hører til en konsern eller juridisk enhet kalles et *selskap*. Når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)], får du et demoselskap og et tomt selskap, *Mitt selskap*. Bytte mellom selskaper er enkelt - simpelthen til **Mine innstillinger** og bytte til det andre selskapet. Du kan også opprette nye selskaper i [!INCLUDE[d365fin](includes/d365fin_md.md)], avhengig av forretningsbehovene. Når du oppretter et nytt selskap, gir en guide for assistert oppsett deg det grunnleggende. Deretter kan du importere aktuelle data fra det gamle systemet eller et annet selskap i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="create-new-company"></a>Opprett nytt selskap
Hvis du vil legge til et selskap til din [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du bruke veiviseren **Opprett nytt selskap** med assistert oppsett for å komme i gang. Oppsettsveiviseren er tilgjengelig fra **Selskaper**-vinduet og fra oppslaget i **Selskap**-feltet i **Mine innstillinger**.  

Oppsettsveiviseren har tre maler:

-   **Suite-evaluering**  
    Dette oppretter et selskap som ligner på demoselskapet, med eksempeldata og oppsettsdata.  
-   **Suite-produksjon**  
    Dette oppretter et selskap som ligner på **Mitt selskap**, med oppsettsdata, men uten eksempeldata.  
-   **Ny**  
    Dette oppretter et tomt selskap uten oppsettsdata.  

Hvis du ønsker å begynne med et nytt selskap, må du velge **Suite-produksjon** og deretter importere egne forretningsdata, for eksempel kunder, varer og leverandører. Velg **Ny**-malen hvis du vil definere alt fra begynnelsen. I så fall kan du bruke veiviseren **Selskapsoppsett** med assistert oppsett for å komme i gang med grunnleggende oppsettsdata.  

> [!NOTE]  
>   Når du oppretter et nytt selskap, tar litt tid før du kan bruke det i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Statusen for oppsettet i vinduet **Selskaper** viser når det nye selskapet er klart. Deretter du kan bytte til et nytt selskap ved hjelp av **Mine innstillinger**.  

Du kan opprette så mange nye selskaper under 30 dagers prøveperioden, men de er bare tilgjengelige under prøveperioden. Ta kontakt med din [!INCLUDE[d365fin](includes/d365fin_md.md)]-partner for mer informasjon.  

## <a name="company-setup"></a>Selskapsoppsett
Når du logger deg på et nytt selskap, kjøres veiviseren **Selskapsoppsett** automatisk og hjelper deg med å komme i gang. Du blir bedt om informasjon om selskapet, for eksempel adressen, bankdetaljer og lagerkostmetoden. Vi ber om opplysningene fordi de brukes som grunnlag for mange områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], som du ikke kan definere senere manuelt.  

For eksempel firmaadressen er inkludert i fakturaer og andre dokumenter, bankinformasjonen brukes i betalinger og kostmetoden brukes til å beregne priser og lagerverdisetting.  

Når du har det grunnleggende på plass, kan du definere gjenstående kjerneområder. Deretter er du klar til å legge til forretningsdataene, for eksempel kunder og leverandører. Hvis du vil ha mer informasjon, se [Konfigurere Dynamics 365 for Financials](setup.md).  

## <a name="see-also"></a>Se også
[Konfigurere Dynamics 365 for Financials](setup.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Endre grunnleggende innstillinger](ui-change-basic-settings.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  

