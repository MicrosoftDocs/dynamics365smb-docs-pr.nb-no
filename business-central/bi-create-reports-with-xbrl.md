---
title: Opprette rapporter med XBRL
description: 'XBRL er et XML-basert språk for merking av økonomiske data, slik at selskaper kan behandle og dele data på en effektiv og nøyaktig måte.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/14/2022
ms.author: edupont
---
# <a name="create-reports-with-xbrl"></a><a name="create-reports-with-xbrl"></a>Opprette rapporter med XBRL

> [!NOTE]
> Vi er i ferd med å fjerne funksjonene for XBRL-rapportering fra [!INCLUDE[prod_short](includes/prod_short.md)]. Lær mer om [Endringer i lanseringsbølge 1 for 2022](/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-w1).

XBRL (e**X**tensible **B**usiness **R**eporting **L**anguage) er et språk basert på eXtensible Markup Language (XML) for merking av økonomiske data, slik at selskaper kan behandle og dele data på en effektiv og nøyaktig måte. XBRL-initiativet gjør det mulig med global finansrapportering fra flere ERP-programvareselskaper og internasjonale regnskapsorganisasjoner. Målet med initiativet er å skape en standard for enhetlig rapportering av økonomisk informasjon for banker, investorer og myndigheter. Slik forretningsrapportering kan omfatte følgende:  

* Årsregnskap  
* Økonomisk informasjon  
* Ikke-økonomisk informasjon  
* Lovpålagte innleveringer, for eksempel årsrapporter og kvartalsrapporter  

> [!NOTE]
> Du kan importere finansrelaterte skjemaer og opprette XBRL-forekomstdokumenter ved å knytte finansdata fra kontoplanen til varer i taksonomier som er utformet for finansrapporter, for eksempel balanse, resultat regnskap og så videre.
>
> XBRL-funksjonene i Business Central støtter taksonomier for spesifikasjon 2.1. Taksonomier kan imidlertid inneholde elementer som for eksempel formelkoblingsbaser eller iXBRL (innebygd XBRL), eller de kan ha andre strukturelle forskjeller. Vi anbefaler at du validerer XBRL-funksjonen før du bruker den til rapportering.
>
> Full støtte for taksonomier kan kreve tredjeparts XBRL-koder og -verktøy. Den internasjonale organisasjonen for XBRL har en liste over verktøy og tjenester. Avhengig av kravene til XBRL-rapportering for en gitt taksonomi kan det være lurt å undersøke disse ressursene. Hvis du vil ha mer informasjon, kan du se [Komme i gang for bedrifter](https://go.microsoft.com/fwlink/?linkid=2153466) og [Verktøy og tjenester](https://go.microsoft.com/fwlink/?linkid=2153356).

## <a name="extensible-business-reporting-language"></a><a name="extensible-business-reporting-language"></a>eXtensible Business Reporting Language

XBRL-taksonomiene vedlikeholdes av www.xbrl.org. Du kan laste ned taksonomiene og få mer detaljerte opplysninger på webområdet for XBRL.  

La oss si at noen ønsker økonomisk informasjon fra deg. De gir deg en taksonomi (et XML-dokument) som inneholder ett eller flere skjemaer med en eller flere linjer som skal fylles ut. Linjene samsvarer med de enkelte økonomiske opplysninger som senderen ber om. Du importerer denne taksonomien og fyller ut skjemaene ved å angi hvilke(n) konto/konti som hører til hver linje og hvilken beregning som gjelder, for eksempel bevegelse eller saldo per dato. I noen tilfeller kan du i stedet legge inn en konstant, for eksempel antall ansatte. Du er nå klar til å sende kjøringsdokumentet (et XML-dokument) til anmoderen. Tanken er at dette skjer gjentatte ganger, slik at med mindre det gjøres endringer i taksonomien, trenger du bare eksportere nye kjøringsdokumenter for nye perioder når du blir bedt om det.

## <a name="xbrl-comprises-the-following-components"></a><a name="xbrl-comprises-the-following-components"></a>XBRL består av følgende komponenter

XBRL- **spesifikasjonen** forklarer hva XBRL er og hvordan det er mulig å lage kjøringsdokumenter og taksonomier. XBRL-spesifikasjonen gir en teknisk forklaring på hva XBRL er, og er rettet mot et publikum som er teknisk kyndig.  

XBRL- **skjemaene** er de viktigste grunnkomponentene til XBRL. Skjemaet er den fysiske XSD-filen (også kalt XML-skjermadefinisjon) som uttrykker hvordan XBRL-forekomstdokumenter og taksonomier bygges opp.

XBRL **koblingsbaser** er de fysiske XML-filene som inneholder informasjon om de elementene som er definert i XBRL-skjemaene, for eksempel etiketter på ett eller flere språk, hvordan de forholder seg til hverandre, hvordan elementene summeres og så videre.  

En XBRL- **taksonomi** er et "ordforråd" eller en "ordbok" som en gruppe har utviklet i samsvar med XBRL-spesifikasjonen, som aktiverer utveksling av forretningsopplysninger.  

Et XBRL- **kjøringsdokument** er en forretningsrapport, for eksempel et regnskap gjort i samsvar med XBRL-spesifikasjonen. Verdiene i kjøringsdokumentet forklares i taksonomien. Et kjøringsdokument er nokså verdiløst hvis du ikke kjenner taksonomien det er laget for.  

## <a name="layered-taxonomies"></a><a name="layered-taxonomies"></a>Lagdeling av taksonomier

En taksonomi kan bestå av en grunntaksonomi, for eksempel US GAAP (vanligvis aksepterte regnskapsprinsipper i USA) eller IAS (internasjonale regnskapsstandarder), og deretter ha én eller flere utvidelser. Dermed refererer en taksonomi til ett eller flere skjemaer, som alle er separate taksonomier. Når tilleggstaksonomiene lastes inn i databasen, legges de nye elementene rett og slett til de eksisterende elementene.  

## <a name="linkbases"></a><a name="linkbases"></a>Koblingsbaser

I XBRL-spes. 2 beskrives taksonomien i flere XML-filer. Den primære XML-filen er selve taksonomiskjemafilen (XSD-fil) som bare inneholder en usortert liste over elementer eller fakta som skal rapporteres. I tillegg til dette er vanligvis noen koblingsbasefiler (XML). Koblingsbasisfilene inneholder data som utfyller grunntaksonomien (XSD-fil). Det finnes seks typer koblingsbasefiler, hvorav fire er relevante for [!INCLUDE[prod_short](includes/prod_short.md)]. Disse er:

* Etikettkoblingsbase: Denne koblingsbasen inneholder etiketter, eller navn på elementer. Filen kan inneholde etiketter på forskjellige språk, som angis ved hjelp av en XML-egenskap som kalles "lang". XMLs språkidentifikator består vanligvis av to bokstaver, og selv om det skulle være enkelt nok å gjette hva forkortelsene betyr, har de ingenting verken med språkkodene i Microsoft Windows eller språkkodene i demodataene å gjøre. Når du slår opp i språkene for en taksonomi, vil du derfor se alle etikettene for det første elementet i taksonomien, slik at du kan se et eksempel på hvert av språkene. En taksonomi kan ha flere etikettkoblingsbaser knyttet til seg, så lenge disse koblingsbasene inneholder ulike språk.  
* Presentasjonskoblingsbase: Denne koblingsbasen inneholder informasjon om strukturen til elementene eller, nærmere bestemt, taksonomiforfatterens forslag til hvordan programmet presenterer taksonomien for deg. Koblingsbasen inneholder en rekke koboinger som hver kobler to elementer i en overordnet-underordnet relasjon. Ved hjelp av alle disse koblingene kan elementene vises på en hierarkisk ordnet måte. Merk at det er nettopp dette presentasjonskoblingsbasen gjør: Den presenterer elementene for deg.
* Beregningskoblingsbase: Denne koblingsbasen inneholder informasjon om hvordan elementene rulles opp. Strukturen ligner på presentasjonskoblingsbasen, bortsett fra at hver kobling er vektet. Vektingen kan være 1 eller –1, og angir om elementet skal legges til eller trekkes fra et overordnet element i hierarkiet. Merk at opprulleringene ikke nødvendigvis stemmer overens med den grafiske presentasjonen.  
* Referansekoblingsbase: Referansekoblingsbasen er en xml-fil som inneholder tilleggsopplysninger om de dataene som taksonomiforfatteren trenger.

## <a name="set-up-xbrl-lines"></a><a name="set-up-xbrl-lines"></a>Konfigurer XBRL-linjer

Etter at du har lest inn eller oppdatert taksonomien, må fylles ut med alle nødvendige opplysninger for å tilfredsstille de spesifikke regnskapskravene. Denne informasjonen inneholder grunnleggende selskapsopplysninger, faktiske regnskapstall, noter til regnskap, ytterligere planer og annen nødvendig regnskapsinformasjon.  

Du definerer XBRL-linjer ved å tilordne taksonomidataene til finansdataene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **XBRL-taksonomier**, og velg deretter den relaterte koblingen.  
2. Velg en taksonomi fra listen på siden **XBRL-taksonomier**.  
3. Velg handlingen **Linjer**.  
4. Velg en linje og fyll ut feltene.  
5. Hvis du vil lese detaljerte opplysninger om hva som skal fylles ut, velger du **Informasjon**.  
6. Hvis du vil konfigurere tilordning av finanskontiene i kontoplanen for XBRL-linjer, velger du handlingen **Knytt til finans**.  
7. Hvis du vil legge til merknader i regnskapet, velger du **Merknader**.  

   > [!TIP]
   > Hvis du vil utelate linjer fra eksporterte data, velger du **IKKE I BRUK** som kildetypen.

   > [!NOTE]  
   > Du kan bare eksportere data som samsvarer med det du har valgt i feltet **Kildetype**. Dette omfatter beskrivelser og merknader.  

   > [!NOTE]  
   > Taksonomier kan inneholde elementer som [!INCLUDE[prod_short](includes/prod_short.md)] ikke støtter. Hvis et element ikke støttes, viser feltet **Kildetype** **Ikke i bruk** og feltet **Beskrivelse** viser en feilmelding, for eksempel **Uventet type: spesifikk type er ikke gjenkjent**. Hvis du må eksportere elementet, velger du en tilsvarende kildetype. Dette er vanligvis en konstant eller en beskrivelse. Dette gir deg muligheten til å skrive inn og eksportere data, slike elementer kan imidlertid ha valideringsregler som ikke kan kontrolleres før eksportert.

## <a name="import-an-xbrl-taxonomy"></a><a name="import-an-xbrl-taxonomy"></a>Importere en XBRL-taksonomi

Første trinn i arbeidet med XBRL-funksjonaliteten, er å lese taksonomien inn i selskapsdatabasen. En taksonomi består av ett eller flere skjemaer og noen koblingsbaser. Når du har fullført innlesingen av både skjemaer og koblingsbaser, og har brukt koblingsbasene på skjemaet, kan du definere linjene og tilordne finanskontiene i kontoplanen til riktig taksonomilinje.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **XBRL-taksonomier**, og velg deretter den relaterte koblingen.  
2. Opprett en ny linje på siden **XBRL-taksonomier** og angi navn og beskrivelse for taksonomien.  
3. Velg **Skjemaer**, og sett inn beskrivelsen av skjemaet.  
4. Hvis du vil importere skjemaet, velger du handlingen **Importer** på siden **XBRL-skjemaer**, og deretter gjør du et av følgende for å laste opp filen:

   [!INCLUDE[file-upload](includes/file-upload.md)]
5. Hvis du vil importere koblingsbasen, velger du handlingen **Importer** på siden **Koblingsbaser**, og deretter gjør du et av følgende for å laste opp filen:

   [!INCLUDE[file-upload](includes/file-upload.md)] 
6. Du kan nå velge å bruke koblingsbasen på skjemaet. Gjenta dette helt til du har importert alle koblingsbasene.  
7. Velg **Bruk på taksonomi** for å bruke koblingsbasen på skjemaet.  

> [!IMPORTANT]  
> I stedet for å bruke koblingsbasene hver for seg etter at du har importert dem, kan du vente til du har importert alle koblingsbasene, og deretter bruke dem samtidig. Dette gjør du ved å velge **NEI** når du blir spurt om du vil bruke den nylig importerte koblingsbasen på skjemaet. Merk så linjene med koblingsbasene du vil bruke.  

## <a name="update-an-xbrl-taxonomy"></a><a name="update-an-xbrl-taxonomy"></a>Oppdatere en XBRL-taksonomi

Når en taksonomi endres, må du oppdatere den gjeldende taksonomien tilsvarende. Årsaken til oppdateringen kan være et endret skjema, en endret koblingsbase eller en ny koblingsbase. Når du har oppdatert taksonomien, trenger du bare å samordne linjene for de endrede eller nye linjene.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **XBRL-taksonomier**, og velg deretter den relaterte koblingen.  
2. På siden **XBRL-taksonomier** velger du handlingen **Skjemaer**.  
3. Du oppdaterer et skjema ved å velge skjemaet du vil oppdatere, og deretter velge **Importer**.  
4. Hvis du vil oppdatere eller legge til en ny koblingsbase, velger du **Koblingsbaser**.  
5. Velg den aktuelle koblingsbasen, eller velg <kbd>Ctrl</kbd>+<kbd>N</kbd> for en ny linje, velg koblingsbasetypen og sett deretter inn en beskrivelse.  
6. Du importerer koblingsbasen ved å velge den **Importer**.  
7. Velg **Ja** for å bruke koblingsbasen på skjemaet.  

## <a name="see-related-training-at-microsoft-learn"></a><a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/xbrl-reports-dynamics-365-business-central/index).

## <a name="see-also"></a><a name="see-also"></a>Se også

[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
