---
title: Bruk Business Central-appene i Power BI
description: 'Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Business Central-apper for Power BI.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 04/01/2021
ms.author: jswymer
---
# Bruk [!INCLUDE [prod_short](includes/prod_short.md)]-appene i Power BI

> **GJELDER:** [!INCLUDE [prod_long](includes/prod_long.md)] Online 

[!INCLUDE [prod_long](includes/prod_long.md)] publiserer følgende Power BI-apper, som inneholder detaljerte instrumentbord for visning av data:

- [!INCLUDE [prod_long](includes/prod_long.md)] – CRM  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Finance  
- [!INCLUDE [prod_long](includes/prod_long.md)] – Sales

## Oversikt

Hver app inneholder flere rapporter som du kan se etter data i, og har blant annet følgende funksjoner:

- Velg hvilken som helst visualisering på instrumentbordet for å hente frem en av de underliggende rapportene.  
- Filtrere rapporten eller legg til felt som du vil overvåke.  
- Fest en tilpasset visning på instrumentbordet for å fortsette sporing.  
  Du kan oppdatere dataene manuelt, og kan du definere en oppdateringstidsplan. Hvis du vil ha mer informasjon, se [Konfigurere planlagt oppdatering](/power-bi/refresh-scheduled-refresh).  

Appene er utformet for å fungere med data fra et hvilket som helst selskap i [!INCLUDE[prod_short](includes/prod_short.md)]. Når du installerer Power BI-appen, angir du én eller flere parametere du vil koble til [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Du kan også lage dine egne rapporter og instrumentbord i Power BI basert på [!INCLUDE[prod_short](includes/prod_short.md)]-dataene dine. Hvis du vil ha mer informasjon, kan du se [Koble forretningsdata til Power BI](across-how-use-financials-data-source-powerbi.md). 

## Forutsetninger

Power BI-apper krever tillatelser til tabellene som dataene hentes fra, og til webtjenestene som brukes til å hente data. Tabellen nedenfor viser webtjenestene som kreves for hver Power BI-app:
    
|App | Webtjenester|
|----|-------------|
|[!INCLUDE[prod_short](includes/prod_short.md)] – CRM| <ul><li>Salgsmuligheter</li><li>Excel-mal – Vis selskapsinformasjon</li><li>Power BI-rapportetiketter</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Finance| <ul><li>PowerBIFinance</li><li>Excel-mal – Vis selskapsinformasjon</li><li>Power BI-rapportetiketter</li></ul>|
|[!INCLUDE[prod_short](includes/prod_short.md)] – Sales| <ul><li>Varesalg etter kunde</li><li>Instrumentbord for salg</li><li>Excel-mal – Vis selskapsinformasjon</li><li>Power BI-rapportetiketter</li></ul>|

> [!TIP]
> Det er enkelt å finne webtjenestene ved å søke etter *webtjenester* i [!INCLUDE[prod_short](includes/prod_short.md)]. På siden **Webtjenester** kontrollerer du at **Publiser**-feltet er valgt for webtjenestene som er oppført over. Hvis du vil ha mer informasjon, kan du se [Publisere en webtjeneste](across-how-publish-web-service.md).

## Gjøre deg klar

Registrer deg for Power BI-tjenesten. Hvis du ikke allerede har registrert deg, går du til [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Når du registrerer deg, bruker du e-postadressen og passordet for jobben din.

## Installere en [!INCLUDE[prod_short](includes/prod_short.md)]-app i Power BI

1. Åpne nettleseren, naviger til [https://powerbi.microsoft.com](https://powerbi.microsoft.com), og logg deg på kontoen din.
2. Velg **Hent data** nederst i navigasjonsruten til venstre.  

    ![Naviger til Hent data.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Du kan også starte fra [!INCLUDE [prod_short](includes/prod_short.md)]. Fra startsiden navigerer du til **Rapportvalg** i Power BI-delen. Velg enten **Service** eller **Min organisasjon** på båndet. Organisasjonsgalleriet i Power BI eller Microsoft AppSource åpnes, filtrert slik at bare apper som er knyttet til [!INCLUDE[prod_short](includes/prod_short.md)], vises.

3. I **Tjenester**-boksen velger du **Hent**.

    Dette trinnet åpner siden **Power BI-apper**, der du kan søke etter Power BI-appen som er tilgjengelig i **AppSource**.  

4. Skriv inn **Dynamics 365 Business Central** i **Søk**-boksen.
5. Velg appen du vil bruke, velg **Få det nå** og deretter **Installer**.  

    Når installasjonen er fullført, er appen tilgjengelig fra **Apper** på navigasjonsmenyen i Power BI.

## Koble [!INCLUDE[prod_short](includes/prod_short.md)]-appen til dataene dine

1. Velg Business Central-appen under **Apper**, og velg deretter **Koble til**.
2. Når du blir bedt om det, fyller du ut **Selskapsnavn** og **Miljø** med informasjon om [!INCLUDE[prod_short](includes/prod_short.md)]-forekomsten du vil koble til.

    - For **Selskapsnavn** må du passe på å bruke fullt navn, ikke visningsnavnet. Du finner selskapsnavnet på **Selskaper**-siden i [!INCLUDE[prod_short](includes/prod_short.md)]. 
    - Hvis du ikke har opprettet flere miljøer, angir du **Produksjon** for **Miljø**.

3. Velg **Neste**.
4. Velg **Pålogging**.
5. Når du blir bedt om det, skriver du inn brukernavn og passord for å logge på [!INCLUDE[prod_short](includes/prod_short.md)].
6. Ved tilkobling legges det til et instrumentbord og rapporter i Power BI-arbeidsområdet. Når du er ferdig, vises dataene fra [!INCLUDE[prod_short](includes/prod_short.md)]-selskapet.

    ![Velg Dynamics 365 Business Central, og velg Få det nå.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## Løse problemer

Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er oppført ovenfor. Det viser data fra demoselskapet eller ditt eget selskap hvis du importerer data fra den gjeldende økonomiløsningen din. Hvis noe går galt, vil denne delen imidlertid gi en løsning for de vanligste problemene.  

### Du har ikke en Power BI-konto

En Power BI-konto er ikke opprettet. Du må ha en lisens for å få en gyldig Power BI-konto. Du må også tidligere ha logget deg på Power BI for å opprette Power BI-arbeidsområdet.  

### Melding: Det finnes ingen aktiverte rapporter. Klikk på Velg rapport for å se en liste over rapporter du kan vise.

Denne meldingen vises hvis standardrapporten ikke kan distribueres til Power BI-arbeidsområdet. Eller rapporten ble distribuert, men ikke oppdatert. Hvis dette problemet oppstår, navigerer du til rapporten i Power BI-arbeidsområdet, velger **Datasett**, **Innstillinger** og oppdaterer deretter legitimasjonen manuelt. Når datasettet er oppdatert, går du tilbake til [!INCLUDE[prod_short](includes/prod_short.md)] og velger rapporten fra **Velg rapporter**-siden manuelt.

### Du trenger en Power BI Pro-lisens for å installere [!INCLUDE[prod_short](includes/prod_short.md)]-appen i Power BI

Du trenger en [Power BI Pro-lisens](/power-bi/service-features-license-type) for å kunne dele innholdet, og det gjør også de du deler den med. Innholdet må være i et arbeidsområde i en [Premium-kapasitet](/power-bi/service-premium-what-is). Hvis du vil ha mer informasjon, kan du se [Måter å dele arbeidet på i Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports).  

### "Parametervalidering mislyktes, du må kontrollere at alle parametrene er gyldige"

Denne feilen angir at én eller flere av parameterne ikke er gyldige.

- Den angitte miljøparameteren samsvarer ikke med eksisterende produksjons- eller sandkassemiljø i [!INCLUDE[prod_short](includes/prod_short.md)].
- Den angitte selskapsparameteren samsvarer ikke med eksisterende [!INCLUDE[prod_short](includes/prod_short.md)]-selskaper. Kontroller selskapsnavnet på **Selskap**-siden i [!INCLUDE[prod_short](includes/prod_short.md)].
- Hvis du kobler til [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, angav du en URL-adresse som ikke er gyldig. Du kan bekrefte URL-adressen på **Webtjenester**-siden i [!INCLUDE[prod_short](includes/prod_short.md)]  
- En port er ikke åpen, så forespørselen kommer ikke gjennom brannmuren.

### Kan ikke logge på

Hvis du får en feilmelding om at påloggingen mislyktes, etter at du har brukt brukerlegitimasjonen for [!INCLUDE[prod_short](includes/prod_short.md)] til å logge på, kan dette skyldes et av følgende problemer:

- Kontoen du bruker, har ikke tillatelse til å hente [!INCLUDE[prod_short](includes/prod_short.md)]-dataene fra kontoen din. Kontroller at du har tilgang til de nødvendige dataene i [!INCLUDE[prod_short](includes/prod_short.md)], og prøv på nytt.
- Du har valgt en annen godkjenningstype enn Enkel hvis du kobler til [!INCLUDE[prod_short](includes/prod_short.md)] lokalt.
- Du har ikke skrevet inn et gyldig brukernavn eller passord.

### Melding: Datakilden kan ikke oppdateres fordi legitimasjonen er ugyldig. Oppdater legitimasjonen, og prøv på nytt.

Når det gjelder [!INCLUDE[prod_short](includes/prod_short.md)] lokalt, kan problemet være at OData URL-adressen bare eksponeres for det lokale nettverket.

### Feil selskapsnavn

En vanlige feil er angi visningsnavnet for selskapet i stedet for selskapsnavnet. Søk etter **Selskaper** for å finne selskapsnavnet. Bruk **Navn**-feltet når du angir selskapsnavnet.

### Nøkkelen samsvarer ikke med noen rader i tabellen

Hvis du angir et ugyldige selskapsnavn under tilkoblingen, kan du få du feilmeldingen Nøkkelen samsvarer ikke med en rad i tabellen. Angi riktig selskapsnavn, og prøv å koble til på nytt.

### Historisk data ser ut til å mangle

Når Power BI-appen er installert og dataene vises i Power BI, oppdager du at ikke alle dataene vises. Datasettene filtreres for å returnere bare de forrige 365 dagene med data. Denne standarden er på plass til å gjøre rapportene raskere.  

### Jeg ser bare data for ett selskap

Power BI-appen viser bare data fra [!INCLUDE[prod_short](includes/prod_short.md)]-selskapet som ble definert da Power BI-appen ble installert. Data fra andre selskaper kan legges til i rapportene ved å legge til nye spørringer som bruker ulike selskaper som datakilde.  

### Hva nå?

- Prøv [å stille et spørsmål i spørsmål og svar-boksen](/power-bi/service-q-and-a-tips) øverst i instrumentbordet.
- [Endre flisene](/power-bi/service-dashboard-edit-tile) i instrumentbordet.  
- [Velge en flis](/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.  
- Som standard er ikke datasettet ditt planlagt for oppdatering. Du kan endre oppdateringsplanen eller prøve å oppdatere det ved behov ved hjelp av **Oppdater nå**. Hvis du vil ha mer informasjon, kan du se [Konfigurere planlagt oppdatering](/power-bi/refresh-scheduled-refresh).

## Se også

[Business Central og Power BI](admin-powerbi.md)  
[Oversikt over komponent og arkitektur for Power BI-integrering for [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Arbeid med [!INCLUDE [prod_short](includes/prod_short.md)]-data i Power BI](across-working-with-business-central-in-powerbi.md)  
[Bygge Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md)  
[Forretningsintelligens](bi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurer [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power Apps-datakilde](across-how-use-financials-data-source-powerapps.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  
[Power BI-dokumentasjon](/power-bi/)  
[Hva er Power BI?](/power-bi/fundamentals/power-bi-overview)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Innføring i datatorg](/power-bi/transform-model/datamarts/datamarts-overview)  
[Innføring i dataflyter og selvbetjent dataklargjøring](/power-bi/transform-model/dataflows/dataflows-introduction-self-service)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
