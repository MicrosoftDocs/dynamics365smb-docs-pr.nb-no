---
title: Gjennomgang – kjøre en salgskampanje | Microsoft-dokumentasjon
description: En kampanje er en hvilken som helst type aktivitet som omfatter flere kontakter. En viktig del av å lage en kampanje er å velge målgruppen for kampanjen. I Business Central kan du opprette et segment eller en gruppe kontakter ved å bruke filtre, for dette formålet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 53bc7faefc01399ae8db1d0763bc6ec91745b7b5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3195294"
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Gjennomgang: kjøre en salgskampanje
En kampanje er en hvilken som helst type aktivitet som omfatter flere kontakter. En viktig del av å lage en kampanje er å velge målgruppen for kampanjen. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du opprette et segment eller en gruppe kontakter ved å bruke filtre, for dette formålet.  

 Du bruker disse funksjonene i Salg og markedsføring til å planlegge markedsføringsaktivitetene omhyggelig og å håndtere samhandling med kontakter og kunder. Du kan opprette kampanjer og definere segmenter for kontaktene for utsendelser og andre typer samhandlinger med kontaktene og potensielle kunder.  

 Du kan bruke funksjonene for kampanje og segment samt de automatiserte prosessene i dem til å planlegge, organisere og holde rede på markedsføringsaktivitetene. Dette øker mulighetene for å få nye kunder og beholde eksisterende kunder.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen  
 Denne gjennomgangen viser fremgangsmåten for oppfølging av en varemesse og utvalg av potensielle kunder (kontakter) i en oppfølgingskampanje.  

 Gjennomgangen introduserer funksjonen for håndtering av kampanje og segment i avdelingen Salg og markedsføring. Denne gjennomgangen tar for seg følgende oppgaver:  

-   Opprette en kampanje  
-   Velge målgruppen  
-   Utvinne data  
-   Sende brev til kontakter  
-   Registrere kampanjesvar  

## <a name="roles"></a>Roller  
 Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

-   Markedsføringssjef eller salgssjef  
-   Markedsføringsmedarbeider  

## <a name="prerequisites"></a>Forutsetninger  
 Før du kan utføre oppgavene i gjennomgangen, må du installere [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="story"></a>Hovedscenario  
 Markedsføringssjefen i salgsavdelingen hos CRONUS har ansvaret for å planlegge og kjøre kampanjer. Han bestemmer også hvilke varemesser de skal delta på, og han evaluerer kampanjefremdriften.  

 Markedsføringsmedarbeideren i markedsføringsavdelingen håndterer produksjon, distribusjon og plassering av markedsføringsmateriell.  

 Selskapet har nettopp lansert et nytt produkt de kaller Millenniumserver. Produktet ble nylig presentert på en varemesse, Data Futurus. Mange kunder viste stor interesse for produktet, og som en del av et salgsfremmende tiltak får kunder Millenniumserver til en egen kampanjepris når de kjøper den i løpet av en kampanjeperiode.  

 En av oppgavene til markedsføringsmedarbeideren etter varemessen er å registrere alle potensielle kunder som kontakter.  

 Markedsføringssjefen oppretter en kampanje og et segment som inneholder alle nye kontakter, og utvinner deretter kontaktdataene for å velge ut målgruppen for kampanjen.  

 Medarbeideren hjelper til med å sende ut takkebrev til alle kontaktene som gav visittkortene sine til de ansatte ved standen, og til slutt registrerer sjefen alle svarene de mottar fra de potensielle kundene.  

## <a name="setting-up-a-campaign"></a>Opprette en kampanje  
 Så snart medarbeideren har registrert visittkortene som ble mottatt på varemessen, oppretter markedsføringssjefen et kampanjekort for å håndtere aktivitetene i kampanjen.  

### <a name="to-set-up-a-campaign"></a>Slik oppretter du en kampanje:  

1.  Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kampanjer**, og velg deretter den relaterte koblingen.  
2.  Velg **Ny** for å opprette en ny kampanje. Trykk Enter på kampanjekortet for å få et kampanjenummer til å settes inn automatisk.  
3.  Skriv inn en beskrivelse for kampanjen i **Beskrivelse**-feltet, for eksempel **FUTURUS varemesse**.  
4.  Velg **Statuskode**-feltet, og velg en statuskode fra listen som åpnes på siden **Kampanjestatus**.  
5.  Fyll ut feltene **Startdato** og **Sluttdato** i kampanjen med de aktuelle datoene.  

## <a name="selecting-the-target-audience"></a>Velge målgruppen  
 Markedsføringssjefen oppretter et segment for å velge kontaktene han vil kommunisere med.  

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Slik oppretter du et segment med de relevante kontaktene:  

1.  Velg handlingen **Segmenter**.  
2.  Velg **Ny** for å opprette et nytt segment. Trykk Enter på segmentkortet for å få et segmentnummer til å settes inn automatisk.  
3.  Skriv inn for eksempel **Besøkende på varemessen FUTURUS** i **Beskrivelse**-feltet på hurtigfanen **Generelt**.  

     Når du har skrevet inn generell informasjon om segmentet, velger du kontaktene som skal inkluderes i det.  

     Du kan bruke mange ulike kriterier for å velge kontakter. Du kan for eksempel velge kontaktpersoner som arbeider hos en kunde eller en potensiell kunde, og som er innkjøpsansvarlige i selskapet.  

     Du bruker filtre til å legge til kontakter i henhold til kriteriene som passer best til formålene. Du kan for eksempel filtrere etter ansvarsområdet til kontaktpersonen eller forretningsforbindelsen eller bransjen til kontaktselskapet. I denne gjennomgangen bruker du **Ansvarsområde**-filteret til å velge kontakter.  

4.  Velg handlingen **Legg til kontakter** på siden **Segment** for å åpne filteret **Legg til kontakter**.  
5.  Velg **Kjøp**-filteret som **Ansvarsområde - kode** på hurtigfanen **Ansvarsområde**, og velg **OK**.  

     **Segment**-siden inneholder nå en liste over kontakter basert på filteret du har angitt. På fanebladet **Generelt**, i feltet **Antall linjer** kan du med et raskt blikk se hvor mange kontakter som oppfyller disse kriteriene.  

    > [!NOTE]  
    >  Du kan lagre segmenteringskriteriene, slik at du kan bruke dem senere.

    1.  På **Segment**-siden velger du handlingen **Segment** og deretter **Lagre kriterier**.  
    2.  Angi en kode for segmentet på siden **Lagre segmentkriterier**. Skriv inn en beskrivelse av segmentkriteriet i **Beskrivelse**-feltet.
    3.  Velg **OK**-knappen.  

## <a name="mining-the-data"></a>Utvinne dataene  
 Markedsføringssjefen ser nærmere på den segmenterte listen over kontakter og finner ut at listen er altfor lang. Han bestemmer seg for å korte ned listen basert på faktiske potensielle kunder for å sikre at han fokuserer på riktig målgruppe. Denne raffineringen og reduseringen av dataene kalles også datautvinning.  

### <a name="to-remove-contacts-from-the-segment"></a>Slik fjerner du kontakter fra segmentet:  

1.  Velg **Kontakter**-handlingen på siden **Segment**, og velg deretter **Reduser kontakter** for å åpne siden **Fjern kontakter - reduser**.  
2.  Velg **PROS**-filteret som **Forretn.forbindelseskode** på hurtigfanen **Forretningsforbindelse**, og velg **OK**.  

     Nå inneholder **Segment**-siden en redusert liste over kontakter, og antallet kontakter som nå oppfyller disse kriteriene, vises nå i feltet **Antall linjer**.  

    > [!NOTE]  
    >  Hvis du må reversere denne fjerningen av en kontaktgruppe, kan du bruke funksjonen **Gå tilbake**. Med andre ord kan du angre den siste segmenteringen.  
    >   
    >  På siden **Segment** velger du handlingen **Segment** og deretter **Gå tilbake**.  
    >   
    >  Kontaktene du nettopp fjernet, legges til i listen over kontakter på nytt.  

## <a name="linking-a-segment-to-a-campaign"></a>Knytte et segment til en kampanje  
 Markedsføringssjefen bestemmer seg for at den reduserte listen er den endelige listen over kontakter han vil skal være en del av kampanjen. Han knytter derfor dette segmentet til kampanjen FUTURUS varemesse.  

### <a name="to-link-a-segment-to-the-campaign"></a>Slik knytter du et segment til kampanjen:  

1.  På siden **Segment** i hurtigfanen **Kampanje** velger du **Kampanjenr.** -feltet for å velge kampanjen som du vil segmentet skal knyttes til, for eksempel **KM0001**.  
2.  Velg **Kampanjemål**-avmerkingsboksen siden dette segmentet er målgruppen for kampanjen.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Sende brev og e-postmeldinger til kontakter  
 Markedsføringsmedarbeideren hjelper markedsføringssjefen med å sende ut korrespondanse til de potensielle kundene, der han takker dem for besøket på varemessen.  

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Slik bruker du et segment til å sende et brev til en kontakt:  

1.  Åpne **Segment**-kortet for **Besøkende på varemessen FUTURUS**.  
2.  På hurtigfanen **Samhandling**, under **Samhandlingsmal - kode**, velger du malen Forretningsbrev, kode **FORR**.  
3.  I feltet **Emne (standard)** angir du følgende eksempeltekst: **Takk for at du besøkte varemessen**.  

    > [!NOTE]  
    >  Denne malen består av flere vedlegg, og hvert av dem er skrevet på et ulikt språk. Engelsk og dansk er eksempler på språk som er inkludert.  

4.  Velg feltet **Språkkode (standard)** for å åpne siden **Samhandlingsspråk for segment**. Velg en språkkode og deretter **OK**-knappen.  
5.  Du kan vise dokumentet på det valgte språket. Velg handlingen **Vedlegg** og deretter **Åpne**.  

     Du svarer på meldingen med spørsmål om tillatelse til å starte Word ved å velge **Tillat for denne klientøkten**.  

     Dette åpner det vedlagte Word-dokumentet slik at du kan undersøke det. Du kan også benytte denne anledningen til å redigere og endre brevet. Lukk Word når du er ferdig.  

6.  Skriv inn emnet for brevet i **Emne**-feltet på språket som er valgt for malen.  
7.  Velg handlingen **Logg**.
8.  Merk av for **Send vedlegg** for å skrive ut vedleggene.  

    1. Merk av for **Opprett oppfølgingssegment**.  
    2. Velg **OK**-knappen for å starte kjørselen **Loggfør segment**.  

9. Vedleggene sendes. Når prosessen er ferdig, velger du **OK** i meldingen om at segmentet er loggført.  

     Brevene skrives ut automatisk og segmentet loggføres. Siden segmentet er loggført, finnes det ikke lenger i listen over segmenter. Det er flyttet til listen over loggførte segmenter. Hvis du vil vise den listen, velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Loggførte segmenter**, og velger deretter den relaterte koblingen.  

10. Når segmentet er loggført, registreres hvert sendte brev som en samhandling, som du kan se i loggen.  

     Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Samhandlingsposter**, og velg deretter den relaterte koblingen. Det finnes en post for hvert sendte brev.  

### <a name="to-send-an-email-message-to-a-contact"></a>Sende en e-postmelding til en kontakt  

1.  På hurtigfanen **Samhandling**, under **Samhandlingsmal - kode**, velger du malen Forretningsbrev, kode **FORR**.  
2.  I feltet **Emne (standard)** angir du følgende eksempeltekst: **Takk for at du besøkte varemessen**.  
3.  Velg **E-post** i **Korrespondansetype**-feltet.  
4.  Angi språkinnstillinger, som i forrige fremgangsmåte.  
5.  Velg handlingen **Logg**. **Loggfør segment**-siden åpnes.  
6.  Merk av for **Send vedlegg** for å sende vedleggene via e-post.  
7.  Merk av for **Opprett oppfølgingssegment**.  
8.  Velg **OK**.  

     Brevene sendes automatisk via e-post og segmentet loggføres. Siden segmentet er loggført, finnes det ikke lenger i listen over segmenter. Det er lagret i listen over loggførte segmenter. Hvis du vil vise den listen, velger du ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Loggførte segmenter**, og velger deretter den relaterte koblingen.  

## <a name="registering-campaign-responses"></a>Registrere kampanjerespons  
 De potensielle kundene svarer på brevet i løpet av de neste par ukene. Markedsføringssjefen ønsker å holde rede på disse svarene og registrerer dem.  

 Opprett et segment for kontaktene som har svart på brevet, for dette formålet.  

### <a name="to-register-campaign-responses"></a>Slik registrerer du kampanjerespons:  

1.  Vis hurtigfanen **Samhandling** på siden **Segment**.  
2.  Velg feltet **Samhandlingsmal - kode**.  

     Det finnes ingen samhandlingsmal for å registrere respons på kampanjer. Opprett derfor en ny mal.  

3.  Velg handlingen **Ny** på siden **Samhandlingsmaler**.  
4.  Angi **RESP** i **Kode**-feltet, og angi **Kampanjerespons** i **Beskrivelse**-feltet.  
5.  Velg **OK**-knappen.  
6.  Velg denne samhandlingsmalen i feltet **Samhandlingsmal - kode**, og bekreft meldingen med spørsmål om du vil oppdatere segmentlinjene med den samme koden for samhandlingsmal.  

     Nå angir du at disse kontaktene har svart på kampanjen:  
7.  I hurtigfanen **Kampanje** i **Kampanjenr.** -feltet, velger du kampanje.  
8.  La **Kampanjenr.** -feltet være tomt, og bekreft meldingen med spørsmål om du vil oppdatere segmentlinjene med den samme koden for samhandlingsmal.  
9. Velg **Kampanjerespons**-feltet, og bekreft den påfølgende meldingen.  

     Loggfør segmentet for å kontrollere at samhandlingene registreres.  
10. Velg **Logg**-handlingen på siden **Segment**.  
11. Fjern merket for **Send vedlegg** på siden **Loggfør segment**, og velg deretter **OK**, og bekreft meldingen som vises.  

     Når segmentet er loggført, blir det automatisk opprettet en post for kampanjen på siden **Kampanjeposter** for å registrere denne handlingen.  

## <a name="see-also"></a>Se også  
[Forbindelser](marketing-relationship-management.md)  
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
