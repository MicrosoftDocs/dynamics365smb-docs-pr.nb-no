---
title: Om definering av merverdiavgift | Microsoft-dokumentasjon
description: "Kontroller at du riktig beregne, postere og rapportere mva for salg og innkjøp."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: ce397b4a492a727211b49d7db2a231bea40d8c43
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---

# <a name="setting-up-to-calculations-and-posting-methods-for-value-added-tax"></a>Definere beregninger og bokføringsmetoder for merverdiavgift
Forbrukere og selskaper betaler merverdiavgift (mva) når de kjøper varer eller tjenester. Mva-beløpet som skal betales, kan variere, avhengig av flere faktorer. I [!INCLUDE[d365fin](includes/d365fin_md.md)] setter du opp for å angi satsene som skal brukes til å beregne mva-beløp som er basert på følgende: 

* Hvem du selger til  
* Hvem du kjøper fra  
* Hva du selger  
* Hva du kjøper  
  
Du kan definere mva-beregninger manuelt, men som kan være vanskelig og tidkrevende. For å gjøre det enkelt har vi laget en assistert oppsettsveiledning kalt **Mva-oppsett** som hjelper deg gjennom fremgangsmåten. Vi anbefaler at du bruker den assisterte oppsettsveiledningen til å definere mva.

> [!NOTE]  
>   Du kan bare bruke veiledningen hvis du har opprettet et Mitt selskap og ikke har bokført transaksjoner som inkluderer mva. Det ville ellers være svært enkelt å bruke forskjellige mva-satser ved en feiltakelse, og gjøre mva-relaterte rapporter unøyaktige.  
  
Hvis du vil definere mva-beregninger selv, eller bare vil lære mer om hvert trinn, inneholder dette emnet beskrivelser av hvert trinn. Disse inkluderer hvordan du:  
  
* Definerer mva-bokføringsgrupper for firma for å definere mva-satsene for markeder du handler med. Du tilordner disse til kunder og leverandører.  
* Definere mva-bokføringsgrupper for varer for å definere mva-satsene for produkter og tjenester du kjøper eller selger.  
  
   > [!NOTE]  
>   Konseptene bak mva-bokføringsgruppene for firma og varer ligner på generelle bokføringsgrupper. Hvis du vil ha mer informasjon, kan du se [Oppsett av bokføringsgrupper](finance-posting-groups.md).
* Kombinere mva-bokføringsgrupper for firma og varer for å opprette mva-oppsett som beregner mva-beløp på salg og kjøp.  
* Tilordne mva-bokføringsgrupper for varer til finanskontoer som du bruker for salg og innkjøp, og varer og ressurser.  

   > [!NOTE]  
>   For å kunne definere mva for ressurser må du aktivere brukeropplevelsen **Løsning** for selskapet. Hvis du vil ha mer informasjon, kan du se [Tilpasse Dynamics 365 for Financials-opplevelsen](ui-experiences.md).
* Bruke omvendt belastet mva for handel mellom EU-land/-områder  
* Forstå mva-avrunding for dokumenter  
* Definere klausuler som forklarer bruken av ikke-standard mva-satser
* Bekrefte organisasjonsnumre

## <a name="use-the-vat-setup-assisted-setup-guide-to-set-up-vat-recommended"></a>Bruke mva-oppsettguiden til å definere mva (anbefales)
Vi anbefaler at du bruker den medfølgende mva-oppsettguiden til å definere mva i [!INCLUDE[d365fin](includes/d365fin_md.md)]. 

Hvis du vil oppsettguiden, gjør du følgende:
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), og angi **Assistert oppsett**.  
2. Velg **Mva-oppsett**.

## <a name="set-up-vat-business-posting-groups"></a>Opprette mva-bokføringsgrupper for firma
Mva-bokføringsgrupper for firma skal representere markeder som du gjør forretninger med kunder og leverandører i, og definere hvordan du skal beregne og bokføre mva for hvert marked. Eksempler på mva-bokføringsgrupper for firma er **Innenlands** og **Den europeiske union (EU)**.  

Bruk koder som er lette å huske, og som beskriver bokføringsgruppen, for eksempel **EU**, **ikke-EU** eller **innenlands**. Koden må være unik. Du kan kan definere så mange koder du vil, men du kan ikke bruke samme kode mer enn én gang i en tabell.
  
Hvis du vil definere en mva-bokføringsgruppe for bedrifter, gjør du følgende:

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-bokføringsgruppe - firma**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

Du oppretter standard mva-bokføringsgrupper for firma ved å knytte dem til firmabokføringsgrupper. [!INCLUDE[d365fin](includes/d365fin_md.md)] tilordner automatisk mva-bokføringsgruppen for firma når du knytter firmabokføringsgruppen til en kunde, leverandør eller finanskonto. 

## <a name="set-up-vat-product-posting-groups"></a>Opprette mva-bokføringsgrupper for varer
Mva-bokføringsgrupper for produkter representerer varer og ressurser du kjøper eller selger, og du kan finne ut hvordan du skal beregne og bokføre mva i henhold til hvilken type vare eller ressurs som blir kjøpt eller solgt.  
Det er lurt å bruke koder som er lette å huske og som beskriver satsen, for eksempel **Ingen mva** eller **Null**, **MVA10** eller **Redusert** for 10 % mva, og **MVA25** eller **Standard** for 25 %.

Hvis du vil definere en mva-bokføringsgruppe for bedrifter, gjør du følgende:

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-bokføringsgrupper - vare**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene etter behov.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinere mva-bokføringsgrupper i mva-bokføringsoppsett
[!INCLUDE[d365fin](includes/d365fin_md.md)] beregner mva-beløp for salg og innkjøp som er basert på mva-posteringsoppsett, som er kombinasjoner av mva-bokføringsgrupper for firma og varer. For hver kombinasjon kan du angi mva-prosenten, mva-beregningstypen og finanskontoene for bokføring av mva i forbindelse med salg, kjøp og snudd avregning. Du kan også angi om mva skal beregnes på nytt når en kontantrabatt brukes eller mottas.  

Du kan definere så mange kombinasjoner du vil. Hvis du vil gruppere kombinasjoner av mva-bokføringsoppsett med lignende attributter, kan du definere en **mva-type** for hver gruppe og tilordne typen til gruppemedlemmene.

Hvis du vil kombinere mva-bokføringsoppsett, følger du denne fremgangsmåten:

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov.

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tilordne mva-bokføringsgrupper som standard til flere enheter
Hvis du vil bruke samme mva-bokføringsgrupper til flere enheter, kan du definere [!INCLUDE[d365fin](includes/d365fin_md.md)] å gjøre det som standard. Det er et par måter å gjøre dette på:

* Du kan tilordne mva-bokføringsgrupper for firma til firmabokføringsgruppen grupper eller maler for kunde eller leverandør 
* Du kan tilordne mva-bokføringsgrupper for varer på varebokføringsgruppene  

Mva-bokføringsgruppe for firma eller vare tilordnes når du velger en bokføringsgruppe for firma eller vare for en kunde, leverandør, vare eller ressurs.

## <a name="assign-vat-posting-groups-to-individual-accounts-customers-vendors-items-and-resources"></a>Tilordne mva-bokføringsgrupper til individuelle konti, kunder, leverandører, varer og ressurser
De følgende delene beskriver hvordan du tilordner du mva-bokføringsgrupper til enkeltenheter.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Tilordne mva-bokføringsgrupper til individuelle finanskonti 
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kontoplan**, og velg deretter den relaterte koblingen.  
2. Åpner **Finans**-kortet for kontoen.
3. På hurtigfanen **Bokføring** i feltet **Bokføringstype** velger du enten **Salg** eller **Kjøp**.  
5. Velg mva-bokføringsgruppene for å bruke for salgs- eller kjøpskontoen.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Tilordne mva-bokføringsgrupper for firma til kunder og leverandører  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kunde** eller **Leverandør**, og velg deretter den relaterte koblingen.  
2. På kortet **Kunde** eller **Leverandør** utvider du hurtigfanen **Fakturering**.  
3. Velg mva-bokføringsgruppen for firma.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Tilordne mva-bokføringsgrupper for vare til individuelle varer og ressurser  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kunde** eller **Leverandør**, og velg deretter den relaterte koblingen.  
2. Gjør ett av følgende:
* På **Vare**-kortet utvider du hurtigfanen **Pris og bokføring** og velger deretter **Vis mer** for å vise feltet **Mva-bokføringsgruppe - vare**.  
* På kortet **Ressurs** utvider du hurtigfanen **Fakturering**.  
3. Velg mva-bokføringsgruppen for vare.

## <a name="set-up-clauses-to-explain-the-use-of-non-standard-vat-rates"></a>Definere klausuler som forklarer bruken av ikke-standard mva-satser
Du kan definere en mva-setningsdel til å beskrive informasjon om hvilken type mva som brukes. Informasjonen kan være nødvendig ifølge bestemmelser fra myndighetene. Når du har definert en mva-setning, og knyttet den til et mva-bokføringsoppsett, vises mva-setningen på utskrevne salgsdokumenter som bruker gruppen for mva-bokføringsoppsett. 

Hvis det er nødvendig, kan du også angi hvordan du kan oversette mva-setningsdeler til andre språk. Deretter, når du oppretter og skriver ut et salgsdokument som inneholder en mva-type, vil det oversatte dokumentet inkludere mva-setningen. Språkkoden som er angitt på kundekortet bestemmer språket.
  
### <a name="to-set-up-vat-clauses"></a>Opprette mva-setninger
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-setninger**, og velg deretter den relaterte koblingen.  
2. På siden **Mva-setninger** oppretter du en ny linje.  
3. Angi en ID for setningen i **KCode**-feltet. Du bruker denne koden til å knytte setningen til mva-bokføringsgrupper.  
4. I feltet **Beskrivelse** angir du teksten som du vil vise på dokumenter som kan inkludere mva. I feltet **Beskrivelse 2** angir du ekstra tekst ved behov. Teksten vises på de nye linjene.  
5. Valgfritt: Hvis du vil tilordne mva-setningsdelen til en mva-bokføringsoppsettet umiddelbart, velger du **Oppsett**, og deretter velge setningen. Hvis du vil vente, kan du tilordne setningsdelen senere på siden mva-bokføringsoppsett.  
6. Valgfritt: Hvis du vil angi hvordan du vil oversette mva-setningen, velger du **Oversettelser**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Slik tilordner du en mva-setning til et mva-bokføringsoppsett
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.  
2. I kolonnen **Mva-setning** velger du setningen som skal brukes for hvert mva-bokføringsoppsett den gjelder for.  

### <a name="to-specify-translations-for-vat-clauses"></a>Angi oversettelser for mva-setninger
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-setninger**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Oversettelser**.  
3. I feltet **Språkkode** velger du hvilket språk du skal oversette til.  
4. I feltene **Beskrivelse** og **Beskrivelse 2** skriver du inn oversettelsen av beskrivelsene. Denne teksten vises i de oversatte mva-rapportdokumentene.  
  
## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Opprette et mva-bokføringsoppsett for å håndtere Import-mva
Du bruker funksjonen for import-mva når du skal bokføre et dokument der hele beløpet er mva. Dette bruker du hvis du mottar en faktura fra skattemyndighetene for mva for importerte varer.  
  
Følg disse trinnene for å opprette koder for import-mva:  
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-bokføringsgrupper - vare**, og velg deretter den relaterte koblingen.  
2. Gå til siden Mva-bokføringsgrupper - vare. Definer en ny mva-varebokføringsgruppe for import-mva.  
3. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Mva-bokføringsoppsett**, og velg deretter den relaterte koblingen.  
4. Gå til siden Mva-bokføringsoppsett. Opprett en ny linje, eller bruk en eksisterende mva-bokføringsgruppe for firma sammen med den nye mva-varebokføringsgruppen for import-mva.  
5. I feltet **Mva-beregningstype** velger du **Full mva**.  
6. I feltet **Inngående mva-konto** angir du hvilken finanskonto som skal brukes til å bokføre import-mva. Alle andre kontoer er valgfrie.  
  
## <a name="verify-vat-registration-numbers"></a>Bekrefte organisasjonsnumre
Det er viktig at organisasjonsnumrene du har for kunder, leverandører og kontakter, er gyldige. For eksempel selskaper noen ganger endre status for mva-ansvar, og i noen land kan skattemyndighetene ber deg om å gi rapporter, for eksempel rapporten EU-salgslisten som listen mva registreringsnumre du bruker når du gjør forretninger. 
  
EU-kommisjonen gir tjenesten EU-mva-nummer validering på webområdet sitt, som er felles og gratis. [!INCLUDE[d365fin](includes/d365fin_md.md)] kan spare deg for et trinn, og du kan bruke tjenesten VIES til å validere og spore mva-numre for kunder, leverandører og kontakter direkte fra kunde-, leverandør- og kontaktkort. Tjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] kalles **Tjeneste for validering av EU-organisasjonsnr.**. Tjenesten er tilgjengelig på siden **Tjenestetilkoblinger**, og du kan begynne å bruke den med en gang. Tjenestetilkoblingen er gratis, og registrering er ikke nødvendig.

Når du bruker tjenestetilkoblingen vår, registrerer vi en logg over mva-numre og bekreftelser for hver kunde, leverandør eller kontakt i **Organisasjonsnummerlogg**, så du kan enkelt spore dem. Loggen er spesifikk for hver kunde. Loggen er for eksempel nyttig for å bevise at du har bekreftet at gjeldende mva-nummeret er riktig. Når du godkjenner et mva-nummer, gjenspeiler kolonnen **ID for forespørsel** i loggen at du har gjort noe. 

Du kan vise loggen mva-registrering på kortene for kunde, leverandør eller kontakt på den **fakturering** hurtigfanen, ved å velge knappen Slå opp i den **Organisasjonsnr.** .  

Tjenesten kan også spare deg tid når du oppretter en kunde eller leverandør. Hvis du kjenner kundens mva-nummer, kan du angi det i feltet **Organisasjonsnr.** på kunde- eller leverandørkortene, og så fyller vi ut kundenavnet for deg. Noen land gir også firmaadresser i et strukturert format. I disse landene fyller vi ut adressen også.  

> [!NOTE]  
> Det er et par ting å merke seg når det gjelder EU-mva-nummer validering-tjenesten:

* Denne webtjenesten bruker HTTP-protokollen, som betyr at data som overføres via tjenesten, ikke er kryptert.  
* Du kan oppleve nedetid for denne tjenesten som Microsoft ikke er ansvarlig. Tjenesten er en del av en omfattende EU-nettverk av nasjonale mva-registre.

## <a name="using-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Bruke snudd avregning for handel mellom EU-land/-områder
Enkelte selskaper må bruke snudd avregning ved handel med andre selskaper. Denne regelen gjelder for eksempel for kjøp fra EU-land og -regioner og salg til EU-land og -regioner.  
  
> [!NOTE]  
> Denne regelen gjelder ved handel med selskaper som er registrert som mva-pliktige i andre EU-land/-regioner. Hvis du handler direkte med forbrukere i andre EU-land/-regioner, så bør du kontakte skattemyndighetene for å høre hvordan gjeldende mva-regler er.  
  
> [!TIP]  
> Du kan kontrollere at et selskap er registrert som mva-pliktig i et annet EU-land, ved hjelp av tjenesten for validering av EU-organisasjonsnummer. Tjenesten er tilgjengelig gratis i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se delen kalt _Bekrefte organisasjonsnumre_ i dette emnet.

### <a name="sales-to-eu-countries-or-regions"></a>Salg til EU-land eller -regioner
Mva beregnes ikke på salg til mva-pliktige selskaper i andre EU-land/-regioner. Du må rapportere verdien av slike salg til EU-land/-regioner separat i mva-oppgaven.  

For å beregne riktig mva på salg til EU-land /-regioner bør du:  
  
* Definere en linje for salg med samme informasjon for kjøp. Hvis du allerede har definert linjer på siden Mva-bokføringsoppsett for kjøp fra EU-land/-regioner, kan du også bruke disse linjene for salg.  
* Tilordne mva-bokføringsgruppene for firma i feltet **Mva-bokføringsgruppe – firma** på hurtigfanen **Fakturering** på kundekortet for hver EU-kunde. Du må også angi kundens organisasjonsnummer i feltet **Organisasjonsnr.** på hurtigfanen **Utenrikshandel**.  

Når du bokfører et salg til en kunde i andre EU-land/-regioner, beregnes mva-beløpet, og det opprettes en mva-post ved hjelp av informasjon om snudd avregning og mva-grunnlaget, som er beløpet som brukes til å beregne mva-beløpet. Ingen poster bokføres til mva-konti i Finans.

## <a name="understanding-vat-rounding-for-documents"></a>Om mva-avrunding for dokumenter
Beløp i dokumenter som ikke er bokført ennå, rundes av og vises på en måte som tilsvarer den endelige avrundingen av beløp som faktisk er bokført. Mva beregnes for et fullstendig dokument, som betyr at mva beregnes basert på summen av alle linjer med samme mva-type i dokumentet.

## <a name="see-also"></a>Se også  
[Definere urealisert merverdiavgift](finance-setup-unrealized-vat.md)
