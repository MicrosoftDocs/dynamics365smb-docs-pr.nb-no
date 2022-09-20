---
title: Motta varer
description: Denne artikkelen er en oversikt over ulike måter å motta varer på i et lager, for eksempel varer med en bestilling eller varer ved hjelp av et lagermottak.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008
ms.date: 09/02/2022
ms.author: edupont
ms.openlocfilehash: 8bd79a13bb7ecc806fea0dcdea33ec604bd98c41
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460890"
---
# <a name="receive-items"></a>Motta varer

Når varene ankommer et lager som ikke er definert til lagermottaksbehandling, må du ganske enkelt registrere mottaket i det relaterte forretningsdokumentet, for eksempel en bestilling, en ordreretur eller en inngående overføringsordre.

Når varene ankommer et lager som er definert til lagermottaksbehandling, mottar du de linjene i kildedokumentet som utløste mottaket. Hvis du har hyller, kan du godta standardhyllen som fylles ut eller, hvis varen aldri har blitt mottatt i lageret tidligere, fylle ut hyllen der varen skal plasseres. Deretter må du fylle ut antall barer du har mottatt, og bokføre mottaket.  

## <a name="receive-items-with-a-purchase-order"></a>Motta varer med bestilling

Følgende beskriver hvordan du mottar varer med en bestilling. Fremgangsmåten er lik for ordrereturer og overføringsordrer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Åpne en eksisterende bestilling eller opprett en ny. Finn ut mer under [Registrer kjøp](purchasing-how-record-purchases.md).
3. I feltet **Motta (antall)** angir du det mottatte antallet.

   > [!NOTE]
   > Hvis det mottatte antallet er høyere enn bestilt i bestillingen per antallet i feltet **Antall**, og leverandøren er definert til å tillate overmottak, bruker du feltet **Overmottak** til å håndtere det overflødige antallet. Finn ut mer i delen [Slik mottar du flere varer enn bestilt](warehouse-how-receive-items.md#receive-more-items-than-ordered).
4. Velg handlingen **Bokfør**.

  Verdien i feltet **Mottatt ant.** oppdateres. Hvis dette er et delvis mottak, vil verdien være mindre enn verdien i feltet **Antall**.

> [!NOTE]
> Hvis du bruker et lagerdokument til å bokføre mottaket, kan du ikke bruke handlingen **Bokfør** på bestillingen. I stedet har en lagerarbeider allerede bokført bestillingsantallet som mottatt. Finn ut mer under [Slik mottar du varer med et lagermottak](warehouse-how-receive-items.md#receive-items-with-a-warehouse-receipt).

## <a name="receive-items-with-a-warehouse-receipt"></a>Motta varer med et lagermottak

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagermottak** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  

    Fyll ut feltene på hurtigfanen **Generelt**. Når du mottar kildedokumentlinjer, kopieres noe av informasjonen til hver linje.  

    For lageroppsett med lagerstyring: Hvis lokasjonen har en standard sone og hylle for mottak, fylles feltene **Sonekode** og **Hyllekode** ut automatisk, men du kan endre dem slik det passer.  

    > [!NOTE]  
    > Hvis du vil motta varer med andre lagerklassekoder enn lagerklassekoden til hyllen i feltet **Hyllekode** i dokumenthodet, må du slette innholdet i feltet **Hyllekode** fra hodet før du henter kildedokumentlinjene for varene.  
3. Velg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter** åpnes.

    Fra et nytt eller åpent lagermottak kan du bruke siden **Filtre for henting av kildedok** til å hente linjene i det frigitte kildedokument som definerer hvilke varer som skal mottas eller leveres.

    1. Velg handlingen **Bruk filtre til å hente k.dok...**.  
    2. Hvis du vil definere et nytt filter, angir du en beskrivende kode i feltet **Kode** og velger deretter handlingen **Endre**.  
    3. Definer typen kildedokumentlinjer som du vil hente, ved å fylle ut de relevante filterfeltene.  
    4. Velg **Kjør**.  

    Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, settes nå inn på siden **Lagermottak** der du aktiverte filterfunksjonen. 

    Filterkombinasjonene du definerer, lagres på siden **Filtre for henting av kildedok** til neste gang du trenger dem. Du kan opprette et ubegrenset antall filterkombinasjoner. Du kan når som helst endre kriteriene ved å velge handlingen **Endre**.

4. Velg kildedokumentene som du vil motta varer for, og velg deretter **OK**.  

    Kildedokumentlinjene vises på siden **Lagermottak**. Feltet **Motta (antall)** er fylt ut med antall utestående for hver linje, men du kan endre antallet slik det er nødvendig. Hvis du sletter innholdet i feltet **Hyllekode** i hurtigfanen **Generelt** før du henter linjene, må du fylle ut riktig hyllekode på hver mottakslinje.  

    > [!NOTE]  
    >  Når du skal fylle ut alle linjer i **Motta (antall)**-feltet med null, velger du handlingen **Slett antall som skal mottas**. Hvis du vil fylle det ut på nytt med restantallet, velger du handlingen **Autoutfyll ant som skal mottas**.  
    >
    >  Du kan ikke motta flere varer enn det som er angitt i feltet **Restantall** på kildedokumentlinjen. Hvis du vil motta flere varer, må du hente et annet kildedokument som inneholder en linje for varen, ved å bruke filterfunksjonen.  

5. Bokfør lagermottaket. Antallsfeltene oppdateres i kildedokumentene, og varene registreres som en del av selskapets lager.  

Hvis du bruker plassering, sendes mottakslinjene til lagerplasseringsfunksjonen. Selv om varene er mottatt, kan de ikke plukkes før de er plassert. De mottatte varene identifiseres som tilgjengelig beholdning først når plasseringen er registrert.  

Hvis du ikke bruker plassering, men bruker hyller, registreres plasseringen av varene i hyllen som er angitt på kildedokumentlinjen.  

> [!NOTE]  
> Hvis du bruker funksjonen **Bokfør og Skriv ut**, vil du både bokføre mottaket og skrive ut en plasseringsinstruksjon som viser hvor varene skal plasseres i lageret.  
>
> Hvis lokasjonen din bruker lagerstyring, brukes plasseringsmaler for å beregne den beste plasseringen av varene. Dette skrives så ut i plasseringsinstruksjonen.

## <a name="receive-more-items-than-ordered"></a>Motta flere varer enn bestilt

Når du mottar flere varer enn du har bestilt, kan det være lurt å motta dem i stedet for å annullere mottaket. Det kan for eksempel være billigere å beholde det overskytende i beholdningen enn å returnere det, eller leverandøren kan tilby deg en rabatt for å beholde leveransen.

### <a name="set-up-over-receipts"></a>Sett opp overmottak

Du må definere en prosentverdi der du kan overskride det bestilte antallet ved mottak. Du definerer dette med en overmottakskode, som inneholder prosenten i feltet **Toleranseprosent for overmottak**. Deretter tilordner du koden til kortene for relevante varer og/eller leverandører.  

Nedenfor ser du hvordan du definerer og tilordner en overmottakskode til en vare. Trinnene er de samme for å sette opp dette for en leverandør.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.
2. Åpne kortet for en vare du har mistanke om at noen ganger kan bli levert med et høyere antall enn bestilt.
3. Velg **Oppslag** i feltet **Overmottakskode**.
4. Velg handlingen **Ny**.
5. På siden **Overmottakskoder** oppretter du én eller flere nye linjer som definerer forskjellige policyer for overmottak. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
6. Velg en linje og velg deretter **OK**.

Overmottakskoden tilordnes til varen. Alle bestillinger eller lagermottak for varen tillater nå mottak av mer enn det bestilte antallet i henhold til den angitte toleranseprosent for overmottak.

> [!NOTE]
> Du kan definere en godkjenningsarbeidsflyt som krever at overmottak må godkjennes før de kan håndteres. I så fall må du merke av for **Krever godkjenning** på siden **Overmottakskoder**. Finn ut mer under [Opprett arbeidsflyter](across-how-to-create-workflows.md).

### <a name="perform-an-over-receipt"></a>Utfør et overmottak

På kjøpslinjer og lagermottakslinjer brukes feltet **Antall overmottak** til å registrere overmottatt antall, noe som betyr et antall som overskred verdien for bestilt antall i feltet **Antall**.

Når du håndterer et overmottak, kan du øke verdien i feltet **Motta (antall)** til det faktisk mottatte antallet. Feltet **Antall overmottak** oppdateres deretter for å vise det overflødige antallet. Du kan eventuelt angi det ekstra antallet i feltet **Antall overmottak**. Feltet **Motta (antall)** oppdateres deretter for å vise det bestilte antallet pluss det overflødige antallet. Følgende fremgangsmåte beskrev hvordan du fyller ut feltet **Motta (antall)**.  

1. I en bestilling eller et lagermottaksdokument der det mottatte antallet er høyere enn bestilt, angir du det faktiske mottatte antallet i feltet **Motta (antall)**.

    Hvis økningen er innenfor toleransen som er angitt av en tildelt overmottakskode, oppdateres feltet **Antall overmottak** til å vise antallet som verdien i feltet **Aantall** er overskredet med.

    Hvis økningen er over den angitte toleransen, tillates ikke overmottak. I dette tilfellet kan du undersøke om det finnes en annen overmottakskode som kan tillate det. Ellers kan bare det bestilte antallet mottas, og det overflødige antallet må håndteres på en annen måte, for eksempel ved å returnere det til leverandøren.

2. Bokfør mottaket på samme måte som for andre mottak.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] inkluderer ikke funksjonalitet for automatisk å starte økonomisk administrasjon for overmottak. Du må håndtere dette manuelt og være enig med leverandøren, for eksempel leverandøren som videresender en ny eller oppdatert faktura.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/receive-invoice-dynamics-d365-business-central/index).

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Designdetaljer: Warehouse Management](design-details-warehouse-management.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
