---
title: Designdetaljer – Kostjustering | Microsoft-dokumentasjon
description: Hovedformålet med kostjustering er å videresende kostnadsendringer fra kostnadskilder til kostnadsmottakere, i samsvar med lagermetoden for en vare, for å gi riktig lagerverdisetting.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 9b00ab8cd91b921a35c3228972e50e8933ed4ee5
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387002"
---
# <a name="design-details-cost-adjustment"></a>Designdetaljer: Kostjustering

Hovedformålet med kostjustering er å videresende kostnadsendringer fra kostnadskilder til kostnadsmottakere, i samsvar med lagermetoden for en vare, for å gi riktig lagerverdisetting.  

En vare kan være fakturert før den har blitt kjøpsfakturert, slik at den registrerte lagerverdien for salget ikke samsvarer med faktisk innkjøpskostnad. Kostjustering oppdaterer kostnadene for solgte varer (VAREFORBRUK) for historiske salgsposter, slik at de samsvarer med kostnadene for innkommende transaksjoner som de brukes for. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Vareutligning](design-details-item-application.md).  

Følgende er sekundære formål med, eller funksjoner i, kostjustering:  

* Fakturer ferdige produksjonsordrer:  

  * Endring av statusen for verdiposter fra **Forventet** til **Faktisk**.  
  * Fjern VIA-konti. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre produksjonsordre](design-details-production-order-posting.md).  
  * Bokføre avvik. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Avvik](design-details-variance.md).  
  * Oppdater enhetskosten på varekortet.  

Lagerkostnader må justeres før de tilknyttede verdipostene kan avstemmes med Finans. Hvis du vil ha mer informasjon, se [Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>Registrere justeringen

Oppgaven med å finne ut om kostjustering skal skje, utføres hovedsakelig av rutinen Varekladd – bokfør linje, mens oppgaven med å beregne og generere kostjusteringspostene utføres av kjørselen **Juster kostverdi – vareposter**.  

For å kunne videresende kostnader fastslår gjenkjenningsmekanismen hvilke kilder som har endrede kostnader, og hvilket mål disse kostnadene skal videresendes til. Følgende tre gjenkjenningsfunksjoner finnes i [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Vareutligningspost  
* Inngangspunkt for gjennomsnittlig kostjustering  
* Ordrenivå  

### <a name="item-application-entry"></a>Vareutligningspost

Denne gjenkjenningsfunksjonen brukes for varer som bruker lagermetodene FIFO, LIFO, Standard og Serienummer, og for scenarier med fast utligning. Funksjonen fungerer som følger:  

* Kostjustering registreres ved å merke kildevarepostene som *Utlignet post som skal justeres* hver gang en varepost eller verdipost bokføres.  
* Kost videresendes i henhold til kostkjedene som registreres i tabellen **Vareutligningspost**.  

### <a name="average-cost-adjustment-entry-point"></a>Inngangspunkt for gjennomsnittlig kostjustering

Denne gjenkjenningsfunksjonen brukes for varer som bruker lagermetoden Gjennomsnitt. Funksjonen fungerer som følger:  

* Kostjustering registreres ved å merke en post i tabellen **Utgangspunkt for justering av gjennomsnittskost** hver gang en verdipost bokføres.  
* Kost videresendes ved å utligne kostnadene mot verdiposter med en senere verdisettingsdato.  

### <a name="order-level"></a>Ordrenivå

Denne gjenkjenningsfunksjonen brukes i konverteringsscenarier, produksjon og montering. Funksjonen fungerer som følger:  

* Kostjustering registreres ved å merke ordren hver gang et materiale / en ressurs bokføres som forbrukt/brukt.  
* Kost videresendes ved å utligne kostnadene fra materiale/ressurs mot avgangsposter som er knyttet til samme ordre.  

Funksjonen for ordrenivå brukes til å gjenkjenne justeringer i monteringsbokføring. Figuren nedenfor viser justeringspoststrukturen:  

![Flyt av poster i kostjustering](media/design_details_assembly_posting_3.png "Flyt av poster i kostjustering")  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md).  

## <a name="manual-versus-automatic-cost-adjustment"></a>Manuell kontra automatisk kostjustering

Kostjustering kan utføres på to måter:  

* Manuelt, ved å kjøre kjørselen **Juster kostverdi - vareposter**. Du kan kjøre denne kjørselen for alle varer eller bare for bestemte varer eller varekategorier. Denne kjørselen kjører en kostjustering for varene på lageret som en inngående transaksjon er opprettet for, for eksempel et kjøp. Den satsvise jobben utfører også en justering hvis det opprettes utgående transaksjoner for varer som bruker lagermetoden Gjennomsnitt.  
* Automatisk, ved å justere kostnadene hver gang du bokfører en lagertransaksjon, og når en produksjonsordre er ferdig. Kostjusteringen kjøres bare for den bestemte varen eller de bestemte varene som påvirkes av bokføringen. Dette defineres når du merker av for **Automatisk kostjustering** på siden **Lageroppsett**.  

Det er lurt å kjøre kostjusteringen automatisk når du bokfører, fordi enhetskosten oppdateres oftere og er derfor mer nøyaktig. Ulempen er at ytelsen til databasen kan bli påvirket hvis kostjusteringen kjøres så ofte.  

Siden det er viktig å holde enhetskost for en vare oppdatert, anbefales det at du kjører den satsvise jobben **Juster kostverdi - vareposter** så ofte som mulig utenfor arbeidstiden. Du kan også bruke automatisk kostjustering. Dette sikrer at enhetskosten oppdateres daglig for varer.  

Uavhengig av om du kjører kostjusteringen manuelt eller automatisk, er justeringsprosessen og konsekvensen den samme. [!INCLUDE[prod_short](includes/prod_short.md)] beregner verdien av den inngående transaksjonen og videresender denne kostnaden til en hvilken som helst utgående transaksjoner, for eksempel salg eller forbruk, som er brukt på den inngående transaksjonen. Kostjusteringen oppretter verdiposter som inneholder justeringsbeløp og beløp som kompenserer for avrunding.  

De nye verdipostene for justering og avrunding har bokføringsdatoen til den tilknyttede fakturaen. Unntak er hvis verdipostene faller i en lukket regnskapsperiode eller lagerperiode, eller hvis bokføringsdatoen er tidligere enn datoen i feltet **Bokf. tillatt fra** på siden **Finansoppsett**. Hvis dette skjer, tilordner den satsvise jobben bokføringsdatoen som den første datoen i den neste åpne perioden.  

## <a name="adjust-cost---item-entries-batch-job"></a>Kjørselen Juster kostverdi – vareposter

Når du kjører kjørselen **Juster kostverdi - vareposter**, kan du kjøre kjørselen for alle varer eller bare for bestemte varer eller kategorier.  

> [!NOTE]  
> Vi anbefaler at du alltid kjører kjørselen for alle varer og bare bruker filtreringsalternativet til å redusere kjøretiden til kjørselen, eller til å rette kostnaden for en bestemt vare.  

### <a name="example"></a>Eksempel

Følgende eksempel viser hva som skjer hvis du bokfører en kjøpt vare som mottatt og fakturert 01.01.20. Senere bokfører du den solgte varen som levert og fakturert 15.01.20. Deretter kjører du de satsvise jobbene **Juster kostverdi - vareposter** og **Bokfør lagerkost i Finans**. Følgende poster opprettes.  

#### <a name="value-entries-1"></a>Verdiposter (1) 

|Bokføringsdato|Vareposttype|Kostbeløp (faktisk)|Bokført kost|Fakturert antall|Løpenr.|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01.01.20|Kjøp|10,00|10,00|1|1|  
|15.01.20|Salg|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Relasjonsposter i tabellen Finans – varepostrelasjon (1)

|Finansløpenr.|Verdiløpenummer|Finansjournalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Finansposter (1)

|Bokføringsdato|Finanskonto|Kontonummer (En-US-demo)|Beløp|Løpenr.|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01.01.20|[Lagerkonto]|2130|10,00|1|  
|01.01.20|[Konto utl. kj.pris/prod.kost]|7291|-10,00|2|  
|15.01.20|[Lagerkonto]|2130|-10,00|3|  
|15.01.20|[Vareforbrukskonto]|7290|10,00|4|  

Senere bokfører du et relatert varegebyr på NOK 2,00 fakturert 10.02.20. Du kjører den satsvise jobben **Juster kostverdi - vareposter** og deretter **Bokfør lagerkost i Finans**. Kjørselen for kostjustering justerer kostnadene for salget tilsvarende med NOK -2,00, og kjørselen **Bokfør lagerkost i Finans** bokfører de nye verdipostene i finans. Resultatet blir som følger.  

#### <a name="value-entries-2"></a>Verdiposter (2)  

|Bokføringsdato|Vareposttype|Kostbeløp (faktisk)|Bokført kost|Fakturert antall|Justering|Løpenr.|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|10.02.20|Kjøp|2,00|2,00|0|Nei|3|  
|15.01.20|Salg|-2,00|-2,00|0|Ja|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Relasjonsposter i tabellen Finans – varepostrelasjon (2)

|Finansløpenr.|Verdiløpenummer|Finansjournalnr.|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Finansposter (2)

|Bokføringsdato|Finanskonto|Kontonummer (En-US-demo)|Beløp|Løpenr.|  
|------------|-----------|------------------------|------|---------|  
|10.02.20|[Lagerkonto]|2130|2,00|5|  
|10.02.20|[Konto utl. kj.pris/prod.kost]|7291|-2,00|6|  
|15.01.20|[Lagerkonto]|2130|-2,00|7|  
|15.01.20|[Vareforbrukskonto]|7290|2,00|8|  

## <a name="automatic-cost-adjustment"></a>Automatisk kostjustering

Du kan definere kostjustering slik at den kjører automatisk når du bokfører en lagertransaksjon, ved å bruke feltet **Automatisk kostjustering** på **Lageroppsett**-siden. I dette feltet kan du velge hvor langt tilbake i tid du vil at automatisk kostjustering skal utføres, fra gjeldende arbeidsdato. Følgende alternativer finnes.  

|Alternativ|Beskrivelse|
|------|-----------|
|Aldri|Kostnader justeres ikke når du bokfører.|  
|Dag|Kostnader justeres hvis bokføring skjer innen én dag etter arbeidsdatoen.|  
|Uke|Kostnader justeres hvis bokføring skjer innen én uke etter arbeidsdatoen.|  
|Måned|Kostnader justeres hvis bokføring skjer innen én måned etter arbeidsdatoen.|  
|Kvartal|Kostnader justeres hvis bokføring skjer innen ett kvartal etter arbeidsdatoen.|  
|År|Kostnader justeres hvis bokføring skjer innen ett år etter arbeidsdatoen.|  
|Alltid|Kostnader justeres alltid når du bokfører, uavhengig av bokføringsdatoen.|  

Valget du gjør i feltet **Automatisk kostjustering**, er viktig for ytelse og nøyaktigheten til kostnadene. Kortere tidsperioder, for eksempel **Dag** eller **Uke**, påvirker systemytelsen mindre, fordi den automatiske justeringen begrenses til kostnader som er bokført bare den siste dagen eller uken. Dette betyr at den automatiske kostjusteringen ikke kjører like ofte og påvirker dermed systemytelsen mindre. Dette betyr imidlertid også at enhetskosten kan være mindre nøyaktige.  

### <a name="example"></a>Eksempel

Følgende eksempel viser et scenario med automatisk kostjustering:  

* 10. januar bokfører du en kjøpt vare som mottatt og fakturert.  
* 15. januar bokfører du en ordre for varen som levert og fakturert.
* 5. februar mottar du en faktura for et frakttillegg på det opprinnelige kjøpet. Du bokfører dette fraktgebyret og utligner det mot den opprinnelige kjøpsfakturaen, som øker kostnadene for det opprinnelige kjøpet.  

Hvis du har angitt at automatisk kostjustering skal gjelde for bokføringer som forekommer innen en måned eller et kvartal fra gjeldende arbeidsdato, kjøres den automatiske kostjusteringen, og kjøpskostnaden blir videresendt til salget.  

Hvis du har angitt at automatisk kostjustering skal gjelde for bokføringer som forekommer innen en dag eller en uke fra gjeldende arbeidsdato, kjøres ikke den automatiske kostjusteringen, og kjøpskostnaden blir videresendt til salget før du kjører den satsvise jobben **Juster kostverdi - vareposter**.  

## <a name="see-also"></a>Se også

[Justere varekost](inventory-how-adjust-item-costs.md)  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Designdetaljer: Avstemming med konti i Finans](design-details-reconciliation-with-the-general-ledger.md)  
[Designdetaljer: Lagerbokføring](design-details-inventory-posting.md)  
[Designdetaljer: Avvik](design-details-variance.md)  
[Designdetaljer: Bokføre monteringsordre](design-details-assembly-order-posting.md)  
[Designdetaljer: Bokføre produksjonsordre](design-details-production-order-posting.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]