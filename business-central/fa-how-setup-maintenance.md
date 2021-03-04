---
title: Definere aktivavedlikehold | Microsoft-dokumentasjon
description: For å administrere aktivareparasjoner og -service angir du generelle vedlikeholdsopplysninger, koder for typen arbeid og en bokføringskonto for kost.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 60080b0a8982420ff2f3a6654d496395733bc425
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749221"
---
# <a name="set-up-fixed-asset-maintenance"></a>Definere aktivavedlikehold
For å styre vedlikehold av aktiva, må du først definere noen generelle vedlikeholdsopplysninger, en bokføringskonto for vedlikeholdskostnader og vedlikeholdskoder for typer arbeid, for eksempel rutineservice eller reparasjon.

## <a name="to-set-up-general-maintenance-information"></a>Slik definerer du generelle vedlikeholdsopplysninger:
Hvis du definerer vedlikeholdsfeltene, kan du bokføre vedlikeholdsutgifter fra aktivakladden.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet du vil definere forsikringsdekning for, og velg deretter handlingen **Rediger**.
3. Fyll ut feltene på hurtigfanen **Vedlikehold** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-maintenance-codes"></a>Slik definerer du vedlikeholdskoder
Når du bokfører vedlikeholdskostnader fra en finanskladd, fyller du ut feltet **Vedlikeholdskode** for å registrere hva slags vedlikehold som er utført, for eksempel rutineservice eller reparasjon.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vedlikehold**, og velg deretter den relaterte koblingen.
2. På **Vedlikehold**-siden definerer du koder for ulike typer vedlikeholdsarbeid.

## <a name="to-set-up-maintenance-expense-accounts"></a>Slik definerer du utgiftskonti for vedlikehold
Du må først angi et kontonummer på siden **Bokf.grupper - aktiva** for å kunne bokføre vedlikeholdskostnader.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokføringsgrupper – aktiva**, og velg deretter den relaterte koblingen.
2. Fyll ut feltet **Konto for vedlikeholdsutgifter** for hver enkelt bokføringsgruppe.

> [!NOTE]  
>   Hvis du vil at vedlikeholdskostnader skal fordeles på avdelinger eller prosjekter, må du definere en fordelingsnøkkel. Hvis du vil ha mer informasjon, kan du se [Definere generelle aktivafunksjoner](fa-how-setup-general.md).

## <a name="see-also"></a>Se også
[Definere aktiva](fa-setup.md)  
[Aktiva](fa-manage.md)  
[Finans](finance.md)  
[Komme i gang](product-get-started.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]