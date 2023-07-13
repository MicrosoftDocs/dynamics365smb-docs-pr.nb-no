---
title: Innføring i Contoso Coffee-produksjon
description: Oversikt over scenarioer for hvordan Contoso Coffee-demo data kan hjelpe deg å lære hvordan du bruker produksjonsfunksjonene i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: 4760
author: edupont04
ms.author: andreipa
---

# <a name="introduction-to-contoso-coffee-manufacturing"></a>Innføring i Contoso Coffee-produksjon

Contoso Coffee er et fiktivt selskap som produserer forbrukerkaffemaskiner og kommersielle kaffemaskiner. **Contoso Coffee**-appene for Business Central legger til demonstrasjonsdata som du kan bruke til å lære hvordan du bruker produksjonsfunksjonene i Business Central.  

Appen har fire produkter som er optimalisert for ulike scenarioer:

- **SP-SCM1009 Airpot**  

  Dette produktet er en stykkliste med en delmontering, **Ruting**. Bruk dette til å demonstrere standard produksjonsflyt. Den er definert med alternative rutinger som du kan bruke til å demonstrere ulike scenarioer som involverer underleverandører. Lagermetoden er *Standard*.  

- **SP-SCM1011 Airpot Duo**  

  Dette produktet krever varesporing og har en komponent som også krever varesporing. Lagermetoden er *Spesifikk*.  

- **SP-SCM1004 Autodrip**  

  Dette produktet er en stykkliste med en delmontering, **Ruting**. Vi anbefaler den for å demonstrere de forskjellige trekkmetodene, både for komponenter og operasjoner. Lagermetoden er *Standard*.

- **SP-SCM1006 AutoDripLite**

  Dette produktet har tre varianter og tre stykklister som kan knyttes til lagerføringsenheter. Produktet bruker fantomstykklistekonseptet. Lagermetoden er *Standard*.

Produksjonsaktivitetene for alle scenarioene bruker *NORD*-lokasjonen.  

> [!IMPORTANT]
> Før du kjører noen av scenarioene for Contoso Coffee, må du bokføre eventuelle varekladdelinjer med åpningssaldoer. Hvis du vil ha flere krav, kan du se [Konfigurer Contoso Coffee-data](#set-up-contoso-coffee-manufacturing-data).

## <a name="set-up-contoso-coffee-manufacturing-data"></a>Konfigurer data for Contoso Coffee-produksjon

For å kunne bruke demodata for Contoso Coffee-produksjon må du installere to apper i det aktuelle selskapet i [!INCLUDE [prod_short](../../includes/prod_short.md)]:  

- **Demodatasett for Contoso Coffee**  

    Denne appen inneholder demonstrasjonsdata for basisprogrammet.  
- **Demodatasett for Contoso Coffee (land-ID)**  

    Denne appen legger til land- eller områdespesifikt innhold oppå basisprogrammet.

Legg til appene i et tomt selskap i et betalt abonnement eller som en del av en prøveversjon. Opprett for eksempel et nytt selskap uten eksempeldata fra den assisterte veiledningen **Opprett nytt selskap** som du kan åpne fra **Selskaper**-oversikten. Deretter legger du til appene fra [markedsplassen](../../ui-extensions-install-uninstall.md#install), hvis de ikke allerede er oppført på siden **Utvidelsesbehandling**-side.  

Når de relevante appene er installert, går du til [Demodata for Contoso Coffee](https://businesscentral.dynamics.com/?page=4760)-siden i [!INCLUDE [prod_short](../../includes/prod_short.md)] og endrer standardinnstillingene etter behov. Tabellen nedenfor beskriver innstillingene:  

|Felt  |Beskrivelse  |
|---------|---------|
|**Startår** |Angir det første året du vil bruke for Contoso Coffee-demondataene. Året er enten et kalenderår eller et regnskapsår, avhengig av firmaoppsettet.|
|**Produksjonslokasjon** |Angir lageret som du vil bruke for produksjonsoperasjoner. Standarden er *NORD*, men du kan endre den etter behov.|
|**Selskapstype**    |Angir om det aktuelle selskapet må rapportere mva. eller salgsmva. |
|**Innenlands – generell firmabokføringsgrupper**|Angir en firmakode for innenlandske kunder og leverandører. Firmakodene brukes når transaksjoner bokføres. |
|**Kapasitet – generell varebokføringsgruppe**    |Angir en kode for varer eller ressurser som må brukes for bokføring av kapasitet.|
|**Detalj – generell varebokføringsgruppe**    |Angir en kode for varer eller ressurser som må brukes for bokføring av detaljhandel.|
|**Rå – generell varebokføringsgruppe**    |Angir en kode for varer eller ressurser som må brukes for bokføring av råvarer. |
|**Standard mva-kode**    |Angir en eksisterende mva-varebokføringsgruppe som skal brukes for varer.|
|**Ferdigkode**    |Angir en eksisterende varebokføringsgruppe som skal brukes for ferdige varer.|
|**Prisfaktor**     |Angir en faktor for å konvertere en pris fra USD/EUR til den lokale valutaen. *1* betyr at prisen er det samme beløpet i hvilken som helst valuta. Et høyere nummer brukes til å hente prisen i lokal valuta. |
|**Avrundingspresisjon**  |Definerer hvordan beregnet forbruksantall avrundes når de er angitt på forbrukskladdelinjer. Antall som er mindre enn 0,5 vil bli rundet ned. Antall som er større eller lik 0,5 vil bli rundet opp.|

Når du er klar, velger du **Opprett demonstrasjonsdata**-handling. Det tar noen minutter å legge til dataene i den underliggende databasen, men da er du klar til å kjøre de ulike scenarioene.  

## <a name="scenarios"></a>Scenarier

Demodata for Contoso Coffee-produksjon støtter nå følgende scenarioer for test og opplæring:

1. [Opprett en ny produksjonsstykkliste og stykklisteversjon](create-new-production-bom-version.md)  
2. [Opprett en ny rute](create-new-routing.md)  
3. [Opprett en fast planlagt produksjonsordre og endre den](create-firm-planned-production-order-change.md)  
4. [Kombiner automatisk og manuell trekking](combine-automatic-manual-flushing.md)  
5. [Bruk ordreplanlegging til å opprette og reservere forsyning](order-planning-create-reserve-supply.md)  
6. [Definer og behandle en underleveranseoperasjon](set-up-process-subcontracting-operation.md)  
7. [Definer ny kapasitet](set-up-new-capacity.md)  
8. [Forutse behov for varevarianter med ulike stykklister tildelt](variants.md)  

Les trinnene for hvert scenario i den relevante artikkelen.  

> [!IMPORTANT]
> Disse gjennomgangene krever at brukeropplevelsen er satt til *Premium* på siden **Firmainformasjon**.

## <a name="see-also"></a>Se også

[Produksjon](../../production-manage-manufacturing.md)  
[Produksjonsrapporter og analyser i Business Central](../../production-reports.md)  
