---
title: Finance and Operations, Business edition og Power BI-innholdspakker | Microsoft-dokumentasjon
description: "Få innsikt, forretningsintelligens og ytelsesindikatorer fra Finance and Operations, Business edition-dataene på en enkel måte med innholdspakkene Power BI og Finance and Operations, Business edition."
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 09/05/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 8c8a52f20abe27de7063a0879f529086263d0675
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere forretningsdata for Power BI
Få innsikt i [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene på en enkel måte med Power BI og [!INCLUDE[d365fin](includes/d365fin_md.md)]-innholdspakkene. Power BI henter dataene, og deretter bygger du et forhåndskonfigurert instrumentbord og rapporter basert på dataene.  

Microsoft har publisert følgende innholdspakker:

| App | Description |
| --- | --- |
| Microsoft Finance and Operations, Business edition | Gir et instrumentbord med viktige økonomiske data over tid, for eksempel inntekter kontra utgifter, driftsmargin og kontantsyklus.|
| Microsoft Finance and Operations, Business edition – CRM | Inneholder et instrumentbord med viktige opplysninger om salgsmuligheter og kontakter.  |
| Microsoft Finance and Operations, Business edition – Sales | Inneholder et instrumentbord med viktige opplysninger om salg og beholdning. |

## <a name="using-the-dashboards"></a>Bruke instrumentbordene
Hver innholdspkke inneholder rapporter som du kan se på:

* Velg hvilken som helst visning på instrumentbordet for å hente frem en av de underliggende rapportene.  
* Filtrere rapporten eller legg til felt som du vil overvåke.  
* Fest denne tilpassede visningen på instrumentbordet for å fortsette sporing.  
  Du kan oppdatere dataene manuelt, og kan du definere en oppdateringstidsplan. Hvis du vil ha mer informasjon, se [Konfigurere planlagt oppdatering](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Innholdspakkene er forhåndskonfigurert til å arbeide med data fra demonstrasjonsselskapet som du får når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du installerer appene i Power BI og kobler til dine egne data, fungerer noen av rapportene ikke, fordi de er avhengige av data som selskapet ditt ikke har. I slike tilfeller kan du bare fjerne rapporten fra instrumentbordet.  

> [!NOTE]  
>   Du kan også lage dine egne rapporter og instrumentbord i Power BI basert på [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene dine. Hvis du vil ha mer informasjon, kan du se [Koble forretningsdata til Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="accessing-included365finincludesd365finmdmd-in-power-bi"></a>Tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI
Hvis du vil se [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene i Power BI, må du ha følgende:  

* Tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Finance and Operations, Business edition](http://go.microsoft.com/fwlink/?LinkID=759714).  
* Tilgang til Power BI. Hvis du vil ha mer informasjon , kan du se [Power BI](https://powerbi.microsoft.com).

På Power BI-nettstedet finner du mer informasjon om [hvordan du kobler til tjenester med innholdspakker for Power BI](http://go.microsoft.com/fwlink/?LinkID=760850).  

For å få tilgang til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data i Power BI må du på tilkoblingssiden angi følgende informasjon:

| Felt | Beskrivelse |
| --- | --- |
| **Nettadresse for OData-feed** |OData URL-adressen slik at Power IB kan ha tilgang til data fra selskapet ditt, som for eksempel https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('Mine%2Business'). |
| **Godkjenningsmetode** |Velg **Grunnleggende**. |
| **Brukernavn** |Ditt navn slik det vises for kontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], som *John Smith*. |
| **Passord** |Dette er tilgangsnøkkelen for webtjenesten for brukerkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)]. |

Dette betyr at du må ha to deler av informasjon fra [!INCLUDE[d365fin](includes/d365fin_md.md)]: *Nettadressen for OData* og *tilgangsnøkkelen for webtjenesten* for din brukerkonto.  

### <a name="getting-the-url"></a>Hente nettadressen
Når du legger til [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI, må du angi en nettadresse slik at Power BI kan få tilgang til data fra firmaet. På tilkoblingssiden kalles nettadressen **Nettadresse for OData-feed**, og den må ha følgende format:

         https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
I dette eksemplet er *mittfirma* navnet på [!INCLUDE[d365fin](includes/d365fin_md.md)]-tjenesten, og *CRONUS US* er navnet på demonstrasjonsselskapet der *%20* representerer mellomrommet i navnet.   
Hvis du vil hente nettadressen, søler du etter og åpner vinduet **Webtjeneste** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dette vinduet viser webtjenester som er tilgjengelige, og du kan kopiere koblingen fra feltet **Nettadresse for OData** for en av de standard OData-webtjenestene.  

### <a name="getting-the-user-name-and-the-web-service-access-key"></a>Få brukernavnet og tilgangnøkkelen for webtjenesten
Hvis du vil bruke data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI, i vinduet **Koble til Financials** må du angi et brukernavn og et passord. Brukernavnet er navnet som vises for kontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], slik at Power BI kan logge på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Passordet er tilgangsnøkkelen for webtjenesten som er angitt for brukerkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Du finner denne informasjonen, i [!INCLUDE[d365fin](includes/d365fin_md.md)], søk etter **Brukere**-vinduet, og åpne deretter kortet for din brukerkonto. På den **Generelt** hurtigfanen, kopiere innholdet i **Brukernavn**-feltet og hurtigfanen **Tilgang til webtjeneste**, kopiere innholdet i feltet **Webtjeneste – tilgangsnøkkel**. Hvis feltet **Webtjeneste – tilgangsnøkkel** er tomt, går du til båndet og velger **Endre tilgangsnøkkel for webtjeneste**, velger feltet **Nøkkel utløper aldri** og velger deretter OK. Deretter kan du kopiere nøkkelen.  

## <a name="getting-data-from-included365finincludesd365finmdmd"></a>Hente data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]
[!INCLUDE[d365fin](includes/d365fin_md.md)]-instrumentbordet viser de vanligste rapportene som du vil bruke til å spore din virksomhet. Dataene blir hentet fra [!INCLUDE[d365fin](includes/d365fin_md.md)]-firmaet ved hjelp av webtjenester for å lese sanntidsdata. I [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder vinduet **Webtjenester** webtjenester som er angitt for deg.

> [!NOTE]  
>   Hvis du endrer navnet på noen av disse webtjenestene, vises ikke dataene i Power BI.  
Hvis du vil legge til bruker andre data i Power BI, må du finne tabellene i [!INCLUDE[d365fin](includes/d365fin_md.md)], vise dem som webtjenester og deretter legge dem til i Content Pack. Dette er et avansert scenario, og vi anbefaler at du starter med data som allerede er tilgjengelige i Power BI.  

## <a name="troubleshooting"></a>Feilsøking
Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er nevnt ovenfor, og du vil se data fra demonstrasjonsselskapet eller ditt eget selskap hvis du importerer data fra din gjeldende økonomiløsning. Hvis noe går galt, vil denne delen imidlertid gir en løsning for de vanligste problemene.  

**"Parametervalidering mislyktes, må du kontrollere at alle parametrene er gyldige"**  
Hvis du ser denne feilen når du angir nettadressen for [!INCLUDE[d365fin](includes/d365fin_md.md)], må du kontrollere at følgende krav er oppfylt:  

* Nettadressen har nøyaktig dette mønsteret:

    https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')  
* Slett all tekst etter firmanavnet i parentes  
* Kontroller at det ikke er en etterfølgende skråstrek på slutten av nettadressen.  
* Kontroller at det er en sikker tilkobling, som angis ved at nettadressen begynner med *https*.  

**"Påloggingen mislyktes"**  
Hvis du får en "påloggingen mislyktes"-feil når du logger på instrumentbordet ved hjelp av [!INCLUDE[d365fin](includes/d365fin_md.md)]-legitimasjonen, kan dette skyldes ett av følgende problemer:

* Kontoen du bruker har ikke tillatelse til å lese [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene fra kontoen din.

    Kontroller brukerkontoen i [!INCLUDE[d365fin](includes/d365fin_md.md)], og kontroller at du har brukt riktig tilgangsnøkkel for webtjeneste som passord, og prøv deretter på nytt.  
* [!INCLUDE[d365fin](includes/d365fin_md.md)]-forekomsten som du prøver å koble til, har ikke et gyldig SSL-sertifikat. I dette tilfellet vil du se en mer detaljert feilmelding ("kan ikke opprette en klarert relasjon for SSL").

    > [!NOTE]  
>   Selvsignerte sertifikater støttes ikke.  

**"Oops"**  
Hvis du ser en "Oops"-feilmelding etter at du har fullført godkjenningsdialogboksen, forårsakes dette vanligvis av et problem med tilkoblingen til dataene for Content Pack.

* Kontroller at nettadressen følger mønsteret som ble angitt tidligere:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')`  
* En vanlig feil er å angi den fullstendige nettadressen for en bestemt webtjeneste:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/Company('CRONUS%20US')/powerbifinance`
* Det kan også hende du har glemt å angi navnet på firmaet:

    `https://mybusiness.financials.dynamics.com:7048/MS/ODataV4/`

## <a name="see-also"></a>Se også
[Forretningsintelligens](bi.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Overføre forretningsdata fra andre økonomisystemer](upload-data.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for Power BI](across-how-use-financials-data-source-powerbi.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

