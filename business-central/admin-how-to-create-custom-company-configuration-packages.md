---
title: Opprette egendefinerte konfigurasjonspakker for selskap | Microsoft-dokumentasjon
description: Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine. Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 99fad48961dc201a25af061cf982a1c65d9446bd
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878868"
---
# <a name="create-custom-company-configuration-packages"></a>Opprette egendefinerte konfigurasjonspakker for selskap
Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine. Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt.  

Vanligvis oppretter du en konfigurasjonspakke per funksjonsområde. Du kan for eksempel opprette en pakke for produksjonsfunksjonaliteten. Dette gjør at du kan bruke og definere nye områder i et selskap etter hvert som du trenger dem.  

En annen tilnærming ville være å opprette en pakke som inneholder tabeller som definerer oppsett, for eksempel følgende:  

-   Aktivaoppsett  
-   Finansoppsett  
-   Lageroppsett  
-   Produksjonsoppsett  
-   Kjøpsoppsett  
-   Markedsføringsoppsett  
-   Serviceoppsett  
-   Oppsett av kunde- og leverandørkonto  
-   Lagerstyringsoppsett  
-   Generelt bokføringsoppsett  
-   Mva-bokføringsoppsett  
-   Lagerbokføringsoppsett  

Hvis du vil se en fullstendig liste over oppsettstabeller, velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Manuelt oppsett** og velger deretter den relaterte koblingen.  

## <a name="to-create-a-custom-company-configuration-package"></a>Opprette egendefinerte konfigurasjonspakker for selskap  
1.  Opprett et nytt selskap. Hvis du vil ha mer informasjon, kan du se [Opprette nye selskaper i Business Central](about-new-company.md).  
3.  Konfigurere det nye selskapet etter dine behov. Fyll ut alle nødvendige oppsettstabeller.  
4.  Åpne det nye selskapet.
5. Åpne siden **Konfigurasjonsforslag**.  
6.  Legg til tabellene du vil overføre til et annet selskap, i forslaget. Tilordne forslagslinjene til pakken.  
7.  Opprett et spørreskjema for de mest brukte oppsettstabellene.  
8.  Opprett konfigurasjonsmaler for å gjøre det enklere å opprette hoveddata, for eksempel kunder eller varer.  
9.  Eksporter pakken som en .rapidstart-fil.  

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)
