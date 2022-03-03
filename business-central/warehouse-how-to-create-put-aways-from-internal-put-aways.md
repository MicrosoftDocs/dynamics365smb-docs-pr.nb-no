---
title: Opprett plasseringer fra interne plasseringer
description: Dette emnet dekker hvordan du kan plukke og plassere uten et kildedokument, både hvordan du oppretter en intern plukking, og hvordan du oppretter en intern plassering.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 609564faa1e0d5b1e7c364360315ca71b9ba3d06
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8140088"
---
# <a name="pick-and-put-away-without-a-source-document"></a>Plukke og plassere uten et kildedokument
Når varer er plassert, og før de blir plukket for å oppfylle behovene i en produksjonsordre eller følgeseddel, blir de lagret i lageret som en del av tilgjengelig lager.  

Det kan oppstå situasjoner der varer må tas ut av plukkhyller midlertidig, for eksempel for å tjene som demonstrasjonsmodeller i en salgspresentasjon. Disse elementene eies fortsatt av firmaet og er en del av beholdningen, men er ikke tilgjengelige for plukking. De er registrert i en spesiell hylle som du oppretter for dette formålet. Teknisk sett er varene på lageret, men fysisk kan de være i et konferanserom eller demonstrasjonsrom.  

I andre situasjoner kan produksjonsenheten få uventet behov for noen få deler til en prosess. Du kan plukke varer for produksjonshyllen ved hjelp av den interne plukken. Når prosessen er over og avgangen er opprettet, bokfører du forbruket av varene og tømmer produksjonshyllen, som i sin tur reduserer antallet av varen i din lokasjon.  

På samme måte kan varer returneres til lageret for plassering. Varene kan ha vært tatt ut av det tilgjengelige lageret for en produksjonsordre og så ikke blitt brukt i det hele tatt. For å få dem til å bli en del av det tilgjengelige lageret igjen, må de plasseres i hyllen.  

Med **Intern plassering** kan du utføre plasseringer uten å måtte referere til et bestemt kildedokument. Du kan enkelt sette opp all den informasjonen du trenger til å opprette en lagerinstruksjon for plassering.  

> [!NOTE]  
>  Hvis du ikke bruker intern plukking og intern plassering, kan disse justeringene utføres med metodene for å flytte varer fra hylle til hylle eller for å bokføre antallsjusteringer i en hylle.  
>   
>  Når lokasjonen bruker lagerstyring, og derfor bruker hylletyper, kan du ikke manuelt flytte varer til eller fra en hylle av hylletypen RECEIVE, fordi varer som er i en slik hylle må registreres som plassert før de blir en del av det tilgjengelige lageret.  

## <a name="to-create-an-internal-pick"></a>Opprette en intern plukking  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Intern plukk**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltet **Nr.** feltet **Lokasjonskode** og **Til hylle-kode** i hurtigfanen **Generelt**. Feltet **Til hylle-kode** angir hyllen der du vil plassere de plukkede varene. Til produksjonsformål ville denne hyllen være den inngående produksjonshyllen eller den åpne produksjonshyllen. Til andre formål velger du en hyllekode for en hylletype som ikke brukes til plukking, sannsynligvis en hylle for oppsamling, levering eller spesielle formål.  
4.  Velg en vare i feltet **Varenr.**, og fyll ut antallene du vil plukke.  
5. Velg handlingen **Opprett plukk**. En plukkinstruksjon er nå klar til utføring av en lageransatt. Du kan også velge **Frigi**-handlingen og opprette lagerplukk ved hjelp av **Plukk-forslaget**. Hvis du vil ha mer informasjon, kan du se [Planlegge plukkinger i forslaget](warehouse-how-to-plan-picks-in-worksheets.md)

## <a name="to-create-an-internal-put-away"></a>Opprette en intern plassering  
1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Intern plassering**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut hodet til den nye interne plasseringen med minst feltet **Nr.**. og **Lokasjonskode**.
4. Fyll ut en linje for hver vare du vil flytte til lageret. Du trenger bare å fylle ut feltene **Varenr.** og **Antall**.

  > [!NOTE]  
  > Når du velger feltet **Varenr.**, åpnes **Hylleinnholdsoversikt** i stedet for **Vareoversikt**. Det kommer av at du ønsker å plassere varer som er i en bestemt hylle – *hylleinnhold* – ikke bare en vare, og du vet allerede hvilken hylle varen skal tas fra.  <!--If you filled in **From Bin Code** in the header, the bin content will be filtered by value defined in the **From Bin Code**.-->
5. Hvis du vil fylle ut linjene med hele hylleinnholdet eller det filtrerte hylleinnholdet i hyller i lokasjonen, velger du handlingen **Hent hylleinnhold**.  
6. Velg handlingen **Opprett plassering**. En plasseringsinstruksjon er nå klar til utføring av en lageransatt. Du kan også velge **Frigi**-handlingen og opprette lagerplasseringer ved hjelp av **Plasser-forslaget**. Hvis du vil ha mer informasjon, kan du se [Planlegge plasseringer i forslag](warehouse-how-to-plan-put-aways-in-worksheets.md).

## <a name="see-also"></a>Se også  
[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
