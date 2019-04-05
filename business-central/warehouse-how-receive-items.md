---
title: Motta varer| Microsoft-dokumentasjon
description: Når varene ankommer et lager som er definert til lagermottaksbehandling, mottar du de linjene i kildedokumentet som utløste mottaket.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: e56105cbd2410befea964c5445d8227021058d4f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803252"
---
# <a name="receive-items"></a>Motta varer
Når varene ankommer et lager som ikke er definert til lagermottaksbehandling, må du ganske enkelt registrere mottaket i det relaterte forretningsdokumentet, for eksempel en bestilling, en ordreretur eller en inngående overføringsordre.

Når varene ankommer et lager som er definert til lagermottaksbehandling, mottar du de linjene i kildedokumentet som utløste mottaket. &#160:Hvis du har hyller, kan du godta standardhyllen som fylles ut eller, hvis varen ikke har vært i lageret tidligere, fylle ut hyllen der varen skal plasseres. Deretter må du fylle ut antall barer du har mottatt, og bokføre mottaket.  

## <a name="to-receive-items-with-a-purchase-order"></a>Slik mottar du varer med bestilling
Følgende beskriver hvordan du mottar varer med en bestilling. Fremgangsmåten er lik for ordrereturer og overføringsordrer.  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bestillinger**, og velg deretter den relaterte koblingen.
2. Åpne en eksisterende bestilling eller opprett en ny. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).
3. I feltet **Motta (antall)** angir du det mottatte antallet.

    Verdien i feltet **Mottatt ant.** oppdateres. Hvis dette er et delvis mottak, vil verdien være mindre enn verdien i feltet **Antall**.
4. Velg handlingen **Bokfør**.

## <a name="to-receive-items-with-a-warehouse-receipt"></a>Slik mottar du varer med et lagermottak
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Lagermottak**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  

    Fyll ut feltene på hurtigfanen **Generelt**. Når du mottar kildedokumentlinjer, kopieres noe av informasjonen til hver linje.  

    For lageroppsett med lagerstyring: Hvis lokasjonen har en standard sone og hylle for mottak, fylles feltene **Sonekode** og **Hyllekode** ut automatisk, men du kan endre dem slik det passer.  

    > [!NOTE]  
    >  Hvis du vil motta varer med andre lagerklassekoder enn lagerklassekoden til hyllen i feltet **Hyllekode** i dokumenthodet, må du slette innholdet i feltet **Hyllekode** fra hodet før du henter kildedokumentlinjene for varene.  
3.  Velg handlingen **Hent kildedokumenter**. Siden **Kildedokumenter** åpnes.

    Fra et nytt eller åpent lagermottak kan du bruke siden **Filtre for henting av kildedok** til å hente linjene i det frigitte kildedokument som definerer hvilke varer som skal mottas eller leveres.

    1. Velg handlingen **Bruk filtre til å hente k.dok...**.  
    2. Hvis du vil definere et nytt filter, angir du en beskrivende kode i feltet **Kode** og velger deretter handlingen **Endre**.  
    3. Definer typen kildedokumentlinjer som du vil hente, ved å fylle ut de relevante filterfeltene.  
    4. Velg handlingen **Kjør**.  

    Alle frigitte kildedokumentlinjer som oppfyller filterkriteriene, settes nå inn på siden **Lagermottak** der du aktiverte filterfunksjonen.  

    Filterkombinasjonene du definerer, lagres på siden **Filtre for henting av kildedok** til neste gang du trenger dem. Du kan opprette et ubegrenset antall filterkombinasjoner. Du kan når som helst endre kriteriene ved å velge handlingen **Endre**.

4.  Velg kildedokumentene som du vil motta varer for, og velg deretter **OK**-knappen.  

    Linjene i kildedokumentet vises på siden **Lagermottak**. Feltet **Motta (antall)** er fylt ut med antall utestående for hver linje, men du kan endre antallet slik det er nødvendig. Hvis du sletter innholdet i feltet **Hyllekode** i hurtigfanen **Generelt** før du henter linjene, må du fylle ut riktig hyllekode på hver mottakslinje.  

    > [!NOTE]  
    >  Når du skal fylle ut **Motta (antall)**-feltet på alle linjene med null, velger du handlingen **Slett antall som skal mottas**. Hvis du vil fylle det ut på nytt med restantallet, velger du handlingen **Autoutfyll ant som skal mottas**.  

    > [!NOTE]  
    >  Du kan ikke motta flere varer enn det som er angitt i feltet **Restantall** på kildedokumentlinjen. Hvis du vil motta flere varer, må du hente et annet kildedokument som inneholder en linje for varen, ved å bruke filtreringsfunksjonen for å hente kildedokumenter med varen.  

5.  Bokfør lagermottaket. Antallsfeltene oppdateres i kildedokumentene, og varene registreres som en del av selskapets lager.  

Hvis du bruker plassering, sendes mottakslinjene til lagerplasseringsfunksjonen. Selv om varene er mottatt, kan de ikke plukkes før de er plassert. De mottatte varene identifiseres som tilgjengelig beholdning først når plasseringen er registrert.  

Hvis du ikke bruker plassering, men bruker hyller, registreres plasseringen av varene i hyllen som er angitt på kildedokumentlinjen.  

> [!NOTE]  
>  Hvis du bruker funksjonen **Bokfør og Skriv ut**, vil du både bokføre mottaket og skrive ut en plasseringsinstruksjon som viser hvor varene skal plasseres i lageret.  
>   
>  Hvis lokasjonen din bruker lagerstyring, brukes plasseringsmaler for å beregne den beste plasseringen av varene. Dette skrives så ut i plasseringsinstruksjonen.  

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
