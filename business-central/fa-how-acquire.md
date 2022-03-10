---
title: Anskaffe aktiva
description: Du kan definere et aktivum, tilordne et avskrivningstablå og registrere anskaffelseskosten for aktivumet.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: 5605, 5551, 5600, 5628, 5629
ms.date: 12/03/2021
ms.author: edupont
ms.openlocfilehash: e0a60cbb82c99e3497a6f8d1907c261b6199e7ec
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8141213"
---
# <a name="acquire-fixed-assets"></a>Anskaffe aktiva
For hvert enkelt aktiva må du definere et kort som inneholder opplysninger om aktivaet. Du kan definere bygninger eller produksjonsutstyr som hovedaktiva i en komponentoversikt, og du kan gruppere dem på forskjellige måter, som etter klasse, avdeling eller lokasjon. Et avskrivningstablå må defineres og tilordnes til hvert enkelt aktiva før du kan anskaffe det.

Når et aktiva er definert og et avskrivningstablå tilordnet, må du anskaffe det. For å anskaffet et aktiva registrerer du anskaffelseskosten i den relevante finanskontoen, bankkontoen eller leverandøren ved å bokføre en anskaffelsestransaksjon fra **Aktiva finanskladd**-siden. Du kan bruke **Assistert aktivaanskaffelse**-siden for å opprette og bokføre de nødvendige finanskladdelinjene automatisk.

Skrapverdien er restverdien for et aktiva som ikke lenger kan brukes. Du kan bokføre skrapverdien samtidig som du bokfører anskaffelseskosten. Hvis du vil ha mer informasjon, kan du se [Avskrive eller amortisere aktiva](fa-how-depreciate-amortize.md).

Indeksregulering brukes til å justere verdier for generelle endringer i prisnivået. Kjørselen **Indeksreg. aktiva** kan brukes til å beregne anskaffelseskostnader i forbindelse med gjenskaffelseskostnader.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a>Slik oppretter du et anleggsmiddel og anskaffer det automatisk:
Følgende fremgangsmåte beskriver hvordan du oppretter et aktiva og deretter anskaffer det ved hjelp av **Assistert aktivaanskaffelse**-siden for å opprette og bokføre de nødvendige aktivafinanskladdelinjene. Du kan også opprette og bokføre kladdelinjene manuelt. Hvis du vil ha mer informasjon, se [Slik bokfører du en aktivaanskaffelse manuelt med aktivafinanskladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.  
2. Velg **Ny**, og deretter fyller du ut feltene i **Generelt**-hurtigfanen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. På hurtigfanen **Avskrivningstablå** fyller du ut feltene etter behov. Dette trinnet tilordner et avskrivningstablå til aktivaet.  
4. Hvis du vil tilordne mer enn ett avskrivningstablå til aktivaet, velger du **Legg til flere avskrivningstablåer**. Se [Slik tilordner du et avskrivningstablå til et aktiva](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset) hvis du vil ha mer informasjon.

    Når alle nødvendige felt for å anskaffe et anleggsmiddel er fylt ut, vises varselet **Du er klar til å anskaffe aktivaet** øverst på siden.
5. Velg handlingen **Anskaffe** i varselet.
6. Følg trinnene på **Assistert aktivaanskaffelse**-siden for å fullføre den automatiske anskaffelsen av aktivaet.

> [!NOTE]  
>   Du kan også bokføre anskaffelseskosten som et kreditbeløp. Husk i så fall at verdien i **Anskaffelseskost inkl. mva**-feltet må ha et minustegn for å angi et kreditbeløp.

Når du velger **Fullfør**, blir **Bokført verdi**-feltet på **Aktivakort**-siden fylt ut, som indikerer at aktivaet er anskaffet til den angitte anskaffelseskosten.  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a>Slik definerer du en komponentoversikt for et hovedaktiva:
Du kan gruppere aktiva i hovedaktiva og komponenter i hovedaktivaene. Det kan for eksempel tenkes at du har en produksjonsmaskin som består av mange deler som du vil gruppere på denne måten.  

Både hovedaktivaet og alle komponentene må defineres som individuelle aktivakort. Når du har definert en komponentoversikt, fyller [!INCLUDE[prod_short](includes/prod_short.md)] automatisk ut feltene **Hovedaktiva/komponent** og **Komponent til hovedaktiva** på aktivakortene.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktiva**, og velg deretter den relaterte koblingen.
2. Velg aktivaet som er hovedaktivaet, og velg deretter **Hovedaktivakomponenter**-handlingen.
3. På siden **Hovedaktivakomponenter** velger du feltet **Aktivanr.** og velger deretter aktivaet du vil legge til som en komponent av hovedaktivaet.
4. Lukk siden.
5. Gjenta trinnene 3 og 4 for hvert komponentaktiva som du vil legge til.
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivaoppsett** og velger den relaterte koblingen.
7. Merk av for **Tillat bokf. til hovedaktiva**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a>Slik bokfører du en aktivaanskaffelse manuelt med aktivafinanskladden:
Følgende fremgangsmåte beskriver hvordan du anskaffer et aktiva manuelt ved å opprette og bokføre linjer på **Aktiva finanskladd**-siden. Du kan også anskaffe et aktiva automatisk ved hjelp av **Assistert aktivaanskaffelse**-siden. Hvis du vil ha mer informasjon, kan du se trinn 5 i [Slik oppretter du et anleggsmiddel og anskaffer det automatisk](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   Du kan også bokføre anskaffelseskosten som et kreditbeløp. Husk i så fall at verdien i **Beløp**-feltet må ha et minustegn for å angi et kreditbeløp.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Aktivafinanskladder**, og velg deretter den relaterte koblingen.
2. På **Aktiva finanskladd**-siden i **Aktivabokf.type**-feltet velger du **Anskaffelseskost**.
3. Fyll ut feltene som gjenstår, etter behov.
4. Velg handlingen **Bokfør**.  

> [!TIP]  
>   Hvis du fyller ut feltet **Forsikringsnr.** i aktivafinanskladden når du bokfører en anskaffelseskost, bokfører [!INCLUDE[prod_short](includes/prod_short.md)] også anskaffelseskosten for aktivaet i forsikringsdekningsposten. Hvis du vil ha mer informasjon, kan du se [Forsikre aktiva](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a>Slik kansellerer du en anskaffelseskostbokføring for ett aktiva:
Hvis du gjør en feil når du bokfører en anskaffelseskostnad, kan du fjerne posten via kjørselen **Kanseller aktivaposter** og deretter bokføre den riktige anskaffelsesposten. Feilaktige poster overføres til **Aktivafeilposter**-siden.

Hvis du for eksempel bokfører en anskaffelse med feil dato, må du korrigere den så snart som mulig fordi aktivabokføringsdatoen brukes for mange beregninger.

> [!IMPORTANT]  
> Du kan ikke bruke funksjonen **Tilbakefør transaksjon** for aktivaposter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , skriv inn **Aktivaposter**, og velg deretter den relaterte koblingen.  
2. På siden **Aktivaposter** velger du posten eller postene du vil kansellere.  
3. Velg menyen **Handlinger**, og velg deretter handlingen **Kanseller poster**.
4. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Velg **OK**-knappen for å kjøre kjørselen.
6. Når feil post eller poster er kansellert, fortsetter du med å bokføre riktig anskaffelseskost.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a>Slik bokfører du skrapverdien sammen med anskaffelseskosten:
Du kan bokføre skrapverdien sammen med anskaffelseskosten fra en aktivakladd.

> [!NOTE]
> Denne prosessen krever kanskje at du tilpasser tabellen Aktivakladder ved å legge til feltet Skrapverdi. Som standard vises ikke feltet på siden. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Aktivakladder** og velger den relaterte koblingen.
2. På siden **Aktivakladder** oppretter du anskaffelseslinjen. Hvis du vil ha mer informasjon, se [Slik bokfører du en aktivaanskaffelse manuelt med aktivafinanskladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. I **Skrapverdi**-feltet på kladdelinjen angir du beløpet for skrapverdien som et kreditbeløp (med et minustegn foran, for eksempel **-** 100).
4. Velg handlingen **Bokfør**.

> [!NOTE]
> Hvis det finnes en skrapverdi for et aktiva, brukes denne verdien i avskrivningsbokføring i stedet for verdien i feltet **Slutt bokført verdi** på siden **Aktivaavskrivningstablå**. Hvis du vil ha mer informasjon, se [Slik håndterer du siste bokførte verdi](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-also"></a>Se også
[Aktiva](fa-manage.md)  
[Definere aktiva](fa-setup.md)  
[Finans](finance.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]