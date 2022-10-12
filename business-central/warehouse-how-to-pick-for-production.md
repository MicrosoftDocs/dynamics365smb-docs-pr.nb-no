---
title: Plukke for produksjon, montering eller jobber i enkelt lager
description: Når lagerlokasjonen krever at du behandler plukk, men ikke leveringer, bruker du siden Lagerplukk til å organisere og registrere komponentene som ble plukket.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/02/2022
ms.author: bholtorf
ms.openlocfilehash: 859c70ebc51f2649000d41817d173292ed5b0870
ms.sourcegitcommit: b4da421c19c3aa3031b0344ec2829d2038be6642
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/03/2022
ms.locfileid: "9617880"
---
# <a name="pick-for-production-assembly-or-jobs-in-basic-warehouse-configurations"></a>Plukke for produksjon, montering eller jobber i enkle lageroppsett

Hvordan du plasserer plukkomponenter for produksjons- eller monteringsordrer avhenger av hvordan lageret er definert som lokasjon. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).

## <a name="pick-for-production-in-basic-warehouse-configurations"></a>Plukke komponenter for produksjon i grunnleggende lageroppsett.

Hvis en lokasjon krever plukkbehandling, men ikke leveringsbehandling, kan du bruker siden **Lagerplukk**. Med siden **Lagerplukk** kan du organisere og registrere plukking av varer der trekkmetoden er satt til **Manuell**. Når du registrerer et lagerplukk, bokføres forbruket for de plukkede komponentene. Du kan også bruke en **lagerflytting** med referanse til et kildedokument for å tildele komponenter som har trekkmetoden er satt til **Manuell**, **Plukk + Fremover** eller **Plukk + Bakover**, til produksjonsordrer.

Hvis produksjon er integrert med lagerprosesser gjennom hyller eller via lagerstyring, vil hyllen som komponentene tas fra hyllen på produksjonsordrelinjen. Alle obligatoriske komponenter må være tilgjengelig i denne hyllen. Ellers stoppes den manuelle eller trukne forbruksbokføringen for den komponenten.

> [!NOTE]  
> Følgende viktige forskjeller finnes mellom lagerplukkinger og lagerflyttinger:  
>
> - Når du registrerer en lagerplukking for en intern operasjon, for eksempel produksjon, bokføres forbruket av de plukkede komponentene samtidig. Når du registrerer en lagerflytting for en intern operasjon, registrerer du bare den fysiske flyttingen av de nødvendige komponentene til en hylle i operasjonsområdet, uten å bokføre forbruket.  
> - Når du bruker lagerplukk, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinje hvilken *Hent*-hylle komponentene reduseres fra ved bokføring av forbruk. Når du bruker lagerflyttinger, definerer feltet **Hyllekode** på produksjonsordrekomponentlinjer hyllen *Plasser* i operasjonsområdet der lagermedarbeideren må plassere komponentene.  

For å plukke eller flytte komponenter for kildedokumenter må en utgående lagerforespørsel varsle lagerområdet om komponentbehovet. Den utgående lagerforespørselen opprettes når du gjør følgende:

- endre statusen for en produksjonsordre til Frigitt.
- Opprett en frigitt produksjonsordre.  

Trekkmetodene påvirker også flyten av komponenter i produksjon. Hvis du vil ha mer informasjon, kan du se [Lagertrekke komponenter i henhold til operasjonsavgang](production-how-to-flush-components-according-to-operation-output.md). **Lagerflytting** med referanser til kildedokumentet og **Lagerplukk**, kan ikke brukes til å plukke komponenter med trekkmetodene *Fremover* og *Bakover*. **Lagerplukk** kan ikke brukes til å plukke komponenter med trekkmetoden *Manuell*. Hvis du vil behandle de gjenværende komponentene, bruker du **Lagerflytting** uten referanse til et kildedokument. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i enkle lageroppsett](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md).

I avanserte lagerkonfigurasjoner der lokasjoner krever både plukkinger og leveringer, må du bruke siden **Lagerplukk** til å hente komponenter som har trekkmetode satt til *Manuell*, *Plukk + Fremover* eller *Plukk + Bakover*, til produksjonsordrer. Hvis du vil ha mer informasjon, se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="to-pick-components-for-production-and-jobs-in-basic-warehouse-configurations"></a>Slik plukker du komponenter for produksjon og jobber i grunnleggende lageroppsett

I enkle lageroppsett der lokasjonen er definert slik at bare plukking brukes, kan du plukke komponenter for produksjonsaktiviteter og jobbplanleggingslinjer ved å bruke **Lagerplukk**-siden. Hvis du vil ha mer informasjon, kan du se [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).

> [!NOTE]
> Muligheten til å plukke komponenter for prosjektplanleggingslinjer ble lagt til [!INCLUDE[d365fin](includes/d365fin_md.md)] i lanseringsbølge 2 i 2022. Hvis du starter å bruke funksjonen, må en administrator aktivere **Funksjonsoppdatering: Aktiver lager og lagerplugg fra prosjekter** på **Funksjonsstyring**-siden.
>
>[!INCLUDE[prod_short](includes/prod_short.md)] bruker verdien i **Restantall**-feltet på prosjektplanleggingslinjen når det opprettes lagerplukk. Hvis du vil bruke lagerplukk for prosjekter, må du aktivere **Bruk forbrukskobling** på siden **Jobbkort** for prosjektet. Dette gjør at du kan spore forbruk mot planen din. Hvis du ikke aktiverer/deaktiverer, vil restantallet være **0** og lagerplukkingen opprettes ikke. Hvis du vil ha mer informasjon, kan du se [Slik definerer du sporing av prosjektbruk](projects-how-setup-jobs.md?tabs=current-experience#to-set-up-job-usage-tracking).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplukk**, og velg deretter den relaterte koblingen.  
2. Du får tilgang til produksjonsordrekomponentene ved å velge handlingen **Hent kildedokumenter** og deretter velge den frigitte produksjonsordren.  
3. Plukk komponenten, og registrer deretter plukkinformasjonen i feltet **Ant. som skal håndt.**.  
4. Når linjene er klare for bokføring, velger du handlingen **Bokfør**. Bokføringen oppretter de nødvendige lagerpostene og bokfører forbruket av varene.  

Du kan også opprette en **Lagerplukk** direkte fra den frigitte produksjonsordren. Velg handlingen **Opprett lagerplassering/-plukking/-flytting**, merk av for **Opprett lagerplukking**, og velg deretter **OK**-knappen.

Som et alternativ kan du bruke en **lagerflytting** med referanse til kildedokumentet for å flytte varer mellom hyller. Du må registrere forbruket separat. Hvis du vil ha mer informasjon, kan du se [Massebokføre produksjonsforbruk](production-how-to-post-consumption.md)

## <a name="pick-for-assembly-in-basic-warehouse-configurations"></a>Plukke for montering i grunnleggende lagerkonfigurasjoner

Bruk følgende sider til å plukke for monteringsordrer:

- Siden **Lagerflytting**.
- Hvis lokasjonen krever plukk, men ikke leveringer, bruker du **Lagerplukk**-siden til å plukke, montere og levere for salgsordrer der varer må monteres før de kan leveres. Hvis du vil ha mer informasjon, kan du se [Håndtere montere-til-ordre-varer i lagerplukk](warehouse-how-to-pick-for-production.md#handling-assemble-to-order-items-with-inventory-picks).  

I avanserte lageroppsett der lokasjoner krever både plukk og leveringer, må du bruke siden **Lagerplukk** til å bringe komponenter til monteringsordrer. Hvis du vil ha mer informasjon, se [Plukke for montering eller produksjon i avansert lageroppsett](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md).

## <a name="handling-assemble-to-order-items-with-inventory-picks"></a>Håndtere montere-til-ordre-varer med lagerplukk

**Lagerplukk**-siden brukes også til å plukke og levere for salg der varer må monteres før de kan leveres. Hvis du vil ha mer informasjon, kan du se [Selge varer som er montert til ordre](assembly-how-to-sell-items-assembled-to-order.md).

Monter til ordre-varer som skal leveres, anses ikke som til stede i en hylle før de er montert og bokført som avgang til en hylle i monteringsområdet. Derfor følger plukking av disse varene for levering en spesiell flyt. Lagermedarbeidere tar monteringsvarene fra en hylle til leveringssonen og bokfører deretter lagerplukkingen. Det bokførte lagerplukket bokfører deretter monteringsavgangen, komponentforbruket og følgeseddelen.

Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til å automatisk opprette en lagerflytting når lagerplukkingen for monteringsvaren opprettes. Hvis du vil opprette flyttinger automatisk, må du velge feltet **Opprett flyttinger automatisk** på siden **Monteringsoppsett**. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

[!INCLUDE[prod_short](includes/prod_short.md)] oppretter lagerplukklinjer for salgsvarer forskjellig avhengig av om ingen, noen eller alle salgslinjeantallene er montert til ordre.

- I salg der du bruker lagerplukk til å bokføre lagerforsendelse, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] én lagerplukklinje for hver salgsordrelinje. Hvis varen er plassert i forskjellige hyller, opprettes det mer enn én linje. Plukklinjene er basert på antallet i **Levere (antall)**-feltet.
- I salg der hele antallet på ordrelinjen er montert til ordre, opprettes én lagerplukklinje for dette antallet. Verdien i feltet Antall å montere er det samme som verdien i feltet **Levere (antall)**. **Monter til ordre**-feltet er valgt på linjen.

Hvis en monteringsavgangsflyt er definert for lokasjonen, blir verdien i feltene **Hyllek. lev. fra m. til ordre** eller **Fra-Hyllekode for montering** satt inn (i denne rekkefølgen) i **Hyllekode-feltet på** lagerplukklinjen.

Hvis ingen hyllekode er angitt på ordrelinjen og ingen monteringsavgangsflyt er definert for lokasjonen, er **Hyllekode**-feltet på lagerplukklinjen tomt. Lagermedarbeideren må åpne **Hylleinnhold**-siden og velge hyllen der monteringsvarene er montert.

Når del av antallet først må monteres og en annen del må plukkes fra lager, oppretter [!INCLUDE[prod_short](includes/prod_short.md)] minst to lagerplukklinjer. Én plukklinje er til montere-til-ordre-antallet. Den andre plukklinjen avhenger av hvilke hyller som kan oppfylle det gjenværende antallet fra lageret. Hyllekoder på de to linjene er fylt ut på forskjellige måter som beskrevet for de to ulike salgstypene. Hvis du vil ha mer informasjon, kan du se delen "Kombinasjonsscenarier" i [Forstå montere til ordre og montere til lager](assembly-assemble-to-order-or-assemble-to-stock.md).

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
