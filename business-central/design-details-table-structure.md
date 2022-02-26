---
title: Designdetaljer – Tabellstruktur | Microsoft-dokumentasjon
description: For å forstå hvordan lagring og bokføring av dimensjonsposter er omformet, er det viktig å forstå tabellstrukturen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: 6d418633eb884f0b8cfca2f46fc69103a8fabdb2
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215731"
---
# <a name="design-details-table-structure"></a>Designdetaljer: Tabellstruktur
For å forstå hvordan dimensjonsoppføringer lagres og bokføres, er det viktig å forstå tabellstrukturen.  

## <a name="table-480-dimension-set-entry"></a>Tabell 480, Dimensjonssettpost  
Du kan ikke endre denne tabellen. Når data er skrevet til tabellen, kan du slette eller redigere dem.

|Feltnr.|Feltnavn|Datatype|Merknad|  
|---------------|----------------|---------------|-------------|  
|1|**ID**|Heltall|> 0,0 er reservert for det tomme dimensjonssettet. Refererer til felt 3 i tabell 481.|  
|2|**Dimensjonskode**|Kode 20|Tabellrelasjon til tabell 348.|  
|3|**Dimensjonsverdikode**|Kode 20|Tabellrelasjon til tabell 349.|  
|4|**Dimensjonsverdi-ID**|Heltall|Refererer til felt 12 i tabell 349. Dette er sekundærnøkkelen som brukes ved traversering av tabell 481.|  
|5|**Dimensjonsnavn**|Tekst 30|CalcField. Oppslag i tabell 348.|  
|6|**Navn på dimensjonsverdi**|Tekst 30|CalcField. Oppslag i tabell 349.|  

## <a name="table-481-dimension-set-tree-node"></a>Tabell 481, Trenode for dimensjonssett  
Du kan ikke endre denne tabellen. Den brukes til å søke etter et dimensjonssett. Hvis dimensjonssettet ikke blir funnet, blir det opprettet et nytt sett.  

|Feltnr.|Feltnavn|Datatype|Merknad|  
|---------------|----------------|---------------|-------------|  
|1|**Overordnet dimensjonssett-ID**|Heltall|0 for node på øverste nivå.|  
|2|**Dimensjonsverdi-ID**|Heltall|Tabellrelasjon til felt 12 i tabell 349.|  
|3|**Dimensjonssett-ID**|Heltall|AutoIncrement. Brukes i felt 1 i tabell 480.|  
|4|**I bruk**|Boolsk|Usann hvis ikke i bruk.|  

## <a name="table-482-reclas-dimension-set-buffer"></a>Tabell 482 Reklass. dimensjonssettbuffer  
Denne tabellen brukes når du endrer en dimensjonsverdikode, for eksempel på en varepost ved hjelp av siden **Varereklassifiseringskladd**.  

|Feltnr.|Feltnavn|Datatype|Merknad|  
|---------------|----------------|---------------|-------------|  
|1|**Dimensjonskode**|Kode 20|Tabellrelasjon til tabell 348.|  
|2|**Dimensjonsverdikode**|Kode 20|Tabellrelasjon til tabell 349.|  
|3|**Dimensjonsverdi-ID**|Heltall|Refererer til felt 12 i tabell 349.|  
|4|**Ny dimensjonsverdikode**|Kode 20|Tabellrelasjon til tabell 349.|  
|5|**Ny dimensjonsverdi-ID**|Heltall|Refererer til felt 12 i tabell 349.|  
|6|**Dimensjonsnavn**|Tekst 30|CalcField. Oppslag i tabell 348.|  
|7|**Navn på dimensjonsverdi**|Tekst 30|CalcField. Oppslag i tabell 349.|  
|8|**Nytt navn på dimensjonsverdi**|Tekst 30|CalcField. Oppslag i tabell 349.|  

## <a name="transaction-and-budget-tables"></a>Transaksjons- og budsjettabeller  
I tillegg til andre dimensjonsfelt i denne tabellen er dette feltet viktig:  

|Feltnr.|Feltnavn|Datatype|Merknad|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensjonssett-ID**|Heltall|Refererer til felt 1 i tabell 480.|  

### <a name="table-83-item-journal-line"></a>Tabell 83, Varekladdlinje  
I tillegg til andre dimensjonsfelt i denne tabellen er disse feltene viktige:  

|Feltnr.|Feltnavn|Datatype|Merknad|  
|---------------|----------------|---------------|-------------|  
|480|**Dimensjonssett-ID**|Heltall|Refererer til felt 1 i tabell 480.|  
|481|**Ny dimensjonssett-ID**|Heltall|Refererer til felt 1 i tabell 480.|  

### <a name="table-349-dimension-value"></a>Tabell 349, Dimensjonsverdi  
I tillegg til andre dimensjonsfelt i denne tabellen er disse feltene viktige:  

|Feltnr.|Feltnavn|Datatype|Merknad|  
|---------------|----------------|---------------|-------------|  
|12|**Dimensjonsverdi-ID**|Heltall|AutoIncrement. Brukes til referanser i tabell 480 og tabell 481.|  

### <a name="tables-that-contain-the-dimension-set-id-field"></a>Tabeller som inneholder Dimensjonssett-ID-feltet
 Feltet **Dimensjonssett-ID** (480) finnes i følgende tabeller: For tabellene som inneholder bokførte data vil feltet bare inneholde en ikke-redigerbar visning av dimensjoner, som er markert som detaljer. Feltet kan redigeres for tabeller som inneholder arbeidsdokumenter. Buffertabellene som brukes internt, trenger ikke redigerbar eller ikke-redigerbar funksjonalitet.  

 Felt 480 kan ikke redigeres i tabellene nedenfor.  

|Tabellnr.|Tabellnavn|  
|---------------|----------------|  
|17|**Finanspost**|  
|21|**Kundepost**|  
|25|**Leverandørpost**|  
|32|**Varepost**|  
|110|**Følgeseddelhode**|  
|111|**Følgeseddellinje**|  
|112|**Salgsfakturahode**|  
|113|**Salgsfakturalinje**|  
|114|**Salgskreditnotahode**|  
|115|**Salgskreditnotalinje**|  
|120|**Mottakshode**|  
|121|**Mottakslinje**|  
|122|**Kjøpsfakturahode**|  
|123|**Kjøpsfakturalinje**|  
|124|**Kjøpskreditnotahode**|  
|125|**Kjøpskreditnotalinje**|  
|169|**Prosjektpost**|  
|203|**Ressurspost**|  
|271|**Bankkontopost**|  
|281|**Vareopptellingspost**|  
|297|**Utstedt purrehode**|  
|304|**Utstedt rentenotahode**|  
|5107|**Salgshode - arkiv**|  
|5108|**Salgslinje - arkiv**|  
|5109|**Bestillingshode - arkiv**|  
|5110|**Bestillingslinje - arkiv**|  
|5601|**Aktivapost**|  
|5625|**Vedlikeholdspost**|  
|5629|**Forsikringsdekningspost**|  
|5744|**Overføringseddelhode**|  
|5745|**Overføringsseddellinje**|  
|5746|**Overføringsmottakshode**|  
|5747|**Overføringsmottakslinje**|  
|5802|**Verdipost**|  
|5832|**Kapasitetspost**|  
|5907|**Servicepost**|  
|5908|**Servicehode**|  
|5933|**Serviceordrebokføringsbuffer**|  
|5970|**Arkivert servicekontrakt - hode**|  
|5990|**Servicefølgeseddelhode**|  
|5991|**Servicefølgeseddellinje**|  
|5992|**Servicefakturahode**|  
|5993|**Servicefakturalinje**|  
|5994|**Salgskreditnotahode (service)**|  
|5995|**Salgskreditnotalinje (service)**|  
|6650|**Returforsendelse - hode**|  
|6651|**Returforsendelseslinje**|  
|6660|**Returseddelhode**|  
|6661|**Returseddellinje**|  

Felt 480 kan redigeres i tabellene nedenfor.  

|Tabellnr.|Tabellnavn|  
|---------------|----------------|  
|36|**Salgshode**|  
|37|**Salgslinje**|  
|38|**Bestillingshode**|  
|39|**Bestillingslinje**|  
|81|**Finanskladdelinje**|  
|83|**Varekladdelinje**|  
|89|**Stykklistekladdelinje**|  
|96|**Budsjettpost**|  
|207|**Res.kladdelinje**|  
|210|**Prosjektkladdelinje**|  
|221|**Fordeling**|  
|246|**Bestillingsforslagslinje**|  
|295|**Purrehode**|  
|302|**Rentenotahode**|  
|5405|**Produksjonsordre**|  
|5406|**Prod.ordrelinje**|  
|5407|**Prod.ordrekomponent**|  
|5615|**Aktivafordeling**|  
|5621|**Aktivakladdelinje**|  
|5635|**Forsikringskladdelinje**|  
|5740|**Overføringshode**|  
|5741|**Overføringslinje**|  
|5900|**Servicehode**|  
|5901|**Servicevarelinje**|  
|5902|**Servicelinje**|  
|5965|**Servicekontrakthode**|  
|5997|**Standard servicefakturalinje**|  
|7134|**Varebudsjettpost**|  
|99000829|**Planleggingskomponent**|  

Felt 480 finnes i følgende buffertabeller.  

|Tabellnr.|Tabellnavn|  
|---------------|----------------|  
|49|**Fakturabokf.buffer**|  
|212|**Bokføringsbuffer - prosjekt**|  
|372|**Betalingsbuffer**|  
|382|**Buffer for KL-post**|  
|461|**Fakturalinjebuffer for forskudd**|  
|5637|**Aktivafinansbokf.buffer**|  
|7136|**Buffer for varebudsjett**|  

## <a name="see-also"></a>Se også

[Dimensjonssettposter – oversikt](design-details-dimension-set-entries-overview.md)  
[Designdetaljer: Søke etter dimensjonskombinasjoner](design-details-searching-for-dimension-combinations.md)   
