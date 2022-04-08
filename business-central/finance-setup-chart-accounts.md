---
title: Definere kontoplanen (inneholder video)
description: Kontoplanen viser finanskontoene som lagrer dine økonomiske data. Du kan endre standardkontoene i kontoplanen, og du kan legge til nye kontoer.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: COA, cha of acc
ms.search.form: 16, 17, 18, 118, 386, 391
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: f2ef4432d91d9f647a4bea58febbdfd5513a4350
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8520285"
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Definere eller endre kontoplanen

Kontoplanen viser finanskontoene som lagrer dine økonomiske data. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din.
Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Legg til eller endre kontoer

For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Hvis det er nødvendig kan du bruke mer enn én linje for et finanskontonavn. På siden **Finanskontokort**, i gruppen **Konto** velger du **Utvidede tekster** og fyller inn en eller flere linjer med tekst som skal kopieres, og kontonavnet.  

Når det gjelder konti av typen **Total** må du fylle ut feltet **Sammentelling**. På konti av typen **Til-sum**, fylles dette feltet ut automatisk av funksjonen Innrykking. Når du har definert alle kontiene, velger du handlingen **Behandle** og velger **Innrykk kontoplan**.  

> [!IMPORTANT]
> Hvis du har angitt definisjoner i feltet **Sammentelling** for konti av typen **Til-sum** før du utfører innrykkingen, må du skrive dem inn på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-feltene.

## <a name="delete-accounts"></a>Slett kontoer

Du kan slette en finanskonto. Før du sletter den, må imidlertid følgende være oppfylt:  

* Saldo på kontoen må være null.  
* Feltet **Tillat sletting av finanskto. før** må være satt på siden **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.  
* Hvis feltet **Kontroller finanskontobruk** er valgt på siden **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.  

[!INCLUDE[prod_short](includes/prod_short.md)] hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.  

## <a name="block-deletion-of-gl-accounts"></a>Blokker sletting av finanskontoer

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Lanseringsbølge 2 for 2022 innfører ekstra beskyttelse mot utilsiktet sletting av finanskontoer selv i scenarioene der kriteriene oppfylles.  

Et nytt felt, **Sperr sletting av finanskontoer**, legges til på **Finansoppsett**-siden. Feltet fungerer som en ekstra validering når en bruker prøver å slette en konto der det finnes poster etter datoen som er angitt i feltet **Kontroller finanskonto sletting etter**.

Når **Sperr sletting av finanskontoer**-feltet er angitt til *Ja*, kan du ikke slette finanskontoer som har poster etter datoen i feltet **Kontroller finanskontosletting etter**. Hvis du vil slette en slik konto, må en bruker med tilgang til **Finansoppsett**-siden først sette dette feltet til *Nei*. Kontoen kan deretter slettes.  

Det anbefales at du angir *Ja* i feltet **Sperr sletting av finanskontoer**. Vi anbefaler at du alltid har en dato som er angitt i feltet **Kontroller finanskonto sletting etter**, for eksempel tiden du trenger for å lagre finansdataene.  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Finans og kontoplanen](finance-general-ledger.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbeide med kontoskjemaer](bi-how-work-account-schedule.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lukk resultatregnskapskonti i den franske versjonen](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Skriv ut resultatregnskap i den australske versjonen](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Skriv ut resultatregnskap i versjonen for New Zealand](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Definer og lukk resultatregnskapssaldi i den spanske versjonen](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Rykk inn og valider kontoplanen i den spanske versjonen](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]