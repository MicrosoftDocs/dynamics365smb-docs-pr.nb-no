---
title: Innholdspakker for Business Central og Power BI | Microsoft Docs
description: Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Power BI- og Business Central-innholdspakkene.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: f51de349c4b13eaabd185cdb728d59006dfe6db6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2019
ms.locfileid: "916377"
---
# <a name="enabling-your-business-data-for-power-bi"></a>Aktivere forretningsdata for Power BI
Få innsikt i [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene på en enkel måte med Power BI- og [!INCLUDE[d365fin](includes/d365fin_md.md)]-innholdspakkene. Power BI henter dataene, og deretter bygger du et forhåndskonfigurert instrumentbord og rapporter basert på dataene.  

Du må ha en gyldig konto med Power BI og med Dynamics 365. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) hvis du vil opprette et egne Power BI-rapporter. Power BI-innholdspakker krever tilgang til tabellene der opplysningene hentes fra. Du finner mer informasjon om kravene nedenfor.  

Microsoft har publisert følgende innholdspakker:

| App | Description |
| --- | --- |
| Microsoft Business Central | Gir et instrumentbord med viktige økonomiske data over tid, for eksempel inntekter kontra utgifter, driftsmargin og kontantsyklus.|
| Microsoft Business Central - CRM | Inneholder et instrumentbord med viktige opplysninger om salgsmuligheter og kontakter.  |
| Microsoft Business Central - Sales | Inneholder et instrumentbord med viktige opplysninger om salg og beholdning. |

## <a name="using-the-dashboards"></a>Bruke instrumentbordene
Hver innholdspkke inneholder rapporter som du kan se på:

* Velg hvilken som helst visning på instrumentbordet for å hente frem en av de underliggende rapportene.  
* Filtrere rapporten eller legg til felt som du vil overvåke.  
* Fest denne tilpassede visningen på instrumentbordet for å fortsette sporing.  
  Du kan oppdatere dataene manuelt, og kan du definere en oppdateringstidsplan. Hvis du vil ha mer informasjon, se [Konfigurere planlagt oppdatering](https://powerbi.microsoft.com/en-us/documentation/powerbi-refresh-scheduled-refresh/).  

Innholdspakkene er forhåndskonfigurert til å arbeide med data fra demonstrasjonsselskapet som du får når du registrerer deg for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Når du installerer appene i Power BI og kobler til dine egne data, fungerer noen av rapportene ikke, fordi de er avhengige av data som selskapet ditt ikke har. I slike tilfeller kan du bare fjerne rapporten fra instrumentbordet.  

> [!NOTE]  
>   Du kan også lage dine egne rapporter og instrumentbord i Power BI basert på [!INCLUDE[d365fin](includes/d365fin_md.md)]-dataene dine. Hvis du vil ha mer informasjon, kan du se [Koble forretningsdata til Power BI](across-how-use-financials-data-source-powerbi.md).  

## <a name="how-to-connect"></a>Koble til
1. Velg **Hent data** nederst i navigasjonsruten til venstre.  
![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Du kan også starte fra Dynamics 365 Business Edition. Gå til rollesenteret og deretter **Rapportvalg** i rollesenterdelen i Power BI. Velg enten **Service** eller **Min organisasjon** på båndet. Når en av disse handlingene er valgt, kommer du enten til organisasjonsgalleriet i Power BI eller til tjenestebiblioteket i Power BI, som også filtreres for å bare vise innholdspakker knyttet til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. I **Tjenester**-boksen velger du **Hent**. Dette åpner en side med **AppSource** og **Apper for Power BI-apper**.  
![Velge innholdspakker fra elektroniske tjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Velg **Apper** fra fanen **Apper for Power BI-apper**, velg innholdspakken **Microsoft Dynamics 365 Business Central** som du vil bruke, og velg deretter **Få det nå**.  
![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Når du blir spurt, skriver du inn navnet på *selskapet ditt* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dette er ikke visningsnavnet. Du finner selskapsnavnet på siden Selskaper i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-forekomst.  
![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Når du er tilkoblet, lastes det automatisk inn et instrumentbord, en rapport og et datasett i Power BI-arbeidområdet. Når du er ferdig, oppdateres flisene med dataene fra [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-selskapet.
![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hva nå?

- Prøv [å stille et spørsmål i spørsmål og svar-boksen](https://docs.microsoft.com/en-us/power-bi/service-q-and-a-tips) øverst i instrumentbordet.
- [Endre flisene](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i instrumentbordet.  
- [Velge en flis](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.  
- Selv om det er planlagt at datasettet ditt oppdateres daglig, kan du endre oppdateringstidsplanen eller prøve å oppdatere den ved behov ved hjelp av **Oppdater nå**.

## <a name="system-requirements"></a>Systemkrav
Hvis du vil importere [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene til Power BI, må du ha tilgang til webtjenestene som brukes for å hente data. Webtjenestene som kreves for hver innholdspakke:

## <a name="role-center-reports"></a>Rapporter i rollesenter

**Microsoft Dynamics 365 Business Central – CRM**
- Salgsmuligheter
- Excel-mal – Vis selskap
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel-mal – Vis selskap
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Jobs**
- Prosjektoversikt
- Prosjektplanleggingslinjer
- Prosjektoppgavelinjer
- Power BI-rapportetiketter
- Excel-mal – Vis selskap

**Microsoft Dynamics 365 Business Central – Sales**
- Instrumentbord for salg
- Excel-mal – Vis selskap
- Power BI-rapportetiketter

## <a name="list-page-reports"></a>Rapporter for siden Liste

**Microsoft Dynamics 365 Business Central – Customers List**
- Varesalg etter kunde
- Varekjøpsliste for Power BI
- Varesalgsliste for Power BI
- Instrumentbord for salg
- Power BI Kundeoversikt
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Finansbeløpsliste for Power BI
- Finansbudsjettert beløp for Power BI
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Items List**
- Varesalg etter kunde
- Varekjøpsliste for Power BI
- Varesalgsliste for Power BI
- Instrumentbord for salg
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Jobs List**
- Prosjektliste for Power BI
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Kjøpsliste for Power BI
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Salgsoversikt for Power BI
- ExcelTemplateViewCompany
- Power BI-rapportetiketter


**Microsoft Dynamics 365 Business Central – Vendors List**
- Varekjøpsliste for Power BI
- Varesalgsliste for Power BI
- Leverandørliste for Power BI
- ExcelTemplateViewCompany
- Power BI-rapportetiketter

## <a name="web-services"></a>Webtjenester
Det er enkelt å finne webtjenestene ved å søke etter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Pass på at det er merket av for Publiser i listen for webtjenestene som vises ovenfor.

## <a name="troubleshooting"></a>Feilsøking
Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er nevnt ovenfor, og du vil se data fra demoselskapet eller ditt eget selskap hvis du importerer data fra din gjeldende økonomiløsning. Hvis noe går galt, vil denne delen imidlertid gir en løsning for de vanligste problemene.

### <a name="incorrect-company-name"></a>Feil selskapsnavn  
En vanlige feil er angi visningsnavnet for selskapet i stedet for selskapsnavnet. Søk etter **Selskaper** for å finne selskapsnavnet. Bruk **Navn**-feltet når du angir selskapsnavnet.

### <a name="incorrect-user-name-and-password"></a>Feil brukernavn og passord  
Brukernavnet og passordet som brukes for å koble til, er det samme som brukes for å koble til Microsoft Office 365-kontoen.  

Innholdspakker krever også at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto. Når du angir legitimasjonen, finner vi automatisk Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leietakerne du har tilgang til. Hvis du ikke har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto som er lisensiert eller en prøveversjon, vises en feilmelding.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nøkkelen samsvarer ikke med en rad i tabellen
Hvis du angir et ugyldige selskapsnavn under tilkoblingen, kan du få du feilmeldingen Nøkkelen samsvarer ikke med en rad i tabellen. Angi riktig selskapsnavn, og prøv å koble til på nytt.

## <a name="see-also"></a>Se også
[Kom i gang med Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI – grunnleggende begreper](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Importere forretningsdata fra andre økonomisystemer](across-import-data-configuration-packages.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde for PowerApps](across-how-use-financials-data-source-powerapps.md)  
[Ved hjelp av [!INCLUDE[d365fin](includes/d365fin_md.md)] i Microsoft Flow](across-how-use-financials-data-source-flow.md)   

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
