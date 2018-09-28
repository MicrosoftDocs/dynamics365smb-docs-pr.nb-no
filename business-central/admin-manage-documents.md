---
title: Administrere, slette eller komprimere dokumenter | Microsoft-dokumentasjon
description: Behold dine historiske data, eller slett dem.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Administrere dokumenter
En sentral rolle, for eksempel programadministrator, må regelmessig håndtere oppsamlede historiske dokumenter ved å slette eller komprimere dem.  

## <a name="delete-documents"></a>Slette dokumenter
I enkelte situasjoner kan det hende du må slette fakturerte bestillinger som ikke allerede er slettet. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer at de slettede bestillingene er fullstendig fakturert. Du kan ikke slette bestillinger som ikke er fullstendig fakturert og mottatt.  

Ordrereturer slettes vanligvis etter at de er fakturert. Når du bokfører en faktura, overføres den til vinduet **Bokført kjøpskreditnota**. Hvis du merket av for **Returforsendelse i kreditnota** i **Kjøpsoppsett**-vinduet, overføres fakturaen til vinduet **Bokført returforsendelse**. Du kan slette dokumentene ved hjelp av kjørselen **Slett fakturerte best.returer**. Før du sletter, kontrollerer kjørselen om bestillingsreturer er fullstendig levert og fakturert.  

Rammebestillinger slettes ikke når du har behandlet og fakturert alle de relaterte bestillingene. Du kan slette rammebestillinger med kjørselen **Slett fakturerte rammebestillinger**.  

Fakturerte serviceordrer slettes vanligvis automatisk etter at de er fullstendig fakturert. Når en faktura bokføres, opprettes en tilhørende post i vinduet **Bokførte servicefakturaer**. Det bokførte dokumentet kan vises i vinduet **Bokført servicefaktura**.  

Serviceordrer slettes ikke automatisk hvis det totale antallet i ordren ikke er bokført fra selve serviceordren, men fra **Servicefaktura**-vinduet. Da må du kanskje slette fakturerte ordrer som ikke er slettet. Du kan gjøre dette ved hjelp av kjørselen **Slett fakturerte serviceordrer**.  

## <a name="see-also"></a>Se også  
[Administrasjon](admin-setup-and-administration.md)  

