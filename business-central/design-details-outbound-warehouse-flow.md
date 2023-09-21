---
title: Oversikt over utgående lagerprosesser
description: Denne artikkelen beskriver den utgående lagerarbeidsflyten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# <a name="outbound-warehouse-processes"></a>Utgående lagerprosesser

Utgående prosesser i lagre starter når du frigir et kildedokument for å ta varene ut av en lagerlokasjon. Det kan for eksempel være å sende varene et eller annet sted eller flytte dem til en annen selskapslokasjon. I prinsippet består leveringsprosessen av utgående ordrer av to aktiviteter:

* Plukk varer fra hyller.
* Leveringsvarer fra lageret.

Kildedokumentene for utgående lagerflyt er:  

* Ordre  
* Utgående overføringsordre  
* Bestillingsretur  
* Serviceordre  

> [!NOTE]
> Produksjons- og monteringsordrer med komponentbehov representerer også utgående kildedokumenter. Produksjons- og monteringsordrer er litt forskjellige fordi de vanligvis er interne prosesser som ikke involverer levering. De brukes i stedet til å plassere varer som er produsert, eller til å flytte komponentene som trengs for å montere en vare i et monteringsområde. Finn ut mer om disse prosessene under [Utformingsdetaljer: Interne lagerflyter](design-details-internal-warehouse-flows.md).  

I [!INCLUDE[prod_short](includes/prod_short.md)] plukker og leverer du varer ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Utgående prosess|Plukk nødv.|Levering nødv.|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Bokføre plukking og levering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre plukking og levering fra et lagerplukkdokument|Slått på||Grunnleggende: ordre for ordre.|  
|U|Bokføre plukking og levering fra en lagerfølgeseddel||Slått på|Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre plukking fra et lagerplukkdokument og bokføre leveringen fra en lagerfølgeseddel|Slått på|Slått på|Avansert|  

Hvilken metode som er aktuell å velge, avhenger av lagerpraksis og organisasjonens kompleksitet. Nedenfor følger noen eksempler som kan hjelpe deg med å bestemme.

* I et ordre for ordre-miljø med enkle prosesser og enkel hyllestruktur, er metode A riktig, plukk og forsendelse fra ordrelinjen.
* Hvis varene for en ordrelinje kommer fra mer enn én hylle, eller hvis lagerarbeidere ikke kan arbeide med ordredokumenter, er bruken av separate plukkdokumenter passende, metode B.
* Hvis plukk- og leveringsprosessene omfatter flere ordrer og krever større kontroll og oversikt, kan du velge å bruke et lagerleveringsdokument og et lagerplukkdokument til å skille plukk- og leveringsoppgaver, metode C og D.  

I metode A, B og C kombineres plukk- og leveringsaktiviteter i ett trinn når et dokument bokføres som levert. I metode D registrerer du først plukk, og deretter bokføres leveringen på et senere tidspunkt fra et annet dokument.

> [!NOTE]
> Selv om lagerplukk og lagerplukk høres ut, er de forskjellige dokumenter og brukes i forskjellige prosesser.
> * Lagerplukk som brukes i metode B sammen med informasjon om plukkinformasjon, bokfører også leveringen av kildedokumentet.
> * Lagerplukk som brukes i metode D, kan ikke bokføres, og den registrerer bare plukk. Registreringsprosessen gjør varer tilgjengelige for lagerlevering, men bokfører ikke leveringen. I utgående flyt krever lagerplukk en lagerlevering.

## <a name="no-dedicated-warehouse-activity"></a>Ingen dedikert lageraktivitet

Følgende artikler inneholder informasjon om hvordan du behandler mottak for kildedokumenter hvis du ikke har egne lageraktiviteter.

* [Selg produkt](sales-how-sell-products.md)
* [Overføringsordrer](inventory-how-transfer-between-locations.md)
* [Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)
* [Opprette serviceordrer](service-how-to-create-service-orders.md)

## <a name="basic-warehouse-configurations"></a>Enkle lageroppsett

Diagrammet nedenfor illustrerer utgående lagerprosesser for ulike typer dokumenter i enkle lageroppsett. Tallene i diagrammet svarer til trinnene nedenfor diagrammet.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Viser trinnene i en grunnleggende utgående flyt på et lager.":::

### <a name="1-release-a-source-document"></a>1: Frigi et kildedokument

Når du bruker handlingen **Frigi** i et kildedokument, for eksempel en ordre eller overføringsordre, er varene i dokumentet klare til å håndteres i lageret. For eksempel plukket og plassert i hyllen som er angitt i dokumentet. Du kan også opprette lagerplukkdokumenter for enkelte ordrelinjene på ordrer med en push-metode, basert på angitte hyller og antall som skal håndteres.  

### <a name="2-create-an-inventory-pick"></a>2: Opprett et lagerplukk

På siden **Lagerplukking**  henter lagerarbeideren, i en hent-måte, kildedokumentlinjene. Det kan også hende at lagerplukklinjene allerede er opprettet med en push-metode, av brukeren som er ansvarlig for kildedokumentet.  

### <a name="3-post-an-inventory-pick"></a>3: Bokfør et lagerplukk

På hver linje for varer som er plukket eller flyttet, helt eller delvis, fyller du ut feltet **Antall** og bokfører deretter lagerplukket. Kildedokumenter som er knyttet til lagerplukkingen, bokføres som levert eller forbrukt.  

For vareplukk blir det opprettet negative vareposter og lagerposter, og plukkforespørselen slettes hvis ferdigbehandlet. Eksempel: Feltet **Levert (antall)** i den utgående kildedokumentlinjen oppdateres. Det opprettes et postert leveringsdokument som for eksempel gjenspeiler ordren og de leverte varene.  

## <a name="advanced-warehouse-configurations"></a>Avanserte lageroppsett

Diagrammet nedenfor illustrerer utgående lagerprosesser for ulike typer dokumenter i avanserte lageroppsett. Tallene i diagrammet svarer til trinnene nedenfor diagrammet.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Viser trinnene i en avansert utgående lagerflyt.":::

### <a name="1-release-a-source-document-1"></a>1: Frigi et kildedokument

Å frigi et kildedokument i avanserte oppsett gjør det likt for enkle oppsett. Varene blir tilgjengelige for behandling i lageret. De kan for eksempel inkluderes i en levering.  

### <a name="2-create-a-warehouse-shipment"></a>2: Opprett en lagerlevering

På siden **Lagerlevering** hentes linjene fra det frigitte kildedokumentet. Du kan kombinere linjer fra flere kildedokumentlinjer i én lagerlevering.  

### <a name="3-create-a-warehouse-pick"></a>3: Opprett et lagerplukk

På siden **Lagerlevering** oppretter du lagerplukkaktiviteter for lagerleveringer på en av to måter:

- På en push-måte, der du bruker **Opprett plukk**-handlingen. Velg linjene som skal plukkes, og klargjør plukkingene ved å angi hvilke hyller det skal tas fra og hvilke det skal plasseres i, og hvor mange enheter som skal håndteres. Hyllene kan være forhåndsdefinert for lagerlokasjonen eller ressursen.
- På en pull-måte, der du bruker **Frigi**-handlingen. På siden **Plukkforslag** kan lagerarbeidere bruke handlingen **Hent lagerdokumenter** til å få tildelt plukkinger. Når lagerplukkingene er fullstendig registrert, slettes linjene i **Plukkforslag**.

### <a name="4-register-a-warehouse-pick"></a>4: Registrer et lagerplukk

På siden **Lagerplukk** fyller lagermedarbeider ut feltet **Antall** for hver linje som er fullstendig eller delvis plukket, og registrerer plukket.

Lagerposter opprettes, og lagerplukklinjene slettes hvis hele antallet ble plukket. Lagerplukkdokumentet holdes åpent til hele antallet for lagerleveringen er registrert. Feltet **Plukket ant.** på lagerleveringslinjene oppdateres tilsvarende.  

### <a name="5-post-the-warehouse-shipment"></a>5: Bokfør lagerleveringen

Når alle varene i lagerleveringsdokumentet er registrert som plukket, bokfører lagermedarbeideren leveringen. Bokføring oppdaterer varepostene slik at de gjenspeiler reduksjonen i lageret. Eksempel: Feltet **Levert (antall)** i den utgående kildedokumentlinjen oppdateres.  

## <a name="see-also"></a>Se også

[Lagerstyring](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
