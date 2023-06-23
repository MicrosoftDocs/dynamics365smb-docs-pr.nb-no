---
title: Definer eller endre kontoplanen (inneholder video)
description: 'Kontoplanen viser finanskontoene som lagrer dine økonomiske data. Du kan endre standardkontoene i kontoplanen, og du kan legge til nye kontoer.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 01/21/2022
ms.author: edupont
---
# <a name="set-up-or-change-the-chart-of-accounts" />Definere eller endre kontoplanen

Kontoplanen viser finanskontoene som lagrer dine økonomiske data. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din. Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts" />Legg til eller endre kontoer

For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Hvis det er nødvendig kan du bruke mer enn én linje for et finanskontonavn. På siden **Finanskontokort**, i gruppen **Konto** velger du **Utvidede tekster** og fyller inn en eller flere linjer med kontonavnet og kopiert tekst.  

Når det gjelder konti av typen **Total** må du fylle ut feltet **Sammentelling**. På konti av typen **Til-sum**, fylles dette feltet ut automatisk av funksjonen Innrykking. Når du har definert alle kontiene, velger du handlingen **Behandle** og velger **Innrykk kontoplan**.  

> [!IMPORTANT]
> Hvis du har angitt definisjoner i feltet **Sammentelling** for konti av typen **Til-sum** før du utfører innrykkingen, må du skrive dem inn på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-feltene.

## <a name="delete-accounts" />Slett kontoer

Du kan slette en finanskonto. Før du sletter den, må imidlertid følgende være oppfylt:  

* Saldo på kontoen må være null.  
* Feltet **Tillat sletting av finanskto. før** må være satt på siden **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.  
* Hvis feltet **Kontroller finanskontobruk** er valgt på siden **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.  

[!INCLUDE[prod_short](includes/prod_short.md)] hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.  

## <a name="block-deletion-of-gl-accounts" />Blokker sletting av finanskontoer

[!INCLUDE [2022_releasewave1](includes/2022_releasewave1.md)]

Lanseringsbølge 2 for 2022 innfører ekstra beskyttelse mot utilsiktet sletting av finanskontoer selv i scenarioene der kriteriene oppfylles.  

Et nytt felt, **Sperr sletting av finanskontoer**, er lagt til på **Finansoppsett**-siden. Når feltet er angitt til *Ja*, fungerer feltet som en ekstra validering som betyr at du ikke kan slette finanskontoer med poster etter datoen i feltet **Kontroller finanskontosletting etter**. Hvis du vil slette en slik konto, må en bruker med tilgang til **Finansoppsett**-siden først sette dette feltet til *Nei*.  

Når du setter feltet **Sperr sletting av finanskontoer** til *Ja*, kan det anses som en beste fremgangsmåte, som er å definere datoen i feltet **Kontroller finanskonto sletting etter**, for eksempel til datoen du må lagre finansdataene fra.  

## <a name="see-related-microsoft-trainingtrainingmoduleschart-accounts-dynamics-365-business-centralindex" />Se relatert [Microsoft-opplæring](/training/modules/chart-accounts-dynamics-365-business-central/index)

## <a name="see-also" />Se også

[Finans og kontoplanen](finance-general-ledger.md)  
[Avstemme bankkonter](bank-manage-bank-accounts.md)  
[Arbeid med dimensjoner](finance-dimensions.md)  
[Importere data fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Arbeid med finansrapporter](bi-how-work-account-schedule.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Lukk resultatregnskapskonti i den franske versjonen](LocalFunctionality/France/how-to-close-income-statement-accounts.md)  
[Skriv ut resultatregnskap i den australske versjonen](LocalFunctionality/Australia/how-to-print-income-statements.md)  
[Skriv ut resultatregnskap i versjonen for New Zealand](LocalFunctionality/NewZealand/how-to-print-income-statements.md)  
[Definer og lukk resultatregnskapssaldi i den spanske versjonen](LocalFunctionality/Spain/how-to-set-up-and-close-income-statement-balances.md)  
[Rykk inn og valider kontoplanen i den spanske versjonen](LocalFunctionality/Spain/how-to-indent-and-validate-chart-of-accounts.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
