---
author: brentholtorf
ms.topic: include
ms.date: 03/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
Når du mottar en faktura fra et selskap i utenlandsk valuta, er det ganske enkelt å beregne den lokale valutaverdien (LV) for fakturaen basert på dagens valutakurs. Fakturaen leveres imidlertid ofte med betalingsbetingelser, slik at du kan forsinke betalingen til en senere dato, som innebærer en mulig annen valutakurs. Dette problemet i kombinasjon med at valutakurser alltid avviker fra de offisielle valutakursene gjør det umulig å forutse det nøyaktige beløpet i den lokale valutaen (LV) som kreves for å dekke fakturaen. Hvis fakturaens forfallsdato går til neste måned, må du kanskje også revaluere det lokale valutabeløpet (LV) på slutten av måneden. Du må definere valutajusteringen fordi den nye LV-verdien som kreves for å dekke fakturabeløpet, kan være forskjellig, og selskapets gjeld for leverandøren er muligens endret. Det nye beløpet i LV kan være høyere eller lavere enn det forrige beløpet, og representerer derfor en gevinst eller et tap. Men siden fakturaen ikke er betalt ennå, regnes gevinst eller som *urealisert*. Senere betales fakturaen, og banken har returnert den med den faktiske valutakursen for betalingen. Det er ikke før nå *realisert* gevinst eller tap er beregnet. Urealisert gevinst eller tap tilbakeføres deretter, og faktisk gevinst eller tap bokføres i stedet.

I eksemplet nedenfor er en faktura mottatt den 1. januar med valutabeløpet på 1 000. På tidspunktet er valutakursen er 1,123.

|Dato|Handling|Valutabeløp|Dokumentsats|LV-beløp på dokument|Justeringssats|Beløp for urealisert agio|Betalingssats|Beløp for realisert disagio|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Fakturering**|1000|1,123|1123|||||
|1/31|**Justering**|1000||1125|1,125|2|||
|2/15|**Justeringstilbakeføring på betaling**|1000||||-2|||
|2/15|**Betaling**|1000||1120|||1,120|–3|

På slutten av måneden utføres det en valutajustering der justeringsvalutakursen er satt til 1,125, som utløser en urealisert agio på 2.

På betalingstidspunktet viser den faktiske valutakursen som er registrert på banktransaksjonen, en valutakurs på 1,120.

Her finnes en urealisert transaksjon, og derfor blir den tilbakeført sammen med betalingen.

Til slutt registreres betalingen, og det faktiske tapet blir postert til kontoen for realisert disagio.
