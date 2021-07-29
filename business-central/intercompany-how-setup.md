---
title: Definere bokføring av konserninterne transaksjoner
description: Opprett konserninterne leverandører og kunder som såkalte konserninterne partnere, og definer en konsernintern kontoplan.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: IC, group, consolidation, affiliate, subsidiary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9f43141d4280fcadedc8072194f0d4d52e50cdf2
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441271"
---
# <a name="set-up-intercompany-transaction-posting"></a>Definere bokføring av konserninterne transaksjoner

Hvis du vil sende en transaksjon (for eksempel en salgskladdelinje) fra ett selskap og få den tilsvarende transaksjonen (for eksempel en kjøpskladdelinje) til å opprettes automatisk i partnerselskapet, må de involverte selskapene bli enige om en felles kontoplan og et felles sett av dimensjoner som skal brukes under konserninterne transaksjoner. Den konserninterne kontoplanen kan for eksempel være en forenklet versjon av morselskapets kontoplan. Hvert selskap tilordner hele kontoplanen til den delte, konserninterne kontoplanen, og hvert selskap tilordner dimensjonene til de konserninterne dimensjonene.  

Du må også definere en konsernintern partnerkode for hvert partnerselskap, som avtales mellom alle selskapene, og tilordne dem til kunde- og leverandørkortene henholdsvis ved å fylle ut feltet **Konsernintern partnerkode**.  

Hvis du oppretter eller mottar konserninterne linjer med varer, kan du bruke dine egne varenumre eller definere partnerens varenumre for hver relevante vare, enten i feltet **Leverandørs varenr.** eller i feltet **Felles varenr.** på varekortet. Du kan også bruke funksjonen **Varekryssreferanse** til å tilordne varenumrene til de konserninterne partnerbeskrivelsene av varene, åpne kortet for hver vare og deretter velge handlingen **Kryssreferanser** for å definere kryssreferanser mellom varebeskrivelsene dine og dem til den konserninterne partneren. Se [Bruke varekryssreferanser](inventory-how-use-item-cross-refs.md) for mer informasjon. 

Hvis du vil utføre konserninterne salgstransaksjoner som inkluderer ressurser, må du fylle ut feltet **Finanskontonr. for KI-partnerkjøp** på ressurskortet for hver relevante ressurs. Dette er nummeret til den konserninterne finanskontoen der beløpet for denne ressursen skal bokføres i partnerens selskap. Hvis du vil ha mer informasjon, kan du se [Definere ressurser](projects-how-setup-resources.md).

## <a name="to-set-up-companies-for-intercompany-transactions"></a>Slik definerer du selskaper for konserninterne transaksjoner
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.  
2. På siden **Selskapsopplysninger** fyller du ut feltet **Konsernintern partnerkode**, **Konsernintern innbokstype**. og feltet **Detaljer om konsernintern innboks**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-intercompany-partners"></a>Slik konfigurerer du konserninterne partnere
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne partnere**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. På siden **Konsernintern partner** fyller du ut feltene etter behov.[!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> I [!INCLUDE[prod_short](includes/prod_short.md)] Online kan du ikke bruke filplasseringer til å overføre transaksjoner til partnerne fordi [!INCLUDE[prod_short](includes/prod_short.md)] ikke har tilgang til det lokale nettverket. Hvis du velger **Filplassering** i **Overføringstype**-feltet, er derfor ikke **Mappebane**-feltet tilgjengelig. Filen lastes i stedet ned til Nedlastinger-mappen på datamaskinen. Du sender deretter filen til noen i partnerselskapet, for eksempel via e-post. Vi anbefaler at du i stedet velger **E-post** for å bruke en mer direkte fremgangsmåte.

## <a name="to-set-up-intercompany-vendors-and-intercompany-customers"></a>Slik definerer du konserninterne leverandører og kunder
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Du kan også få tilgang til leverandøren fra feltet **Leverandørnr.** på siden **Konsernintern partner**.
3. Åpne kortet for en leverandør som er en konsernintern partner. Hvis du vil ha mer informasjon, kan du se [Registrere nye leverandører](purchasing-how-register-new-vendors.md).
4. I feltet **Konsernintern partnerkode** velger du den relevante konserninterne partnerkoden.
5. Gjenta trinn 1 til og med 4 for kunder.

## <a name="to-set-up-intercompany-charts-of-accounts"></a>Slik definerer du den konserninterne kontoplanen
Hvis en gruppe selskaper skal kunne lage konserninterne transaksjoner, må de bli enige om en kontoplan som skal brukes som felles referanse. Du må bli enig med partnerselskapene om kontonumrene som alle skal bruke ved oppretting av konserninterne transaksjoner. Morselskapet i gruppen oppretter for eksempel en forenklet versjon av sin egen kontoplan, eksporterer denne konserninterne kontoplanen fra databasen til en XML-fil og distribuerer den til alle selskapene i gruppen.  

Hvis selskapet ditt er det overordnede selskapet og har den definerende konserninterne kontoplanen som gruppen skal bruke som felles referanse, følger du fremgangsmåten [Slik setter du opp den definerende konserninterne kontoplanen](intercompany-how-setup.md#to-set-up-the-defining-intercompany-chart-of-accounts).  

Hvis selselskapet er et underselskap og du har mottatt en XML-fil som inneholder den felles konserninterne kontoplanen, følger du fremgangsmåten [Slik importerer du den konserninterne kontoplanen](intercompany-how-setup.md#to-import-the-intercompany-chart-of-accounts).  

### <a name="to-set-up-the-defining-intercompany-chart-of-accounts"></a>Slik setter du opp den definerende konserninterne kontoplanen
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsernintern kontoplan** og velg deretter den relaterte koblingen.
2. Angi hver konto på en linje på siden **Konsernintern kontoplan**.  
3. Hvis den konserninterne kontoplanen vil være identisk med eller vil ligne på den vanlige kontoplanen, kan du fylle ut siden automatisk ved å velge handlingen **Kopier fra kontoplan**. Du kan redigere de nye linjene etter behov.

### <a name="to-export-an-intercompany-chart-of-accounts"></a>Slik eksporterer du en konsernintern kontoplan
Hvis du vil at de konserninterne partnerne skal kunne importere den definerende kontoplanen, må du eksportere den til en fil.      
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsernintern kontoplan** og velg deretter den relaterte koblingen.
2. På siden **Konsernintern kontoplan** velger du **Eksporter**-handlingen og velger deretter **Lagre**-knappen.
3. Angi filnavnet og lokasjonen der du vil lagre XML-filen, og velg deretter **Lagre**.  

### <a name="to-import-the-intercompany-chart-of-accounts"></a>Slik importerer du den konserninterne kontoplanen  
Når det finnes en fil for den definerende konserninterne kontoplanen, kan konserninterne partnere importere den for å sikre at de har de samme kontiene.  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsernintern kontoplan** og velg deretter den relaterte koblingen.  
2. På siden **Konsernintern kontoplan** velger du handlingen **Importer**.  
3. Velg filnavnet og lokasjonen for XML-filen, og velg deretter **Åpne**-knappen.  

Siden **KI-kontoplan** fylles ut med nye eller redigerte finanskontolinjer i henhold til den konserninterne kontoplanen i filen. Eventuelle eksisterende urelaterte linjer på siden forblir uendret.

### <a name="to-map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Slik tilordner du den konserninterne kontoplanen til selskapets kontoplan  
Når du har definert eller importert den konserninterne kontoplanen du og de konserninterne partnerne har blitt enige om å bruke, må du knytte hver av de konserninterne finanskontiene til én av selskapets finanskonti. På siden **KI-kontoplan** angir du hvordan konserninterne finanskonti i innkommende transaksjoner vil bli oversatt til finanskonti fra selskapets kontoplan.

Hvis kontiene i den konserninterne kontoplanen har samme numrene som de tilsvarende kontiene i kontoplanen, kan du tilordne kontoene automatisk.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konsernintern kontoplan** og velg deretter den relaterte koblingen.  
2. Velg linjene du vil tilknytte automatisk, og velg deretter **Samkjør med konto med samme nummer**.  
3. For hver konserninterne finanskonto som ikke ble tilknyttet automatisk, fyller du ut feltet **Samkjør med finanskontonr.**  

## <a name="to-set-up-default-intercompany-partner-general-ledger-accounts"></a>Slik setter du opp standard finanskonti for konsernintern partner  
Når du oppretter en konsernintern salgs- eller kjøpslinje som skal sendes som en utgående transaksjon, angir du en konto fra den konserninterne kontoplanen som standard for hvilken konto i partnerens selskap som beløpet skal bokføres på. På **Kontoplan**-siden kan du angi en standard finanskonto for konsernintern partner for konti du bruker ofte i utgående konserninterne salgslinjer eller kjøpslinjer. For samlekontoen for kunder kan du for eksempel angi tilsvarende samlekonto for leverandører fra den konserninterne kontoplanen.  

Når du nå angir en finanskonto i feltet **Motkontonr.** i en konsernintern linje med **Konsernintern partner** i feltet **Kontotype**, blir feltet **Finanskonto for KI-partner** automatisk fylt ut.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kontoplan** og velger deretter den relaterte koblingen.  
2. På linjen for en finanskonto er brukt for konserninterne transaksjoner, i feltet **Standard finanskonto for KI-Partner** angir du den konserninterne finanskontoen partneren skal bokføre til når du bokfører i finanskontoen på linjen.  
3. Gjenta trinn 2 for hver konto du ofte angir, i feltet **Motkontonr.** på en linje i en konsernintern kladd eller et konserninternt dokument.

## <a name="to-set-up-intercompany-dimensions"></a>Slik definerer du konserninterne bokføringer

Hvis du og de konserninterne partnerne vil ha mulighet til å utveksle transaksjoner med tilknyttede dimensjoner, må dere bli enige om dimensjonene som alle skal bruke. Morselskapet i gruppen oppretter for eksempel en forenklet versjon av sitt eget sett med dimensjoner, eksporterer disse konserninterne dimensjonene fra databasen til en XML-fil og distribuerer den til alle selskapene i gruppen. Hvert av datterselskapene importerer deretter XML-filen til siden **Konserninterne dimensjoner** og knytter de konserninterne dimensjonene til dimensjonene i sin egen **Dimensjoner**-side.  

> [!NOTE]
> Hvert selskap i [!INCLUDE [prod_short](includes/prod_short.md)] må tilordne dimensjoner til konserninterne dimensjoner for utgående dokumenter, og tilordne konserninterne dimensjoner til egne dimensjoner for inngående dokumenter. Denne tilordningen bidrar til å sikre konsekvens på tvers av selskapene. Hvis du vil ha mer informasjon, kan du se delen [Slik tilordner du konserninterne dimensjoner til selskapets dimensjoner](#to-map-intercompany-dimensions-to-your-companys-dimensions).

Hvis selskapet ditt er det overordnede selskapet og har det definerende settet med konerninterne dimensjoner som gruppen din skal bruke som en felles referanse, følger du fremgangsmåten [Slik definerer du de konserninterne dimensjonene](intercompany-how-setup.md#to-define-the-intercompany-dimensions).

Hvis selskapet er et datterselskap og du har mottatt en XML-fil som inneholder de konserninterne dimensjonene som gruppen skal bruke som felles referanse, følger du fremgangsmåten [Slik importerer du konserninterne dimensjoner](intercompany-how-setup.md#to-import-the-intercompany-dimensions).

### <a name="to-define-the-intercompany-dimensions"></a>Slik definerer du de konserninterne dimensjonene
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne dimensjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Konserninterne dimensjoner** angir du hver dimensjon på en linje på siden.

    Hvis de konserninterne dimensjonene vil være identiske med eller vil ligne på selskapsdimensjonene, kan du fylle ut siden automatisk ved hjelp av funksjonen **Kopier fra dimensjoner** og deretter redigere resultatlinjene.  
3. Hvis du vil eksportere de konserninterne dimensjonene til en XML-fil for distribusjon til partnerselskapene, velger du **Eksporter**-handlingen.  
4. Angi filnavnet og lokasjonen der du vil lagre XML-filen, og velg deretter **Lagre**.  

### <a name="to-import-the-intercompany-dimensions"></a>Slik importerer du de konserninterne dimensjonene  
Når det finnes en fil for de definerende konserninterne dimensjonene, kan konserninterne partnere importere den for å sikre at de har de samme dimensjonene.  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne dimensjoner**, og velg deretter den relaterte koblingen.  
2. På siden **Konserninterne dimensjoner** velger du handlingen **Importer**.  
3. Angi filnavnet og lokasjonen for XML-filen, og velg deretter **Åpne**-knappen.  

Linjene på siden **Konserinterne dimensjoner** og siden **Konserinterne dimensjonsverdier** importeres.  

### <a name="to-map-intercompany-dimensions-to-your-companys-dimensions"></a>Slik tilordner du konserninterne dimensjoner til selskapets dimensjoner
Når du har definert og importert dimensjonene du og de konserninterne partnerne er blitt enige om å bruke, må du knytte hver av de konserninterne dimensjonene til én av dimensjonene i selskapet ditt, og omvendt. På siden **Konserninterne dimensjoner** angir du hvordan konserninterne dimensjoner for *innkommende transaksjoner* blir oversatt til dimensjoner fra selskapets liste over dimensjoner. På **Dimensjon**-siden angir du hvordan dimensjonene skal oversettes til konserninterne dimensjoner i *utgående transaksjoner*.

Hvis noen av de konserninterne dimensjonene har samme kode som de tilsvarende dimensjonene i selskapets liste over dimensjoner, kan du få programmet til å tilknytte dimensjonene automatisk.  

I fremgangsmåten nedenfor tilordner du først konserninterne dimensjoner til dimensjoner for inngående dokumenter på siden **Konserninterne dimensjoner**. Deretter tilordner du dimensjoner til konserninterne dimensjoner for utgående dokumenter på siden **Dimensjoner**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Konserninterne dimensjoner**, og velg deretter den relaterte koblingen.
2. På siden **Konserninterne dimensjoner** velger du linjene du vil tilknytte automatisk, og deretter velger du **Samkjør med dimensjon med samme kode**.
3. Fyll ut feltet **Samkjør med dimensjonskode** for hver konserninterne dimensjon som ikke tilordnes automatisk.

    Det kan være du må legge til feltet i visningen. Hvis du vil ha mer informasjon, kan du se [Tilpasse arbeidsområdet](ui-personalization-user.md).
4. Velg handlingen **Konserninterne dimensjonsverdier**.
5. På siden **Konserninterne dimensjonsverdier** fyller du ut feltet **Samkjør med dimensjonsverdikode**.

    Fortsett med å tilknytte dimensjoner til konserninterne dimensjoner ved å utføre lignende fremgangsmåter.
6. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Dimensjoner**, og velg deretter den relaterte koblingen.
7. På siden **Dimensjoner** velger du linjene du vil tilknytte automatisk, og deretter velger du **Samkjør med KI-dimensjon med samme kode**.
8. Fyll ut feltet **Samkjør med KI-dimensjonsverdikode** for hver konserninterne dimensjon som ikke tilordnes automatisk.
9. Velg handlingen **Dimensjonsverdier**.
10. På siden **Dimensjonsverdier** fyller du ut feltet **Samkjør med KI-dimensjonsverdikode**.

## <a name="see-also"></a>Se også

[Behandle konserninterne transaksjoner](intercompany-manage.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Arbeide med finanskladder](ui-work-general-journals.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]