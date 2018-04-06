---
title: Opprette egendefinerte konfigurasjonspakker for selskap | Microsoft-dokumentasjon
description: "Etter hvert som virksomheten øker, kommer du sannsynligvis til å være avhengig av et sett med selskapstyper som du bruker med de fleste av kundene dine. Du kan forenkle implementeringsprosessen ved å gjøre disse typene om til selskapskonfigurasjonspakker som kan brukes på nytt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7feaa0e41cf5800ffd51d5807a90f6929492804e
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

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

Hvis du vil vise en fullstendig liste over oppsettstabeller, velger du ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angir **Oppsett** og velger deretter den relaterte koblingen.  

## <a name="to-create-a-custom-company-configuration-package"></a>Opprette egendefinerte konfigurasjonspakker for selskap  
1.  Opprette en ny [!INCLUDE[d365fin](includes/d365fin_md.md)]. ***IKKE MULIG Kobling til hjelp for "Opprette en ny leier"***.   
2.  Opprett et nytt selskap for bransje- eller løsningsmalen. Hvis du vil ha mer informasjon, kan du se [Opprette et nytt selskap](admin-how-to-create-a-new-company.md).  
3.  Konfigurer det nye selskapet etter dine behov. Fyll ut alle nødvendige oppsettstabeller.  
4.  Åpne det nye selskapet.
5. Åpne vinduet **Konfigurasjonsforslag**.  
6.  Legg til tabellene du vil overføre til et annet selskap, i forslaget. Tilordne forslagslinjene til pakken.  
7.  Opprett et spørreskjema for de mest brukte oppsettstabellene.  
8.  Opprett konfigurasjonsmaler for å gjøre det enklere å opprette hoveddata, for eksempel kunder eller varer.  
9.  Eksporter pakken som en .rapidstart-fil.  

## <a name="see-also"></a>Se også  
[Konfigurere et selskap med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administrasjon](admin-setup-and-administration.md)

