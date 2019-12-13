---
title: Aktivere forretningsdata for Power BI| Microsoft Docs
description: Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Business Central-apper for Power BI.
author: bmeier90
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.reviewer: edupont
ms.date: 10/01/2019
ms.author: bmeier
ms.openlocfilehash: 0750f1724260eb7767757d947f30dcb074ef1aeb
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2879109"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere forretningsdata for Power BI

Få innsikt i [!INCLUDE[prodshort](includes/prodshort.md)]-dataene på en enkel måte med [!INCLUDE[prodshort](includes/prodshort.md)]-appene for Power BI. Power BI henter dataene, og deretter bygger du et forhåndskonfigurert instrumentbord og rapporter basert på dataene.  

Du må ha en gyldig konto med [!INCLUDE[prodshort](includes/prodshort.md)] og med Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/desktop/) hvis du vil opprette et egne Power BI-rapporter. Power BI-apper krever tilgang til tabellene der opplysningene hentes fra. Du finner mer informasjon om kravene nedenfor.  

> [!IMPORTANT]
> Power BI-appene som er beskrevet i denne artikkelen, er utformet for å bruke Azure Active Directory som godkjenningsmekanisme med mindre annet er angitt. Hvis du vil installere en Power BI-app, må du også ha en Power BI Pro-lisens.  Når Power BI-appen er installert, kan den deles med brukere med en hvilken som helst lisenstype.

[!INCLUDE [prodlong](includes/prodlong.md)] har publisert følgende apper for Power BI:

- [!INCLUDE [prodlong](includes/prodlong.md)] – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)] – Sales  
- [!INCLUDE [prodlong](includes/prodlong.md)](lokalt) – CRM  
- [!INCLUDE [prodlong](includes/prodlong.md)](lokalt) – Finance  
- [!INCLUDE [prodlong](includes/prodlong.md)](lokalt) – Sales  

## <a name="using-the-include-prodshortincludesprodshortmd-dashboards-in-power-bi"></a>Bruke [!INCLUDE [prodshort](includes/prodshort.md)]-instrumentbordene i Power BI

Hver app inneholder rapporter som du kan se på:

- Velg hvilken som helst visning på instrumentbordet for å hente frem en av de underliggende rapportene.  
- Filtrere rapporten eller legg til felt som du vil overvåke.  
- Fest denne tilpassede visningen på instrumentbordet for å fortsette sporing.  
  Du kan oppdatere dataene manuelt, og kan du definere en oppdateringstidsplan. Hvis du vil ha mer informasjon, se [Konfigurere planlagt oppdatering](/power-bi/refresh-scheduled-refresh).  

Appene er utformet for å fungere med data fra et hvilket som helst selskap du har i [!INCLUDE[prodshort](includes/prodshort.md)]. Når du installerer Power BI-appen, angir du én eller flere parametere du vil koble til [!INCLUDE [prodshort](includes/prodshort.md)].  

> [!NOTE]
> Du kan også lage dine egne rapporter og instrumentbord i Power BI basert på [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene dine. Hvis du vil ha mer informasjon, kan du se [Koble forretningsdata til Power BI](across-how-use-financials-data-source-powerbi.md).  

### <a name="to-connect-your-data-in-power-bi"></a>Slik kobler du sammen dataene i Power BI

1. Åpne leseren, naviger til https://powerbi.microsoft.com, og logg deg på kontoen din.
2. Velg **Hent data** nederst i navigasjonsruten til venstre.  

    ![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

    Du kan også starte fra [!INCLUDE [prodshort](includes/prodshort.md)]. Fra startsiden navigerer du til **Rapportvalg** i Power BI-delen. Velg enten **Service** eller **Min organisasjon** på båndet. Når en av disse handlingene er valgt, kommer du enten til organisasjonsgalleriet i Power BI eller til Microsoft AppSource, som også filtreres for å bare vise apper knyttet til [!INCLUDE[prodshort](includes/prodshort.md)].

3. I **Tjenester**-boksen velger du **Hent**. Dette åpner en side som viser **AppSource** og **Apper for Power BI**.  

<!--    ![Choose apps from online services that you use.](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)-->
4. Velg **Apper** fra fanen **Apper for Power BI**, velg **Microsoft Dynamics 365 Business Central**-appen du vil bruke, og velg deretter **Få det nå**.  
<!--    ![Select Dynamics 365 Business Central and select Get it now](./media/across-how-to-connect-powerbi-d365-content-packspowerbi-dynamics365-for-financials-get-it-now.png)/-->
5. Når du blir spurt, skriver du inn navnet på miljøet og selskapet i [!INCLUDE[prodshort](includes/prodshort.md)]-appen du vil koble til. Hvis du ikke har opprettet flere miljøer, angir du **Produksjon**. Pass på at du angir navnet og ikke visningsnavnet for selskapsparameteren. Du finnner selskapsnavnet på siden **Selskap** i [!INCLUDE[prodshort](includes/prodshort.md)]-forekomsten.  

    > [!NOTE]
    > Hvis du kobler til [!INCLUDE [prodshort](includes/prodshort.md)] lokalt, må du angi parameteren for *Nettadresse for webtjeneste*. Finn denne på siden **Webtjenester** i [!INCLUDE [prodshort](includes/prodshort.md)]. [!INCLUDE [server](includes/server.md)]-forekomsten må være konfigurert for enkel godkjenning, og du må angi en bruker og nettilgangsnøkkelen til denne brukeren som passord. I eksemplet nedenfor erstatt *myserver:7048* med [!INCLUDE [server](includes/server.md)]-navnet ditt og *CRONUS%20US* med selskapsnavnet ditt.  
    > ```https://myserver:7048/BC140/ODataV4/Company('CRONUS%20US')/```

6. Ved tilkobling legges det til et instrumentbord og rapporter i Power BI-arbeidsområdet. Når du er ferdig, vises dataene fra [!INCLUDE[prodshort](includes/prodshort.md)]-selskapet.

    ![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

### <a name="what-now"></a>Hva nå?

- Prøv [å stille et spørsmål i spørsmål og svar-boksen](/power-bi/service-q-and-a-tips) øverst i instrumentbordet.
- [Endre flisene](/power-bi/service-dashboard-edit-tile) i instrumentbordet.  
- [Velge en flis](/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.  
- Som standard er ikke datasettet ditt satt til å oppdatere. Du kan endre oppdateringsplanen eller prøve å oppdatere det ved behov ved hjelp av **Oppdater nå**. Hvis du vil ha mer informasjon, se [Konfigurere planlagt oppdatering](/power-bi/refresh-scheduled-refresh).

## <a name="power-bi-in-include-prodshortincludesprodshortmd"></a>Power BI i [!INCLUDE [prodshort](includes/prodshort.md)]

Startsiden i [!INCLUDE [prodshort](includes/prodshort.md)] kan inneholde et Power BI-kontrollelement som kan konfigureres til å vise Power BI-rapporter på startsiden.

> [!IMPORTANT]
> Du må ha en gyldig konto med [!INCLUDE [prodshort](includes/prodshort.md)] og med Power BI. Hvis du vil endre noen av rapportene, må du også laste ned Power BI Desktop. Hvis du vil ha mer informasjon, kan du se [Bruke Business Central som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md).  

### <a name="on-first-login"></a>Ved første pålogging

Når du logger på [!INCLUDE [prodshort](includes/prodshort.md)] første gang, vil du legge merke til en tom Power BI-del på startsiden. Hvis du vil vise rapportene, må du først koble til Power BI ved å velge koblingen *Kom i gang med Power BI*.

[!INCLUDE [prodshort](includes/prodshort.md)] kommuniserer deretter med Power BI-tjenesten for å finne ut om du har en gyldig Power BI-konto. Når lisensen er kontrollert, vises standard Power BI-rapporter på startsiden din.

### <a name="selecting-power-bi-reports"></a>Velge Power BI-rapporter

Power BI-kontrollen på startsiden kan vise en hvilken som helst Power BI-rapport. Hvis du vil vise en eksisterende rapport, velger du **Velg rapport**-handlingen fra Power BI-rullegardinkommandolisten.  

Rapportsiden viser en oversikt over alle Power BI-rapportene du har tilgang til. Denne listen er hentet fra Power BI-arbeidsområdet. Aktiver hver rapport du vil vise på startsiden, og klikk deretter OK. Du kommer tilbake til startsiden, og den siste rapporten du aktiverte, vises. Ved hjelp av rullegardinmenyen bruker du forrige eller neste kommando til å navigere mellom rapporter.  

### <a name="get-reports"></a>Hente rapporter

Hvis du ikke ser noen rapporter på Velg rapporter-siden eller ikke ser rapporten du vil bruke. Du kan velge å få rapporter fra *Min organisasjon* eller fra *Tjenester*.
Velg *Min organisasjon* for å gå til Power BI-tjenestene der du kan vise rapportene i organisasjonen som du har tilgang til å vise, og legg dem til i arbeidsområdet. Velg *Tjenester* for å gå til Microsoft AppSource, der du kan installere Power BI-apper.  

Du kan også velge å opprette nye Power BI-rapporter. Når disse rapportene er publisert på Power BI-arbeidsområdet, vil de vises på denne siden.  

### <a name="managing-reports"></a>Administrere rapporter

I Power BI-inndelingen på startsiden kan du velge **Behandle rapport**-handlingen fra rullegardinlisten, slik at du kan endre rapporten som var i fokus i rollesenteret.  

Endringer kan gjøres i rapporten og lagres.  Eventuelle endringer som gjøres i rapporten, vil bli endret for alle brukere denne rapporten deles med, siden du endrer rapporten som er lagret i Power BI-tjenesten.  

Velg Lagre når du har fullført endringene. Hvis dette er en delt rapport, bør du velge Lagre som for å unngå å gjøre endringer for alle brukere.
Gå tilbake til rollesenteret, så vil du se den oppdaterte rapporten. Hvis du valgte Lagre som-kommandoen, må du åpne siden Velg rapport og aktivere den nye rapporten.

### <a name="uploading-reports"></a>Laste opp rapporter

Du kan laste opp nye Power BI-rapporter og dele dem med alle brukerne av [!INCLUDE [prodshort](includes/prodshort.md)]. Rapportene deles i hvert selskap i [!INCLUDE [prodshort](includes/prodshort.md)].  

For å laste opp en rapport velger du handlingen **Last opp rapport** fra rullegardinkommandolisten. Deretter kan du laste opp en pbix-fil som definerer rapportene du vil dele. Du kan endre standardnavnet på filen.  

Når rapporten er lastet opp til Power BI-arbeidsområdet, blir det automatisk lastet opp til Power BI-arbeidsområdene til alle andre brukere i selskapet neste gang de logger på [!INCLUDE [prodshort](includes/prodshort.md)].

## <a name="system-requirements"></a>Systemkrav

Hvis du vil importere [!INCLUDE[prodshort](includes/prodshort.md)]-data til Power BI, må du ha tilgang til webtjenestene som brukes for å hente data. Webtjenestene som kreves for hver Power BI-app, inneholder:

### <a name="microsoft-dynamics-365-business-central--crm"></a>Microsoft Dynamics 365 Business Central – CRM

- Salgsmuligheter
- Excel-mal – Vis selskapsinformasjon
- Power BI-rapportetiketter

### <a name="microsoft-dynamics-365-business-central--finance"></a>Microsoft Dynamics 365 Business Central – Finance

- PowerBIFinance
- Excel-mal – Vis selskapsinformasjon
- Power BI-rapportetiketter

### <a name="microsoft-dynamics-365-business-central---sales"></a>Microsoft Dynamics 365 Business Central – Sales

- Varesalg etter kunde
- Instrumentbord for salg
- Excel-mal – Vis selskap
- Power BI-rapportetiketter

> [!NOTE]
> [!INCLUDE [prodshort](includes/prodshort.md)] lokalt bruker samme webtjenesteendepunkt som [!INCLUDE [prodshort](includes/prodshort.md)] online.

## <a name="web-services"></a>Webtjenester

Det er enkelt å finne webtjenestene ved å søke etter *webtjenester* i [!INCLUDE[prodshort](includes/prodshort.md)]. På siden **Webtjenester** kontrollerer du at **Publiser**-feltet er valgt for webtjenestene som er oppført over.

## <a name="troubleshooting"></a>Feilsøking

Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er nevnt ovenfor, og du vil se data fra demoselskapet eller ditt eget selskap hvis du importerer data fra din gjeldende økonomiløsning. Hvis noe går galt, vil denne delen imidlertid gir en løsning for de vanligste problemene.  

### <a name="you-do-not-have-a-power-bi-account"></a>Du har ikke Power BI-konto

En Power BI-konto er ikke satt opp. For at du skal kunne ha gyldig Power BI-konto, må du ha en lisens, og du må ha logget på Power BI tidligere for at Power BI-arbeidsområdet skal kunne opprettes.  

### <a name="message-there-are-no-enabled-reports-choose-select-report-to-see-a-list-of-reports-that-you-can-display"></a>Melding: Det finnes ingen aktiverte rapporter. Klikk Velg rapport for å se en liste over rapporter du kan vise.

Denne meldingen vil vises hvis standardrapporten ikke ble distribuert til Power BI-arbeidsområdet, eller rapporten ble distribuert, men ble ikke oppdatert. Hvis dette skjer, navigerer du til rapporten i Power BI-arbeidsområdet, velger **Datasett**, **Innstillinger** og deretter oppdaterer legitimasjonen manuelt. Når datasettet er oppdatert, går du tilbake til Business Central og velger rapporten fra **Velg rapporter**-siden manuelt. 

### <a name="you-need-a-power-bi-pro-license-to-install-the-include-prodshortincludesprodshortmd-app-in-power-bi"></a>Du trenger en Power BI Pro-lisens for å installere [!INCLUDE [prodshort](includes/prodshort.md)]-appen i Power BI

Power BI-apper kan bare installeres av brukere som har en Power BI Pro-lisens. Når Power BI-appen er installert, kan du dele den med brukere som ikke har en Power BI Pro-lisens.  

### <a name="parameter-validation-failed-please-make-sure-all-parameters-are-valid"></a>"Parametervalidering mislyktes, du må kontrollere at alle parametrene er gyldige"

Denne feilen angir at en av parameterne ikke er gyldige.

- Den angitte miljøparameteren samsvarer ikke med eksisterende [!INCLUDE [prodshort](includes/prodshort.md)]-produksjon eller sandkassemiljø. 
- Den angitte selskapsparameteren samsvarer ikke med eksisterende [!INCLUDE [prodshort](includes/prodshort.md)]-selskaper. Kontroller selskapsnavnet på **Selskap**-siden i [!INCLUDE [prodshort](includes/prodshort.md)].
- Hvis du kobler til [!INCLUDE [prodshort](includes/prodshort.md)] lokalt. Du har skrevet inn en ugyldig URL-adresse. Du kan bekrefte URL-adressen på **Webtjenester**-siden i [!INCLUDE [prodshort](includes/prodshort.md)]  
- En port er ikke åpen for å tillate at forespørselen din går gjennom brannmuren.

### <a name="login-failed"></a>Påloggingen mislyktes

Hvis du får en "påloggingen mislyktes"-feil etter at du bruker [!INCLUDE [prodshort](includes/prodshort.md)]-legitimasjonen din for å logge deg på, kan dette skyldes et av følgende problemer:

- Kontoen du bruker, har ikke tillatelse til å hente [!INCLUDE [prodshort](includes/prodshort.md)]-dataene fra kontoen din. Kontroller at du har tilgang til de nødvendige dataene i [!INCLUDE [prodshort](includes/prodshort.md)], og prøv på nytt.
- Du har valgt en annen godkjenningstype enn Enkel hvis du kobler til [!INCLUDE [prodshort](includes/prodshort.md)] lokalt.
- Du har ikke skrevet inn et gyldig brukernavn eller passord.

### <a name="incorrect-company-name"></a>Feil selskapsnavn

En vanlige feil er angi visningsnavnet for selskapet i stedet for selskapsnavnet. Søk etter **Selskaper** for å finne selskapsnavnet. Bruk **Navn**-feltet når du angir selskapsnavnet.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nøkkelen samsvarer ikke med noen rader i tabellen

Hvis du angir et ugyldige selskapsnavn under tilkoblingen, kan du få du feilmeldingen Nøkkelen samsvarer ikke med en rad i tabellen. Angi riktig selskapsnavn, og prøv å koble til på nytt.

### <a name="historical-data-appears-to-be-missing"></a>Historisk data ser ut til å mangle

Når Power BI-appen er installert og dataene vises i Power BI, oppdager du kanskje at ikke alle dataene vises. Datasettene filtreres for å returnere bare de forrige 365 dagene med data. Denne standarden er på plass til å gjøre rapportene raskere.  

### <a name="i-only-see-data-for-a-single-company"></a>Jeg ser bare data for ett selskap

Power BI-appen viser bare data fra [!INCLUDE [prodshort](includes/prodshort.md)]-selskapet som ble definert da Power BI-appen ble installert. Data fra andre selskaper kan legges til i rapportene ved å legge til nye spørringer som bruker ulike selskaper som datakilde.  

## <a name="see-also"></a>Se også

[Power BI for forbrukere](/power-bi/consumer/end-user-consumer)  
[Nytt utseende på Power BI-tjenesten](/power-bi/service-new-look)  
[Hurtigstart: Koble til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-dokumentasjon](/power-bi/)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for Power Apps](across-how-use-financials-data-source-powerapps.md)  
[Ved hjelp av [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power Automate](across-how-use-financials-data-source-flow.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
