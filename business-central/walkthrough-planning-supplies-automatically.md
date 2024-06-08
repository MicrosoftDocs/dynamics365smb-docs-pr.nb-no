---
title: Gjennomgang – planlegg forsyninger automatisk
description: Denne gjennomgangen beskriver hvordan du bruker forsyningsplanleggingssystemet til å planlegge automatisk bestillinger og produksjonsordrer på forskjellige ordrer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/06/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="walkthrough-planning-supplies-automatically"></a>Gjennomgang: Planlegg forsyninger automatisk

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Uttrykk som «kjør planlegging» og «kjør MRP» refererer til beregningen av hovedproduksjonsplanen (MPS) og materialbehovsplanen (MRP) basert på faktisk og prognostisert behov.  

-   MPS er beregningen av en hovedproduksjonsplan basert på faktisk behov og behovsprognosen. MPS-beregningen brukes for sluttvarer som har en prognose- og/eller ordrelinje. Disse varene kalles "MPS-varer" og identifiseres dynamisk når beregningen starter.  
-   MRP er beregningen av materialbehov basert på faktisk behov for komponenter og behovsprognosen på komponentnivå. MRP beregnes bare for varer som ikke er MPS-varer. Det generelle formålet med MRP er å lage formelle planer med tidsfaser, etter vare, for å kunne levere det riktige antallet av riktig vare til riktig adresse i rett tid.  

 Planleggingsalgoritmene som brukes til MPS og MRP, er identiske. Planleggingsalgoritmene bruker nettoberegning, gjenbruk av eksisterende forsyningsordrer og handlingsmeldinger. Planleggingssystemprosessen undersøker hva som trengs eller kommer til å trengs (behov), og hva som er tilgjengelig eller forventet (forsyning). Når disse antallene nettoberegnes mot hverandre, vises handlingsmeldinger i planleggingsforslaget. Handlingsmeldinger er forslag om å opprette en ny forsyningsordre, endre en forsyningsordre (antall eller dato) eller kansellere en eksisterende forsyningsordre. Forsyningsordrer kan være produksjonsordrer, bestillinger og overføringsordrer. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  

 Planleggingsresultatet beregnes delvis ut fra settene med behov/forsyning i databasen og delvis av oppsettet for lagerføringsenhetskort eller varekort, produksjonsstykklister og ruter.  

## <a name="about-this-walkthrough"></a>Om denne gjennomgangen
 Denne gjennomgangen beskriver hvordan du bruker forsyningsplanleggingssystemet til å planlegge automatisk alle bestillinger og produksjonsordrer som kreves for å produsere 15 tursykler som etterspørres på forskjellige ordrer. For en klar og realistisk gjennomgang er antall planleggingslinjer avgrenset ved å filtrere ut alle behovs-/forsyningssett i demonselskapet CRONUS, bortsett fra salgsbehovet på lokasjonen ØST.  

 Denne gjennomgangen tar for seg følgende oppgaver:  

-   Opprette ordrer og beregne en komplett forsyningsplan  
-   Vise planleggingsparametere og sporingsposter bak planleggingslinjene  
-   Opprette de foreslåtte forsyningsordrene automatisk  
-   Opprette nytt salgsbehov og planlegge på nytt i henhold til dette  

## <a name="roles"></a>Roller

-   Produksjonsplanlegger  
-   Innkjøper  

## <a name="prerequisites"></a>Forutsetninger
 Du trenger følgende for å fullføre denne gjennomgangen:  

-   Installere demoselskapet CRONUS Norge AS  
-   Endre ulike vareoppsettverdier ved å følge fremgangsmåten under Klargjøre eksempeldata, senere i denne gjennomgangen.  

## <a name="story"></a>Hovedscenario
 Kunden, Kontorkomplett AS, bestiller fem tursykler for levering 05.02.2021 (5. februar).  

 Martin, produksjonsplanleggeren, foretar rutinemessig forsyningsplanlegging for den første uken i februar 2021. Eduardo filtrerer etter sin egen lokasjon, ØST, og angir et planleggingsintervall for arbeidsdatoen (23.01.2021) til 07.02.2021 før han beregner en innledende forsyningsplan.  

 Det eneste behovet den uken gjelder ordren for Kontorkomplett AS. Eduardo ser at ingen av planleggingslinjene har advarsler, og begynner å opprette forsyningsordrer uten endringer for de foreslåtte planleggingslinjene.  

 Neste dag, før noen av de første forsyningsordrene er startet eller bokført, blir Eduardo varslet når en annen kunde bestiller ti tursykler for levering 12.02.2021. Eduardo beregner på nytt for å justere forsyningsplanen i henhold til endringen i behovet. Den nye beregningen gir deg en bevegelsesplan der det blir foreslått endring av både tid og antall i enkelte av forsyningsordrene som ble opprettet ved første kjøring.  

 Martin slår opp i de involverte ordrene i de ulike planleggingstrinnene og bruker sporingsfunksjonen til å vise hvilket behov som dekkes av hvilken forsyning.  

## <a name="preparing-sample-data"></a>Klargjør eksempeldata
 Opprett lagerføringsenheter (LFEer) for tursykkelen og et utvalg av komponentene for den, varenummer 1001 til 1300. (Noen komponenter utelates for å forenkle fremgangsmåtene.) Juster planleggingsparameterne for de valgte komponentene for å få et mer gjennomsiktig planleggingsresultat.  

### <a name="to-create-stockkeeping-units"></a>Slik oppretter du lagerføringsenheter

1.  Åpne varekortet for vare 1001, tursykkel.  
2.  Velg **Opprett lagerføringsenhet**-handlingen.  
3.  Behold alle alternativer og filtre uendret på siden **Opprett lagerføringsenhet**, og velg deretter **OK**.  
4.  Gjenta trinn 1 til og med 3 for alle varer i nummerintervallet mellom 1100 og 1300.  

### <a name="to-change-selected-planning-parameters"></a>Slik endrer du valgte planleggingsparametre:

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerføringsenheter**, og velg deretter den relaterte koblingen.  
2.  Åpne lagerføringsenhetskortet ØST for vare 1100, forhjul.  
3.  På hurtigfanen **Planlegging** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Gjenbestillingsprinsipp|Sikkerhetslagerantall|Akkumuleringsperiode for parti|Periode for ny planlegging|  
    |-------------------------------------------|-----------------------------------------------|-------------------------------------------------|---------------------------------------------|  
    |Parti for parti|Tom|2U|2U|  

4.  Gjenta trinn 2 og 3 for alle LFEer i nummerintervallet mellom 1100 og 1300.  

 Nå har du fullført klargjøringen av eksempeldataene for gjennomgangen.  

## <a name="creating-a-regenerative-supply-plan"></a>Opprett en replanlegging for forsyning
 Etter å ha mottatt en ny ordre for fem tursykler, begynner John planleggingen ved å angi alternativer, filtre og planleggingsintervall for å utelate alt annet behov enn behovet for første uke i februar i ØST. Ricardo begynner med å beregne en hovedproduksjonsplan (MPS) og beregner deretter en komplett forsyningsplan for alt behov på lavere nivåer (MRP).  

### <a name="to-create-the-sales-order"></a>Slik oppretter du ordren

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3.  På siden **Ordre** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Salg til-kundenavn|Forsendelsesdato|Varenr.|Lokasjon|Antall|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Kontorkomplett|05-02-2014|1001|ØST|5|  

4.  Godta tilgjengelighetsadvarselen, og velg **Ja** for å registrere den nye behovsmengden.  

### <a name="to-create-a-regenerative-plan-to-fulfill-demand-at-location-east"></a>Slik oppretter du en ny planlegging for å dekke behovet i ØST

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Planleggingsforslag**, og velg deretter den relaterte koblingen.  
2.  Velg **Beregn replanlegging**-handlingen.  
3.  I siden **Beregn plan - planl.forslag** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Beregn plan|Startdato|Sluttdato|Vis resultater:|Begrens totaler til|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Nei|23.01.2021<br /><br /> (arbeidsdato)|07.02.2021|1001..1300|Lokasjonsfilter = ØST|  

4.  Velg **OK**-knappen for å starte planleggingskjøringen.  

     Det opprettes en planleggingslinje med forslag om at det utstedes en planlagt produksjonsordre for å produsere ti tursykler, vare 1001, innen 05.02.2021, forsendelsesdatoen i ordren.  

     Kontroller deretter at denne planleggingslinjen er knyttet til ordren for Kontorkomplett AS ved å bruke **Sporing**-funksjonen, som dynamisk kobler behov til den planlagte forsyningen.  

5.  Merk den nye planleggingslinjen, og velg deretter **Sporing**-handlingen.  
6.  På siden **Sporing** velger du handlingen **Vis**.  

     Ordren for fem tursykler som skal leveres til kunde nummer 10 000 den 05.02.2021, vises.  

7.  Lukk sidene **Ordre** og **Sporing**.  

### <a name="to-calculate-mrp-to-include-underlying-component-needs"></a>Slik beregner du MRP for å inkludere underliggende komponentbehov

1.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Planleggingsforslag**, og velg deretter den relaterte koblingen.  
2.  Velg **Beregn replanlegging**-handlingen.  
3.  I siden **Beregn plan - planl.forslag** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Beregn|Startdato|Sluttdato|Vis resultater:|Begrens totaler til:|  
    |---------------|-------------------|-----------------|-------------------|----------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|23.01.2021|07.02.2021|1001..1300|Lokasjonsfilter = ØST|  

4.  Velg **OK**-knappen for å starte planleggingskjøringen.  

     Det opprettes i alt 14 planleggingslinjer med forslag om forsyningsordrer for alt behov som ordren med tursykler i ØST representerer.  

## <a name="analyze-the-planning-result"></a>Analyser planleggingsresultatet
 Martin viser detaljer for valgte planleggingslinjer for å analysere de foreslåtte antallene og vise sporingsposter og planleggingsparametere.  

 På **Planleggingsforslag**-siden merker du at de foreslåtte forsyningsordrene er planlagt bakover i **Forfallsdato**-kolonnen fra forfallsdatoen for ordren, 05.02.2021. Tidslinjen starter på øverste planleggingslinje med produksjonsordren for å produsere de ferdige tursyklene. Tidslinjen slutter på nederste planleggingslinje med bestillingen for én av varene på nederste nivå, 1255 (Hylse - bak), som forfaller 30.01.2021. Som planleggingslinjen for vare 1251, bakhjulsaksel, representerer denne linjen en bestilling for komponenter som forfaller på startdatoen for den produserte overordnede varen, delmonteringsvare 1250, som deretter forfaller 02.03.2014. I hele regnearket kan du se at alle underliggende varer forfaller på startdatoen for overordnede varer.  

 Planleggingslinjen for vare 1300 (Kjedemontering) inneholder et forslag på ti stykker. Dette avviker fra de fem delene som vi forventer å trenge for å oppfylle salgsordren. Fortsett med å vise ordresporingspostene.  

### <a name="to-view-order-tracking-entries-for-item-1300"></a>Slik viser du ordresporingsposter for element 1300:

1.  Merk planleggingslinjen for vare 1300, og velg deretter **Sporing**-handlingen.  

     De to linjene på **Sporing**-siden viser at fem stykker er sporet fra planleggingslinjen (første sporingslinje) til ordre 1001 (andre sporingslinje). De fem siste stykkene som er foreslått på planleggingslinjen, er ikke knyttet til noen dokumentlinjer, men til en planleggingsparameter, prognosepost eller rammeordrepost. Slike ikke-sporede antall er summert i feltet **Ikke-sporet antall** i hodet på **Sporing**-siden.  

2.  Velg **Ikke-sporet antall**-feltet.  

     Siden **Ikke-sporede planleggingselementer** viser at vare 1300 bruker en planleggingsparameter, Min. bestillingsantall, på 10,00. Derfor er planleggingslinjen for ti stykker i alt, men bare fem stykker kan spores til et behov. De fem siste stykkene er et ikke-sporet antall for å oppfylle planleggingsparameteren. Fortsett med å vise planleggingsparameteren.  

### <a name="to-check-the-planning-parameter"></a>Slik kontrollerer du planleggingsparameteren:

1.  Velg sporingslinjen for vare 1300 på siden **Ikke-sporede planleggingselementer**.  
2.  Velg feltet **Varenr.**, og velg deretter **Avansert**-handlingen.  
3.  På siden **Vareoversikt** velger du handlingen **Lagerføringsenheter**.  
4.  På siden **Lagerføringsenhet – oversikt** åpner du lagerføringsenhetskortet for ØST.  
5.  I hurtigfanen **Planlegging**, legg merke til at feltet **Min. bestillingsantall** inneholder 10.  
6.  Lukk alle sider unntatt **Planleggingsforslag**-siden.  

### <a name="to-view-more-order-tracking-entries"></a>Slik viser du flere ordresporingsposter:

1.  Merk planleggingslinjen for vare 1110, Felg, og velg deretter **Sporing**-handlingen.  

     **Sporing**-siden viser at fem felger kreves for hver produksjonsordre for henholdsvis for- og bakhjul.  

     Samme sporing gjelder for planleggingslinjene for vare 1120 1160 og 1170. For vare 1120, er **Antall per**-feltet i produksjonsstykklisten for hver hjulvare 50 stk, noe som resulterer i et totalt behov på 100.  

     Planleggingslinjen for vare 1150 for seks stykker ser uregelmessig ut. Fortsett med å analysere.  

2.  Merk planleggingslinjen for vare 1150, og velg deretter **Sporing**-handlingen.  

     **Sporing**-siden viser at fem enheter spores til forhjulet, og én enhet er ikke-sporet. Fortsett med å vise ikke-sporet antall.  

3.  Velg **Ikke-sporet antall**-feltet.  

     Siden **Ikke-sporede planleggingselementer** viser at vare 1150 bruker en planleggingsparameter, Bestillingsfaktor, på 2,00, som angir at når varen bestilles, må det være i et antall som kan deles med 2. Tallet som er nærmest fem og kan deles på to, er seks.  

     Den samme ordresporingen gjelder for planleggingslinjer for fornavkomponentene, varene 1151 og 1155, bortsett fra at hvert behov multipliseres med svinnprosenten som er definert for varen 1150 i feltet **Svinnprosent**, på varekortet.  

 Nå har du fullført analysen av den innledende forsyningsplanen. Vær oppmerksom på at det er merket av for **Godta handlingsmelding** i alle planleggingslinjer for å angi at de er klare til å bli konvertert til forsyningsordrer.  

## <a name="carrying-out-action-messages"></a>Utfør handlingsmeldinger
 Nå skal Martin konvertere de foreslåtte planleggingslinjene til forsyningsordrer ved å bruke funksjonen **Utfør handlingsmelding**.  

### <a name="to-automatically-create-the-suggested-supply-orders"></a>Slik oppretter du de foreslåtte forsyningsordrene automatisk:

1.  Merk av for **Godta handlingsmelding** for alle planleggingslinjer med en advarsel av typen Unntak.  
2.  Velg **Utfør handlingsmelding**-handlingen.  
3.  På siden **Utfør handlingsmelding - plan.** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Produksjonsordre|Bestilling|Overføringsordre|  
    |----------------------|--------------------|--------------------|  
    |Fast planlagt|Lag bestilling|Lag overføringsordrer|  

4.  Velg **OK**-knappen for å opprette alle de foreslåtte forsyningsordrene automatisk.  
5.  Lukk den tomme **Planleggingsforslag**-siden.  

 Nå har du fullført den innledende beregningen, analysen og opprettelsen av en forsyningsplan for behov i ØST i den første uken av februar. I delen nedenfor bestiller en annen kunde ti tursykler, og Martin må planlegge på nytt.  

## <a name="creating-a-net-change-plan"></a>Opprett en bevegelsesplan
 Neste dag, før noen forsyningsordrer er startet eller bokført, kommer det en ny ordre fra Stilmøbler AS for ti tursykler som skal leveres 12.02.2021. Eduardo blir varslet om det nye behovet og begynner å planlegge på nytt for å justere den aktuelle forsyningsplanen. Martin bruker funksjonen for bevegelsesplan til å beregne bare endringene av behov eller forsyning siden siste planleggingskjøring. I tillegg utvider Eduardo planleggingsperioden til 14.02.2021 slik at den inkluderer det nye salgsbehovet den 12.02.2021.  

 Planleggingssystemet beregner den beste måten å dekke behovet for disse to identiske produktene på, for eksempel å konsolidere enkelte bestillinger og produksjonsordrer, planlegge andre ordrer på nytt og opprette nye ordrer der det er nødvendig.  

### <a name="to-create-the-new-sales-demand-and-replan-accordingly"></a>Slik oppretter du det nye salgsbehovet og planlegger på nytt i henhold til dette

1.  Velg handlingen **Ny**.  
2.  På siden **Ordre** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Salg til-kundenavn|Forsendelsesdato|Varenr.|Lokasjon|Antall|  
    |----------------------------|-------------------|--------------|--------------|--------------|  
    |Stilmøbler AS|12.02.2021|1001|ØST|10|  

3.  Godta tilgjengelighetsadvarselen, og velg **Ja** for å registrere behovsmengden.  
4.  Fortsett med å planlegge på nytt for å justere den aktuelle forsyningsplanen.  
5.  Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Planleggingsforslag**, og velg deretter den relaterte koblingen.  
6.  Velg **Beregn bevegelsesplan**-handlingen.  
7.  I siden **Beregn plan - planl.forslag** fyller du ut feltene som beskrevet i tabellen nedenfor.  

    |Beregn plan|Startdato|Sluttdato|Vis resultater:|Begrens totaler til|  
    |--------------------|-------------------|-----------------|-------------------|---------------------|  
    |**MPS** = Ja<br /><br /> **MRP** = Ja|23.01.2021|14.02.2021|1001..1300|Lokasjonsfilter = ØST|  

8.  Velg **OK**-knappen for å starte planleggingskjøringen.  

 Det opprettes i alt 14 planleggingslinjer. Legg merke til at i den første planleggingslinjen vises **Ny** i **Handlingsmelding**-feltet, 10 i **Antall**-feltet og 12.02.21 i **Forfallsdato**-feltet. Denne nye linjen for den overordnede toppvaren 1001 (Tursykkel) opprettes fordi gjenbestillingsprinsippet **Ordre** brukes for varen, som betyr at den må forsynes i et én-til-én-forhold til behovet, ordren med ti stykker.  

 De neste to planleggingslinjene er produksjonsordrene for tursykkelhjul. Hver eksisterende ordre med fem i feltet **Opprinnelig antall** økes til 15, i feltet **Antall**. Begge produksjonsordrer har uendret forfallsdato, som angitt i feltet **Handlingsmelding** som inneholder **Endre ant.** Dette er også tilfellet for planleggingslinjen for varen 1300, bortsett fra at bestillingsfaktoren på 10,00 runder det sporede behovet for 15 stykker opp til 20.  

 Alle andre planleggingslinjer har handlingsmeldingen **Tidsplanl. på nytt og endre ant.**. Dette betyr at i tillegg til at antallet økes, flyttes forfallsdatoene i forhold til forsyningsplanen for å inkludere det ekstra antallet i tilgjengelig produksjonstid (kapasitet). Innkjøpte komponenter planlegges på nytt og økes for å forsyne produksjonsordrene. Fortsett med å analysere den nye planen.  

## <a name="analyze-the-changed-planning-result"></a>Analyser det endrede planleggingsresultatet
 Fordi alle parti-for-parti-planlagte varer i filteret, 1100 til 1300, har en periode for ny planlegging på to uker, endres alle eksisterende forsyningsordrer for å oppfylle det nye behovet, som skjer innen de angitte to ukene.  

 Flere planleggingslinjer multipliseres med tre for å gi 15 tursykler i stedet for 5, og forfallsdatoene flyttes tilbake i tid for å gi de økte antallene basert på leveringsdatoen for salgsordren til Kontorkomplett AS. Alle antall kan spores for disse planleggingslinjene. De gjenværende planleggingslinjene økes med ti stykker i tillegg til at forfallsdatoene flyttes. For disse planleggingslinjene er en del av antallene ikke-sporet på grunn av ulike planleggingsparametre. Fortsett med å vise noen av disse ordresporingspostene.  

### <a name="to-view-order-tracking-entries-for-item-1250"></a>Slik viser du ordresporingsposter for element 1250:

1.  Merk planleggingslinjen for vare 1250, og velg deretter **Sporing**-handlingen.  

     De sju linjene på **Sporing**-siden viser at fem og ti deler blir sporet gjennom henholdsvis bakhjulet til tursyklene på de to salgsordrene.  

     De siste fem delene er ikke-sporet. Fortsett med å analysere.  

2.  Velg **Ikke-sporet antall**-feltet.  

     Siden **Ikke-sporede planleggingselementer** viser at vare 1250 bruker en planleggingsparameter, Bestillingsfaktor, på 10,00. Planleggingslinjen er derfor på 20 deler i alt for å avrunde det faktiske behovet opp til nærmeste tall som er delelig med 10. De fem siste stykkene er et ikke-sporet antall for å oppfylle planleggingsparameteren.  

3.  Lukk alle sider unntatt **Planleggingsforslag**-siden.  

### <a name="to-view-an-existing-order"></a>Slik viser du en eksisterende ordre:

1.  Velg **Ref.ordrenr.** i planleggingslinjen for vare 1250. .  
2.  Åpne siden **Fast planlagt prod.ordre** for baknavet. Den eksisterende ordren for ti enheter, som du opprettet i den første planleggingskjøringen, åpnes.  
3.  Lukk den fast planlagte produksjonsordren.  

 Nå har du gått gjennom hvordan planleggingssystemet brukes til å oppdage behov automatisk, beregne de aktuelle forsyningsordrene i henhold til behov og planleggingsparametere og deretter automatisk opprette ulike typer forsyningsordrer med riktige datoer og antall.  

## <a name="see-also"></a>Se også
 [Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Manually](walkthrough-planning-supplies-manually.md)    -->
 [Utformingsdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
