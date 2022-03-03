---
title: Definere aktivaavskrivning
description: Det finnes ulike avskrivningsmetoder. I Business Central definerer du avskrivningsmetoden for et aktivum på siden **Aktivakort**.
author: edupont04
ms.topic: conceptual
ms.search.keywords: write down
ms.date: 06/28/2021
ms.author: edupont
ms.openlocfilehash: 228ca9aa8b1f476e5063bd0f8d6728f18cfafaf3
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8136273"
---
# <a name="set-up-fixed-asset-depreciation"></a>Definere avskrivning for aktiva

Du kan bruke ulike avskrivningsmetoder når du skal forberede regnskapsoppgjør og selvangivelse. Mange store selskaper bruker lineær avskrivning i sine regnskapsoppgjør ettersom denne avskrivningsmetoden vanligvis tillater rapportering av høyere inntjening. Når det gjelder inntektsskatt, bruker imidlertid mange virksomheter en hurtig avskrivningsmetode, for eksempel saldoavskrivningsmetoden for aktivaet. Du definerer et aktivas avskrivningsmetode med **Avskrivningsmetode**-feltet på siden **Aktivakort**. Hvis du vil ha mer informasjon om hva de forskjellige metodene gjør, se [Avskrivningsmetoder](fa-depreciation-methods.md).

Du konfigurerer avskrivningstablåer der du definerer de ulike måtene avskrivning må beregnes på for ulike typer aktiva. Hvert avskrivningstablå spesifiserer individuelle avskrivningsbetingelser. Du kan for eksempel angi at et aktiva skal avskrives over en periode på tre år i ett tablå, og over en periode på fem år i et annet tablå.

Når du har opprettet de relevante avskrivningstablåene, må du tilordne minst ett avskrivningstablå til hvert enkelt aktiva. Et avskrivningstablå som tilordnes til et aktiva, blir referert til som et avskrivningstablå for aktiva. Du kan definere et ubegrenset antall avskrivningstablåer for et aktivum.  

## <a name="to-create-a-depreciation-book"></a>Slik oppretter du et avskrivningstablå:

I et aktivaavskrivningstablå angir du hvordan aktiva skal avskrives. Hvis du vil tilpasse ulike avskrivningsmetoder, kan du definere flere avskrivningstablåer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.
2. På siden **Avskrivningstablå - oversikt** velger du handlingen **Ny**.
3. På siden **Avskrivningstablåkort** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Du kan registrere aktivatransaksjoner på siden **Aktivafinanskladd** eller **Aktivakladd**, avhengig av om transaksjonene er for finansiell rapportering eller intern håndtering. Følg neste trinn for å definere hvilken type kladd som brukes for de ulike aktivaaktivitetene som standard.
4. I **Integrasjon**-hurtigfanen merker du av for hver aktivaaktivitet som har transaksjoner du vil bokføre ved hjelp av **Aktivafinanskladd**-siden.
5. Gjenta trinn 2 til 4 for hver avskrivningsmetode eller bokføringsmetode som du vil tilordne til aktiva som et avskrivningstablå.

> [!IMPORTANT]
> Velg feltet **Bruk avrunding i period.avskr.** til å avrunde de beregnede periodiske avskrivningsbeløpene til hele tall. Hvis selskapet for eksempel også bruker fakturaavrunding til hele tall på siden **Finansoppsett**, kan avrunding av også avskrivningsbeløp til hele tall bidra til å gi gjennomsiktighet.

Hvis du for eksempel selger et aktiva der avskrivningstablået ikke angir avrunding, men selskapets finansoppsett krever avrunding, vil du få en feilmelding om at et beløp må avrundes i en post når du kvitter deg med aktivumet.  

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Slik tilordner du et avskrivningstablå til et aktiva:
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet som du vil definere et aktivaavskrivningstablå for.
3. På hurtigfanen **Avskrivningstablå** fyller du ut feltene etter behov.
4. Hvis du vil tilordne mer enn ett avskrivningstablå til aktivaet, velger du **Legg til flere avskrivningstablåer**.
5. Du kan også velge handlingen **Avskrivningstablåer** for å angi ett eller flere avskrivningstablåer for aktiva.

    > [!NOTE]  
    >   Når du bruker den manuelle avskrivningsmetoden, må du angi avskrivning manuelt i aktivafinanskladden. Funksjonen **Beregn avskrivninger** utelater aktiva som avskrives etter den manuelle metoden. Du kan bruke denne metoden for aktiva som ikke skal avskrives, for eksempel tomter.

    > [!NOTE]  
    > Når du bruker den brukerdefinerte avskrivningsmetoden, må du tilordne avskrivningstablået på en annen måte. Hvis du vil ha mer informasjon, kan du se [Slik definerer du brukerdefinerte avskrivningsmetoder](fa-how-setup-user-defined-depreciation-method.md).

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Slik tilordner du et avskrivningstablå til flere aktiva med en kjørsel:
Hvis du vil knytte et avskrivningstablå til flere aktiva, kan du bruke kjørselen **Opprett aktivaavskr.tablåer** til å opprette aktivaavskrivningstablåer.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet som du vil tilordne et avskrivningstablå til, og velg deretter **Rediger**-handlingen.
3. På **Avskrivningstablåkort**-siden velger du **Opprett aktivaavskr.tablåer**.
4. På siden **Opprett aktivaavskr.tablåer** fyller du ut **Avskrivningstablå**-feltet.
5. Velg feltet **Kopier fra aktivanr.**, og velg aktivanummeret du vil bruke som grunnlag for å opprette nye aktivaavskrivningstablåer for aktiva.

    Hvis du fyller ut dette feltet, vil avskrivningsfeltene i de nye aktivaavskrivningstablåene inneholde samme informasjon som de tilsvarende feltene i aktivaavskrivningstablået du kopierer fra. La feltet stå tomt hvis du vil opprette nye aktivaavskrivningstablåer med tomme avskrivningsfelt.  
6. På hurtigfanen **Aktiva** kan du definere et filter for å velge hvilke aktiva du vil det skal opprettes aktivaavskrivningstablåer for.
7. Velg **OK**.

## <a name="to-set-up-depreciation-posting-types"></a>Slik definerer du bokføringstyper for avskrivning:
For hvert avskrivningstablå må du definere hvordan du vil at [!INCLUDE[prod_short](includes/prod_short.md)] skal håndtere ulike bokføringstyper. Du må for eksempel angi om bokføringen skal være debet eller kredit, og om bokføringstypen skal tas med i avskrivningsgrunnlaget.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
2. Velg avskrivningstablået du vil definere, og velg deretter handlingen **Aktivabokf.type - oppsett**.
3. Fyll ut resten av feltene på siden **Aktivabokf.type - oppsett** etter behov.

    > [!NOTE]  
    >   Du kan ikke sette inn eller slette linjer på siden **Aktivabokf.type - oppsett**. Du kan bare foreta endringer i de eksisterende linjene.

Vi anbefaler at du ikke endrer oppsettet av avskrivningstablåer med poster som allerede er bokført. Endringene påvirker ikke poster som allerede er bokført, noe som ville forårsaket feilaktig statistikk for avskrivningstablåene.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Slik definerer du standardmaler og kladder for aktivaavskrivning:
Du kan definere et standardoppsett for maler og kladder for hvert enkelt avskrivningstablå. Du kan bruke disse standardene til å kopiere linjer fra en kladd til en annen, opprette kladdelinjer ved hjelp av kjørslene **Beregn avskrivning** eller **Indeksreg. aktiva**, duplisere anskaffelseskostnader i forsikringskladden.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Avskrivningstablåer**, og velg deretter den relaterte koblingen.  
2. Velg avskrivningstablået du vil definere standardkladder for, og velg deretter handlingen **Aktivakladdoppsett**.  
3. Hvis du vil bruke et standardoppsett for alle brukerne, velger du **Bruker-ID**-feltet som skal velges fra siden **Brukere**.  
4. Velg kladdemalen eller kladden som skal brukes som standard i de andre feltene.  

## <a name="fiscal-year-365-days-field-depreciation"></a>Regnskapsår 365 dager-feltavskriving

Når kjørselen Beregn avskrivninger beregner avskrivninger, brukes vanligvis et standardisert år på 360 dager, der hver av de 12 månedene har 30 dager.

Hvis du velger dette feltet, bruker kjørselen Beregn avskrivninger i stedet kalenderåret på 365 dager, der hver måned beregnes med samme antall dager som i kalenderen. Det eneste unntaket er februar i skuddår, som kjørselen behandler som om den har 28 dager, ikke 29. Derfor anses alle år, inkludert skuddår, for å ha 365 dager.


## <a name="see-also"></a>Se også
[Definere aktiva](fa-setup.md)  
[Aktiva](fa-manage.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
