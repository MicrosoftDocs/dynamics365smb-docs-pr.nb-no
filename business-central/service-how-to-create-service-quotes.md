---
title: Opprette servicetilbud | Microsoft-dokumentasjon
description: Du kan bruke siden **Servicetilbud** til å opprette dokumenter der du angir opplysninger om en service, for eksempel reparasjon og vedlikehold, på servicevarer etter forespørsel fra kunde. Du kan bruke et servicetilbud som et foreløpig utkast til en serviceordre, og deretter konvertere tilbudet til en serviceordre.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 1486be71b0b848aa48996f4161f8987322a09e32
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "802396"
---
# <a name="create-service-quotes"></a>Opprette servicetilbud
Du kan betrakte servicetilbud som grunnlag for serviceordrer. De er faktisk omtrent like. Begge inneholder opplysninger som hvem kunden er, ordretype, varen som trenger service, fakturerings- og leveringsopplysninger og informasjon om det faktiske servicearbeidet.
 
Du kan bruke et servicetilbud som et foreløpig utkast til en serviceordre, og deretter konvertere tilbudet til en serviceordre.  
  
## <a name="to-create-a-service-quote"></a>Slik oppretter du et servicetilbud  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicetilbud**, og velg deretter den relaterte koblingen.  
2. Opprett et nytt servicetilbud.  
3. I **Nr.** -feltet angir du et nummer for servicetilbudet. Hvis du har definert en nummerserie for servicetilbud på siden **Serviceoppsett**, kan du eventuelt trykke Enter for å velge det neste tilgjengelige servicetilbudsnummeret.  
4. I feltet **Kundenr.**  -feltet velger du den aktuelle kunden fra listen.  

  > [!Note]  
  >  Kundefeltene fylles ut automatisk med informasjonen fra **Kunde**-kortet. Hvis et **Kunde**-kort ikke finnes for kunden og du har definert en kundemal, kan du opprette kunden fra servicetilbudet. Fyll ut de relevante feltene, og velg deretter handlingen **Opprett kunde**.  
  
5. Avhengig av innstillingene på hurtigfanen **Obligatoriske felt** på siden **Serviceoppsett** kan det hende du må fylle ut feltet **Serviceordretype** og **Selgerkode**.  
6. Fylle ut servicevarelinjene.  
7. Registrere beregnet kost i servicelinjene.  
  
## <a name="see-also"></a>Se også  
[Opprette serviceordrer](service-how-to-create-service-orders.md)  
[Arbeide med serviceoppgaver](service-how-to-work-on-service-tasks.md)  

 