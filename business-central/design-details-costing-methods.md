---
title: 'Designdetaljer: Kostmetoder'
description: Dette emnet beskriver hvordan lagermetoden påvirker hvordan de faktiske og budsjetterte verdiene kapitaliseres og brukes i kostnadsberegningen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Designdetaljer: Kostmetoder

Lagermetoden avgjør om det er en faktisk eller en budsjettert verdi som kapitaliseres og brukes i kostnadsberegningen. Sammen med bokføringsdatoen og rekkefølgen påvirker lagermetoden også hvordan kostnadsflyten registreres.

> [!NOTE]
> Du kan ikke endre varens lagermetode hvis det finnes vareposter for varen. Hvis du vil ha mer informasjon, kan du se [Utformingsdetaljer: Endre lagermetode for varer](design-details-changing-costing-methods.md).

Følgende metoder støttes i [!INCLUDE[prod_short](includes/prod_short.md)]:  

| Lagermetode | Beskrivelse | Når den brukes |
|--|--|--|
| FIFO | Enhetskosten for en vare er den faktiske verdien for alle mottak av varen, valgt av FIFO-regelen.<br /><br /> Lagerverdisetting antar at de første varene som plasseres på lager, selges først. | I forretningsmiljøer der produktkost er stabil.<br /><br /> (Når prisene stiger, viser balansen større verdi. Dette betyr at skatteforpliktelser økes, men kredittverdigheten og mulighetene til å låne penger blir bedre.)<br /><br /> For varer med en begrenset holdbarhet, fordi de eldste varene må selges før de overskrider siste salgsdato. |
| LIFO | Enhetskosten for en vare er den faktiske verdien for alle mottak av varen, valgt av LIFO-regelen.<br /><br /> Lagerverdisetting antar at de siste varene som plasseres på lager, selges først. | Ikke tillatt i mange land/regioner, siden det kan brukes til å redusere fortjeneste.<br /><br /> (Når prisene stiger, reduseres verdien i resultatregnskapet. Dette betyr at skatteforpliktelser reduseres, men mulighetene til å låne penger blir mindre.) |
| Gjennomsnitt | Enhetskosten for en vare beregnes som den gjennomsnittlige enhetskostnaden på hvert tidspunkt etter et kjøp.<br /><br /> Lagerverdisetting antar at alle beholdninger selges samtidig. | I forretningsmiljøer der produktkost er ustabil.<br /><br /> Når beholdninger er stablet eller blandet sammen og ikke kan kan differensieres, for eksempel kjemikalier. |
| Bestemt | Enhetskosten for en vare er den nøyaktige kosten da den bestemte enheten ble mottatt. | I produksjon av eller handel med lett gjenkjennelige varer med relativt høy enhetskost.<br /><br /> For varer som er underlagt regulering.<br /><br /> For varer med serienumre. |
| Standard | Enhetskosten for en vare er forhåndsinnstilt basert på estimert kostnad.<br /><br /> Når de faktiske kostnadene senere realiseres, må standardkosten justeres til faktisk kost gjennom avviksverdier. | Der kostnadskontroll er kritisk.<br /><br /> I gjentatt produksjon for å verdsette kostnadene for direkte materialer, direkte arbeid og indirekte produksjon.<br /><br /> Der det er disiplin og ansatte for å opprettholde standardene. |

Bildet nedenfor viser hvordan kost flyter gjennom lageret for hver lagermetode.  

![Lagermetoder visualisert.](media/design_details_inventory_costing_7_costing_methods.png "Lagermetoder visualisert")  

Lagermetodene varierer med hensyn til hvordan de verdisetter lagerreduksjoner og om de bruker faktiske kostnad eller standard kostnad som verdisettingsgrunnlag. Tabellen nedenfor forklarer de ulike egenskapene. (LIFO-metoden er utelukket fordi den er lik FIFO-metoden.)  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Generelle kjennetegn|Utligning/justering |Revaluering|Diverse |
|-|---------|---------|---------|---------|
|**FIFO**     |Lett å forstå|Utligning holder orden på **det gjenværende antallet**.<br /><br /> Justering videresender kostnader i henhold til antallsutligning. |Revaluerer bare fakturert antall.<br /><br /> Kan utføres per vare eller per varepost.<br /><br /> Kan utføres bakover i tid.|Hvis du tilbakedaterer en lagerreduksjon, brukes IKKE eksisterende oppføringer på nytt for å gi en riktig FIFO-kostnadsflyten.|
|**Gjennomsnitt**     |Basert på periodealternativer: **Dag**/**Uke**/**Måned**/**Kvartal**/**Regnskapsperiode**.<br /><br /> Kan beregnes per vare eller per vare/lokasjon/variant.|Utligning holder orden på **det gjenværende antallet**.<br /><br /> Kostnader beregnes og videresendt på **verdisettingsdato**. |Revaluerer bare fakturert antall.<br /><br /> Kan bare utføres per vare.<br /><br /> Kan utføres bakover i tid. |Hvis du tilbakedaterer lagerøkning eller -reduksjon, blir gjennomsnittskost beregnet på nytt, og alle berørte poster blir justert.<br /><br /> Hvis du endrer periode- eller beregningstype, må alle berørte poster justeres.|
|**Standard**     |Enkel å bruke, men krever kvalifisert vedlikehold.|Utligning holder orden på **det gjenværende antallet**.<br /><br /> Utligning er basert på FIFO.|Revaluerer fakturerte og ikke-fakturerte antall.<br /><br /> Kan utføres per vare eller per varepost.<br /><br /> Kan utføres bakover i tid.|Bruk **Standardforslag**-siden til å oppdatere og opprullere standardkostnader regelmessig.<br /><br /> Støttes IKKE per LFE.<br /><br /> Det finnes ingen historiske poster for standardkost.|
|**Bestemt**     |Krever varesporing på både inngående og utgående transaksjon.<br /><br /> Brukes vanligvis for serialiserte varer.|Alle utligninger er faste.|Revaluerer bare fakturert antall.<br /><br /> Kan utføres per vare eller per varepost.<br /><br /> Kan utføres bakover i tid.|Du kan bruke spesifikk varesporing uten å bruke lagermetoden Serienummer. Kostnadene følger ikke partinummeret, men i stedet kostnadsforutsetningen i den valgte lagermetoden.|

## Eksempel

Denne delen inneholder eksempler på hvordan ulike lagermetoder påvirker lagerverdi.  

Tabellen nedenfor viser lagerøkningene og -reduksjonene som eksemplene er basert på.  

|Bokføringsdato|Antall|Løpenr.|  
|------------------|--------------|---------------|  
|01.01.20|1|1|  
|01.01.20|1|2|  
|01.01.20|1|3|  
|01.02.20|-1|4|  
|01.03.20|-1|5|  
|01.04.20|-1|6|  

> [!NOTE]  
> Det resulterende antallet på lageret er null. Lagerverdien må derfor være null, uavhengig av lagermetoden.  

### Virkningen økes av lagermetoder på verdisetting av lagerbeholdning  

Lagerøkninger verdisettes som varens anskaffelseskost for varer som bruker andre lagermetoder som verdisettingsgrunnlag (**FIFO**, **LIFO**, **Gjennomsnitt** eller **Spesifikk**).  

- **Standard**  

    Når det gjelder varer som bruker lagermetoden **Standard**, verdisettes lagerøkningene til varens gjeldende standardkost.  

#### Standard  

Når det gjelder varer som bruker lagermetoden **Standard**, verdisettes lagerøkningene til varens gjeldende standardkost.  

### Virkningen reduseres av lagermetoder på verdisetting av lagerbeholdning

- **FIFO**  

    Varer som bruker **FIFO**-lagermetode og som ble kjøpt først, selges alltid første (løpenumrene 3, 2 og 1 i dette eksemplet) . Lagerreduksjoner verdisettes derfor ved å fastsette verdien på de første lagerøkningene.  

     VAREFORBRUK beregnes ved hjelp av verdien i de første lageranskaffelsene.  

     Tabellen nedenfor viser hvordan lagerreduksjoner verdisettes for lagermetoden **FIFO**.  

    |Bokføringsdato|Antall|Kostbeløp (faktisk)|Løpenr.|  
    |------------------|--------------|----------------------------|---------------|  
    |01.02.20|-1|-10,00|4|  
    |01.03.20|-1|-20,00|5|  
    |01.04.20|-1|-30,00|6|  

- **LIFO**  

    Varer som bruker **LIFO**-lagermetode og som ble kjøpt sist, selges alltid første (løpenumrene 3, 2 og 1 i dette eksemplet) . Lagerreduksjoner verdisettes derfor ved å fastsette verdien på de siste lagerøkningene.  

     VAREFORBRUK beregnes ved hjelp av verdien i de nyeste lageranskaffelsene.  

     Tabellen nedenfor viser hvordan lagerreduksjoner verdisettes for lagermetoden **LIFO**.  

    |Bokføringsdato|Antall|Kostbeløp (faktisk)|Løpenr.|  
    |------------|--------|--------------------|---------|  
    |01.02.20|-1|-30,00|4|  
    |01.03.20|-1|-20,00|5|  
    |01.04.20|-1|-10,00|6|  

- **Gjennomsnitt**  

    Når det gjelder varer som bruker lagermetoden **Gjennomsnitt**, verdisettes lagerreduksjoner ved å beregne et avveid gjennomsnitt av restbeholdningen den siste dagen i gjennomsnittskostperioden som lagerreduksjonen ble bokført i. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Gjennomsnittskost](design-details-average-cost.md).  

     Tabellen nedenfor viser hvordan lagerreduksjoner verdisettes for lagermetoden **Gjennomsnitt**.  

    | Bokføringsdato | Antall | Kostbeløp (faktisk) | Løpenr. |
    |--|--|--|--|
    | 01.02.20 | -1 | -20,00 | 4 |
    | 01.03.20 | -1 | -20,00 | 5 |
    | 01.04.20 | -1 | -20,00 | 6 |

- **Standard**  

    For varer som bruker lagermetoden **Standard** verdisettes lagerreduksjoner på samme måte som lagermetoden **FIFO**, med unntak av at verdisettingen er basert på en standardkost, ikke de faktiske kostnadene.  

    Tabellen nedenfor viser hvordan lagerreduksjoner verdisettes for lagermetoden **Standard**.  

    |Bokføringsdato|Antall|Kostbeløp (faktisk)|Løpenr.|  
    |------------------|--------------|----------------------------|---------------|  
    |01.02.20|-1|-15,00|4|  
    |01.03.20|-1|-15,00|5|  
    |01.04.20|-1|-15,00|6|  

- **Serienummer**  

    Lagermetoder genererer en antakelse om hvordan kostflyter går fra en lagerøkning til en lagerreduksjon. Hvis det finnes riktigere informasjon om kostnadsflyten, kan du imidlertid overstyre denne antakelsen ved å opprette en fastsatt utligning mellom poster. En fastsatt utligning oppretter en kobling mellom en lagerreduksjon og en bestemt lagerøkning, og angir kostnadsflyten i henhold til dette.  

    Lagerreduksjoner verdisettes i henhold til lagerøkningen som den er koblet til med fast utligning, for varer som bruker lagemetoden **Serienummer**.  

    Tabellen nedenfor viser hvordan lagerreduksjoner verdisettes for lagermetoden **Serienummer**.  

    |Bokføringsdato|Antall|Kostbeløp (faktisk)|Utligningspost|Løpenr.|
    |------------|--------|--------------------|----------------|---------|  
    |01.02.20|-1|-20,00|**2**|4|  
    |01.03.20|-1|-10,00|**1**|5|  
    |01.04.20|-1|-30,00|**3**|6|  

## Se også

[Utformingsdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Utformingsdetaljer: Avvik](design-details-variance.md)  
[Utformingsdetaljer: Gjennomsnittskost](design-details-average-cost.md)  
[Utformingsdetaljer: Vareutligning](design-details-item-application.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Ordliste over termer i Dynamics 365-forretningsprosesser](/dynamics365/guidance/business-processes/glossary)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
