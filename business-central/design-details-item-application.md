---
title: Designdetaljer – Vareutligning | Microsoft-dokumentasjon
description: Dette emnet beskriver hvor lagerantallet og verdien registreres når du bokfører en lagertransaksjon.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, items, ledger entries, posting, inventory
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: fd37ec9ca5cc2de00f18f26bccc32aa81cd5659a
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215031"
---
# <a name="design-details-item-application"></a>Designdetaljer: Vareutligning

Når du bokfører en lagertransaksjon, registreres antallsbokføringen i varepostene og verdibokføringen i verdipostene. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Lagerbokføring](design-details-inventory-posting.md).  

I tillegg utføres en vareutligning for å koble kostnadsmottaker til kostnadskilden for å angi videresending av kostnader i henhold til lagermetoden. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostmetoder](design-details-costing-methods.md).  

[!INCLUDE[prod_short](includes/prod_short.md)] utfører to typer vareutligning.  

|Utligningstype|Beskrivelse|  
|----------------------|---------------------------------------|  
|Antallsutligning|Opprettes for alle lagertransaksjoner|  
|Kostutligning|Opprettes for innkommende poster sammen med antallsutligning som et resultat av brukerhandling i spesialprosesser.|  

Vareutligninger kan utføres på følgende måter.  

|Metode|Beskrivelse|Utligningstype|  
|------------|---------------------------------------|----------------------|  
|Automatisk|Forekommer som videresending av generelle kostnader i henhold til lagermetoden|Antallsutligning|  
|Fast|Utføres av brukeren når:<br /><br /> -   Behandler returer<br />-   Bokfører rettelser<br />-   Angrer antallsbokføringer<br />-   Oppretter direkte leveringer **Obs!**  Du kan gjøre fast utligning manuelt ved å skrive inn et postnummer i feltet **Utlignet fra-varepost**, eller ved å bruke en funksjon, for eksempel **Hent bokførte dokumentlinjer som skal tilbakeføres**.|Antallsutligning<br /><br /> Kostutligning **Obs!**  Kostutligning oppstår bare i innkommende transaksjoner når feltet **Utlignet fra-varepost** fylles ut for å opprette en fastsatt utligning. Se den neste tabellen.|  

Om det er antallsutligninger eller kostutligninger som utføres, avhenger av retningen til lagertransaksjonen og om vareutligningen utføres automatisk eller er fast, i forbindelse med spesialprosesser.  

Tabellen nedenfor viser hvordan kostnader flyter avhengig av transaksjonsretningen, basert på de sentrale utligningsfeltene på lagertransaksjonslinjer. Dette angir også når og hvorfor vareutligning er av typen antall eller kost.  

|-|Feltet Utligningsvarepost|Feltet Utlignet fra-varepost|  
|-|--------------------------------|----------------------------------|  
|Utligning for utgående post|Den utgående posten henter kostnaden fra den åpne inngående posten.<br /><br /> **Antallsutligning**|Støttes ikke|  
|Utligning for inngående post|Den inngående posten skyver kostnaden over på den utgående posten.<br /><br /> Den inngående posten er kostnadskilden.<br /><br /> **Antallsutligning**|Den inngående posten henter kostnaden fra den utgående posten. **Obs!** Når denne faste utligningen foretas, behandles den inngående transaksjonen som en ordreretur. Derfor holdes den utlignede utgående posten åpen. <br /><br /> Den inngående posten er IKKE kostnadskilden.<br /><br /> **Kostutligning**|  

> [!IMPORTANT]  
> En ordreretur regnes IKKE som en kostnadskilde når fast brukes.  
>
> Salgsposten forblir åpen til den faktiske kilden er bokført.  

En vareutligningspost inneholder følgende informasjon.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Varepostnr.**|Nummeret på vareposten for transaksjonen som denne utligningsposten er opprettet for.|  
|**Inngående vareløpenr.**|Varepostnummeret for lagerøkningen som transaksjonen skal knyttes til, hvis det er aktuelt.|  
|**Utgående vareløpenr.**|Varepostnummeret for lagerreduksjonen som transaksjonen skal knyttes til, hvis det er aktuelt.|  
|**Antall**|Antallet som utlignes.|  
|**Bokføringsdato**|Bokføringsdatoen for transaksjonen.|  

## <a name="inventory-increase"></a>Lagerøkning  
Når du bokfører en lagerøkning, registreres en enkel vareutligningspost uten en utligning til en utgående post.  

### <a name="example"></a>Eksempel  
Tabellen nedenfor viser vareutligningsposten som opprettes når du bokfører et kjøpsmottak av 10 enheter.  

|Bokføringsdato|Inngående vareløpenr.|Utgående vareløpenr.|Antall|Varepostnr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01.01.20|1|0|10|1|  

## <a name="inventory-decrease"></a>Lagerreduksjon  
Når du bokfører en lagerreduksjon, opprettes en vareutligningspost som knytter lagerreduksjonen til en lagerøkning. Denne koblingen opprettes ved hjelp av varens lagermetode som en retningslinje. Koblingen er basert på prinsippet om først-inn-først-ut for varer som bruker lagermetodene FIFO, Standard og Gjennomsnitt. Lagerreduksjonen utlignes mot lagerøkningen med den tidligste bokføringsdatoen. Koblingen er basert på prinsippet om sist-inn-først-ut for varer som bruker LIFO-lagermetoden. Lagerreduksjonen utlignes mot lagerøkningen med den seneste bokføringsdatoen.  

I **Varepost**-tabellen viser **Restantall**-feltet antallet som ennå ikke er utlignet. Hvis det restantallet er større enn 0, vil det være merket av for **Åpne**.  

### <a name="example"></a>Eksempel  
Eksemplet nedenfor viser vareutligningsposten som opprettes når du bokfører en følgeseddel på 5 enheter for varene som ble mottatt i det forrige eksemplet. Den første vareutligningsposten er kjøpsmottaket. Den andre utligningsposten er følgeseddelen.  

Tabellen nedenfor viser de to vareutligningspostene som er resultatet av henholdsvis lagerøkningen og lagerreduksjonen.  

|Bokføringsdato|Inngående vareløpenr.|Utgående vareløpenr.|Antall|Varepostnr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01.01.20|1|0|10|1|  
|03.01.20|1|2|-5|2|  

## <a name="fixed-application"></a>Fast utligning  
Du oppretter en fast utligning når du angir at kostbeløpet for en lagerøkning skal utlignes mot en bestemt lagerreduksjon, eller omvendt. Den faste utligningen påvirker restantallene for postene, men den faste utligningen tilbakefører også opprinnelig kostpris for den opprinnelige posten du utligner mot eller fra.  

Hvis du vil opprette en fast utligning, bruker du feltet **Utligningsvarepost** eller **Utlignet fra-varepost** på dokumentlinjene til å angi vareposten du vil at transaksjonen skal utlignes mot (eller fra). Du kan for eksempel opprette en fast utligning når du vil opprette en kostutligning som angir at en ordreretur skal utlignes mot en bestemt følgeseddel for å tilbakeføre kostbeløpet for følgeseddelen. I dette tilfellet ignorerer [!INCLUDE[prod_short](includes/prod_short.md)] lagermetoden og utligner lagerreduksjonen (eller lagerøkningen hvis det er snakk om en ordreretur) mot vareposten du angir. Fordelen med å opprette en fast utligning er at kostnadsbeløpet for den opprinnelige transaksjonen sendes til den nye transaksjonen.  

### <a name="example--fixed-application-in-purchase-return"></a>Eksempel – fast utligning i bestillingsretur  
Følgende eksempel, som illustrerer resultatet av fast utligning av en bestillingsretur for en vare som bruker lagermetoden FIFO, er basert på følgende scenario:  

1. Brukeren bokfører et kjøp med en kostnad på LV 10,00 i oppføring 1.  
2. Brukeren bokfører et kjøp med en kostnad på LV 20,00 i oppføring 2.  
3. I oppføring 3 bokfører brukeren en bestillingsretur. Brukeren foretar en fastsatt utligning mot det andre kjøpet ved å skrive inn varepostnummeret i feltet **Utligningsvarepost** på bestillingsreturlinjen.  

Tabellen nedenfor viser varepostene som er et resultat av scenariet.  

|**Bokføringsdato**|**Vareposttype**|**Antall**|**Kostbeløp (faktisk)**|**Varepostnr.**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|04.01.20|Kjøp|10|10.00|1|  
|05.01.20|Kjøp|10|20.00|2|  
|06.01.20|Kjøp (retur)|-10|-20,00|3|  

Fordi en fastsatt utligning skjer fra bestillingsretur til den andre kjøpsposten, returneres varene med riktig kost. Hvis brukeren ikke hadde utført den faste utligningen, ville den returnerte varen ha feilverdien LV 10,00, fordi avkastningen ville bli brukt på den første kjøpsposten i henhold til FIFO-prinsippet.  

Tabellen nedenfor viser vareutligningsposten som blir resultatet av den faste utligningen.  

|Bokføringsdato|Inngående vareløpenr.|Utgående vareløpenr.|Antall|Varepostnr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|06.01.20|2|3|10|3|  

Kostbeløpet for det andre kjøpet, LV 20,00, blir deretter korrekt sendt til bestillingsreturen.  

### <a name="example--fixed-application-with-average-cost"></a>Eksempel – fast utligning med gjennomsnittskost  
Følgende eksempel, som illustrerer resultatet av fast utligning, er basert på følgende scenario for en vare som bruker lagermetoden Gjennomsnitt:  

1. I løpenummer 1 og 2 legger brukeren inn to kjøpsfakturaer. Den andre fakturaen har en direkte enhetskost på LV 1 000,00, som er feil.  
2. I løpenummer 3 legger brukeren inn en kjøpskreditnota med en fast utligning for kjøpsposten med feil direkte enhetskost. Summen i feltet **Kostbeløp (faktisk)** for de to fast utlignede verdipostene blir 0,00.  
3. I løpenummer 4 legger brukeren inn en annen kjøpsfaktura med den riktige direkte enhetskosten LV 100,00  
4. I løpenummer 5 bokfører brukeren en salgsfaktura.  
5. Lagerantallet er 0, og lagerverdien er også 0,00.  

Følgende tabell viser resultatet av scenariet i varens verdiposter.  

Følgende tabell viser resultatet av scenarioet for varens verdiposter etter at bokføringen er fullført og kostnadsjustering er kjørt.

|Bokføringsdato|Vareposttype|Verdisatt antall|Kostbeløp (faktisk)|Utligningsvarepost|Valuert av gj.sn.kost|Varepostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01.01.20|Kjøp|1|200.00||Nei|1|1|  
|01.01.20|Kjøp|1|1000.00||Nei|2|2|  
|01.01.20|Kjøp|-1|-1000|2|Nei|3|3|  
|01.01.20|Kjøp|1|100,00||Nei|4|4|  
|01.01.20|Salg|-2|-300,00||Ja|5|5|  

Hvis brukeren ikke hadde ikke gjort fast utligning mellom kjøpskreditnotaen og kjøp med feil direkte enhetskost (trinn 2 i det forrige scenariet), må kostnadene justeres på en annen måte.  

Følgende tabell viser resultatet i varens verdiposter hvis trinn 2 i forrige scenario utføres uten en fastsatt utligning.  

|Bokføringsdato|Vareposttype|Verdisatt antall|Kostbeløp (faktisk)|Utligningsvarepost|Valuert av gj.sn.kost|Varepostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01.01.20|Kjøp|1|200.00||Nei|1|1|  
|01.01.20|Kjøp|1|1000.00||Nei|2|2|  
|01.01.20|Kjøp|-1|433,33||Ja|3|3|  
|01.01.20|Kjøp|1|100,00||Nei|4|4|  
|01.01.20|Salg|-2|866,67||Ja|5|5|  

I løpenummer 3 verdisettes feltet **Kostbeløp (faktisk)** etter gjennomsnittsverdi, og det inneholder derfor den feile bokføringen 1000,00. Derfor blir det - 433,33, som er et høyt kostbeløp. Beregningen er 1300 / 3 = .-433,33.  

I løpenummer 5 er verdien av feltet **Kostbeløp (faktisk)** for denne posten også unøyaktig av samme årsak.  

> [!NOTE]  
>  Hvis du oppretter en fast utligning for en lagerreduksjon for en vare som bruker lagermetoden Gjennomsnitt, mottar ikke reduksjonen gjennomsnittskostbeløpet for varen som vanlig, men mottar i stedet kostbeløpet for lagerøkningen du angir. Lagerreduksjonen er ikke da lenger en del av gjennomsnittskostberegningen.  

### <a name="example--fixed-application-in-sales-return"></a>Eksempel – fast utligning i ordreretur  
Faste utligninger er også en svært god metode for kosttilbakeføring, for eksempel som i ordrereturer.  

Følgende eksempel, som illustrerer hvordan en fast utligning sikrer opprinnelig kostpris, er basert på følgende scenario:  

1.  Du bokfører en kjøpsfaktura.  
2.  Brukeren bokfører en salgsfaktura.  
3.  Brukeren bokfører en salgskreditnota for den returnerte varen, som utlignes mot salgsposten, for å tilbakeføre kosten riktig.  
4.  Det kommer fraktkostnader som er knyttet til bestillingen som ble postert tidligere. Brukeren bokfører det som et varegebyr.  

Følgende tabell viser resultatet av scenariets trinn 1 til og med 3 i varens verdiposter.  

|Bokføringsdato|Vareposttype|Verdisatt antall|Kostbeløp (faktisk)|Utlignet fra-varepost|Varepostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01.01.20|Kjøp|1|1000.00||1|1|  
|01.02.20|Salg|-1|1000.00||2|2|  
|01.03.20|Salg (kreditnota)|1|1000|2|3|3|  

Tabellen nedenfor viser verdiposten som er et resultat av trinn 4 i scenariet, bokføring av varegebyret.  

|Bokføringsdato|Vareposttype|Verdisatt antall|Kostbeløp (faktisk)|Utlignet fra-varepost|Varepostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01.04.20|(Varegebyr)|1|100.00||1|4|  

Følgende tabell viser resultatet av nøyaktig tilbakeføring av kostnad i varens verdiposter.  

|Bokføringsdato|Vareposttype|Verdisatt antall|Kostbeløp (faktisk)|Utlignet fra-varepost|Varepostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01.01.20|Kjøp|1|1000.00||1|1|  
|01.02.20|Salg|-1|1100.00||2|2|  
|01.03.20|Salg (kreditnota)|1|1100.00|2|3|3|  
|01.04.20|(Varegebyr)|1|100.00||1|4|  

Når du kjører kjørselen **Juster kostverdi - vareposter**, økes kostnaden for kjøpsposten på grunn av varegebyret, og den økte kostnaden videresendes til salgsposten (postnummer 2). Salgsposten videresender deretter denne økte kostnaden til salgskreditposten (post nummer 3). Sluttresultatet er at kostnaden er riktig tilbakeført.  

> [!NOTE]  
>  Hvis du arbeider med returer eller kreditnotaer og har definert feltet **Bruk opprinnelig kostpris** enten på siden **Kjøpsoppsett** eller siden **Salgsoppsett**, avhengig av hva som er aktuelt i din situasjon, fyller [!INCLUDE[prod_short](includes/prod_short.md)] automatisk ut disse feltene når du bruker funksjonen **Kopier fra dokument**. Hvis du bruker funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres**, fylles feltene alltid ut automatisk.  

> [!NOTE]  
>  Hvis du bokfører en transaksjon med en fast utligning, og vareposten som du utligner mot, er lukket, som betyr at restantallet er null, angres den gamle utligningen automatisk, og vareposten utlignes på nytt ved hjelp av den faste utligningen du angav.  

## <a name="transfer-application"></a>Overføringsutligning  
Når en vare overføres fra én lokasjon til en annen i selskapets lager, opprettes en utligning mellom de to overføringspostene. Verdisettingen av en overføringspost avhenger av lagermetoden. Verdisetting utføres ved hjelp av gjennomsnittskost i gjennomsnittskostperioden der oppstår verdisettingsdatoen for overføringen finnes, for varer som bruker lagermetoden Gjennomsnitt. Verdisetting utføres ved sporing tilbake til kostnadene for den opprinnelige lagerøkningen for varer som bruker andre lagermetoder.  

### <a name="example--average-costing-method"></a>Eksempel – lagermetoden Gjennomsnitt  
Følgende eksempel, som illustrerer hvordan overføringsposter utlignes, er basert på følgende scenario for en vare som bruker lagermetoden Gjennomsnitt og gjennomsnittskostperioden Dag.  

1. Brukeren kjøper varen for LV 10,00.  
2. Brukeren kjøper varen på nytt for LV 20,00.  
3. Brukeren overfører varen fra ØST til VEST lokasjon.  

Følgende tabell viser resultatet av overføringen i varens verdiposter.  

|Bokføringsdato|Vareposttype|Lokasjonskode|Verdisatt antall|Kostbeløp (faktisk)|Løpenr.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01.01.20|Kjøp|ØST|1|10,00|1|  
|01.01.20|Kjøp|ØST|1|20,00|2|  
|01.02.20|Overfør|ØST|-1|15,00|3|  
|01.02.20|Overfør|VEST|1|15,00|4|  

### <a name="example--standard-costing-method"></a>Eksempel – lagermetoden Standard  
Følgende eksempel, som illustrerer hvordan overføringsposter utlignes, er basert på følgende scenario for en vare som bruker lagermetoden Standard og gjennomsnittskostperioden Dag.  

1. Brukeren kjøper varen for LV 10,00, som er standardkost.  
2. Brukeren overfører varen fra ØST til VEST lokasjon for en standardkost på LV 12,00.  

Følgende tabell viser resultatet av overføringen i varens verdiposter.  

|Bokføringsdato|Vareposttype|Lokasjonskode|Verdisatt antall|Kostbeløp (faktisk)|Løpenr.|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01.01.20|Kjøp|ØST|1|10,00|1|  
|01.02.20|Overfør|ØST|-1|10,00|2|  
|01.02.20|Overfør|VEST|1|10,00|3|  

Siden verdien til den opprinnelige lagerøkningen er LV 10,00, får overføringen denne verdien, ikke LV 12,00.  

## <a name="reapplication"></a>Utligne på nytt  
På grunn av måten som enhetskostbeløpet for en vare beregnes på, kan en feil vareutligning føre til en skjev gjennomsnittskost og enhetskost. Følgende scenarier kan føre til uriktige vareutligninger, som krever at du angrer vareutligninger og utligner vareposter på nytt:  

* Du har glemt å opprette en fast utligning.  
* Du har opprettet en feil fast utligning.  
* Du vil overstyre utligningen som opprettes automatisk når du bokfører, i samsvar med lagermetoden for varen.  
* Du må returnere en vare som et salg allerede er manuelt utlignet mot, uten å bruke funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres**, og du må derfor angre utligningen.  

[!INCLUDE[prod_short](includes/prod_short.md)] har en funksjon for analyse og korrigering av vareutligninger. Dette arbeidet utføres på siden **Utligningsforslag**.  

## <a name="see-also"></a>Se også  
[Designdetaljer: Kjent vareutligningsproblem](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Kostmetoder](design-details-costing-methods.md)  
[Designdetaljer: Gjennomsnittskost](design-details-average-cost.md)   
[Designdetaljer: Kostjustering](design-details-cost-adjustment.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]