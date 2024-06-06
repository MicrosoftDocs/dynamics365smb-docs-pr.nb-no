---
title: Fordele inntekter og kostnader til flere finanskontoer
description: Lær hvordan du fordeler kostnader til én eller flere konti i økonomimodulen.
author: brentholtorf
ms.author: bholtorf
ms.date: 09/04/2023
ms.topic: conceptual
ms.search.keywords: 'allocate, allocation, accounts'
ms.search.form: '39, 2673, 2670, 2674,'
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="allocate-revenue-and-costs-to-multiple-general-ledger-accounts"></a>Fordele inntekter og kostnader til flere finanskontoer

Denne artikkelen beskriver hvordan du bruker fordelingskonti til å distribuere beløp i salgs- og kjøpsdokumenter og finanskladdelinjer til ulike finanskonti. Du kan fordele beløp gjennom en fast eller variabel fordeling.  

Fordeling deler en finanskladdelinje inn i linjene som er definert på siden **Fordelingskonto** . Hvis du for eksempel deler en leieutgift på tre måter ved hjelp av dimensjoner, har du tre linjer å bokføre for fordelingen. Derfor har du seks finanslinjer (eller muligens flere hvis du bruker mva. eller merverdiavgift). Selv om dette bokfører flere finansposter enn du kanskje trenger, kan du tilbakeføre enkeltlinjer i stedet for å tilbakeføre hele fordelingen.

Tildelingskontoer fungerer også med utsettelser. Hvis du vil vite mer om utsettelser, kan du gå til [Utsette inntekter og utgifter](finance-how-defer-revenue-expenses.md).

Tabellen nedenfor gir en innføring i fordelingsmetodene du kan bruke.

|Tildelingsmetode  |Description  |
|---------|---------|
|Løst     | Når du vil dele opp utgiftene på en måte som gjentas over en lengre periode, kan du bruke en fast fordeling. Med en fast fordeling kan du definere fordelingsfordelingen. Denne delingen endres bare når du endrer oppsettet på siden **Fordelingskonto** .        |
|Variabel     | Hvis du vil fordele inntekter eller utgifter basert på verdier som endres over tid, bruker du metoden variabel fordeling. Med variable fordelinger kan du angi kildene som skal brukes til å beregne fordelingsprosentene. Denne metoden er for eksempel nyttig for å dele opp personalkostnader i henhold til varierende antall ansatte i avdelinger eller divisjoner. Et annet eksempel er fordeling av leiekostnader basert på opptak fra produksjonsgulvet som kan variere per produksjonslinje over tid. Variabelfordelinger bruker en kombinasjon av dimensjoner og statistiske kontoer til å bestemme hvordan beløp distribueres over en tidsperiode. Hvis du vil vite mer om statistiske kontoer, kan du gå til [Analysere data med statistiske kontoer](bi-use-statistical-accounts.md). Hvis du vil ha mer informasjon om dimensjoner, kan du gå til [Arbeide med dimensjoner](finance-dimensions.md).        |

## <a name="use-a-fixed-share-or-percentage-method-to-allocate-amounts"></a>Bruke en fast andel eller prosentmetode til å fordele beløp

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tildelingskonto**, og velg deretter den relaterte koblingen.  
1. På siden **Tildelingskontoer** velger du handlingen **Ny**.
1. Fyll ut feltet **Nr.** og **Navn**-feltene.
1. Velg **Fast** i **Kontotype**-feltet.
1. I feltet **Destinasjonskontotype** velger du **Finanskonto** eller **Bankkonto**.
1. I feltet **Destinasjonskontonummer** velger du kontoen du vil bokføre verdien på.
1. Valgfritt: Velg **Dimensjoner**, og angi deretter dimensjonene som skal bokføres for linjen.
1. I feltene **Del** og **Prosent** angir du hvordan beløp skal fordeles til målkontoen.
  
   > [!TIP]
   > Hvis du angir det faktiske beløpet som skal fordeles til en fast fordeling i **Del-feltet**, viser **Prosent**-feltet prosenten av totalbeløpet.
1. Gjenta denne prosessen for hver konto som skal tas med i fordelingen.

## <a name="use-a-variable-method-to-allocate-amounts"></a>Bruke en variabel metode til å fordele beløp

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Tildelingskonto**, og velg deretter den relaterte koblingen.  
1. På siden **Tildelingskontoer** velger du handlingen **Ny**.
1. Fyll ut feltet **Nr.** og **Navn**-feltene.
1. Velg **Variabel** i **Kontotype**-feltet.
1. Angi **Finanskonto** i **Målkontotype**-feltet.
1. I feltet **Destinasjonskontonummer** velger du kontoen du vil bokføre verdien på.
1. Angi **Statistisk konto** i **Type nedbrytingskonto**-feltet.
1. I **Beregningsperiode**-feltet velger du perioden beløpene skal fordeles for.
1. Valgfritt: Hvis du vil filtrere etter bestemte globale dimensjonsverdier, velger du handlingen **Filtre for nedbrytingskontosaldo**, og deretter angir du filterverdiene.
1. Valgfritt: Velg **Dimensjoner**, og angi deretter dimensjonene som skal bokføres for linjen.

## <a name="allocate-amounts-on-the-fly"></a>Fordele beløp på farten

Du oppretter fordelingskontoer for å dele inntekter og kostnader for finanskonti og bankkonti. Automatisering av tildeling kan spare tid. Hvis du imidlertid vil bruke fordelingskontoer, men ikke vil opprette dem for hver finanskonto, kan du spare enda mer tid.

Med alternativet Arv fra overordnet kan du bruke fordelingskontoen til å dele beløp for en hvilken som helst finanskonto på en linje i et bilag eller en kladd. I **Kontotype**-feltet på et bilag eller kladdelinje velger du en finanskonto, og deretter velger du fordelingskontoen i **Fordelingskontonr.**-feltet. Beløpet på linjen deles for finanskontoen i henhold til oppsettet i fordelingskontoen. Det er en mindre gjennomsiktig måte å fordele på, men du trenger ikke å opprette en tildelingskonto spesifikt for finanskontoen.

Ad-hoc-tildelinger er enkle å sette opp. I stedet for å angi en bank- eller finanskonto i feltet **Målkontotype** på siden **Fordelingskonto**, velger du alternativet **Arv fra overordnet**. La feltet **Målkontonummer** stå tomt. Når du velger finanskontoen på bilags- eller kladdelinjen, brukes denne kontoen til å fordele beløp.

## <a name="verify-that-amounts-distribute-correctly-before-you-post-them"></a>Kontroller at beløpene distribueres riktig før du bokfører dem

Det finnes et par måter å bekrefte at beløpene distribueres riktig på:

* På siden **Tildelingskonto** velger du **Test fordeling**. Bruk feltet **Beløp å tildele** til å teste forskjellige beløp.
* På siden **Finanskladder** velger du journalen og bruker deretter handlingen **Forhåndsvisning av bokføring**.

## <a name="adjust-the-distribution"></a>Juster fordelingen

Hvis du finner noe i en fordeling som du vil endre, kan du justere fordelingen før du bokfører den.  

1. Åpne dokumentet eller kladden som har fordelingen du vil endre.
1. Velg linjen med fordelingen, og velg deretter handlingen **Fordel kontotildelinger på nytt**.
1. Gjør justeringen på siden **Endre tildelinger**.

## <a name="post-an-allocation-transaction"></a>Bokføre en fordelingstransaksjon

Trinnene nedenfor beskriver hvordan du bokfører en fordelingstransaksjon fra en finanskladd. Trinnene er de samme for kjøps- og salgsdokumenter.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Finanskladder**, og velg deretter den relaterte koblingen.  
1. Opprett en ny linje. Fyll ut feltene på samme måte som for alle andre typer finanskladder.
1. Hvis du bruker en fast eller variabel fordeling, fyller du ut følgende felt:
    1. Angi **Tildelingskonto** i **Kontotype**-feltet.
    1. Angi tildelingskonto i **Kontonr.**-feltet.
1. Hvis du bruker en fordeling som bruker alternativet Arv fra overordnet, gjør du følgende:
    1. Angi **Finanskonto** i **Kontotype**-feltet.
    1. I feltet **Kontonr.** velger du finanskontoen.
    1. I **Fordelingskontonr.** -feltet velger du tildelingskontoen som er konfigurert til å bruke alternativet Arv fra overordnet. 
1. Velg **Bokfør**.

## <a name="see-also"></a>Se også

[Arbeid med finanskladder](ui-work-general-journals.md)  
