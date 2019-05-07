---
title: Se gjennom og tilpasse eksisterende databasedata | Microsoft-dokumentasjon
description: Når du oppretter en konfigurasjonpakke for en løsning, kan du vise og tilpasse de tilgjengelige databasedataene etter kundens behov. Databasetabellen må ha en tilknyttet side.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: admin-how-to-create-custom-company-configuration-packages
ms.openlocfilehash: 95b16dc77bcdb0051447a4f153dd720661c52cf9
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "917939"
---
# <a name="review-and-customize-existing-database-data"></a>Se gjennom og tilpasse eksisterende databasedata
Når du oppretter en konfigurasjonpakke for en løsning, kan du vise og tilpasse de tilgjengelige databasedataene etter kundens behov. Databasetabellen må ha en tilknyttet side.  

### <a name="to-customize-data-in-the-database"></a>Slik tilpasser du data i databasen:  

1.  Finn tabellene i konfigurasjonsforslaget som inneholder dataene du vil vise eller tilpasse.  

    > [!NOTE]  
    >  Kontroller at hver tabell er tilordnet en side-ID. For standard [!INCLUDE[d365fin](includes/d365fin_md.md)]\-tabeller, fylles denne verdien ut automatisk. For egendefinerte tabeller må du oppgi ID\-en.  

2.  I fanebladet **Handlinger** under **Vis** velger du **Databasedata**.  

     Siden [!INCLUDE[d365fin](includes/d365fin_md.md)] for siden åpnes.  

3.  Se gjennom informasjonen som er tilgjengelig. Endre den etter behov ved å slette poster som ikke er relevante eller ved å legge til nye.  

## <a name="see-also"></a>Se også  
 [Behandle selskapskonfigurasjon i et forslag](admin-how-to-manage-company-configuration-in-a-worksheet.md)
