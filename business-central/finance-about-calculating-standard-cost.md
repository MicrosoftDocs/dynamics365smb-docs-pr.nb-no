---
title: Om beregning av standardkost
description: En standard kostprissystem bestemmer lagerenhetskosten basert på rimelige historiske eller forventede kostnader.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
---
# Om beregning av standardkost

Mange produksjonsselskaper bruke standardkost som verdisettingsgrunnlag. Dette gjelder også for selskaper som utfører lett produksjon, for eksempel montering og kitting. En standard kostprissystem bestemmer lagerenhetskosten basert på noen rimelige historiske eller forventede kostnader. Undersøkelser av tidligere og anslåtte fremtidige kostdata danner grunnlaget for standardkost. Disse kostnadene fryses til det tas en beslutning om å endre dem. Den faktiske kostnaden for å produsere et produkt kan avvike fra de beregnede standardkostnadene. Når det gjelder administrasjonskontroll, sammenlignes faktisk kostnad med standardkostnad for en bestemt vare, og forskjeller, eller *avvik*, identifiseres og analyseres.  

Standardkost kan vedlikeholdes for varer som etterfylles gjennom kjøp, montering og produksjon. Standardkostnader kan bestå av følgende elementer for hver etterfyllingsmetode.  

|Etterfyllingssystem|Standard kostelementer|  
|--------------------------|----------------------------|  
|**Kjøp**|Direkte materialkostnad og indirekte materialkostnad om nødvendig.|  
|**Montering**|Direkte materialkostnader, direkte eller faste arbeidskostnader og indirekte kostnader.|  
|**Prod.ordre**|Direkte materialkostnader, arbeidskostnader, underleverandørkostnader og indirekte kostnader.|  

## Definere standardkostnader

Siden standardkostbeløpet for en produsert eller montert vare kan bestå av flere kostelementer, inkludert materialkost, kapasitetskost (arbeid) og direkte og indirekte underleverandørkost, må standardkost opprettes for hvert av disse elementene.  

Regnskapsoppgaven for et vareproduksjonsselskap som bruker standardkostberegning, er følgende:  

- Beregne et standardkostbeløp for den ferdige varen og definere det på varekortet.  
- Registrere og fordele faktisk kost for nøkkelkostelementene, og å gjøre greie for avvik.  

For å fastsette direkte kostnad for en ferdig vare må alle komponentkostbeløpene summeres. En montert eller produsert vare kan inkludere halvfabrikater, som også består av flere komponenter.  

Følgende nøkkelkostelementer utgjør den totale direkte kostnaden for en ferdigbehandlet vare:  

- Materialkost.  
- Kapasitetskostnad  
- Underleverandørkost bare for produserte varer.  

### Materialkostnader

Materialkost er kostnader som er knyttet til delmonteringer og kjøpte råvarer. Materialenhetskost kan bestå av direkte og indirekte kostelementer.  

- Direkte materialkost representerer et fakturert beløp for kjøpte råmaterialer eller behandlingskost for en halvfabrikat.  
- Indirekte materialkost, eller *indirekte kostnader*, kan for eksempel representere elementer som lagerføringskost for den ferdige varen etter at den er produsert.  

Defineringen av materialkost for kjøpte varer som påvirker direkte og indirekte kost, avhenger av lagermetoden du har valgt for den angitte varen. Du definerer kostnadsinformasjonen for hver lagemetode på varekortet. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

Vrakkost (bare for produksjon) er en annen faktor som må tas med i betraktningen når du beregner samlet materialkost. Når en viss mengde råmateriale vrakes under produksjonen eller monteringen av en vare, fører det vanligvis til en økning i antallet komponenter som trengs for å produsere denne varen. Dette øker materialkostbeløpet for komponentene som forbrukes mens en overordnet vare produseres. Du definerer vrakkost for materialer i produksjonsstykklisten eller ruten.  

Materialkostbeløpet for en produsert vare kan representeres på to måter som svarer til følgende grunnlag for standardkostberegning.  

|Basis for kostberegning|Materialkostberegning|  
|----------------------------|-------------------------------|  
|Enkeltnivå|Produsert vare er lik den totale kostnaden for alle kjøpte eller halvfabrikatavarer på den varens produksjonsstykkliste.|  
|Opprullert nivå eller flernivå|Produsert vare er summen av materialkostbeløpet for alle halvfabrikater på stykklisten for varen og kostbeløpet for alle kjøpte varer på produksjonsstykklisten for varen.|  

### Kapasitetskostnader

Kapasitetskostnader er kostnader som er knyttet til internt arbeid og maskinkostnader. Du må definere disse kostnadene for hver ressurs (i monteringsstyring) og hvert arbeidssenter eller hver produksjonsressurs i ruten (i produksjon). Som med materialer kan du identifisere både direkte og indirekte elementer av kapasitetskost. Direkte kost for et arbeidssenter kan for eksempel være den etablerte produksjonssatsen for å utføre en bestemt funksjon. Indirekte kost for et arbeidssenter kan representere noen generelle fabrikkutgifter, for eksempel belysning, oppvarming og så videre. På lignende måte som med materialkost kan du uttrykke indirekte kapasitetskost som en indirekte kostprosent eller en fast sats for indirekte kost.  

Oppsettet for kapasitetskost for monterte varer består av følgende elementer:  

- Direkte og indirekte enhetskost for ressursen.  
- Fast eller direkte ressursbrukstype.  

Oppsettet for kapasitetskost for produserte varer består av følgende elementer:  

- Direkte og indirekte enhetskost for produksjonsressursen eller arbeidssenteret.  
- Oppsett av tid og partistørrelse.  

For å beregne standard kapasitetskost må du opprette standardtidssatser som er nødvendige for å utføre operasjoner på produksjonsressurser og arbeidssentre. Samlet tid for å fullføre en operasjon består vanligvis av oppstillings-/operasjonstid samt ventetid og transporttid.  

Du definerer satsene for hver av disse tidstypene for hver produksjonsressurs eller arbeidssenter i en individuell rute.  

> [!NOTE]  
>  Mens operasjonstidssatser gjelder for hver vareenhet som produseres, gjelder oppstillingstidssatsene for hvert parti. Derfor må du fordele ruteoppstillingstiden for hver operasjon proporsjonalt over partistørrelsen. Du angir partistørrelsen i det tilsvarende feltet i hurtigfanen **Etterfylling** på siden **Varekort**.  

Hvis du vil angi oppstillingstid i ruten for planlegging, men ikke inkludere denne utgiften i standardkostberegningen, tømmer du feltet **Kost inkl. oppstilling** på siden **Produksjonsoppsett**.  

På et enkeltnivågrunnlag er dette arbeidskost som kreves for å produsere den ferdige produksjonsvaren, og angis i ruten for produksjonsvaren. På et flernivågrunnlag er dette kapasitetskost som angitt for hver enkelt produserte vare som er inkludert i stykklisten for den overordnede varen.  

### Underleverandørkostnader

Underleverandørkost er kost som er knyttet til tjenester som leveres av et selskaps eksterne leverandører eller underleverandører. På lignende måte som med material og kapasitet kan underleverandørkost bestå av både direkte og indirekte kostbeløp. Direkte underleverandørkost representerer faktisk avgift for hver serviceenhet som leveres. Indirekte underleverandørkost kan for eksempel representere frakt og håndteringskost som selskapet pådrar seg med en underleveransebestilling.  

Siden underleveranse er en utkontrahert kapasitet, definerer du kostnaden for både direkte og indirekte underleveransetjenester på arbeidssenterkortet som representerer underleveranseoperasjonen.  

## Oppdatere standardkostnader

Hvis du vil oppdatere eller beregne standardkost for monteringsvarer, bruker du funksjonen fra varekortet.  

Prosessen med å oppdatere eller beregne standardkostnader vanligvis består av følgende oppgaver:  

1.  Oppdatere kost på komponent- og kapasitetsnivået. Hvis du vil ha mer informasjon, se kjørslene **Foreslå standardkost for vare** og **Foreslå standardkost for kapasitet**.  
2.  Konsolidere og opprullere komponent- og kapasitetskost for å beregne samlet monterings- eller produksjonskost for varene. Hvis du vil ha mer informasjon, kan du se [Slik beregner du standardkosten for en monteringsvare](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  Implementere standardkostnadene som angis når du kjører de forrige kjørslene. Standardkostnadene trer ikke i kraft før de blir implementert. Bruk kjørselen **Implementer standard kostendringer** som oppdaterer endringene i standardkostnad på varene med de i tabellen Standardkost – forslag.  
4.  Implementere endringene for å oppdatere **Enhetskost**-feltet på varekortet og utføre revaluering av lager. Hvis du vil ha mer informasjon, kan du se [Revaluere beholdning](inventory-how-revalue-inventory.md).

## Bruk kjørsler til å oppdatere standardkost
Følgende avsnitt beskriver kjørslene du kan bruke til å oppdatere standardkost.
### Foreslått standardkost for vare

 Oppretter forslag til endring av kostnader og kostandeler for standardkostnader på varekort. Når kjørselen er fullført, kan du se resultatet i vinduet Standardkost – forslag.

> [!NOTE]  
> Denne kjørselen er ment bare for kjøpte varer. Hvis du vil oppdatere en vare med en poduksjonsstykkliste eller monteringsstykklise, må du først fylle ut forslaget, med alle komponentene, og deretter starte kjørselen Oppruller standardkost.

Denne kjørselen oppretter bare forslag. Den implementerer ikke endringsforslagene. Hvis du er fornøyd med forslagene og vil implementere dem, det vil si oppdatere dem på varekortene og legge dem inn i revalueringskladden, velger du Implementer endringer i standardkost i vinduet Standardkost – forslag.
#### Alternativer

**Kostpris (standard)**: Angi justeringsfaktor for oppdatering av standardkostnad. Du kan også velge en avrundingsmetode for den nye standardkostnaden. Du må fylle ut feltet med en desimal for prosentøkningen, for eksempel 1,1.

**Indirekte kost-%**: Angi justeringsfaktor for oppdatering av indirekte kost-%. Du kan også velge avrundingsmetode for den nye indirekte kostnadsprosenten. Du må fylle ut feltet med en desimal for prosentøkningen, for eksempel 1,1.

**Sats for indirekte kostnader**: Angi justeringsfaktor for oppdatering av sats for indirekte kostnader. Du kan også velge avrundingsmetode for den nye satsen for indirekte kostnader. Du må fylle ut feltet med en desimal for prosentøkningen, for eksempel 1,1.

### Foreslå std.kost for arb.sent/prod.ress.

Oppretter forslag til endring av kostnader og kostandeler for standardkostnader i arbeidssentre, i produksjonsressurser eller på ressurskort. Når kjørselen er fullført, kan du se resultatet i vinduet **Standardkost – forslag**.

Denne kjørselen oppretter bare forslag. Den implementerer ikke endringsforslagene. Hvis du er fornøyd med forslagene og vil implementere dem, det vil si oppdatere dem på arbeids-/produksjonsressurs og ressurskortene og legge dem inn i vinduet Revalueringskladd, velger du **Implementer endringer i standardkost** i vinduet **Standardkost – forslag**.

Når du har brukt kjørselen og ønsker å se innvirkningen på produksjons- eller monteringsavdelingen, kan du starte kjørselen **Oppruller standardkost** for å oppdatere standardkost for arbeidssentre, produksjonsressurser, monteringsressurser, produksjonsstykklister og monteringsstykklister.
#### Alternativer
**Kostpris (standard)**: Angi justeringsfaktor for oppdatering av standardkostnad. Du kan også velge en **avrundingsmetode** for den nye standardkostnaden. Du må fylle ut feltet med en desimal for prosentøkningen, for eksempel 1,1.

**Indirekte kost-%**: Angi justeringsfaktor for oppdatering av indirekte kost-%. Du kan også velge avrundingsmetode for den nye indirekte kostnadsprosenten. Du må fylle ut feltet med en desimal for prosentøkningen, for eksempel 1,1.

**Sats for indirekte kostnader**: Angi justeringsfaktor for oppdatering av sats for indirekte kostnader. Du kan også velge avrundingsmetode for den nye satsen for indirekte kostnader. Du må fylle ut feltet med en desimal for prosentøkningen, for eksempel 1,1.

### Bokfør lagerkost i Finans

 Registrerer endringene i antall og verdi på lageret i henholdsvis varepostene og verdipostene når du bokfører lagertransaksjoner, for eksempel følgesedler eller kjøpsmottak.

Med mindre du har merket av for **Automatisk kostbokføring** i vinduet **Lageroppsett**, registreres ikke lagerkostnader dynamisk i finans, og VAREFORBRUK beregnes ikke i forbindelse med et salg. Du må derfor bokføre manuelt i Finans ved å utføre kjørselen **Bokfør lagerkost i Finans** for å oppdatere Finans og eventuelt skrive ut en rapport med verdipostene som er bokført.

Kjørselen bruker verdiposter som grunnlag. Den bruker differansen mellom feltene **Kostbeløp (faktisk)** og **Bokført kost i Finans** til å beregne verdien som skal bokføres. Hvis du har valgt alternativet **Bokf. av forventet kost i Finans** i vinduet **Lageroppsett**, bokfører kjørselen også differansen mellom feltene **Kostbeløp (forventet)** og **Forventet kost bokført i Finans** i de midlertidige kontoene i Finans.

> [!NOTE]
> Hvis du ikke har merket av for **Bokf. av forventet kost i Finans** i vinduet **Lageroppsett**, vises verdiposter som er hoppet over fordi de representerer forventede kostnader, i siste del av rapporten.

> [!NOTE] 
> Hvis det oppstår en feil under kjørselen som har å gjøre med dimensjoner eller dimensjonsoppsett, overstyres feilen, og posten bokføres i Finans ved hjelp av dimensjonene til verdiposten.

Hvis du vil forsikre deg om at det ikke oppstår feil når kjørselen kjører, kan du kjøre rapporten **Bokfør lagerkost i Finans – test** for å se alle feil som kan oppstå. Deretter kan du rette opp feilene og kjøre kjørselen **Bokfør lagerkost i Finans**, slik at alle postene behandles.
 
> [!IMPORTANT]  
> Før du bruker denne kjørselen, må du starte kjørselen **Juster kostverdi – vareposter**. Dette sikrer at når du starter denne kjørselen, er kostbeløpene som bokføres i Finans, à jour.
#### Alternativer

|Alternativ  |Description  |
|--------------|---------|
|**Bokføringsmetode**|Kjørselen kan enten bokføre lagerverdien i Finans per bokføringsgruppe eller per bokførte post. Hvis du bokfører per post, får du en detaljert spesifikasjon over hvordan lageret påvirker Finans, men du får også mange finansposter. Hvis du bokfører per bokføringsgruppe, oppretter kjørselen en finanspost per kombinasjon av bokføringsdato per bokføringsgruppe. Dette betyr at det opprettes en finanspost for hver kombinasjon av bokføringsdato, firmabokføringsgruppe, varebokføringsgruppe, lagerbokføringsgruppe og lokasjonskode. I tillegg oppretter kjørselen separate finansposter for kost med ulike fortegn.|
|**Bilagsnr.**|I dette feltet angir du et bilagsnummer hvis du har valgt alternativet Bokfør per bokføringsgruppe - lager. Dokumentnummeret vises på bokførte poster.|
|**Bokfør**|Velg dette feltet hvis du vil at kjørselen skal bokføre automatisk i Finans. Hvis du velger å ikke bokføre lagerkostbeløpet i Finans, skrives det bare ut en kontrollrapport med verdiene som kan bokføres i Finans, og i rapporten står det: **Kontrollutskrift (er ikke bokført)**.|

### Oppruller standardkost

Opprullerer standardkostnadene for monterte og produserte varer. Disse påvirkes av endringen i standardkost for komponenter som foreslås av kjørselen **Foreslå standardkost for vare**. I tillegg påvirkes de av endringene i standardkostnader for produksjonskapasitet og monteringsressurser som foreslås av kjørselen **Foreslå std.kost for arb.sent/prod.ress.**.

Når du har utført den ene eller begge av disse kjørslene, og du utfører en opprulling, introduseres alle endringer i standardkostnader i forslaget, i de tilknyttede produksjons- eller monteringsstykklistene, og kostnadene brukes for alle stykklistenivåer.

> [!NOTE] 
> Denne funksjonen oppruller bare standardkostnad på varekortene, ikke på kortene for lagerføringsenheter.

Denne kjørselen oppretter bare forslag. Den implementerer ikke endringsforslagene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si oppdatere dem på varekortene og legge dem inn i vinduet **Revalueringskladd**, kan du bruke kjørselen **Implementer endring i standardkost**. Du får tilgang til denne kjørselen i vinduet **Standardkost – forslag**.
#### Alternativer

**Beregningsdato**: Angi datoen som gjelder for produksjonsstykklisteversjonen du vil opprullere.
 
### Implementer endring i standardkost

Oppdaterer endringene i standardkostnad i tabellen **Vare** med dem i tabellen **Standardkost – forslag**. Standardkostnadsforslagene kan opprettes med kjørslene **Foreslå standardkost for vare** eller **Foreslå std.kost for arb.sent/prod.ress.**, og du kan også endre dem. Innholdet i alle feltene i standardkostnadsforslaget overføres. Når du implementerer forslag til endringer av standardkostnader, kan du se dem på varekortet og på arbeidssenter- eller produksjonsressurskortet. En revalueringskladd opprettes også, slik at du kan oppdatere lagerverdien.
#### Alternativer

**Bokføringsdato**: Angi dato for revalueringen.

**Dokumentnr.**: Angi nummeret på revalueringskladdelinjene. Hvis det er definert en nummerserie på varekladdnavnet, følger dokumentnummeret postene som er utført av bokføringen av revalueringskladden. Hvis ikke kan du angi et nummer manuelt.

**Varekladdemal**: Angi navnet på revalueringskladdemalen.

**Varekladdenavn**: Angi navnet på den aktuelle revalueringskladden

Velg **OK** når du vil starte kjørselen. Hvis du ikke vil kjøre kjørselen nå, velger du **Avbryt** for å lukke vinduet.

## Se også

[Utformingsdetaljer: Lagermetoder](design-details-costing-methods.md)  
[Oppdater standardkost](finance-how-to-update-standard-costs.md)  
[Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md)  
[Arbeid med monteringsstykklister](assembly-how-work-assembly-boms.md)  
[Opprette produksjonsstykklister](production-how-to-create-production-boms.md)  
[Arbeid med stykklister](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
