---
title: Definere hvordan data utveksles elektronisk | Microsoft-dokumentasjon
description: Du kan bruke en ekstern leverandør av OCR-tjenester for å konvertere PDF- eller bildefiler til elektroniske dokumenter.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 11/26/2018
ms.author: sgroespe
ms.openlocfilehash: 0a8172f0c8770235291e7b9a29663f15932f38b4
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2019
ms.locfileid: "803308"
---
# <a name="set-up-data-exchange-definitions"></a>Definere datautvekslingsdefinisjoner
Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til å utveksle data i bestemte tabeller med data i eksterne filer, for eksempel for å sende og motta elektroniske dokumenter, importere og eksportere bankdata eller andre data, for eksempel lønn, valutakurser og elementkataloger. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).  

Som forberedelse til å opprette en datautvekslingsdefinisjon for en datafil eller -strøm, kan du bruke det tilknyttede XML-skjemaet til å definere hvilke dataelementer skal tas med i hurtigfanen **Kolonnedefinisjoner**. Se trinn 6 under Slik beskriver du formateringen av linjer og kolonner i filen. Hvis du vil ha mer informasjon, kan du se [Bruke XML-skjemaer til å forberede datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Vanligvis setter du opp datautvekslingsdefinisjoner på siden **Datautvekslingsdefinisjon**. Men når du setter opp en datautvekslingsdefinisjon for å oppdatere valutakurser, starter du prosessen på den forenklede siden **Kort for oppsett for val.kursoppdatering**.  

> [!NOTE]  
>  Hvis filen som konverteres, er i XML-format, skal begrepet *kolonne* i dette emnet tolkes som *et XML-element som inneholder data*.  

Dette emnet inneholder følgende fremgangsmåter:  

* Slik oppretter du en datautvekslingsdefinisjon:  
* Slik eksporterer en datautvekslingsdefinisjon som en XML-fil som andre kan bruke:  
* Slik importerer du en XML-fil for en eksisterende datautvekslingsdefinisjon:  

## <a name="to-create-a-data-exchange-definition"></a>Slik oppretter du en datautvekslingsdefinisjon:  
Oppretting av en datautvekslingsdefinisjon omfatter to oppgaver:  

1. På siden **Datautvekslingsdefinisjon** beskriver du formateringen for linjer og kolonner i filen.  
2. På siden **Tilordning for datautveksling** tilordner du kolonner i datafilen til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

     Dette er beskrevet i følgende fremgangsmåter.  

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Slik beskriver du formateringen av linjer og kolonner i filen:  
1. Skriv inn **Datautvekslingsdefinisjoner** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
2. Velg handlingen **Ny**.  
3. I hurtigfanen **Generelt** beskriver du datautvekslingsdefinisjonen og datafiltypen ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Definisjon|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Skriv inn en kode for å identifisere datautvekslingsdefinisjonen.|  
    |**Navn**|Angi et navn for datautvekslingsdefinisjonen.|  
    |**Filtype**|Angi hvilken type fil datautvekslingsdefinisjonen brukes til. Du kan velge mellom fire filtyper:<br /><br /> -   **XML**: lagdelte strenger med innhold og kode omgitt av koder som angir funksjon.<br />-   **Variabel tekst**: Poster har variabel lengde og er atskilt med et tegn, for eksempel komma eller semi\-kolon. Kalles også *kommadelt fil*.<br />-   **Fast tekst**: Poster har samme lengde ved hjelp av utfyllingstegn, og hver post er på en separat linje. Kalles også *fil med fast bredde*.<br />- **Json**: Lagvise strenger med innhold i JavaScript.|  
    |**Type**|Angi hvilken type forretningsvirksomhet datautvekslingsdefinisjonen brukes til, for eksempel **betalingseksport**.|  
    |**Kodeenhet for datahåndtering**|Angi kodeenheten som overfører data inn i og ut av tabeller i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Kodeenhet for validering**|Angi kodeenheten som brukes til å validere data mot forhåndsdefinerte forretningsregler.|  
    |**Kodeenhet for lesing/skriving**|Angi kodeenheten som behandler importerte data før tilordning og eksporterte data etter tilordning.|  
    |**XMLport for lesing/skriving**|Angir XMLport som en importert datafil eller tjeneste overføres via før tilordning, og som eksporterte data overføres via når de skrives til en datafil eller tjeneste etter tilordning.|  
    |**Kodeenhet for ekstern datahåndtering**|Angi kodeenheten som overfører eksterne data inn i og ut av rammeverket for datautveksling.|  
    |**Kodeenhet for brukertilbakemelding**|Angi kodeenheten som inneholder ulike oppryddinger etter tilordning, for eksempel markerer linjene som eksporteres og sletter midlertidige poster.|  
    |**Filkoding**|Angi kodingen for filen. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Kolonneskilletegn**|Angi hvordan kolonner skilles i datafilen, hvis filen er av typen **Variabel tekst**.|  
    |**Topptekstlinjer**|Angi hvor mange topptekstlinjer det er i filen.<br /><br /> Dette sikrer at topptekstdataene ikke importeres. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Topptekstkode**|Hvis det finnes en topptekst på flere steder i filen, kan du angi teksten i den første kolonnen på topptekstlinjen.<br /><br /> Dette sikrer at topptekstdataene ikke importeres. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Bunntekstkode**|Hvis det finnes en bunntekst på flere steder i filen, kan du angi teksten i den første kolonnen på bunntekstlinjen.<br /><br /> Dette sikrer at bunntekstdataene ikke importeres. **Obs!**  Dette feltet er bare relevant for import.|  

4. I hurtigfanen **Linjedefinisjoner** beskriver du formateringen av linjer i datafilen ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    > [!NOTE]  
    >  For import av bankkontoutdrag kan du bare opprette én linje for enkeltformatet til bankkontoutdragsfilen som du vil importere.  
    >   
    >  For eksport av betalinger kan du opprette en linje for hver betaling du vil eksportere. I slike tilfeller viser hurtigfanen **Kolonnedefinisjoner** forskjellige kolonner for hver betalingstype.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angi en kode som identifiserer linjen i filen.|  
    |**Navn**|Angi et navn som beskriver linjen i filen.|  
    |**Antall kolonner**|Angi hvor mange kolonner det er på linjen i datafilen. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Datalinjemerke**|Angi posisjonen til elementet som representerer hovedposten i datafilen, i det tilknyttede XML-skjemaet. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Navneområde**|Angi navneområdet som forventes i filen, for å aktivere validering av navneområde. Du kan la dette feltet stå tomt hvis du ikke vil aktivere validering av navneområde.|  

5. Gjenta trinn 4 for å opprette en linje for hver fildatatype du vil eksportere.  

     Fortsett med å beskrive formateringen av kolonner i datafilen ved å fylle ut feltene i hurtigfanen **Kolonnedefinisjoner** som beskrevet i tabellen nedenfor. Du kan bruke filstrukturen, for eksempel en XSD-fil, for datafilen til å forhåndsutfylle hurtigfanen med de aktuelle elementene. Hvis du vil ha mer informasjon, kan du se [Bruke XML-skjemaer til å forberede datautvekslingsdefinisjoner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. I hurtigfanen **Kolonnedefinisjoner** velger du **Hent filstruktur**.  
7. På siden **Hent filstruktur** velger du den relaterte strukturfilen og velger deretter **OK**-knappen. Linjene i hurtigfanen **Kolonnedefinisjoner** fylles ut i henhold til strukturen til datafilen.  
8. I hurtigfanen **Kolonnedefinisjoner** redigerer eller fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angi tallet som gjenspeiler kolonneposisjonen på linjen i filen.<br /><br /> For XML-filer angir du tallet som gjenspeiler elementtype i filen som inneholder dataene.|  
    |**Navn**|Angi navnet på kolonnen.<br /><br /> For XML-filer kan du angi markeringen som merker dataene som skal utveksles.|  
    |**Datatype**|Angi om dataene som skal utveksles, er av typen **Tekst**, **Dato** eller **Desimal**.|  
    |**Dataformat**|Angi det eventuelle dataformatet. Eksempel: **dd.MM.åååå** hvis datatypen er **Dato**. **Obs!**  For eksport angir du dataformatet i henhold til [!INCLUDE[d365fin](includes/d365fin_md.md)]. For import angir du dataformatet i henhold til .NET Framework. Hvis du vil ha mer informasjon, kan du se [Standard formatstrenger for dato og klokkeslett](https://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Dataformateringskultur**|Angi den eventuelle kulturen for dataformatet. For eksempel **en-US** hvis datatypen er **Desimal**, for å sikre at komma brukes som skilletegn for .000, i henhold til formatet for USA. Hvis du vil ha mer informasjon, kan du se [Standard formatstrenger for dato og klokkeslett](https://go.microsoft.com/fwlink/?LinkID=323466). **Obs!**  Dette feltet er bare relevant for import.|  
    |**Lengde**|Angi lengden på linjen med fast bredde som inneholder kolonnen, hvis datafilen er av typen **Fast tekst**.|  
    |**Beskrivelse**|Angi en beskrivelse for kolonnen for informasjon.|  
    |**Bane**|Angi posisjonen til elementet i det tilknyttede XML-skjemaet.|  
    |**Identifikator for minustegn**|Angi verdien som brukes i datafilen til å identifisere negative beløp i datafiler som ikke kan inneholde negative fortegn. Denne identifikatoren brukes deretter til å gi de identifiserte beløpene negative fortegn under import. **Obs!**  Dette feltet er bare relevant for import.|  
    |**Konstant**|Angi data du vil eksportere i denne kolonnen, for eksempel tilleggsinformasjon om betalingstypen. **Obs!**  Dette feltet er bare relevant for eksport.|  

9. Gjenta trinn 8 for hvert kolonne- eller XML-element i datafilen som har data du vil utveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Det neste trinnet i å opprette en datautvekslingsdefinisjon er å bestemme hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]som kolonner eller XML-elementer i datafilen skal tilordnes til.  

> [!NOTE]  
>  Den bestemte tilordningen avhenger av forretningsformålet med datafilen som skal utveksles, og av lokale variasjoner. Selv SEPA-bankstandarden har lokale variasjoner. [!INCLUDE[d365fin](includes/d365fin_md.md)] støtter import av SEPA CAMT-bankkontoutdragsfiler \-\-\-. Dette er angitt med **SEPA CAMT**-postkoden for datautvekslingsdefinisjon på siden **Datautvekslingsdefinisjoner**. For informasjon om spesifikk felttilordning av SEPA CAMT-støtten kan du se [Felttilordning ved import av SEPA CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Slik tilordner du kolonner i datafilen til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. I hurtigfanen **Linjedefinisjoner** velger du linjen for tilordning av kolonner til felt, og deretter velger du **Felttilordning**. Siden **Tilordning for datautveksling** åpnes.  
2. I hurtigfanen **Generelt** angir du tilordningsoppsettet ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Tabell-ID**|Angi tabellen som inneholder feltene som data utveksles til eller fra i samsvar med tilordningen.|  
    |**Bruk som foreløpig tabell**|Angi om tabellen du velger i feltet **Tabell-ID**, er en foreløpig tabell der de importerte dataene lagres før de tilordnes til måltabellen.<br /><br /> Du bruker vanligvis en midlertidig tabell når datautvekslingsdefinisjonen brukes til å importere og konvertere elektroniske dokumenter, for eksempel leverandørfakturaer til kjøpsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).|  
    |**Navn**|Angi et navn for tilordningsoppsettet.|  
    |**Kodeenhet for forhåndstilordning**|Angi kodeenheten som klargjør tilordningen mellom felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne data.|  
    |**Kodeenhet for tilordning**|Angi kodeenheten som brukes til å tilordne de angitte kolonnene eller XML-dataelementene til felt i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Kodeenhet for ettertilordning**|Angi kodeenheten som fullfører tilordningen mellom felt i [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne data. **Obs!**  Når tjenesten for bankdatakonvertering brukes, konverterer kodeenheten eksporterte data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til et generelt format som er klart til eksport. For import konverterer kodeenheten eksterne data til et format som er klar for import til [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  I hurtigfanen **Felttilordning** angir du hvilke kolonner som er tilordnet hvilke felt i [!INCLUDE[d365fin](includes/d365fin_md.md)], ved å fylle ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angi hvilken kolonne i datafilen du vil definere en tilordning for.<br /><br /> Du kan bare velge kolonner som vises som linjer i hurtigfanen **Kolonnedefinisjoner** på siden **Datautvekslingsdefinisjon**.|  
    |**Felt-ID**|Angi hvilket felt kolonnen i feltet **Kolonnenr.** er tilordnet.<br /><br /> Du kan bare velge blant felt som finnes i tabellen du har angitt i **Tabell**-feltet i hurtigfanen **Generelt**.|  
    |**Valgfritt**|Angi at tilordningen hoppes over hvis feltet er tomt. **Obs!**  Hvis du ikke merker av for alternativet, vil det oppstå en eksportfeil hvis feltet er tomt. **Obs!**  Dette feltet er bare relevant for eksport.|  
    |**Måltabell-ID**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angirtabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Måltabelloverskrift**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi navnet på tabellen i feltet **Måltabell-ID**, som er tabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Målfelt-ID**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi feltet i måltabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Målfelttekst**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi navnet på feltet i måltabellen som verdien i feltet **Kolonneoverskrift** blir tilordnet til når du bruker en foreløpig tabell for dataimport.|  
    |**Valgfritt**|Synlig bare når det er merket av for **Bruk som foreløpig tabell**.<br /><br /> Angi om tilordningen skal hoppes over hvis feltet er tomt. Hvis du ikke merker av for alternativet, vil det oppstå en eksportfeil hvis feltet er tomt.|  

Datautvekslingsdefinisjonen er nå klar til å aktiveres for brukere. Hvis du vil ha mer informasjon, kan du se [Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Definere SEPA-kredittoverføring](finance-how-to-set-up-sepa-credit-transfer.md), [Definere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md) og [Betale med tjenesten for bankdatakonvertering eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

Når du har opprettet datautvekslingsdefinisjonen for en bestemt datafil, kan du eksportere datautvekslingsdefinisjonen som en XML-fil som kan brukes til å aktivere import av den aktuelle datafilen raskt. Dette er beskrevet i følgende fremgangsmåte.  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Slik eksporterer en datautvekslingsdefinisjon som en XML-fil som andre kan bruke:  
1. Skriv inn **Datautvekslingsdefinisjoner** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
2. Velg datautvekslingsdefinisjonen du vil eksportere.  
3. Velg **Eksporter datautvekslingsdefinisjon**.  
4. Lagre XML-filen som representerer datautvekslingsdefinisjonen, på en passende plassering.  

    Hvis en datautvekslingsdefinisjon allerede er opprettet, trenger du bare å importere XML-filen til rammeverket for datautveksling. Dette er beskrevet i følgende fremgangsmåte.  

### <a name="to-import-an-existing-data-exchange-definition"></a>Slik importerer du en eksisterende datautvekslingsdefinisjon:  
1. Lagre XML-filen som representerer datautvekslingsdefinisjonen, på en passende plassering.  
2. Skriv inn **Datautvekslingsdefinisjoner** i **Søk**-boksen, og velg deretter den tilknyttede koblingen.  
3. Velg handlingen **Ny**. Siden **Datautvekslingdefinisjon** åpnes.  
4. Velg **Importer datautvekslingsdefinisjon**.  
5. Velg filen du lagret i trinn 1.  

## <a name="see-also"></a>Se også  
[Definere datautveksling](across-set-up-data-exchange.md)  
[Konfigurere sending og mottak av elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Definere SEPA-kredittoverføring](finance-how-to-set-up-sepa-credit-transfer.md)  
[Definere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)  
[Betale med tjenesten for bankdatakonvertering eller SEPA-kredittoverføring](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inngående dokumenter](across-income-documents.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)  
