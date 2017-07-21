---
title: Telle, justere og reklassifisere lagerbeholdning | Microsoft-dokumentasjon
description: "Beskriver hvordan du utfører fysisk telling og foretar negative eller positive justeringer, og hvordan du endrer informasjon, for eksempel lokasjons- eller partinummer, i vareposter eller lagerposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: db79c257585fe89237ef4e8d61fa49ce46ec682f
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-count-adjust-and-reclassify-inventory"></a>Telle, justere og reklassifisere lagerbeholdning
Minst én gang hvert regnskapsår må du utføre en vareopptelling, det vil si telle alle varer på lager, for å se om antallet som er registrert i databasen, er det samme som det faktiske antallet i lageret. Når det faktiske antallet er funnet, må det bokføres i Finans som en del av verdifastsettelsen av lageret ved periodens avslutning.

Selv om du teller alle varene i beholdningen minst én gang i året, kan du ha bestemt deg for å telle noen varer oftere, kanskje fordi de er mer verdifulle eller fordi de har rask omløpstid og utgjør en stor del av forretningene. Hvis du vil gjøre dette, kan du tilordne spesielle opptellingsperioder til disse varene. Hvis du vil ha mer informasjon, kan du se delen «Slik utfører du syklustelling».

Hvis du har bruk for å justere registrerte lagerantall, i forbindelse med opptellinger eller til andre formål, kan du bruke en varekladd til å endre lagerpostene direkte, uten å bokføre forretningstransaksjoner. Du kan også justere for én vare på varekortet.

Hvis du har bruk for å endre lagerpostattributter i tillegg til antallet, kan du bruke varereklassifiseringskladden. Attributter som ofte reklassifiseres, er serie-/partinumre, utløpsdatoer og dimensjoner.

## <a name="to-perform-a-physical-inventory"></a>Utføre en vareopptelling
Ved slutten av et regnskapsår, eller oftere, må du foreta en vareopptelling, altså telle den faktiske varebeholdningen, for å se om det antallet som er registrert i programmet er identisk med det fysiske antallet som er på lager. Hvis det er en differanse, må denne bokføres til varekontiene før du kan fastsette verdien av lageret.

Bortsett fra den fysiske opptellingsaktiviteten omfatter hele prosessen følgende tre oppgaver:

- Beregn forventet beholdning.
- Skriv ut rapporten som skal brukes ved telling.
- Angir og bokfør faktisk opptalt lagerbeholdning.

### <a name="to-calculate-the-expected-inventory"></a>Slik beregner du forventet beholdning:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Vareopptellingskladder**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Beregn beholdning**.
3. Angi betingelsene som skal brukes ved opprettelse av kladdelinjene, for eksempel om varer uten registrert beholdning skal tas med, i vinduet **Beregn beholdning**.
4. Angi filtre hvis du bare vil beregne lager for bestemte varer, hyller, lokasjoner eller dimensjoner.
5. Velg **OK**.

> [!NOTE]  
>   Varepostene behandles på bakgrunn av opplysninger du har angitt, og linjer opprettes i opptellingskladden. Merk deg at feltet **Antall (opptalt)** automatisk fylles ut med samme antall som i feltet **Antall (beregnet)**. Når du bruker denne funksjonen, er det ikke nødvendig å angi den opptalte lagerbeholdningen for varer som er lik beregnet antall. Hvis imidlertid det opptalte antallet er forskjellig fra det som er angitt i feltet **Antall (beregnet)**, må du overskrive det med det faktisk opptalte antallet.

### <a name="to-print-the-report-used-when-counting"></a>Skrive ut rapporten som brukes ved telling
1. Velg handlingen **Skriv ut** i vinduet **Vareopptellingskladd** som inneholder den beregnede forventede beholdningen.
2. Angi om rapporten skal vise det beregnede antallet og om rapporten skal vise lagervarer etter serie-/partinumre, i vinduet **Opptellingsoversikt**.
3. Angi filtre hvis du bare vil skrive ut rapporten for bestemte varer, hyller, lokasjoner eller dimensjoner.
4. Velg **Skriv ut**.

Ansatte kan nå fortsette med å telle lagerbeholdningen og registrere eventuelle avvik på den utskrevne rapporten.

### <a name="to-enter-and-post-the-actual-counted-inventory"></a>Slik angir og bokfører du faktisk opptalt lagerbeholdning:
1. Angi den faktiske beholdningen i feltet **Antall (opptalt)** for hver linje i vinduet **Vareopptellingskladd** der den faktiske lagerbeholdningen, som fastsatt ved fysisk opptelling, avviker fra det beregnede antallet.

    De relaterte feltene oppdateres tilsvarende.

    > [!NOTE]  
>   Hvis opptellingen avdekker avvik som skyldes at varer er bokført med feilaktige lokasjonskoder, må du ikke angi avviket i opptellingskladden. Bruk i stedet reklassifiseringskladden eller en overføringsordre til å omadressere varene til de riktige lokasjonene. Hvis du vil ha mer informasjon, kan du se Varereklassif.kladd eller Opprette overføringsordrer.

2. Hvis du vil justere beregnet antall til faktisk opptalt antall, velger du handlingen **Bokfør**.

    Både vareposter og fysiske vareopptellingsposter opprettes. Åpne varekortet for å vise de resulterende vareopptellingspostende.

3. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.
4. Du kan kontrollere vareopptellingen ved å åpne det aktuelle varekortet og deretter velge handlingen **Vareopptellingsposter**.

# <a name="to-perform-cycle-counting"></a>Utføre syklustelling
Selv om du teller alle varene i beholdningen minst én gang i året, kan du ha bestemt deg for å telle noen varer oftere, kanskje fordi de er mer verdifulle eller fordi de har rask omløpstid og utgjør en stor del av forretningene. Hvis du vil gjøre dette, kan du tilordne spesielle opptellingsperioder til disse varene.

> [!NOTE]  
>   Hvis lokasjonen er definert for lagerstyring, bruker du først vinduet **Lageropptellingskladd** og deretter funksjonen **Beregn lagerjustering** i vinduet **Varekladd**.

## <a name="to-set-up-counting-periods"></a>Slik definerer du opptellingsperioder
En vareopptelling blir vanligvis foretatt regelmessig, for eksempel hver måned, hvert kvartal eller hvert år. Du kan definere de opptellingsperiodene som kreves.

Definer opptellingsperiodene du vil bruke, og tilordne deretter én til hver vare. Når du utfører en vareopptelling og bruker **Beregn opptellingsperiode** i vareopptellingskladden, opprette linjer for varene automatisk.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Vareopptellingsperioder**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-counting-period-to-an-item"></a>Tilordne en opptellingsperiode til en vare  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.  
2. Velg varen du vil tilordne en opptellingsperiode til.  
3. Velg den aktuelle opptellingsperioden i vinduet **Vareopptell.periode - kode**.  
4. Velg **Ja**-knappen for å endre koden og beregne den første opptellingsperioden for varen. Neste gang du velger å beregne en opptellingsperiode i vareopptellingskladden, vises varen som en linje i vinduet **Vareutvalg for vareopptelling**. Du kan deretter begynne å telle varen periodisk.

## <a name="to-initiate-a-count-based-on-counting-periods"></a>Starte en opptelling basert på opptellingsperioder
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Vareopptellingskladd**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Beregn opptellingsperiode**.

    Vinduet **Vareutvalg for vareopptelling** åpnes og viser varene som har opptellingsperioder tilordnet, og som må telles, i samsvar med opptellingsperiodene.
3. Utfør vareopptellingen. Hvis du vil ha mer informasjon, kan du se delen «Utføre en vareopptelling».

## <a name="to-adjust-the-inventory-of-one-item"></a>Justere lagerbeholdningen for én vare
Når du har utført en fysisk opptelling av en vare i lagerområdet, kan du bruke funksjonen **Juster lagerbeholdning** til å registrere det faktiske lagerantallet.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varer**, og velg deretter den relaterte koblingen.
2. Velg varen du vil justere lagerbeholdning for, og velg deretter handlingen **Justere lagerbeholdning**.
3. I feltet **Ny beholdning** angir du lagerantallet som du vil registrere for varen.
4. Velg **OK**.

Beholdningen for varen er nå justert. Det nye antallet vises i feltet **Gjeldende beholdning** i vinduet **Juster lagerbeholdning** og i feltet **Lagerbeholdning** i vinduet **Varekort**.

Du kan også bruke funksjonen **Juster lagerbeholdning** til enkel plassering av kjøpte varer på lager, hvis du ikke bruker kjøpsfakturaer eller ordrer til å registrere kjøpene. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Når du har justert lagerbeholdningen, må du oppdatere den med den gjeldende, beregnede verdien. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

## <a name="to-adjust-the-inventory-quantity-of-one-or-more-items"></a>Justere lagerantallet for én eller flere varer
I **Varekladd**-vinduet kan du bokføre varetransaksjoner direkte for å justere lagerbeholdningen i forbindelse med kjøp, salg og positive eller negative justeringer, uten å bruke dokumenter.

Hvis du ofte bruker varekladden til å bokføre identiske eller lignende kladdelinjer, for eksempel i forbindelse med materialforbruk, kan du bruke vinduet **Standard varekladd** til å forenkle dette gjentakende arbeidet. Hvis du vil ha mer informasjon, kan du se delen «Standardkladder» i [Arbeide med finanskladder](ui-work-general-journals.md).

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Varekladder**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg handlingen **Bokfør** for å foreta lagerjusteringene.

> [!NOTE]  
>   Når du har justert lagerbeholdningen, må du oppdatere den med den gjeldende, beregnede verdien. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

## <a name="to-reclassify-an-items-lot-number"></a>Reklassifisere partinummeret for en vare
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Vareoverføringskladder**, og velg deretter den relaterte koblingen.
2. I vinduet **Vareoverføringskladder** fyller du ut feltene etter behov.
3. I feltet **Partinr.** angir du varens gjeldende partinummer.
4. I feltet **Nytt partinr.** angir du varens nye partinummer.
5. Velg handlingen **Bokfør**.

## <a name="see-also"></a>Se også
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

