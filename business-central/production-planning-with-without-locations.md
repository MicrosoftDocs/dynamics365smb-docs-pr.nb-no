---
title: Planlegge med/uten lokasjoner | Microsoft-dokumentasjon
description: Det er viktig å forstå planlegging med eller uten lokasjonskoder på behovslinjer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 49448cc56d76846c70471a53a257986b543f11b3
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4758820"
---
# <a name="planning-with-or-without-locations"></a>Se Planlegge med/uten lokasjoner.
Når det gjelder planlegging med eller uten lokasjonskoder på behovslinjer, fungerer planleggingssystemet på ordinær måte når:  

-   behovslinjene alltid inneholder lokasjonskoder og systemet fullt ut bruker lagerføringsenheter, inkludert det relevante lokasjonsoppsettet.  
-   behovslinjene aldri inneholder lokasjonskoder og systemet ikke bruker lagerføringsenheter eller lokasjonsoppsett (se siste scenario nedenfor).  

Hvis imidlertid behovslinjene noen ganger har lokasjonskoder og andre ganger ikke, følger planleggingssystemet visse regler avhengig av oppsettet.  

## <a name="demand-at-location"></a>Behov i lokasjon  
Når planleggingssystemet oppdager behov i en lokasjon (en linje med en lokasjonskode), fungerer det på ulike måter avhengig av 3 viktige oppsettsverdier.  

Under en kjørsel kontrolleres de 3 oppsettsverdiene etter tur, og planleggingen utføres i tråd med dette:  

1.  Er det merket av i feltet **Lokasjon obligatorisk**?  

    Hvis ja:  

2.  Finnes det lagerføringsenhet for varen?  

    Hvis ja:  

    Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.  

    Hvis nei:  

3.  Inneholder feltet **Komponenter ved lokasjon** den nødvendige lokasjonskoden?  

    Hvis ja:  

    Varen planlegges i henhold til planleggingsparametrene på varekortet.  

    Hvis nei:  

    Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti*, Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme. (Varer som bruker gjenbestillingsprinsippet  *Ordre*, fortsetter med å bruke  *Ordre* samt de andre innstillingene.)  

> [!NOTE]  
>  Dette minimumsalternativet dekker bare eksakt behov. Eventuelle planleggingsparametre som er definert, ignoreres.  

Se variasjoner i scenariene nedenfor.  

## <a name="demand-at-blank-location"></a>Behov i "tom lokasjon"  
Selv om det er merket av i feltet **Lokasjon obligatorisk**, tillater systemet at det opprettes behovslinjer uten en lokasjonskode – også kalt *TOM* lokasjon. Dette er et systemavvik fordi ulike oppsettsverdier er rettet mot lokasjoner (se ovenfor), og planleggingsmotoren vil derfor ikke opprette en planleggingslinje for en slik behovslinje. Hvis det ikke er merket av i feltet **Lokasjon obligatorisk**, men noen av lokasjonsoppsettsverdiene finnes, regnes dette også som et avvik, og planleggingssystemet vil reagere med å benytte "minimumsalternativet":   
Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir *Ordre)*, Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.  

Se variasjoner i oppsettsscenariene nedenfor.  

### <a name="setup-1"></a>Oppsett 1:  

-   Lokasjon obligatorisk = *Ja*  
-   LFE defineres for  *RØD*  
-   Komponenter ved lokasjon =  *BLÅ*  

#### <a name="case-11-demand-is-at--red-location"></a>Eksempel 1.1: Behovet er i  *RØD* lokasjon  

Varen planlegges i henhold til planleggingsparametrene på LFE-kortet (inkludert mulig overføring).  

#### <a name="case-12-demand-is-at--blue-location"></a>Eksempel 1.2: Behovet er i  *BLÅ* lokasjon  

Varen planlegges i henhold til planleggingsparametrene på varekortet.  

#### <a name="case-13-demand-is-at--green-location"></a>Eksempel 1.3: Behovet er i  *GRØNN* lokasjon  

Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.  

#### <a name="case-14-demand-is-at--blank-location"></a>Eksempel 1.4: Behovet er i  *TOM* lokasjon  

Varen planlegges ikke fordi ingen lokasjon er definert på behovslinjen.  

### <a name="setup-2"></a>Oppsett 2:  

-   Lokasjon obligatorisk = *Ja*  
-   LFE finnes ikke  
-   Komponenter ved lokasjon =  *BLÅ*  

#### <a name="case-21-demand-is-at--red-location"></a>Eksempel 2.1: Behovet er i  *RØD* lokasjon  

Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.  

#### <a name="case-22-demand-is-at--blue-location"></a>Eksempel 2.2: Behovet er i  *BLÅ* lokasjon  

Varen planlegges i henhold til planleggingsparametrene på varekortet.  

### <a name="setup-3"></a>Oppsett 3:  

-   Lokasjon obligatorisk = *Nei*  
-   LFE finnes ikke  
-   Komponenter ved lokasjon =  *BLÅ*  

#### <a name="case-31-demand-is-at--red-location"></a>Eksempel 3.1: Behovet er i  *RØD* lokasjon  

Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.  

#### <a name="case-32-demand-is-at--blue-location"></a>Eksempel 3.2: Behovet er i  *BLÅ* lokasjon  

Varen planlegges i henhold til planleggingsparametrene på varekortet.  

#### <a name="case-33-demand-is-at--blank-location"></a>Eksempel 3.3: Behovet er i  *TOM* lokasjon  

Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.  

### <a name="setup-4"></a>Oppsett 4:  

-   Lokasjon obligatorisk = *Nei*  
-   LFE finnes ikke  
-   Komponenter ved lokasjon =  *TOM*  

#### <a name="case-41-demand-is-at--blue-location"></a>Eksempel 4.1: Behovet er i  *BLÅ* lokasjon  

Varen planlegges slik: Gjenbestillingsprinsipp =  *Parti for parti* ( *Ordre* forblir  *Ordre*), Ta med lagerbeholdning =  *Ja*, alle andre planleggingsparametre = tomme.  

#### <a name="case-42-demand-is-at--blank-location"></a>Eksempel 4.2: Behovet er i  *TOM* lokasjon  

Varen planlegges i henhold til planleggingsparameterne på varekortet.  

Som du ser i det siste scenariet, kan du bare få et riktig resultat for en behovslinje uten lokasjonskode ved å deaktivere alle oppsettsverdier som gjelder lokasjoner. På samme måte kan du bare få stabile planleggingsresultater for behov i lokasjoner ved å bruke lagerføringsenheter.  

Hvis du ofte planlegger for behov i lokasjoner, anbefaler vi derfor på det sterkeste å bruke funksjonen Lagerføringsenheter.  

## <a name="see-also"></a>Se også
[Planlegging](production-planning.md)    
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)    
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)   
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
