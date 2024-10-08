---
title: Definere eller endre kontoplanen
description: Finn ut mer om å konfigurere kontoplanen med finanskontoene som lagrer de økonomiske dataene.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'COA, cha of acc'
ms.search.form: '16, 17, 18, 118, 386, 391'
ms.date: 04/23/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="set-up-or-change-the-chart-of-accounts"></a>Definere eller endre kontoplanen

Kontoplanen viser finanskontoene som lagrer dine økonomiske data. [!INCLUDE[prod_short](includes/prod_short.md)] inneholder en standard kontoplan som er klar til å støtte forretningsvirksomheten din. Du kan imidlertid endre standardkontoene, og du kan legge til nye kontoer.
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE43KO9?rel=0]

## <a name="add-or-change-accounts"></a>Legg til eller endre kontoer

For hver kontoplan kan du åpne finanskontoen og legge til eller endre innstillinger. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] 

Hvis det er nødvendig kan du bruke mer enn én linje for et finanskontonavn. På siden **Finanskontokort**, i gruppen **Konto** velger du **Utvidede tekster** og fyller inn en eller flere linjer med kontonavnet og kopiert tekst.  

Når det gjelder konti av typen **Total** må du fylle ut feltet **Sammentelling**. På konti av typen **Til-sum**, fylles dette feltet ut automatisk av funksjonen Innrykking. Når du definerer alle kontoene, velger du handlingen **Behandle** og velger **Innrykk kontoplan**.  

> [!IMPORTANT]
> Hvis du har angitt definisjoner i feltet **Sammentelling** for konti av typen **Til-sum** før du utfører innrykkingen, må du skrive dem inn på nytt fordi funksjonen overskriver verdiene i alle **Til-sum**-feltene.

## <a name="delete-accounts"></a>Slett kontoer

Du kan slette en finanskonto. Før du sletter den, må imidlertid følgende betingelser være oppfylt:  

* Saldo på kontoen må være null.  
* Feltet **Tillat sletting av finanskto. før** må være satt på siden **Finansoppsett**, og kontoen kan ikke ha finansposter på eller etter denne datoen.  
* Hvis feltet **Kontroller finanskontobruk** er valgt på siden **Finansoppsett**, må ikke kontoen brukes i bokføringsgrupper eller bokføringsoppsett.  

[!INCLUDE[prod_short](includes/prod_short.md)] hindrer deg i å slette en finanskonto som lagrer data som er nødvendige i kontoplanen.  

Du kan også angi når folk skal kunne slette kontoer. På siden **Finansoppsett** fungerer vekslebryteren **Blokker sletting av finanskontoer** sammen med datoen i feltet **Kontroller finanskonto sletting etter** for å fungere som en ekstra validering. Hvis du aktiverer vekslebryteren **Sperr sletting av finanskontoer**, kan du ikke slette finanskontoer med poster etter datoen i feltet **Kontroller finanskontosletting etter**. Hvis du vil slette en slik konto, må noen med tilgang til siden **Finansoppsett** må deaktivere vekslebryteren **Blokker sletting av finanskontoer**.  

Hvis du aktiverer feltet **Sperr sletting av finanskontoer**, kan det anses som en anbefalt fremgangsmåte å definere datoen i feltet **Kontroller finanskonto sletting etter**, for eksempel til datoen du må lagre finansdataene til i henhold til forskrifter.  

### <a name="video-guidance"></a>Videoveiledning

Denne videoen viser hvordan du angir om og når folk kan slette finanskontoer.

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RW1g3oY]

## <a name="learning-path-set-up-the-chart-of-accounts-in-dynamics-365-business-central"></a>Læringsbane: Definer kontoplanen i Dynamics 365 Business Central

Vil du lære hvordan du definerer kontoplanen i [!INCLUDE [prod_short](includes/prod_short.md)]? Start deretter på følgende læringsbane [Sett opp kontoplanen i Dynamics 365 Business Central](/training/modules/chart-accounts-dynamics-365-business-central).

## <a name="see-also"></a>Se også

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

## [!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
