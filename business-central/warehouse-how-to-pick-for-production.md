---
title: Plukke for produksjon i enkle lageroppsett | Microsoft-dokumentasjon
description: Når lagerlokasjonen krever plukkbehandling, men ikke krever leveringsbehandling, bruker du siden **Lagerplukk** til å organisere og registrere plukking av komponenter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e58299e7edecc35c7757ebc91d1e444df299ee13
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2310303"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Plukke for montering eller produksjon i enkle lageroppsett
Hvordan du plasserer plukkomponenter for produksjons- eller monteringsordrer avhenger av hvordan lageret er definert som lokasjon. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

I enkle lageroppsett der lokasjonen krever plukkbehandling, men ikke leveringsbehandling, bruker du siden **Lagerplukk** til å organisere og registrere plukking av komponenter.  

I grunnleggende lageroppsett må du plukke for monteringsorder ved å bruke **Lagerflytting**-siden. Hvis du vil ha mer informasjon, kan du se [Håndtere montere-til-ordre-varer i lagerplukk](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

I avanserte lageroppsett der lokasjoner krever både plukk og leveringer, bruker du **Plukk**-siden til å bringe komponenter til produksjons- eller monteringsordrer. Hvis du vil ha mer informasjon, se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

> [!NOTE]  
>  Følgende viktige forskjeller finnes mellom lagerplukkinger og lagerflyttinger:  
>   
>  -   Når du registrerer en lagerplukking for en intern operasjon, for eksempel produksjon, bokføres forbruket av de plukkede komponentene samtidig. Når du registrerer en lagerflytting for en intern operasjon, registrerer du bare den fysiske flyttingen av de nødvendige komponentene til en hylle i operasjonsområdet, uten å bokføre forbruket.  
> -   Når du bruker lagerplukk, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinje hvilken *Hent*-hylle komponentene reduseres fra ved bokføring av forbruk. Når du bruker lagerflyttinger, definerer **Hyllekode**-feltet på produksjonsordrekomponentlinjer *Plasser*-hyllen i operasjonsområdet der lagermedarbeideren må plassere komponentene.  

En systemforutsetning for plukking, eller flytting, av komponenter for kildedokumenter er at det finnes en utgående lagerforespørsel for å varsle lagerområdet om komponentbehovet. Den utgående lagerforespørselen opprettes når produksjonsordrestatusen endres til Frigitt eller når en frigitt produksjonsordre opprettes.  

## <a name="to-pick-components-in-basic-warehouse-configurations"></a>Plukke komponenter i enkle lageroppsett
I enkle lageroppsett der lokasjonen er definert slik at bare plukking brukes, kan du plukke komponenter for produksjonsaktiviteter ved å bruke **Lagerplukk**-siden. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2.  Du får tilgang til produksjonsordrekomponentene ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
3.  Utfør plukkingen, og registrer deretter den aktuelle plukkinformasjonen i vinduet **Plukket ant.**.  
4.  Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføringen oppretter de nødvendige lagerpostene og bokfører forbruket av varene.  

Du kan også opprette en **Lagerplukk** direkte fra den frigitte produksjonsordren. Velg handlingen **Opprett lagerplassering/-plukking**, merk av for **Opprett lagerplukking**, og velg deretter **OK**-knappen.

Du kan også bruke siden **Lagerflytting** til å flytte varer mellom hyller ad hoc, noe som betyr uten referanse til et kildedokument.
Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

### <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtere montere-til-ordre-varer med lagerplukk
**Lagerplukk**-siden brukes også til å plukke og levere for salg der varer må monteres før de kan leveres. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Varer som skal leveres er ikke fysisk til stede i en hylle før de er montert og bokført som avgang til en hylle i monteringsområdet. Dette betyr at plukking av monter-til-ordre-varer til levering følger en spesiell flyt. Lagermedarbeidere tar monteringsvarene fra en hylle til leveringssonen og bokfører deretter lagerplukkingen. Det bokførte lagerplukket bokfører deretter monteringsavgangen, komponentforbruket og følgeseddelen.

Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til å automatisk opprette en lagerflytting når lagerplukkingen for monteringsvaren opprettes. Hvis du vil aktivere dette, må du velge feltet **Opprett flyttinger automatisk** på siden **Monteringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerplukklinjer for salgsvarer opprettes på forskjellige måter avhengig av om ingen, noen eller alle salgslinjeantallene er montert til ordre.

Når du ved vanlig salg bruker lagerplukk til å bokføre levering av lagerantall, opprettes én lagerplukklinje for hver ordrelinje, eller flere hvis varen er plassert i forskjellige hyller. Denne plukklinjen er basert på antallet i **Levere (antall)**-feltet.

I montere-til-ordre-salg der hele antallet på ordrelinjen er montert til ordre, opprettes én lagerplukklinje for dette antallet. Dette betyr at verdien i feltet Antall å montere er det samme som verdien i feltet **Levere (antall)**. **Monter til ordre**-feltet er valgt på linjen.

Hvis en monteringsavgangsflyt er definert for lokasjonen, blir verdien i feltet **Hyllek. lev. fra m. til ordre** eller **Fra-Hyllekode for montering** satt inn (i denne rekkefølgen) i **Hyllekode-feltet på** lagerplukklinjen.

Hvis ingen hyllekode er angitt på ordrelinjen og ingen monteringsavgangsflyt er definert for lokasjonen, er **Hyllekode**-feltet på lagerplukklinjen tomt. Lagermedarbeideren må åpne **Hylleinnhold**-siden og velge hyllen der monteringsvarene er montert.

I kombinasjonsscenarier, der en del av antallet først må monteres og en annen del må plukkes fra lager, opprettes minst to lagerplukklinjer. Én plukklinje er til montere-til-ordre-antallet. Den andre plukklinjen avhenger av hvilke hyller som kan oppfylle det gjenværende antallet fra lageret. Hyllekoder på de to linjene er fylt ut på forskjellige måter som beskrevet for de to ulike salgstypene. Hvis du vil ha mer informasjon, kan du se delen "Kombinasjonsscenarier" i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylle forbrukshyllen
Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.

![Flytskjema for hylle](media/binflow.png "BinFlow")

## <a name="see-also"></a>Se også
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
