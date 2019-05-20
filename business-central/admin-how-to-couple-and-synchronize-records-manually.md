---
title: Sammenkoble og synkronisere poster manuelt | Microsoft Docs
description: Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster i en tabell i Business Central og Dynamics 365 for Sales-enhet som er koblet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245408"
---
# <a name="couple-and-synchronize-records-manually"></a>Sammenkoble og synkronisere poster manuelt
Dette emnet beskriver hvordan du kobler sammen én eller flere poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i [!INCLUDE[crm_md](includes/crm_md.md)]. Kobling av poster lar deg vise [!INCLUDE[crm_md](includes/crm_md.md)]-informasjon fra [!INCLUDE[d365fin](includes/d365fin_md.md)], og omvendt. Kopling lar deg også synkronisere data mellom postene. Du kan koble eksisterende poster, eller du kan opprette og koble nye poster.

> [!Note]
> Koble og synkronisere data med [!INCLUDE[crm_md](includes/crm_md.md)] er bare tilgjengelig hvis systemansvarlig har opprettet en kobling mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)]. En rask måte å kontrollere på, er å åpne **Kunde**-kortet og se etter handlingen **Konfigurer kobling**. Hvis handlingen er tilgjengelig, er appene koblet.   

## <a name="to-couple-a-record"></a>Koble en post  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] åpner du kortet for posten du vil koble. For eksempel kunde- eller kontaktkortet.  

    Du kan også bare åpne listesiden og velge posten du vil koble.  

2.  Velg handlingen **Konfigurer kobling**.  
3.  Fyll ut feltene, og klikk deretter **OK**.  

## <a name="to-synchronize-a-single-record"></a>Synkronisere en enkeltoppføring  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] åpner du kortet for posten du vil koble. For eksempel kunde- eller kontaktkortet.  
2.  Velg **Synkroniser nå**-handlingen.  
3.  Hvis en post kan synkroniseres fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**-knappen.  

## <a name="to-synchronize-multiple-records"></a>Synkronisere flere poster  
1.  I [!INCLUDE[d365fin](includes/d365fin_md.md)] åpner du listesiden for posten, for eksempel listesiden for kunder eller kontakter.  
2.  Velg postene som skal synkroniseres, og velg deretter **Synkroniser nå**-handlingen.  
3.  Hvis postene kan synkroniseres fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**-knappen.  

## <a name="see-also"></a>Se også  
[Bruke Dynamics 365 for Sales fra Business Central](marketing-integrate-dynamicscrm.md)
