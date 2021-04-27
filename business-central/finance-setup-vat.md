---
title: Definere merverdiavgift (mva)
description: Kontroller at du riktig beregne, postere og rapportere mva for salg og innkjøp.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 36714bb2e211c72bf2d953b7c64b9ea58e11f6e7
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770812"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Definer beregninger og bokføringsmetoder for merverdiavgift

Forbrukere og selskaper betaler merverdiavgift (mva) når de kjøper varer eller tjenester. Mva-beløpet som skal betales, kan variere, avhengig av flere faktorer. I [!INCLUDE[prod_short](includes/prod_short.md)] setter du opp for å angi satsene som skal brukes til å beregne mva-beløp som er basert på følgende:

* Hvem du selger til  
* Hvem du kjøper fra  
* Hva du selger  
* Hva du kjøper  

Du kan definere mva-beregninger manuelt, men som kan være vanskelig og tidkrevende. For å gjøre det enkelt har vi laget en assistert oppsettsveiledning kalt **Mva-oppsett** som hjelper deg gjennom fremgangsmåten. Vi anbefaler at du bruker den assisterte oppsettsveiledningen til å definere mva.

> [!NOTE]  
> Du kan bare bruke veiledningen hvis du har opprettet et Mitt selskap og ikke har bokført transaksjoner som inkluderer mva. Det ville ellers være svært enkelt å bruke forskjellige mva-satser ved en feiltakelse, og gjøre mva-relaterte rapporter unøyaktige.  

Hvis du vil definere mva-beregninger selv, eller bare vil lære mer om hvert trinn, inneholder dette emnet beskrivelser av hvert trinn.

## <a name="to-use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Slik bruker du mva-oppsettguiden til å definere mva (anbefales)

Vi anbefaler at du bruker den medfølgende mva-oppsettguiden til å definere mva i [!INCLUDE[prod_short](includes/prod_short.md)].

Hvis du vil oppsettguiden, gjør du følgende:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Assistert oppsett**.  
2. Velg **Angi MVA**, og fullfør trinnene.
3. Når du har fullført det assisterte oppsettet, kan du gå til siden **Mva-bokføringsoppsett** og kontrollere om du må fylle ut flere felt i henhold til de lokale kravene i versjonen av [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se [Lokal funksjonalitet i Business Central](about-localization.md).  

## <a name="to-set-up-vat-registration-numbers-for-your-country-or-region"></a>Definere organisasjonsnumre for landet eller området ditt

Du kan definere formater for organisasjonsnumre som brukes i land og områder som du handler med, for å sikre at det angis gyldige organisasjonsnumre. [!INCLUDE[prod_short](includes/prod_short.md)] viser en feilmelding når noen gjør en feil eller bruker et format som er feil for landet eller området.

Gjør følgende for å definere organisasjonsnumre:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Land/regioner**.
2. Velg landet eller området, og velger deretter handlingen **Formater for org.nr.**.
3. I **Formater**-feltet definerer du formatet ved å angi én eller flere av følgende tegn:  

* **#** Krever et tall med ett siffer.  
* **@** Krever en bokstav. Det skilles ikke mellom store og små bokstaver.  
* **?** Tillater alle tegn.  

    > [!Tip]
    > Du kan bruke andre tegn så lenge de alltid finnes i land- eller områdeformatet. Hvis du for eksempel vil inkludere et punktum eller en tankestrek mellom et sett med tall, kan du for eksempel definere formatet som ##.####.### eller @@-###-###.  

## <a name="to-set-up-vat-business-posting-groups"></a>Slik setter du opp mva-bokføringsgrupper for firma
Mva-bokføringsgrupper for firma skal representere markeder som du gjør forretninger med kunder og leverandører i, og definere hvordan du skal beregne og bokføre mva for hvert marked. Eksempler på mva-bokføringsgrupper for firma er **Innenlands** og **Den europeiske union (EU)**.  

Bruk koder som er lette å huske, og som beskriver bokføringsgruppen, for eksempel **EU**, **ikke-EU** eller **innenlands**. Koden må være unik. Du kan kan definere så mange koder du vil, men du kan ikke bruke samme kode mer enn én gang i en tabell.

Hvis du vil definere en mva-bokføringsgruppe for bedrifter, gjør du følgende:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsgruppe - firma**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

Du oppretter standard mva-bokføringsgrupper for firma ved å knytte dem til firmabokføringsgrupper. [!INCLUDE[prod_short](includes/prod_short.md)] tilordner automatisk mva-bokføringsgruppen for firma når du knytter firmabokføringsgruppen til en kunde, leverandør eller finanskonto.

## <a name="to-set-up-vat-product-posting-groups"></a>Slik setter du opp mva-bokføringsgrupper for varer
Mva-bokføringsgrupper for produkter representerer varer og ressurser du kjøper eller selger, og du kan finne ut hvordan du skal beregne og bokføre mva i henhold til hvilken type vare eller ressurs som blir kjøpt eller solgt.  
Det er lurt å bruke koder som er lette å huske og som beskriver satsen, for eksempel **Ingen mva** eller **Null**, **MVA10** eller **Redusert** for 10 % mva, og **MVA25** eller **Standard** for 25 %.

Hvis du vil definere en mva-bokføringsgruppe for bedrifter, gjør du følgende:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsgrupper - vare**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="to-combine-vat-posting-groups-in-vat-posting-setups"></a>Slik kombinerer du mva-bokføringsgrupper i mva-bokføringsoppsett
[!INCLUDE[prod_short](includes/prod_short.md)] beregner mva-beløp for salg og innkjøp som er basert på mva-posteringsoppsett, som er kombinasjoner av mva-bokføringsgrupper for firma og varer. For hver kombinasjon kan du angi mva-prosenten, mva-beregningstypen og finanskontoene for bokføring av mva i forbindelse med salg, kjøp og snudd avregning. Du kan også angi om mva skal beregnes på nytt når en kontantrabatt brukes eller mottas.  

Du kan definere så mange kombinasjoner du vil. Hvis du vil gruppere kombinasjoner av mva-bokføringsoppsett med lignende attributter, kan du definere en **mva-type** for hver gruppe og tilordne typen til gruppemedlemmene.

Hvis du vil kombinere mva-bokføringsoppsett, følger du denne fremgangsmåten:

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

## <a name="to-assign-vat-posting-groups-by-default-to-multiple-entities"></a>Slik tilordner du mva-bokføringsgrupper som standard til flere enheter
Hvis du vil bruke samme mva-bokføringsgrupper til flere enheter, kan du definere [!INCLUDE[prod_short](includes/prod_short.md)] å gjøre det som standard. Det er et par måter å gjøre dette på:

* Du kan tilordne mva-bokføringsgrupper for firma til firmabokføringsgruppen grupper eller maler for kunde eller leverandør
* Du kan tilordne mva-bokføringsgrupper for varer på varebokføringsgruppene  

Mva-bokføringsgruppe for firma eller vare tilordnes når du velger en bokføringsgruppe for firma eller vare for en kunde, leverandør, vare eller ressurs.

## <a name="assigning-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tilordne mva-bokføringsgrupper til konti, kunder, leverandører, varer og ressurser
De følgende delene beskriver hvordan du tilordner du mva-bokføringsgrupper til enkeltenheter.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Tilordne mva-bokføringsgrupper til individuelle finanskonti
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kontoplan**, og velg deretter den relaterte koblingen.  
2. Åpner **Finans**-kortet for kontoen.  
3. På hurtigfanen **Bokføring** i feltet **Bokføringstype** velger du enten **Salg** eller **Kjøp**.  
5. Velg mva-bokføringsgruppene for å bruke for salgs- eller kjøpskontoen.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Tilordne mva-bokføringsgrupper for firma til kunder og leverandører  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunde** eller **Leverandør**, og velg deretter den relaterte koblingen.  
2. På kortet **Kunde** eller **Leverandør** utvider du hurtigfanen **Fakturering**.  
3. Velg mva-bokføringsgruppen for firma.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tilordne mva-bokføringsgrupper for vare til individuelle varer og ressurser  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Vare** eller **Ressurs**, og velg deretter den relaterte koblingen.  
2. Gjør ett av følgende:  

* På **Vare**-kortet utvider du hurtigfanen **Pris og bokføring** og velger deretter **Vis mer** for å vise feltet **Mva-bokføringsgruppe - vare**.  
* På kortet **Ressurs** utvider du hurtigfanen **Fakturering**.  
3. Velg mva-bokføringsgruppen for vare.  

## <a name="setting-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Definere setninger for å forklare mva-fritak eller ikke-standard-mva-satser
Du kan definere en mva-setningsdel til å beskrive informasjon om hvilken type mva som brukes. Informasjonen kan være nødvendig ifølge bestemmelser fra myndighetene. Når du har definert en mva-setning, og knyttet den til et mva-bokføringsoppsett, vises mva-setningen på utskrevne salgsdokumenter som bruker gruppen for mva-bokføringsoppsett.

Hvis det er nødvendig, kan du også angi hvordan du kan oversette mva-setningsdeler til andre språk. Deretter, når du oppretter og skriver ut et salgsdokument som inneholder en mva-type, vil det oversatte dokumentet inkludere mva-setningen. Språkkoden som er angitt på kundekortet bestemmer språket.

Når ikke-standard mva-satser brukes i forskjellige typer dokumenter, for eksempel fakturaer eller kreditnotaer, må selskaper vanligvis inkludere en unntakstekst (mva-setning) som angir hvorfor en redusert mva eller null mva-sats er beregnet. Du kan definere forskjellige mva-setninger som skal være med i forretningsdokumenter i henhold til dokumenttypen, for eksempel faktura eller kreditnota. Dette gjør du på siden **Mva-setninger etter dokumenttype**.

Du kan endre eller slette en mva-setning, og endringene gjenspeiles i genererte rapporter. [!INCLUDE[prod_short](includes/prod_short.md)] beholder i imidlertid ikke historikk av endringen. Mva-setningsbeskrivelsene skrives ut på rapporten og vises for alle linjene i rapporten ved siden av mva-beløpet og mva-grunnlagsbeløpet. Hvis det ikke er definert en mva-setning for alle linjene i salgsdokumentet, utelates hele delen når rapporten skrives ut.

### <a name="to-set-up-vat-clauses"></a>Opprette mva-setninger
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-setninger**, og velg deretter den relaterte koblingen.  
2. På siden **Mva-setninger** oppretter du en ny linje.  
3. Angi en ID for setningen i **KCode**-feltet. Du bruker denne koden til å knytte setningen til mva-bokføringsgrupper.  
4. I feltet **Beskrivelse** angir du mva-fritaksteksten som du vil vise på dokumenter som kan inkludere mva. I feltet **Beskrivelse 2** angir du ekstra tekst ved behov. Teksten vises på nye dokumentlinjer.
5. Velg handlingen **Beskrivelse etter dokumenttype**.
6. På siden **Mva-setninger etter dokumenttype** fyller du ut feltene for å definere hvilken mva-fritakstekst som skal vises for hvilken dokumenttype.  
7. Valgfritt: Hvis du vil tilordne mva-setningsdelen til en mva-bokføringsoppsettet umiddelbart, velger du **Oppsett**, og deretter velge setningen. Hvis du vil vente, kan du tilordne setningsdelen senere på siden **mva-bokføringsoppsett**.  
8. Valgfritt: Hvis du vil angi hvordan du vil oversette mva-setningen, velger du **Oversettelser**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Slik tilordner du en mva-setning til et mva-bokføringsoppsett
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.  
2. I kolonnen **Mva-setning** velger du setningen som skal brukes for hvert mva-bokføringsoppsett den gjelder for.  

### <a name="to-specify-translations-for-vat-clauses"></a>Angi oversettelser for mva-setninger
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-setninger**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Oversettelser**.  
3. I feltet **Språkkode** velger du hvilket språk du skal oversette til.  
4. I feltene **Beskrivelse** og **Beskrivelse 2** skriver du inn oversettelsen av beskrivelsene. Denne teksten vises i de oversatte mva-rapportdokumentene.  

## <a name="to-create-a-vat-posting-setup-to-handle-import-vat"></a>Slik oppretter du et mva-bokføringsoppsett for å håndtere Import-mva
Du bruker funksjonen for import-mva når du skal bokføre et dokument der hele beløpet er mva. Dette bruker du hvis du mottar en faktura fra skattemyndighetene for mva for importerte varer.  

Følg disse trinnene for å opprette koder for import-mva:  
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsgrupper - vare**, og velg deretter den relaterte koblingen.  
2. Gå til siden Mva-bokføringsgrupper - vare. Definer en ny mva-varebokføringsgruppe for import-mva.  
3. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.  
4. Gå til siden Mva-bokføringsoppsett. Opprett en ny linje, eller bruk en eksisterende mva-bokføringsgruppe for firma sammen med den nye mva-varebokføringsgruppen for import-mva.  
5. I feltet **Mva-beregningstype** velger du **Full mva**.  
6. I feltet **Inngående mva-konto** angir du hvilken finanskonto som skal brukes til å bokføre import-mva. Alle andre kontoer er valgfrie.  


## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Bruke snudd avregning for handel mellom EU-land/-områder
Enkelte selskaper må bruke snudd avregning ved handel med andre selskaper. Denne regelen gjelder for eksempel for kjøp fra EU-land og -regioner og salg til EU-land og -regioner.  

> [!NOTE]  
> Denne regelen gjelder ved handel med selskaper som er registrert som mva-pliktige i andre EU-land/-regioner. Hvis du handler direkte med forbrukere i andre EU-land/-regioner, så bør du kontakte skattemyndighetene for å høre hvordan gjeldende mva-regler er.  

> [!TIP]  
> Du kan kontrollere at et selskap er registrert som mva-pliktig i et annet EU-land, ved hjelp av tjenesten for validering av EU-organisasjonsnummer. Tjenesten er tilgjengelig gratis i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon, kan du se delen kalt _Bekrefte organisasjonsnumre_ i dette emnet.

### <a name="sales-to-eu-countries-or-regions"></a>Salg til EU-land eller -regioner
Mva beregnes ikke på salg til mva-pliktige selskaper i andre EU-land/-regioner. Du må rapportere verdien av slike salg til EU-land/-regioner separat i mva-oppgaven.  

For å beregne riktig mva på salg til EU-land /-regioner bør du:  

* Definere en linje for salg med samme informasjon for kjøp. Hvis du allerede har definert linjer på siden Mva-bokføringsoppsett for kjøp fra EU-land/-regioner, kan du også bruke disse linjene for salg.  
* Tilordne mva-bokføringsgruppene for firma i feltet **Mva-bokføringsgruppe – firma** på hurtigfanen **Fakturering** på kundekortet for hver EU-kunde. Du må også angi kundens organisasjonsnummer i feltet **Organisasjonsnr.** på hurtigfanen **Utenrikshandel**.  

Når du bokfører et salg til en kunde i andre EU-land/-regioner, beregnes mva-beløpet, og det opprettes en mva-post ved hjelp av informasjon om snudd avregning og mva-grunnlaget, som er beløpet som brukes til å beregne mva-beløpet. Ingen poster bokføres til mva-konti i Finans.

## <a name="understanding-vat-rounding-for-documents"></a>Om mva-avrunding for dokumenter
Beløp i dokumenter som ikke er bokført ennå, rundes av og vises på en måte som tilsvarer den endelige avrundingen av beløp som faktisk er bokført. Mva beregnes for et fullstendig dokument, som betyr at mva beregnes basert på summen av alle linjer med samme mva-type i dokumentet.




## <a name="see-also"></a>Se også
[Definere mva-oppgavemaler og mva-oppgavenavn](finance-how-setup-vat-statement.md)   
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)      
[Rapportere mva til skattemyndighetene](finance-how-report-vat.md)      
[Arbeide med mva på kjøp og salg](finance-work-with-vat.md)    
[Arbeide med verktøyet for endring av mva-sats](finance-how-use-vat-rate-change-tool.md)    
[Bekrefte organisasjonsnumre](finance-how-validate-vat-registration-number.md)  
[Lokal funksjonalitet i Business Central](about-localization.md)  

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)


[!INCLUDE[footer-include](includes/footer-banner.md)]