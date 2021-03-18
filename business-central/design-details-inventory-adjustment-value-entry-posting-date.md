---
title: Bokføringsdato på verdiposter
description: Lær hvordan kjørselen Juster kostverdi - vareposter identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: fd8ac52ae5a35114adc2e06ad8653799f7557123
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5389952"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Designdetaljer: Bokføringsdato på verdiposten for justering
Denne artikkelen gir en beskrivelse av funksjonen for kostberegning av beholdning i [!INCLUDE[prod_short](includes/prod_short.md)]. Denne artikkelen beskriver hvordan kjørselen **Juster kostverdi - vareposter** identifiserer og tilordner en bokføringsdato til verdipostene som kjørselen skal opprette.  

Først gjennomgås begrepet om prosessen, hvordan kjørselen identifiserer og tilordner bokføringsdatoen til verdiposten som skal opprettes. Deretter formidler vi noen scenarier som vi i støtteteamet møter på med jevne mellomrom, og til slutt er det en oppsummering av begrepene fra versjon 3.0.  

## <a name="the-concept"></a>Begrepet  
Fra versjon 5.0, **Juster kostverdi - vareposter**-kjørselen tilordner en bokføringsdato til verdiposten den skal opprette, på følgende måte:  

1.  Først er bokføringsdatoen for posten som skal opprettes, samme dato som posten den justerer  

2.  Bokføringsdatoen valideres mot lagerperioder og/eller finansoppsett.  

3.  Tilordning av bokføringsdato: Hvis opprinnelig bokføringsdato ikke er innenfor tillatt datointervall for bokføring, tilordner kjørselen en tillatt bokføringsdato fra finansoppsett eller lagerperiode. Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, tilordnes den seneste datoen av de to til verdiposten for justering.  

 La oss se på prosessen ved hjelp av et praktisk eksempel. Anta at vi har en varepost for salg. Varen ble levert 5. september 2013, og den ble fakturert dagen etter.  

![Status for vareposter i scenariet](media/helene/TechArticleAdjustcost1.png "Status for vareposter i scenariet")  

Den første verdiposten (379) nedenfor representerer leveringen og har samme bokføringsdato som den overordnede vareposten.  

Den andre verdiposten (381) representerer fakturaen.  

 Den tredje verdiposten (391) er en justering av faktureringsverdiposten (381)  

 ![Status for verdiposter i scenariet](media/helene/TechArticleAdjustcost2.png "Status for verdiposter i scenariet")  

 Trinn 1: Verdiposten for justering som skal opprettes, tildeles samme bokføringsdato som posten den justerer, som vist ovenfor ved verdipost 391.  

 Trinn 2: Validering av opprinnelig tilordnet bokføringsdato.  

**Juster kostverdi - vareposter**-kjørselen bestemmer om den første bokføringsdatoen for verdiposten for justering er innenfor tillatt datointervall for bokføring basert på lagerperioder og/eller finansoppsett.  

 La oss gå gjennom salget som er angitt ovenfor, ved å legge til oppsett for tillatt bokføringsdatointervall.  

 Lagerperioder:  

![Lagerperioder i scenariet](media/helene/TechArticleAdjustcost3.png "Lagerperioder i scenariet")

 Den første tillatte bokføringsdatoen er den første dagen i den første åpne perioden. 1. september 2013.  

 Finansoppsett:  

![Finansoppsett i scenariet](media/helene/TechArticleAdjustcost4.png "Finansoppsett i scenariet")

 Første tillatte bokføringsdato er datoen som er angitt i feltet Bokf. tillatt fra: 10. september 2013.  

 Hvis både lagerperioder og tillatte bokføringsdatoer i finansoppsett er definert, definerer den seneste datoen av de to det tillatte bokføringsdatointervallet.  

 Trinn 3: Tilordning av en tillatt bokføringsdato.  

 Første tilordnede bokføringsdato var 6. september, som vist i trinn 1. Men i det andre trinnet identifiserer kjørselen Juster kostverdi – vareposter at den tidligste tillatte bokføringsdatoen er 10. september, og dermed tilordnes 10. september til verdiposten for justeringsposten nedenfor.  

 ![Status for verdiposter i scenariet 2](media/helene/TechArticleAdjustcost5.png "Status for verdiposter i scenariet 2")

 Vi har nå sett på begrepet om å tilordne bokføringsdatoer til verdiposter som opprettes av kjørselen Juster kostverdi - vareposter.  

 La oss fortsette å se på noen scenarioer som vi i støtteteamet møter på fra tid til annen knyttet til tilordnede bokføringsdatoer i kjørselen Juster kostverdi – vareposter og relaterte oppsett.  

## <a name="scenarios"></a>Scenarier  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenario I: Bokføringsdatoen er ikke innenfor tillatte bokføringsdatoer ...  
 Dette er en situasjon der en bruker får denne feilmeldingen når kjørselen Juster kostverdi - vareposter er kjørt.  

 I forrige del der vi beskrev begrepet om tilordning av bokføringsdatoer, var kjørselen Juster kostverdi - vareposter ment å opprette en verdipost med bokføringsdato 10. september.  

![Feilmelding om bokføringsdato](media/helene/TechArticleAdjustcost6.png "Feilmelding om bokføringsdato")

 Vi følge opp med brukeroppsettet:  

![Oppsett av brukerens tillatte bokføringsdatoer](media/helene/TechArticleAdjustcost7.png "Oppsett av brukerens tillatte bokføringsdatoer")

 Brukeren i dette tilfellet har et tillatt bokføringstidsrom fra 11. september til 30. september, og kan dermed ikke bokføre justeringsverdiposten med bokføringsdato 10. september.  

![Oversikt over involvert oppsett for bokføringsdato](media/helene/TechArticleAdjustcost8.png "Oversikt over involvert oppsett for bokføringsdato")

 Kunnskapsbaseartikkel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) beskriver flere scenarioer knyttet til den nevnte feilmeldingen.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenario II: Bokføringsdato på verdipost for justering kontra bokføringsdato på post som forårsaker justeringen, for eksempel revaluering eller varegebyr.  

### <a name="revaluation-scenario"></a>Revalueringsscenario:  
 Forutsetninger:  

 Lageroppsett:  

-   Automatisk kostbokføring = Ja  

-   Automatisk kostjustering = Alltid  

-   Beregn.type for gj.snittskost = vare  

-   Gjennomsnittskostperiode = Dag  

 Finansoppsett:  

-   Bokf. tillatt fra = 1. januar 2014  

-   Bokf. tillatt til = tom  

 Brukeroppsett:  

-   Bokf. tillatt fra = 1. desember 2013.  

-   Bokf. tillatt til = tom  

##### <a name="to-test-the-scenario"></a>Slik tester du scenarioet:  

1.  Opprett varen TEST:  

     Lagerenhet = STK  

     Lagermetode = Gjennomsnitt  

     Velg valgfrie bokføringsgrupper.  

2.  Åpne varekladden, og opprett og bokfør en linje på følgende måte:  

     Bokføringsdato = 15. desember 2013  

     Vare = TEST  

     Posttype = Kjøp  

     Antall = 100  

     Enhetsbeløp = 10  

3.  Åpne varekladden, og opprett og bokfør en linje på følgende måte:  

     Dato = 20. desember 2013  

     Vare = TEST  

     Posttype = Nedjustering  

     Antall = 2  

4.  Åpne varekladden, og opprett og bokfør en linje på følgende måte:  

     Dato = 15. januar 2014  

     Vare = TEST  

     Posttype = Nedjustering  

     Antall = 3  

5.  Åpne revalueringskladden, og opprett og bokfør en linje på følgende måte:  

     Vare = TEST  

     Utligningspost = velg kjøpspost bokført i trinn 2. Bokføringsdatoen for revalueringen blir lik posten den justerer.  

     Enhetskost (revaluert) = 40  

 Følgende vareposter og verdiposter er bokført:  

![Oversikt over resulterende finans- og vareposter 1](media/helene/TechArticleAdjustcost9.png "Oversikt over resulterende finans- og vareposter 1")

 ![Oversikt over resulterende finans- og vareposter 2](media/helene/TechArticleAdjustcost10.png "Oversikt over resulterende finans- og vareposter 2")

 Juster kostverdi – vareposter-kjørselen har gjenkjent en endring i kost og justert nedjusteringene.  

 **Gjennomgang av bokføringsdatoer på opprettede verdiposter for justering:** Den tidligste tillatte bokføringsdatoen som kjørselen Juster kostverdi - vareposter må relateres til, er 1. januar 2014, som angitt i Finansoppsett.  

 **Nedjustering i trinn 3:** Tilordnet bokføringsdato er 1. januar, angitt i finansoppsettet. Bokføringsdatoen for verdiposten i området for justering er 20. desember 2013. I henhold til Finansoppsett er ikke datoen innenfor det tillatte datointervallet for bokføring. Derfor tilordnes bokføringsdatoen som er angitt i feltet Bokf. tillatt fra i finansoppsettet, til verdiposten for justering.  

 **Nedjustering i trinn 4:** Tilordnet bokføringsdato er 15. januar. Verdiposten i området for justering har bokføringsdatoen 15. januar, som er innenfor det tillatte bokføringsdatointervallet i henhold til Finansoppsett.  

 Justeringen foretatt for nedjusteringen i trinn 3 fører til diskusjon. Den beste bokføringsdatoen for verdiposten for justering ville vært 20. desember 20 eller i det minste i desember siden revalueringen som forårsaker endringen i vareforbruk, ble bokført i desember.  

 For å oppnå justering i desember for nedjusteringen i trinn 3, må feltet Bokf. tillatt fra i Finansoppsett angi en dato i desember.  

 **Konklusjon:**  

 Med erfaringene fra dette scenarioet, når du skal vurdere det best egnede oppsettet for tillatt bokføringsdatointervall for et selskap, kan følgende være nyttig: Såfremt endringer i lagerverdien kan bokføres i en periode, desember i dette tilfellet, må oppsettet selskapet bruker for tillatt bokføringsdatoområde, justeres i henhold til denne beslutningen. Bokf. tillatt fra i finansoppsettet, som angir 1. desember, ville tillatt at revalueringen i desember kunne overføres til påvirkede utgående poster i samme periode.  

 Brukergrupper som ikke kan bokføre i desember, men i januar, som sannsynligvis var ment å være begrenset av finansoppsettet i dette scenarioet, bør i stedet løses via brukeroppsettet.  

### <a name="item-charge-scenario"></a>Varegebyrscenario:  
 Forutsetninger:  

 Lageroppsett:  

-   Automatisk kostbokføring = Ja  

-   Automatisk kostjustering = Alltid  

-   Beregn.type for gj.snittskost = vare  

-   Gjennomsnittskostperiode = Dag  

 Finansoppsett:  

-   Bokf. tillatt fra = 1. desember 2013.  

-   Bokf. tillatt til = tom  

 Brukeroppsett:  

-   Bokf. tillatt fra = 1. desember 2013.  

-   Bokf. tillatt til = tom  

##### <a name="to-test-the-scenario"></a>Slik tester du scenarioet:  

1.  Opprett varegebyr:  

     Lagerenhet = STK  

     Lagermetode = Gjennomsnitt  

     Velg valgfrie bokføringsgrupper.  

2.  Opprett ny bestilling  

     Kjøp fra-leverandørnr.: 10000  

     Bokføringsdato = 15. desember 2013  

     Leverandørs fakturanr.: 1234  

     På bestillingslinjen:  

     Vare = GEBYR  

     Antall = 1  

     Direkte enhetskost = 100  

     Bokfør mottak og faktura.  

3.  Opprett ny ordre:  

     Salg til-kundenr.: 10000  

     Bokføringsdato = 16. desember 2013  

     På ordrelinjen:  

     Vare = GEBYR  

     Antall = 1  

     Salgspris = 135  

     Bokfør levering og faktura.  

4.  Finansoppsett:  

     Bokf. tillatt fra = 1. januar 2014  

     Bokf. tillatt til = tom  

5.  Opprett ny bestilling:  

     Kjøp fra-leverandørnr.: 10000  

     Bokføringsdato = 2. januar 2014  

     Leverandørs fakturanr.: 2345  

     På bestillingslinjen:  

     Varegebyr = NC-FRAKT  

     Antall = 1  

     Direkte enhetskost = 3  

     Tilordne varegebyr til kjøpsmottak fra trinn 2.  

     Bokfør mottak og faktura.  

     ![Oversikt over resulterende finans- og vareposter 3](media/helene/TechArticleAdjustcost11.png "Oversikt over resulterende finans- og vareposter 3")

6.  På arbeidsdatoen 3. januar kommer en kjøpsfaktura som inneholder et ekstra varegebyr for kjøpet som ble gjort i trinn 2. Denne fakturaen har bilagsdato 30. desember, og bokføres derfor med bokføringsdatoen 30. desember 2013.  

     Opprett ny bestilling:  

     Kjøp fra-leverandørnr.: 10000  

     Bokføringsdato = 30. desember 2013  

     Leverandørs fakturanr.: 3456  

     På bestillingslinjen:  

     Varegebyr = NC-FRAKT  

     Antall = 1  

     Direkte enhetskost = 2  

     Tilordne varegebyr til kjøpsmottak fra trinn 2  

     Bokfør mottak og faktura.  

   ![Oversikt over resulterende finans- og vareposter 4](media/helene/TechArticleAdjustcost12.png "Oversikt over resulterende finans- og vareposter 4")

 Lagerverdisettingsrapporten skrives ut per 31. desember 2013  

![Innholdet i rapporten Lagerverdisetting](media/helene/TechArticleAdjustcost13.png "Innholdet i rapporten Lagerverdisetting")

 **Sammendrag av scenarioet:**  

 Det beskrevne scenarioet ender opp med en lagerverdisettingsrapport som viser antall = 0 når verdien = 2. Varegebyret som ble bokført i trinn 11, er del av lagerøkningsverdien i desember, mens lagerreduksjonen i samme periode påvirkes ikke.  

 At Finansoppsett angir Bokf. tillatt fra 1. januar var nyttig for det første varegebyret. Kostnadene ved lagerøkning og -reduksjon ble registrert i samme periode. For det andre varegebyret derimot, fører finansoppsettet til at endringen i vareforbruk føres på perioden etter.  

 **Konklusjon:**  

 Det er utfordrende å få lagerverdisettingsrapporten til å vise antall = 0 når verdien <> 0. I dette tilfellet er det også vanskeligere å uttrykke optimale innstillinger når du har kjøpsfakturaer som kommer på samme dag, men på forskjellige perioder eller regnskapsår. Kryssing til et nytt regnskapsår krever vanligvis noe planlegging, og som en del av innsikten fra Juster kostverdi - vareposter-prosessen må føring av vareforbruk vurderes.  

 I dette scenarioet kunne ett alternativ ha vært å angi en dato i desember for noen flere dager i feltet Bokf. tillatt fra i Finansoppsett, og utsette bokføringen av det første varegebyret, slik at alle kostnader for forrige periode/regnskapsår føres for perioden de tilhører først, og kjøre kjørselen Juster kostverdi - vareposter, og deretter flytte den tillatte bokføringsdatoen til den nye perioden\/regnskapsåret. Det første varegebyret med bokføringsdato 2. januar kunne deretter bli bokført.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historikk for kjørselen Juster kostverdi - vareposter  
 Nedenfor finner du et sammendrag av begrepet om tilordning av bokføringsdatoer til verdiposter for justering med kjørselen Juster kostverdi - vareposter siden versjon 3.0.  

### <a name="from-version-30370a"></a>Fra versjon 3.0..3.70.A  
 I forespørselsskjemaet for kjørselen Juster kostverdi - vareposter finnes det en bokføringsdato som skal angis av brukeren. Kjørselen kjører gjennom alle nødvendige endringer og oppretter verdiposter med bokføringsdatoen som er angitt i forespørselsskjemaet. Foreslått bokføringsdato som skal brukes, er dagens dato.  

### <a name="version-370b40"></a>Versjon 3.70.B..4.0  
 I forespørselsskjemaet for kjørselen Juster kostverdi - vareposter finnes det en lukket bokføringsdato for periodepost som skal angis av brukeren. Kjørselen kjører gjennom alle nødvendige endringer og oppretter verdiposter med bokføringsdatoen for den overordnede vareposten (leveringsdatoen for salget som justeringen adresserer). Hvis bokføringsdatoen for den overordnede vareposten ikke er innenfor tillatt bokføringsdatointervall, tilordnes bokføringsdatoen angitt som lukket bokføringsdato for periodepost til verdiposten for justering. En dato regnes å være i en lukket periode når den er før datoen i feltet Bokf. tillatt fra i finansoppsettet.  

### <a name="from-version-50"></a>Fra versjon 5.0:  
 Det finnes ikke lenger en bokføringsdato som skal angis i forespørselsskjemaet for kjørselen Juster kostverdi - vareposter. Kjørselen kjører gjennom alle nødvendige endringer og oppretter verdiposter med bokføringsdatoen for verdiposten den justerer. Hvis bokføringsdatoen ikke er innenfor tillatt datointervall for bokføring, brukes bokføringsdatoen i feltet Bokf. tillatt fra i finansoppsettet, eller hvis lagerperiodene brukes, brukes den seneste datoen av de to. Se beskrevet begrep ovenfor.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historikk for kjørselen Bokfør lagerkost i Finans  
 Kjørselen Bokfør lagerkost i Finans er nært knyttet til kjørselen Juster kostverdi – vareposter, og er grunnen til at denne kjørselen oppsummeres og formidles her også.  

### <a name="from-version-30370a"></a>Fra versjon 3.0..3.70.A  
 I forespørselsskjemaet for kjørselen Bokfør lagerkost i Finans finnes det en bokføringsdato som skal angis av brukeren. Kjørselen kjører gjennom alle eventuelle verdiposter i filteret og oppretter finansposter med bokføringsdatoen som er angitt i forespørselsskjemaet.  

### <a name="version-370b40"></a>Versjon 3.70.B..4.0  
 I forespørselsskjemaet for Bokfør lagerkost i Finans er feltet lukket bokføringsdato for periodepost tilgjengelig. Programmet bruker datoen du angir i dette feltet som bokføringsdato for finanspostene som det oppretter for verdiposter, som har bokføringsdatoer i lukkede regnskapsperioder. Ellers vil finanspostene ha samme bokføringsdato som de opprinnelige verdipostene. En dato regnes å være i en lukket periode når den er før datoen i feltet Bokf. tillatt fra i finansoppsettet. Hvis du bokfører til finans per bokføringsgruppe, må finanspostene ha bokføringsdatoen som er angitt i feltet Bokføringsdato i forespørselsskjemaet.  

 I versjon 3 og 4 søker kjørselen i alle verdiposter for å se om det finnes verdiposter der Kostbeløp (faktisk) er forskjellig fra Bokført kost. Hvis det er en differanse, bokføres beløpet i en finanspost. Hvis bokføring av forventede kostnader brukes, behandles tilsvarende felt på samme måte.  

![Faktiske kostnader og forventede kostnader](media/helene/TechArticleAdjustcost14.png "Faktiske kostnader og forventede kostnader")

### <a name="from-version-50"></a>Fra versjon 5.0:  
 Det finnes ikke lenger en bokføringsdato som skal angis i forespørselsskjemaet for kjørselen Bokfør lagerkost i Finans. Finansposten opprettes med samme bokføringsdato som den relaterte verdiposten. For å fullføre kjørselen må det tillatte bokføringsdatointervallet tillate bokføringsdatoen for den opprettede finansposten. Hvis ikke, må det tillatte bokføringsdatointervallet midlertidig åpnes på nytt ved å endre eller fjerne datoene i feltet Bokf. tillatt fra og Tillat bokf. til i Finansoppsett. For å unngå avstemmingsproblemer må bokføringsdato for finansposten svare til bokføringsdatoen for verdiposten.  

 Kjørselen søker gjennom tabell 5811 - Bokfør verdipost i Finans for å identifisere verdipostene innenfor området for bokføring i Finans. Tabellen tømmes når du har utført kjørselen.

## <a name="see-also"></a>Se også  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Vareutligning](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]