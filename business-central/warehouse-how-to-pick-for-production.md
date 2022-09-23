---
title: Plukk produksjon eller montering i grunnleggende lager
description: Når lagerlokasjonen krever plukkbehandling, men ikke leveringsbehandling, bruker du siden Lagerplukk til å organisere og registrere plukking av komponentene.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 2814fe1f9ca71c3a14bb288427c9b12603d0463a
ms.sourcegitcommit: 3acadf94fa34ca57fc137cb2296e644fbabc1a60
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/19/2022
ms.locfileid: "9529141"
---
# <a name="pick-for-production-or-assembly-in-basic-warehouse-configurations"></a>Plukke for montering eller produksjon i enkle lageroppsett

Hvordan du plasserer plukkomponenter for produksjons- eller monteringsordrer avhenger av hvordan lageret er definert som lokasjon. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Plukke komponenter for produksjon i grunnleggende lageroppsett.

Trekkmetoden påvirker også flyten av komponenter i produksjon. Hvis du vil ha mer informasjon, kan du se [Lagertrekke komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md).

I avanserte lagerkonfigurasjoner der lokasjoner krever både plukkinger og leveringer, må du bruke siden **Lagerplukk** til å hente komponenter som har trekkmetode satt til *Manuell*, *Plukk + Fremover* eller *Plukk + Bakover*, til produksjonsordrer. Hvis du vil ha mer informasjon, se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

I enkle lageroppsett der lokasjonen krever plukkbehandling, men ikke leveringsbehandling, kan du også bruke siden **Lagerplukk** til å organisere og registrere plukking av komponenter med trekkmetoden satt til *Manuell*. Når du registrerer en lagerplukking for en intern operasjon, for eksempel produksjon, bokføres forbruket av de plukkede komponentene samtidig. Du kan også bruke **Lagerflytting** med referanse til et kildedokument for å hente komponenter som har trekkmetoden er satt til *Manuell*, *Plukk + Fremover* eller *Plukk + Bakover*, til produksjonsordrer.

Når produksjonsoperasjoner er integrert med lagerprosesser, enten via hyller eller via lagerstyring, vil hyllen som komponentene tas fra, være hyllen som er definert på hver produksjonsordrekomponentlinje. Alle obligatoriske komponenter må være tilgjengelig i denne hyllen. Ellers stoppes den manuelle eller trukkede forbruksbokføringen for den komponenten.

**Lagerflytting** med referanser til kildedokumentet og **Lagerplukk**, kan ikke brukes til å plukke komponenter med trekkmetodene *Fremover* og *Bakover*. **Lagerplukk** kan bare brukes til å plukke komponenter med trekkmetoden *Manuell*. Hvis du vil behandle de gjenværende komponentene, bruker du **Lagerflytting** uten referanse til et kildedokument. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

> [!NOTE]  
>  Følgende viktige forskjeller finnes mellom lagerplukkinger og lagerflyttinger:  
>   
>  -   Når du registrerer en lagerplukking for en intern operasjon, for eksempel produksjon, bokføres forbruket av de plukkede komponentene samtidig. Når du registrerer en lagerflytting for en intern operasjon, registrerer du bare den fysiske flyttingen av de nødvendige komponentene til en hylle i operasjonsområdet, uten å bokføre forbruket.  
> -   Når du bruker lagerplukk, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinje hvilken *Hent*-hylle komponentene reduseres fra ved bokføring av forbruk. Når du bruker lagerflyttinger, definerer feltet **Hyllekode** på produksjonsordrekomponentlinjer hyllen *Plasser* i operasjonsområdet der lagermedarbeideren må plassere komponentene.  

En systemforutsetning for plukking, eller flytting, av komponenter for kildedokumenter er at det finnes en utgående lagerforespørsel for å varsle lagerområdet om komponentbehovet. Den utgående lagerforespørselen opprettes når produksjonsordrestatusen endres til Frigitt eller når en frigitt produksjonsordre opprettes.  

## <a name="to-pick-production-components-in-basic-warehouse-configurations-using-inventory-pick"></a>Slik plukker du produksjonskomponenter i grunnleggende lagerkonfigurasjoner med Lagerplukk

I enkle lageroppsett der lokasjonen er definert slik at bare plukking brukes, kan du plukke komponenter for produksjonsaktiviteter ved å bruke **Lagerplukk**-siden. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2.  Du får tilgang til produksjonsordrekomponentene ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
3.  Utfør plukkingen, og registrer deretter den aktuelle plukkinformasjonen i feltet **Ant. som skal håndt.**.  
4.  Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføringen oppretter de nødvendige lagerpostene og bokfører forbruket av varene.  

Du kan også opprette en **Lagerplukk** direkte fra den frigitte produksjonsordren. Velg handlingen **Opprett lagerplassering/-plukking/-flytting**, merk av for **Opprett lagerplukking**, og velg deretter **OK**-knappen.

Du kan også bruke **Lagerflytting** med referanse til kildedokumentet for å flytte varer mellom hyller. Du vil måtte registrere forbruket separat. Hvis du vil ha mer informasjon, kan du se [Massebokføre produksjonsforbruk](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Plukke for montering i grunnleggende lagerkonfigurasjoner

I avanserte lageroppsett der lokasjoner krever både plukk og leveringer, må du bruke siden **Lagerplukk** til å bringe komponenter til monteringsordrer. Hvis du vil ha mer informasjon, se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

I grunnleggende lageroppsett kan du også plukke for monteringsorder ved å bruke siden **Lagerflytting**. 

I grunnleggende lagerkonfigurasjoner der lokasjonen krever plukkbehandling, men ikke leveringsbehandling, brukes siden **Lagerplukk** også til å plukke, samle og levere for salgsordrer der varer må monteres før de kan leveres. Hvis du vil ha mer informasjon, kan du se [Håndtere montere-til-ordre-varer i lagerplukk](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtere montere-til-ordre-varer med lagerplukk

**Lagerplukk**-siden brukes også til å plukke og levere for salg der varer må monteres før de kan leveres. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Varer som skal leveres er ikke fysisk til stede i en hylle før de er montert og bokført som avgang til en hylle i monteringsområdet. Dette betyr at plukking av monter-til-ordre-varer til levering følger en spesiell flyt. Lagermedarbeidere tar monteringsvarene fra en hylle til leveringssonen og bokfører deretter lagerplukkingen. Det bokførte lagerplukket bokfører deretter monteringsavgangen, komponentforbruket og følgeseddelen.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til å automatisk opprette en lagerflytting når lagerplukkingen for monteringsvaren opprettes. Hvis du vil aktivere dette, må du velge feltet **Opprett flyttinger automatisk** på siden **Monteringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Lagerplukklinjer for salgsvarer opprettes på forskjellige måter avhengig av om ingen, noen eller alle salgslinjeantallene er montert til ordre.

Når du ved vanlig salg bruker lagerplukk til å bokføre levering av lagerantall, opprettes én lagerplukklinje for hver ordrelinje, eller flere hvis varen er plassert i forskjellige hyller. Denne plukklinjen er basert på antallet i **Levere (antall)**-feltet.

I montere-til-ordre-salg der hele antallet på ordrelinjen er montert til ordre, opprettes én lagerplukklinje for dette antallet. Dette betyr at verdien i feltet Antall å montere er det samme som verdien i feltet **Levere (antall)**. **Monter til ordre**-feltet er valgt på linjen.

Hvis en monteringsavgangsflyt er definert for lokasjonen, blir verdien i feltet **Hyllek. lev. fra m. til ordre** eller **Fra-Hyllekode for montering** satt inn (i denne rekkefølgen) i **Hyllekode-feltet på** lagerplukklinjen.

Hvis ingen hyllekode er angitt på ordrelinjen og ingen monteringsavgangsflyt er definert for lokasjonen, er **Hyllekode**-feltet på lagerplukklinjen tomt. Lagermedarbeideren må åpne **Hylleinnhold**-siden og velge hyllen der monteringsvarene er montert.

I kombinasjonsscenarier, der en del av antallet først må monteres og en annen del må plukkes fra lager, opprettes minst to lagerplukklinjer. Én plukklinje er til montere-til-ordre-antallet. Den andre plukklinjen avhenger av hvilke hyller som kan oppfylle det gjenværende antallet fra lageret. Hyllekoder på de to linjene er fylt ut på forskjellige måter som beskrevet for de to ulike salgstypene. Hvis du vil ha mer informasjon, kan du se delen "Kombinasjonsscenarier" i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

## <a name="filling-the-consumption-bin"></a>Fylle forbrukshyllen

Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.

![Flytskjema for hylle.](media/binflow.png "BinFlow")

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/paths/pick-ship-items-business-central/)

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
