---
title: Opprette hyller
description: Generer grupper med like hyller i forslaget for hylleoppretting, opprett hyller enkeltvis på lokasjonskortet eller automatisk i forslaget for hylleoppretting.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 7368, 7369, 7370, 7371, 7372, 7373
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: ffd6bd12a1655cc330370df2c9d2c64a2d89e0af
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8144388"
---
# <a name="create-bins"></a>Opprette hyller

Den mest effektive metoden for å opprette hyllene i lageret, er å generere grupper av lignende hyller i hylleopprettingsforslaget, men du kan også opprette hyllene individuelt fra lokasjonskortet. Du kan også bruke en funksjon på siden **Hylleoppretting** til å opprette hyller automatisk.  

## <a name="to-create-a-bin-from-the-location-card"></a>Slik oppretter du en hylle fra lokasjonskortet

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg den relaterte koblingen.  
2.  Velg lokasjonen der du vil opprette en hylle, og velg deretter **Hyller**-handlingen.  
3. Velg handlingen **Ny**.
4. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="the-dedicated-field"></a>Feltet Dedikert

Feltet **Dedikert** på siden **Hyller** angir at antallet i hyllen beskyttes mot å bli plukket i forbindelse med andre krav. Antall i dedikerte hyller kan imidlertid fremdeles reserveres. Antallene i dedikerte hyller er på samme måte inkludert i feltet **Totalt disp. antall** på siden **Reservasjon**.

Dedikering av hyller resulterer i lignende funksjonalitet i grunnleggende lageraktiviteter som bruk av hylletyper, som bare er tilgjengelig i avansert lagerstyring. Hvis du vil ha mer informasjon, kan du se [Definere hylletyper](warehouse-how-to-set-up-bin-types.md).

### <a name="example"></a>Eksempel

Et arbeidssenter er definert med en hyllekode i feltet **Til-Hyllekode for produksjon**. Produksjonsordrekomponentlinjer med den hyllekoden krever at komponenter som trekkes fremover plasseres der. Før komponentene forbrukes fra denne hyllen, kan imidlertid andre komponentbehov plukke eller forbruke fra denne hyllen fordi den fortsatt regnes som tilgjengelig hylleinnhold. For å sørge for at hylleinnholdet bare er tilgjengelig for komponentbehov som bruker denne hyllen til produksjon, må du velge feltet **Dedikert** på linjen for denne hyllekoden.

> [!Caution]
> Varer i dedikerte hyller er ikke beskyttet når de blir plukket og forbrukt som produksjons- eller monteringskomponenter med siden **Lagerplukk**. Hvis du vil ha mer informasjon, se [Plukke for montering eller produksjon i enkle lageroppsett](warehouse-how-to-pick-for-production.md).

## <a name="to-create-bins-individually-in-the-bin-creation-worksheet"></a>Slik oppretter du hyller individuelt i hylleopprettingsforslaget

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Hylleoppretting**, og velg den relaterte koblingen.  
2.  På hver linje fyller du ut de feltene som er nødvendig for å gi navn til og karakterisere hyllene du oppretter.  
3.  Velg handlingen **Opprett hyller**.  

## <a name="to-make-bins-automatically-in-the-bin-creation-worksheet"></a>Slik lager du hyller automatisk i hylleopprettingsforslaget

Før du begynner å opprette hyller automatisk, bør du finne ut hvilken slags hylle som er viktig for dine operasjoner, og du bør finne den mest praktiske vareflyten gjennom strukturen i lageret.  

> [!NOTE]  
> Når du bruker en hylle, kan du ikke slette den med mindre den er tom. Men hvis du noen gang ønsker å bruke et annet system for navngivning av hyller, kan du bruke reklassifiseringskladden til å flytte varene til et nytt hyllesystem. Denne prosessen er imidlertid manuell og tidkrevende, så det er best å sette opp hyllene riktig fra starten av.  

For å kunne arbeide på siden **Hylleoppretting** må du defineres som lageransatt på stedet der hyllene er. Hvis du vil ha mer informasjon, kan du se [Definere lageransatte](warehouse-how-to-set-up-warehouse-employees.md).    

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Hylleoppretting**, og velg deretter den relaterte koblingen.  
2.  Velg **Beregn hyller**-handlingen.
3. På siden **Beregn hyller** i feltet **Kode for hyllemal** velger du hyllemalen du vil bruke som modell for hyllene du bruker.
4.  Fyll ut en beskrivelse for hyllene du er i ferd med å opprette.  
5.  Opprett hyllekodene ved å fylle ut feltene **Fra nr.** og **Til nr.** i de tre kategoriene som vises på siden: **Reol**, **Seksjon** og **Nivå.** Hyllekoden kan inneholde opptil 20 tegn.  

    > [!NOTE]  
    >  Antall tegn du har angitt i de tre kategoriene for et hvilket som helst av feltene, for eksempel de tegnene du har angitt i de tre **Fra nr.** -feltene, pluss eventuelle feltskilletegn, må være 20 eller færre.  

     Du kan bruke bokstaver i koden som en identifiserende kombinasjon, men den bokstaven du bruker, må være den samme i **Fra nr.**- og og **Til nr.** -feltene. Du kan for eksempel definere Reol-delen av koden som **Fra nr. A01** og **Til nr. A10**. Programmet er ikke satt opp til å generere koder med bokstavsekvenser, for eksempel fra A01 til F05.  

6.  Hvis du ønsker å bruke et tegn, for eksempel en bindestrek, til å skille kategorifeltene du har definert som en del av hyllekoden, angir du dette tegnet i feltet **Feltseparator**.  
7.  Hvis du vil at programmet ikke skal opprette en linje for en hylle hvis den allerede finnes, velger du feltet **Kontroller eksisterende hylle**.  
8. Når du er ferdig med å fylle ut alle feltene, velger du **OK**.

    Programmet oppretter en linje for hver hylle i forslaget. Du kan nå slette noen av hyllene, for eksempel hvis du har en reol med en passasje gjennom de to første nivåene av et par seksjoner.  

9. Når du har slettet alle unødvendige hyller, velger du handlingen **Opprett hyller**. Programmet vil da opprette hyller for hver linje i forslaget.  

Gjenta prosessen for et annet sett av hyller til du har opprettet alle hyllene i lageret.  

## <a name="see-also"></a>Se også

[Lagerstyring](warehouse-manage-warehouse.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerstyring](warehouse-setup-warehouse.md)     
[Monteringsstyring](assembly-assemble-items.md)    
[Designdetaljer: Lagerstyring](design-details-warehouse-management.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]