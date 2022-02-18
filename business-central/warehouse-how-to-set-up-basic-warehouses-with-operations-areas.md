---
title: Opprette grunnleggende lagre med operasjonsområder
description: Definer lageroperasjonsområder og bruk lagerflytting, plukking og plassering til å flytte varer mellom dem.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 6774, 6775, 6776
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 6dbf91bcf720a3b57f7e6e9446b0a46d1e053987
ms.sourcegitcommit: c05806689d289d101bd558696199cefbd989473e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2022
ms.locfileid: "8115201"
---
# <a name="set-up-basic-warehouses-with-operations-areas"></a>Opprette grunnleggende lagre med operasjonsområder
Hvis det finnes interne operasjonsområder, for eksempel produksjon eller montering, i enkle lageroppsett der lokasjoner bruker oppsettsfeltet **Hylle obligatorisk** og muligens oppsettsfeltene **Plukk nødv.** og **Plassering nødv.**, kan du bruke følgende grunnleggende lagerdokumenter til å registrere lageraktivitetene for interne operasjonsområder:  

- **Lagerflyttingsliste**-siden.  
- **Lagreplukk**-siden.  
- **Lagerplassering**-siden.

> [!NOTE]
> Selv om innstillingene kalles **Plukk nødv.** og **Plassering nødv.**, kan du bokføre mottak og leveringer direkte fra kildedokumenter for firma på lokasjoner der du velger disse avmerkingsboksene.  

Hvis du vil bruke disse sidene med interne operasjoner, for eksempel plukke og flytte komponenter til produksjon, må du følge noen av eller alle følgende konfigurasjonstrinn, avhengig av hvor mye kontroll du trenger:  

- Aktiver dokumenter for lagerplukk, lagerflytting og lagerplassering.  
- Definer standard hyllestrukturer for komponenter og sluttvarer som går til og fra operasjonsressurser.  
- Opprett til- og fra-hyller som er dedikert til en bestemte operasjonsressurser for å hindre at varene blir plukket for utgående dokumenter.

Hyllekoder som er definert på lokasjonskort, definerer en standard lagerflyt for bestemte aktiviteter, for eksempel komponenter i en monteringsavdeling. Det finnes flere funksjoner for å sørge for at når varer blir plassert i en bestemt hylle, kan de ikke flyttes eller plukkes til andre aktiviteter. Hvis du vil ha mer informasjon, kan du se [Slik oppretter du dedikerte komponenthyller](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md#to-create-dedicated-component-bins).

Fremgangsmåtene nedenfor er basert på definisjon av grunnleggende lageraktiviteter rundt et produksjonsområde. Trinnene er de samme for andre operasjonsområder, for eksempel montering, service og jobber.  

> [!NOTE]  
>  I den følgende fremgangsmåten velges oppsettsfeltet **Hylle obligatorisk** som en nødvendig forutsetning fordi det regnes som grunnlaget for ethvert nivå av lagerstyring.  

## <a name="to-enable-inventory-documents-for-internal-operation-activities"></a>Slik aktiverer du lagerdokumenter for interne operasjonsaktiviteter:  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Åpne lokasjonskortet du vil definere.  
3.  På hurtigfanen **Lager**, merker du av for **Plassering nødv.** for å indikere at når et inngående eller internt kildedokument med hyllekode frigis, kan en lagerplassering eller et lagerflyttingsdokument opprettes.  
4.  Merk av for **Plukk nødv.** for å indikere at når det opprettes utgående eller internt kildedokument med hyllekode, må det opprettes et lagerplukk- eller en lagerflyttingsdokument.  

## <a name="to-define-a-default-bin-structure-in-the-production-area"></a>Slik definerer du en standardhyllestruktur i produksjonsområdet:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Åpne lokasjonen du vil definere.  
3.  På hurtigfanen **Hyller**, i feltet **Åpen prod.hyllekode** angir du koden for hyllen i produksjonsområdet som har rikelig med komponenter maskinoperatøren kan forbruke fra uten å be om en lageraktivitet for å bringe dem til hyllen. Varer som er plassert i denne hyllen er vanligvis konfigurert for automatisk bokføring eller trekk. Dette betyr at **Trekkmetode**-feltet inneholder **Fremover** eller **Bakover**.  
4. Angi koden for hyllen i feltet **Til-Hyllekode for produksjon** i produksjonsområdet der komponentene som plukkes til produksjonen på denne lokasjonen, plasseres som standard før de kan brukes. Varer som er plassert i denne hyllen er vanligvis konfigurert for manuell forbruksbokføring. Dette betyr at **Trekkmetode**-feltet inneholder **Manuell** eller **Plukk + Fremover** eller **Plukk + Bakover** for lagerplukkinger og lagerflyttinger.  

    > [!NOTE]  
    > Når du bruker lagerplukk, definerer feltet **Hyllekode** på en produksjonsordrekomponentlinje hvilken *Hent*-hylle komponentene reduseres fra ved bokføring av forbruk. Når du bruker lagerflyttinger, definerer **Hyllekode**-feltet på produksjonsordrekomponentlinjer *Plasser*-hyllen i operasjonsområdet der lagermedarbeideren må plassere komponentene.  

5. På hurtigfanen **Hyller**, i feltet **Fra-Hyllekode for produksjon** angir du koden for hyllen i produksjonsområdet hvor ferdige varer hentes fra som standard når prosessen omfatter en lageraktivitet. I grunnleggende lageroppsett registreres aktiviteten som en lagerplassering eller lagerflytting.  

Nå krever produksjonsordrekomponentlinjer med standard hyllekode at komponenter som trekkes fremover plasseres her. Før komponentene forbrukes fra denne hyllen, kan imidlertid andre komponentbehov plukke eller forbruke fra denne hyllen fordi den fortsatt regnes som tilgjengelig hylleinnhold. For å sørge for at hylleinnholdet bare er tilgjengelig for komponentbehov som bruker denne hyllen til produksjon, må du velge feltet **Dedikert** på linjen for denne hyllekoden på siden **Hyller** som du åpner fra lokasjonskortet.

Dette flytdiagrammet viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til oppsettet.  

![Flytskjema for hylle.](media/binflow.png "BinFlow")

## <a name="to-define-a-default-bin-structure-in-the-assembly-area"></a>Slik definerer du en standardhyllestruktur i monteringsområdet:
Komponenter for monteringsordrer kan ikke plukkes eller bokføres med lagerplukk. Bruk i stedet siden **Lagerflytting**. Hvis du vil ha mer informasjon, kan du se [Flytte komponenter til et operasjonsområde i grunnleggende lagerstyring](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)

Når du plukker og leverer salgslinjeantall som er montert til ordre, må du følge visse regler når du oppretter lagerplukklinjene. Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerplukk i [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).

Hvis du vil ha mer informasjon, se [Monteringsstyring](assembly-assemble-items.md).

### <a name="to-set-up-that-an-inventory-movement-is-automatically-created-when-the-inventory-pick-for-the-assembly-item-is-created"></a>Slik konfigurerer du at en lagerflytting opprettes automatisk når lagerplukkingen for monteringsvaren opprettes
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Monteringsoppsett** og velger den relaterte koblingen.
2. Merk av for **Opprett flyttinger automatisk**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-components-are-placed-by-default-before-they-can-be-consumed-in-assembly"></a>Slik definerer du hyllen i monteringsområdet der komponenter plasseres som standard, før de kan brukes i monteringen:
Verdien i dette feltet settes automatisk inn i **Hyllekode**-feltet på monteringsordrelinjer når denne lokasjonen angis i **Lokasjonskode**-feltet på monteringsordrelinjen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Åpne lokasjonen du vil definere.
3. Fyll ut feltet **Til-Hyllekode for montering**.

### <a name="to-set-up-the-bin-in-the-assembly-area-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-stock"></a>Slik definerer du hvilken hylle i monteringsområdet ferdige monteringsvarer bokføres til når de monteres til lager:
Verdien i dette feltet settes automatisk inn i **Hyllekode**-feltet på monteringsordrehoder når denne lokasjonskoden fylles ut i **Lokasjonskode**-feltet på monteringsordrehodet.

Hyllekoder som er definert på lokasjonskort, definerer en standard lagerflyt for spesifikke lageraktiviteter, for eksempel forbruk av komponenter i et monteringsområde. Det finnes flere funksjoner for å sørge for at når varer blir plassert i en standardhylle, kan de ikke flyttes eller plukkes til andre aktiviteter.

> [!NOTE]
> Dette oppsettet er bare mulig for lokasjoner der Hylle obligatorisk-feltet er valgt.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Åpne lokasjonen du vil definere.
3. Fyll ut feltet **Fra-Hyllekode for montering**.

### <a name="to-set-up-the-bin-where-finished-assembly-items-are-posted-to-when-they-are-assembled-to-a-linked-sales-order"></a>Slik definerer du hvilken hylle ferdige monteringsvarer bokføres til, når de monteres til en tilknyttet ordre:
Fra denne hyllen sendes monteringsvarene øyeblikkelig, via en lagerplukking, for å innfri ordren.

> [!NOTE]
> Dette feltet kan ikke brukes hvis lokasjonen er definert til å bruke lagerstyring.

Hyllekoden kopieres fra ordrelinjen til monteringsordrehodet for å kommunisere til monteringsarbeiderne hvor de skal plassere det ferdige resultatet for å klargjøre det for levering. Det er også kopiert til lagerplukklinjen for å kommunisere til lagerarbeiderne hvor varene som skal leveres skal hentes fra.

> [!NOTE]
> Leveringshyllen for montering til ordre er alltid er tom. Når du bokfører en montere-til-ordre-salgslinje, justeres først hylleinnholdet positivt i forhold til monteringsavgangen. Like etter justeres det negativt med det leverte antallet.

Verdien i dette feltet settes automatisk inn i Hyllekode-feltet på ordrelinjer som inneholder et antall i feltet **Ant. som skal monteres til ordre**, eller hvis varen som skal selges, har **Monter til ordre** i **Etterfyllingssystem**-feltet.

Hvis feltet **Hyllek. lev. fra m. til ordre** er tomt, brukes **Fra-Hyllekode for montering**-feltet i stedet. Hvis begge oppsettsfeltene er tomme, brukes den siste brukte hyllen med innhold i **Hyllekode**-feltet på ordrelinjer.

Den samme hyllekoden kopieres så til **Hyllekode**-feltet på lagerplukklinjen som håndterer leveringen av montere-til-ordre-antallet. Hvis du vil ha mer informasjon, kan du se delen Håndtere montere-til-ordre-varer i lagerplukk i [Plukke varer med lagerplukk](warehouse-how-to-pick-items-with-inventory-picks.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.
2. Åpne lokasjonen du vil definere.
3. Fyll ut feltet **Hyllek. lev. fra m. til ordre**.

## <a name="to-create-dedicated-component-bins"></a>Slik oppretter du dedikerte komponenthyller:
Du kan angi at antall i en hylle beskyttes mot å bli plukket for andre behov enn behov fra deres gjeldende formål.

Antall i dedikerte hyller kan fremdeles reserveres. Antallene i dedikerte hyller er på samme måte inkludert i feltet **Totalt disp. antall** på siden **Reservasjon**.

Et arbeidssenter er for eksempel definert med en hyllekode i feltet **Til-Hyllekode for produksjon**. Produksjonsordrekomponentlinjer med den hyllekoden krever at komponenter som trekkes fremover plasseres der. Før komponentene forbrukes fra denne hyllen, kan imidlertid andre komponentbehov plukke eller forbruke fra denne hyllen fordi den fortsatt regnes som tilgjengelig hylleinnhold. For å sørge for at hylleinnholdet bare er tilgjengelig for komponentbehov som bruker denne hyllen til produksjon, må du velge feltet **Dedikert** på linjen for denne hyllekoden på siden **Hyller** som du åpner fra lokasjonskortet.

Dedikering av hyller gir lignende funksjonalitet som bruk av hylletyper, som bare er tilgjengelig i avansert lagerstyring. Hvis du vil ha mer informasjon, kan du se [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).

> [!Caution]
> Varer i dedikerte hyller er ikke beskyttet når de blir plukket og forbrukt som produksjonskomponenter med siden Lagerplukk.

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen. Velg lokasjonskortet som du vil oppdatere.  
2.  Velg handlingen **Hyller**.  
3.  Velg feltet **Dedikert** for hver hylle du vil bruke utelukkende til bestemte interne operasjoner, og hvor du vil at antallene som er plassert der skal være reservert for den interne operasjonen.  

> [!NOTE]  
>  Hyllen må være tom før du kan velge eller fjerne den **Dedikert**-feltet.

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]