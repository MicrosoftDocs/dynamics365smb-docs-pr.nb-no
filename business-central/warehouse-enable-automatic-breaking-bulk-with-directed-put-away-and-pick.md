---
title: Automatisk samlet oppbryting med lagerstyring og plukk | Microsoft-dokumentasjon
description: For lokasjoner som bruker lagerstyring kan du bryte opp en større enhet til mindre enheter når det oppretter lagerinstruksjoner som oppfyller behovene fra kildedokumenter, produksjonsordrer eller interne plukk og plasseringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: c00a866a731a321c0cf2e7f29dce4fba296b6d06
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385702"
---
# <a name="enable-automatic-breaking-bulk-with-directed-put-away-and-pick"></a>Aktivere automatisk samlet oppbryting med lagerstyring og plukk
For lokasjoner som bruker lagerstyring kan [!INCLUDE[prod_short](includes/prod_short.md)] i enkelte situasjoner utføre automatisk anbrekk, det vil si konvertere en større enhet til mindre enheter når det oppretter lagerinstruksjoner som oppfyller behovene fra kildedokumenter, produksjonsordrer eller interne plukk og plasseringer. Anbrekk betyr også noen ganger å samle mindre enheter, hvis det er nødvendig for å imøtekomme utgående forespørsler. Det vil si å konvertere de større enhetene i kildedokumentet eller produksjonsordren til de mindre enhetene som er tilgjengelig i lageret.   

## <a name="breakbulking-in-picks"></a>Anbrekk i plukkinger  
Hvis du vil lagre varer i flere enheter og vil tillate at de kombineres automatisk etter behov i plukkprosessen, merker du av for **Tillat anbrekk** på lokasjonskortet.  

Når det skal utføres en oppgave, ser programmet automatisk etter en vare i samme enhet. Hvis det ikke kan finne denne varetypen, og du har valgt dette feltet, vil programmet foreslå at du kan konvertere en større enhet til den enheten som er nødvendig.  

Hvis systemet bare kan finne mindre enheter, vil det foreslå at du kan samle varer for å oppfylle antallet i følgeseddelen eller produksjonsordren. I virkeligheten konverterer det den store enheten i kildedokumentet til mindre enheter for plukking.  

## <a name="breakbulking-in-put-aways"></a>Anbrekk i plasseringer  
I plasseringen foreslår programmet automatisk Plasser-handlingslinjer i plasseringsenheten, for eksempel stykkevis, selv om varene ankommer i en annen enhet.  

## <a name="breakbulking-in-movements"></a>Anbrekk i flyttinger  
Programmet utfører også automatisk anbrekk i etterfyllingsflyttinger hvis **Tillat anbrekk**-feltet er valgt på hurtigfanen **Alternativer** på siden **Beregn etterfylling av hylle**.  

Du kan vise resultatene av prosessen med konvertering fra én enhet til en annen som midlertidige anbrekkslinjer i plasserings-, plukk- eller flytteinstruksjonen.  

> [!NOTE]  
>  Hvis du velger feltet **Anbrekksfilter** i lagerinstruksjonshodet, vil programmet skjule anbrekkslinjene når den større enheten skal brukes helt. Hvis en pall for eksempel har 12 stykker, og du skal bruke alle 12, vil plukkingen be deg ta 1 pall i stedet for 12 stykker. Hvis du imidlertid bare skal plukke 9 stykker, skjules ikke anbrekkslinjen, selv om du har valgt **Anbrekksfilter**-feltet, fordi du må sette de resterende tre stykkene et eller annet sted i lageret.  

> [!NOTE]  
>  Hvis du vil at enhetene skal fungere optimalt i lageret, også i forbindelse med anbrekksfunksjonaliteten, bør du prøve følgende der det er mulig:  
>   
> - Definer den grunnleggende vareenheten til den minste enheten du forventer å håndtere i lagerprosessene.  
> - Definer de alternative vareenhetene som multiplum av den grunnleggende enheten.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]