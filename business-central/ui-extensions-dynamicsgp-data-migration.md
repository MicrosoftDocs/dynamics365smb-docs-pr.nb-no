---
title: "Overføre data fra Dynamics GP med utvidelsen for datamigrering | Microsoft-dokumentasjon"
description: "Bruk utvidelsen Dynamics GP-datamigrering til å overføre kunder, leverandører, lagervarer og konti fra Dynamics GP til Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: nb-no
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a>Dynamics GP-utvidelse for dataoverføring for Business Central 
Denne utvidelsen gjør det enkelt å overføre kunder, leverandører og lagervarer og konti fra Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis virksomheten din bruker Dynamics GP i dag, kan du eksportere relevant hovedposter og deretter åpne en assistert oppsettsveiledning for å legge til data i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Imporere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Eksportere data fra Dynamics GP
Du må ha eksportert noen av eller alle dine eksisterende kunder, leverandører, varer og kontoer til en fil ved hjelp av funksjonen for dataeksport i Dynamics GP. I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende datatyper:

* Konto  
* Kunde  
* Element  
* Leverandør  

Utvidelsen Dynamics GP-datamigrering automatisk tilordner de eksporterte dataene, slik at dataene er raskt tilgjengelige for deg i det nye selskapet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Under prosessen opprettes understøttende informasjon om oppsettet, for eksempel bokføringsgrupper. Lagervarer skal hentes inn i systemet med FIFO som kostvaluderingsmetode. Kontoene defineres som hovedkontosegmentet fra Dynamics GP med dimensjoner, fordi [!INCLUDE[d365fin](includes/d365fin_long_md.md)] ikke har kontosegmenter.

## <a name="see-also"></a>Se også
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  

