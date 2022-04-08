---
title: 'Gjennomgang: kjøre en salgskampanje'
description: Denne gjennomgangen gir en detaljert oversikt over alle oppgavene som gjelder når du utfører en salgskampanje i Business Central.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: 4afda1c307f0f327196ad3dc0d53d74842bf3d9f
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523077"
---
# <a name="walkthrough-conducting-a-sales-campaign"></a>Gjennomgang: kjøre en salgskampanje

En kampanje er en hvilken som helst type aktivitet som omfatter flere kontakter. En viktig del av å lage en kampanje er å velge målgruppen for kampanjen. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du opprette et segment eller en gruppe kontakter ved å bruke filtre, for dette formålet.  

 Du bruker disse funksjonene i Salg og markedsføring til å planlegge markedsføringsaktivitetene omhyggelig og å håndtere samhandling med kontakter og kunder. Du kan opprette kampanjer og definere segmenter for kontaktene for utsendelser og andre typer samhandlinger med kontaktene og potensielle kunder.  

 Du kan bruke funksjonene for kampanje og segment samt de automatiserte prosessene i dem til å planlegge, organisere og holde rede på markedsføringsaktivitetene. Dette øker mulighetene for å få nye kunder og beholde eksisterende kunder.  

## <a name="about-this-walkthrough"></a>Denne gjennomgangen

 Denne gjennomgangen viser fremgangsmåten for oppfølging av en varemesse og utvalg av potensielle kunder (kontakter) i en oppfølgingskampanje.  

 Gjennomgangen introduserer funksjonen for håndtering av kampanje og segment i avdelingen Salg og markedsføring. Denne gjennomgangen tar for seg følgende oppgaver:  

- Klargjøre dataene.
- Opprette en kampanje  
- Velge målgruppen  
- Utvinne data  
- Sende brev til kontakter  
- Registrere kampanjesvar  

## <a name="roles"></a>Roller

 Denne gjennomgangen viser oppgaver som utføres av følgende brukerroller:  

- Markedsføringssjef eller salgssjef  
- Markedsføringsmedarbeider  

## <a name="prerequisites"></a>Forutsetninger

 Før du kan utføre oppgavene i gjennomgangen, må du installere [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="story"></a>Hovedscenario

 Markedsføringssjefen i salgsavdelingen hos CRONUS har ansvaret for å planlegge og kjøre kampanjer. Han bestemmer også hvilke varemesser de skal delta på, og han evaluerer kampanjefremdriften.  

 Markedsføringsmedarbeideren i markedsføringsavdelingen håndterer produksjon, distribusjon og plassering av markedsføringsmateriell.  

 Selskapet har nettopp lansert et nytt produkt de kaller Rome Guest Chair. Produktet ble nylig presentert på en varemesse, Office Futurus. Mange kunder viste stor interesse for produktet, og som en del av et salgsfremmende tiltak får kunder Rome Guest Chair til en egen kampanjepris når de kjøper den i løpet av en kampanjeperiode.  

 En av oppgavene til markedsføringsmedarbeideren etter varemessen er å registrere alle potensielle kunder som kontakter.  

 Markedsføringssjefen oppretter en kampanje og et segment som inneholder alle nye kontakter, og utvinner deretter kontaktdataene for å velge ut målgruppen for kampanjen.  

 Medarbeideren hjelper til med å sende ut takkebrev til alle kontaktene som gav visittkortene sine til de ansatte ved standen, og til slutt registrerer sjefen alle svarene de mottar fra de potensielle kundene.  

## <a name="setting-up-a-campaign"></a>Opprette en kampanje

 Så snart medarbeideren har registrert visittkortene som ble mottatt på varemessen, oppretter markedsføringssjefen et kampanjekort for å håndtere aktivitetene i kampanjen.  

### <a name="to-set-up-a-campaign"></a>Slik oppretter du en kampanje:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kampanjer**, og velg deretter den relaterte koblingen.  
2. Velg **Ny** for å opprette en ny kampanje. Trykk på **Enter** på kampanjekortet for å få et kampanjenummer til å settes inn automatisk.  
3. Skriv inn en beskrivelse for kampanjen i **Beskrivelse**-feltet, for eksempel **Office Futurus varemesse**.  
4. Velg **Statuskode**-feltet, og velg statuskoden 1-PLAN. 
5. Fyll ut feltene **Startdato** og **Sluttdato** i kampanjen med de aktuelle datoene.  

## <a name="selecting-the-target-audience"></a>Velge målgruppen

 Markedsføringssjefen oppretter et segment for å velge kontaktene de vil kommunisere med.  
 
 Når du oppretter et segment, kan du bruke en rekke kriterier til å velge hvilke kontakter som skal være mål for segmentet. Du kan for eksempel velge kontaktpersoner som arbeider hos en kunde eller en potensiell kunde, og som er innkjøpsansvarlige i selskapet. Du bruker filtre til å legge til kontakter i henhold til kriteriene som passer best til formålene. Du kan for eksempel filtrere etter ansvarsområdet til kontaktpersonen eller forretningsforbindelsen eller bransjen til kontaktselskapet. I denne gjennomgangen bruker vi **Ansvarsområde**-filteret til å velge kontakter.

### <a name="to-create-a-segment-with-the-relevant-contacts"></a>Slik oppretter du et segment med de relevante kontaktene:  

1. Velg handlingen **Naviger** og deretter **Segmenter**.  
2. Velg **Ny** for å opprette et nytt segment. Velg **Enter** på segmentkortet for å få et segmentnummer til å settes inn automatisk.  
3. Skriv inn for eksempel **Besøkende på varemessen Office Futurus** i **Beskrivelse**-feltet på hurtigfanen *Generelt*.
4. Velg handlingen **Legg til kontakter** for å åpne filteret **Legg til kontakter**.  
5. Bla ned til hurtigfanen **Kontaktens ansvarsområder**, velg **Kjøp**-filteret som **Ansvarsområde – kode**, og velg knappen **OK**.  

**Segment**-siden inneholder nå en liste over kontakter basert på filteret du har angitt. På fanebladet **Generelt**, i feltet **Antall linjer** kan du med et raskt blikk se hvor mange kontakter som oppfyller disse kriteriene.  

> [!NOTE]  
> Du kan lagre segmenteringskriteriene, slik at du kan bruke dem senere.

### <a name="to-save-your-segmentation-criteria"></a>Slik lagrer du segmenteringskriteriene

1. Velg **Handlinger** på siden **Segment**.
2. Velg **Funksjoner**, deretter **Segment** og velg handlingen **Lagre kriterier**.  
3. Angi en kode for segmentet på siden **Lagre segmentkriterier**. Skriv inn en beskrivelse av segmentkriteriet i **Beskrivelse**-feltet.
4. Velg **OK**-knappen.  

## <a name="mining-the-data"></a>Utvinne dataene

 Markedsføringssjefen ser nærmere på den segmenterte listen over kontakter og finner ut at listen er altfor lang. Han bestemmer seg for å korte ned listen basert på faktiske potensielle kunder for å sikre at han fokuserer på riktig målgruppe. Denne raffineringen og reduseringen av dataene kalles også datautvinning.  

### <a name="to-remove-contacts-from-the-segment"></a>Slik fjerner du kontakter fra segmentet:  

1. Velg **Handlinger** på siden **Segment**.
2. På menylinjen under velger du **Funksjoner**, velger **Kontakter** og deretter **Reduser kontakter**.  

  Dette åpner dialogboksen **Fjern kontakter – reduser**.  
4. Velg **KUNDE**-filteret som **Forretn.forbindelseskode** på hurtigfanen **Kontaktens forr.forbindelse**, og velg knappen **OK**.

 Nå inneholder **Segment**-siden en redusert liste over kontakter, og antallet kontakter som nå oppfyller disse kriteriene, vises nå i feltet **Antall linjer**.  

 > [!NOTE]  
 > Hvis du må reversere denne fjerningen av en kontaktgruppe, kan du bruke funksjonen **Gå tilbake**. Med andre ord kan du angre den siste segmenteringen.  

### <a name="to-bring-back-the-removed-contacts"></a>Slik henter du tilbake kontakter som er fjernet

1. Velg **Segment**-handlingen på siden **Segment**.
2. Velg handlingen **Gå tilbake**.

Kontaktene du nettopp fjernet, legges til i listen over kontakter på nytt.

## <a name="linking-a-segment-to-a-campaign"></a>Knytte et segment til en kampanje

Markedsføringssjefen bestemmer seg for at den reduserte listen er den endelige listen over kontakter vedkommende vil skal være en del av kampanjen. Sjefen knytter derfor dette segmentet til kampanjen FUTURUS varemesse.  

### <a name="to-link-a-segment-to-the-campaign"></a>Slik knytter du et segment til kampanjen:  

1. På siden **Segment** i hurtigfanen **Kampanje** velger du **Kampanjenr.** -feltet for å velge kampanjen som du vil segmentet skal knyttes til, for eksempel **KM0001**.
2. Velg **Ja**.  
3. Velg **Kampanjemål**-avmerkingsboksen siden dette segmentet er målgruppen for kampanjen, og velg **Ja**.  

## <a name="sending-letters-and-email-messages-to-contacts"></a>Sende brev og e-postmeldinger til kontakter

 Markedsføringsmedarbeideren hjelper markedsføringssjefen med å sende ut korrespondanse til de potensielle kundene, der han takker dem for besøket på varemessen.

### <a name="to-use-a-segment-to-send-a-letter-to-a-contact"></a>Slik bruker du et segment til å sende et brev til en kontakt:  

> [!NOTE]  
> I denne fremgangsmåten må du legge ved et Word-dokument. Du kan legge til vedlegg på et hvilket som helst språk.

> [!NOTE]  
> Klikk om nødvendig på ikonet **Redigeringsblyant** for å åpne siden i redigeringsmodus.

1. Åpne **Segment**-kortet for **Besøkende på varemessen FUTURUS**.  
2. På hurtigfanen **Samhandling**, under **Samhandlingsmal – kode**, velger du malen Forretningsbrev, kode **FORR.** og velger **Ja**.
3. Velg feltet **Språkkode (standard)** for å åpne siden **Samhandlingsspråk for segment**. Velg en **språkkode** og deretter **OK**-knappen.
4. Kontroller at **Korrespondansetypen (standard)** er satt til **Brev**.
5. Merk av boksen **Ellipse** i feltet **Vedlegg**. Dette åpner dialogboksen Importer vedlegg.
    1. Velg knappen **Velg** for å velge filen.
    1. Finn filen, og velg **Åpne**-knappen for å legge den ved.
6. I feltet **Emne (standard)** angir du følgende eksempeltekst: **Takk for at du besøkte varemessen**. Trykk på TAB-tasten for å gå ut av feltet, og velg **Ja**-knappen.
7. Skyv **Send Word-dok.er som vedl.** til på, og velg **Ja**-knappen.
8. Velg handlingen **Logg**. I popup-vinduet Loggfør segment aktiverer du: **Opprett oppfølgingssegment**
9. Velg **OK**-knappen for å starte kjørselen **Loggfør segment**.  

Vedleggene sendes. Når prosessen er ferdig, velger du **OK** i meldingen om at segmentet er loggført.  

 Brevene skrives ut automatisk og segmentet loggføres. Siden segmentet er loggført, finnes det ikke lenger i listen over segmenter. Det er flyttet til listen over loggførte segmenter. Hvis du vil listen, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Loggførte segmenter**, og velg deretter den relaterte koblingen.  

Når segmentet er loggført, registreres hvert sendte brev som en samhandling, som du kan se i loggen.  

Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Samhandlingsposter** og velger deretter den relaterte koblingen. Det finnes en post for hvert sendte brev.  

### <a name="to-send-an-email-message-to-a-contact"></a>Sende en e-postmelding til en kontakt  

1. På hurtigfanen **Samhandling**, under **Samhandlingsmal - kode**, velger du malen Forretningsbrev, kode **FORR**.  
2. I feltet **Emne (standard)** angir du følgende eksempeltekst: **Takk for at du besøkte varemessen**.  
3. Velg **E-post** i **Korrespondansetype**-feltet.  
4. Angi språkinnstillinger, og legg ved et Word-dokument, som i forrige fremgangsmåte.  
5. Velg handlingen **Logg**. **Loggfør segment**-siden åpnes.  
6. Merk av for **Send vedlegg** for å sende vedleggene via e-post.  
7. Merk av for **Opprett oppfølgingssegment**.  
8. Velg **OK**.  

 Brevene sendes automatisk via e-post og segmentet loggføres. Siden segmentet er loggført, finnes det ikke lenger i listen over segmenter. Det er lagret i listen over loggførte segmenter. Hvis du vil listen, velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Loggførte segmenter**, og velg deretter den relaterte koblingen.  

## <a name="registering-campaign-responses"></a>Registrere kampanjerespons

 De potensielle kundene svarer på brevet i løpet av de neste par ukene. Markedsføringssjefen ønsker å holde rede på disse svarene og registrerer dem.  

 Opprett et segment for kontaktene som har svart på brevet, for dette formålet.  

### <a name="to-register-campaign-responses"></a>Slik registrerer du kampanjerespons:  

1. På siden **Segment** på hurtigfanen **Samhandling** velger du feltet **Samhandlingsmal – kode**.  

 Det finnes ingen samhandlingsmal for å registrere respons på kampanjer. Opprett derfor en ny mal.  

2. Velg handlingen **Ny** på rullegardinmenyen **Samhandlingsmaler**.  
3. Angi **RESP** i **Kode**-feltet, og angi **Kampanjerespons** i **Beskrivelse**-feltet.  
4. Velg **OK**-knappen.
5. Velg **Ja** for å bekrefte at du vil bruke denne koden for samhandlingsmal på alle segmentlinjer.
6. På hurtigfanen **Kampanje** felger du feltet **Kampanjerespons**. Velg **Ja** for å bekrefte meldingen *Du har endret kampanjesvar*.  
7. Velg **Logg**-handlingen på siden **Segment**.  
8. På siden **Loggfør segment** fjerner du merket for **Send vedlegg**. Velg deretter **OK**-knappen for å bekrefte meldingen om at segmentet er loggført.  
  
## <a name="see-also"></a>Se også  
[Forbindelser](marketing-relationship-management.md)  
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
 [Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
