---
title: Samlet oppbryting med lagerstyring og plukk
description: 'Lær hvordan du aktiverer automatisk oppbryting med lagerstyring og plukk samt anbrekk i plukkinger, plasseringer, flyttinger og mer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '5703, 7352'
ms.date: 11/04/2022
ms.author: bholtorf
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick" />Aktivere automatisk samlet oppbryting med lagerstyring og plukk

For lokasjoner som bruker lagerstyring kan [!INCLUDE[prod_short](includes/prod_short.md)] bryte opp større enheter til mindre enheter når det oppretter lagerinstruksjoner for kildedokumenter, produksjonsordrer eller interne plukk og plasseringer. For anbrekk kan også bety å samle varer i mindre enheter som tilsvarer antallet i en større enhet i et kildedokument eller en produksjonsordre.

## <a name="breakbulk-in-picks" />Anbrekk i plukkinger

Hvis du vil lagre varer i flere enheter i en lokasjon og vil tillate at de kombineres automatisk i plukkprosessen, slår du på vekslebryteren **Tillat anbrekk** på siden Lokasjonskort. For å oppfylle en oppgave ser [!INCLUDE [prod_short](includes/prod_short.md)] automatisk etter en vare i samme enhet. Hvis det ikke finner noen, foreslår [!INCLUDE [prod_short](includes/prod_short.md)] at du bryter en større enhet inn i enheten som er nødvendig.  

Hvis bare mindre enheter er tilgjengelige, vil [!INCLUDE [prod_short](includes/prod_short.md)] foreslå at du kan samle varer for å oppfylle antallet i følgeseddelen eller produksjonsordren. I virkeligheten konverterer det den store enheten i kildedokumentet til mindre enheter for plukking.  

## <a name="breakbulk-in-put-aways" />Anbrekk i plasseringer

[!INCLUDE [prod_short](includes/prod_short.md)] foreslår plasseringshandlingslinjer i plasseringsenheten i lagerplasseringer. Det kan for eksempel foreslå stykker selv om varene ankommer i en annen enhet.  

## <a name="breakbulk-in-movements" />Anbrekk i flyttinger

[!INCLUDE [prod_short](includes/prod_short.md)] kan også anbrekke i etterfyllingsbevegelser hvis vekslebryteren **Tillat anbrekk** på siden **Beregn hylleetterfylling** er aktivert.  

Du kan vise resultatene av prosessen med konvertering fra én enhet til en annen som midlertidige anbrekkslinjer i plasserings-, plukk- eller flytteinstruksjonen.  

> [!NOTE]  
> Hvis du velger feltet **Anbrekksfilter** i lagerinstruksjonshodet, vil programmet skjule anbrekkslinjene når den større enheten skal brukes helt. Hvis en pall for eksempel har 12 stykker og du skal bruke alle 12, vil plukkingen be deg ta 1 pall i stedet for 12 stykker. Hvis du imidlertid bare må plukke 9 stykker, er ikke anbrekkslinjer skjult, selv om du har valgt feltet **Anbrekksfilter**. Linjene er ikke skjult fordi du må sette de resterende tre stykkene et sted i lageret.  

> [!NOTE]  
> Hvis du vil at enhetene skal fungere optimalt i lageret, også i forbindelse med anbrekksfunksjonaliteten, bør du prøve følgende:  
>
> - Definer den grunnleggende vareenheten til den minste enheten du forventer å håndtere i lagerprosessene.  
> - Definer de alternative vareenhetene som multiplum av den grunnleggende enheten.  

## <a name="see-also" />Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md) 
[Monteringsstyring](assembly-assemble-items.md)
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
