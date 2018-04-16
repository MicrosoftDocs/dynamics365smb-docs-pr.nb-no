---
title: Koble Power BI til Business Central | Microsoft-dokumentasjon
description: "Få innsikt, forretningsintelligens og KPI-er fra Business Central-dataene på en enkel måte med Power BI og Business Central-innholdspakkene."
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 04/03/2018
ms.author: solsen
redirect_url: admin-powerbi
ms.translationtype: HT
ms.sourcegitcommit: 9cad9c7e2b54506e60af7d38d42f413599a44d01
ms.openlocfilehash: 7b9140611a47b8b823274763731cf000258c681e
ms.contentlocale: nb-no
ms.lasthandoff: 04/03/2018

---
# <a name="connecting-power-bi-to-dynamics-365-business-central-content-packs"></a>Koble Power BI til Dynamics 365 Business Central-innholdspakker
Få innsikt i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene på en enkel måte med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innholdspakkene. Power BI henter dataene, og bygger deretter et forhåndskonfigurert instrumentbord og rapporter basert på dataene.

Du må ha en gyldig konto for Dynamics 365 og Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) hvis du vil opprette dine egne Power BI-rapporter. Power BI-innholdspakker krever tilgang til tabellene der opplysningene hentes fra. Du finner mer informasjon om kravene nedenfor.  

## <a name="how-to-connect"></a>Koble til
1. Velg **Hent data** nederst i navigasjonsruten til venstre.  
![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)

Du kan også komme i gang fra Dynamics 365 Business Edition. Gå til rollesenteret og deretter **Rapportvalg** i rollesenterdelen i Power BI. Velg enten **Service** eller **Min organisasjon** på båndet. Når en av disse handlingene er valgt, kommer du enten til organisasjonsgalleriet i Power BI eller til tjenestebiblioteket i Power BI, som også filtreres for å bare vise innholdspakker knyttet til [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].

2. I **Tjenester**-boksen velger du **Hent**. Dette åpner et vindu med **AppSource** og **Apper for Power BI-apper**.  
![Velge innholdspakker fra elektroniske tjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Velg **Apper** fra fanen **Apper for Power BI-apper**, velg innholdspakken **Microsoft Dynamics 365 Business Central** som du vil bruke, og velg deretter **Få det nå**.  
![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Når du blir spurt, skriver du inn navnet på *selskapet ditt* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dette er ikke visningsnavnet. Du finner selskapsnavnet på siden Selskaper i din [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-forekomst. 
![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Når du er tilkoblet, lastes det automatisk inn et instrumentbord, en rapport og et datasett i Power BI-arbeidområdet. Når du er ferdig, oppdateres flisene med dataene fra [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]-selskapet.
![Velg Dynamics 365 Business Central, og velg Få det nå](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hva nå?

- Prøv [å stille et spørsmål i spørsmål og svar-boksen](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) øverst i instrumentbordet.
- [Endre flisene](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i instrumentbordet.  
- [Velge en flis](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.  
- Selv om det er planlagt at datasettet ditt oppdateres daglig, kan du endre oppdateringstidsplanen eller prøve å oppdatere den ved behov ved hjelp av **Oppdater nå**.

## <a name="system-requirements"></a>Systemkrav
Hvis du vil importere [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene til Power BI, må du ha tillatelse til å webtjenestene som brukes for å hente data. Webtjenestene som kreves for hver innholdspakke:

## <a name="role-center-reports"></a>Rapporter i rollesenter

**Microsoft Dynamics 365 Business Central – CRM**
- Salgsmuligheter
- Excel-mal – Vis selskap
- Etiketter for Power BI-rapport

**Microsoft Dynamics 365 Business Central – Finance**
- PowerBIFinance
- Excel-mal – Vis selskap
- Etiketter for Power BI-rapport

**Microsoft Dynamics 365 Business Central – Jobs**
- Prosjektoversikt
- Prosjektplanleggingslinjer
- Prosjektoppgavelinjer
- Etiketter for Power BI-rapport
- Excel-mal – Vis selskap

**Microsoft Dynamics 365 Business Central - Sales**
- Instrumentbord for salg
- Excel-mal – Vis selskap
- Etiketter for Power BI-rapport

## <a name="list-page-reports"></a>Rapporter for siden Liste 

**Microsoft Dynamics 365 Business Central – Customers List**
- Varesalg etter kunde
- Varekjøpsliste for Power BI
- Varesalgsliste for Power BI
- Instrumentbord for salg
- Kundeliste for Power BI
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport 

**Microsoft Dynamics 365 Business Central - General Ledger Entries List**
- Finansbeløpsliste for Power BI
- Finansbudsjettert beløp for Power BI
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport

**Microsoft Dynamics 365 Business Central – Items List**
- Varesalg etter kunde
- Varekjøpsliste for Power BI
- Varesalgsliste for Power BI
- Instrumentbord for salg
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport

**Microsoft Dynamics 365 Business Central – Jobs List**
- Prosjektliste for Power BI
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport

**Microsoft Dynamics 365 Business Central – Purchase Invoices List**
- Kjøpsliste for Power BI
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport

**Microsoft Dynamics 365 Business Central – Sales Orders List**
- Salgsliste for Power BI
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport


**Microsoft Dynamics 365 Business Central – Vendors List**
- Varekjøpsliste for Power BI
- Varesalgsliste for Power BI
- Leverandørliste for Power BI
- ExcelTemplateViewCompany
- Etiketter for Power BI-rapport

## <a name="web-services"></a>Webtjenester
Det er enkelt å finne webtjenestene ved å søke etter webtjenester i [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Pass på at det er merket av for Publiser i listen for webtjenestene som vises ovenfor.

## <a name="troubleshooting"></a>Feilsøking
Power BI-instrumentbordet er avhengig av de publiserte webtjenestene som er nevnt ovenfor, og du vil se data fra demonstrasjonsselskapet eller ditt eget selskap hvis du importerer data fra din gjeldende økonomiløsning. Hvis noe går galt, vil denne delen imidlertid gir en løsning for de vanligste problemene.

### <a name="incorrect-company-name"></a>Feil selskapsnavn  
En vanlige feil er angi visningsnavnet for selskapet i stedet for selskapsnavnet. Søk etter **Selskaper** for å finne selskapsnavnet. Bruk **Navn**-feltet når du angir selskapsnavnet.

### <a name="incorrect-user-name-and-password"></a>Feil brukernavn og passord  
Brukernavnet og passordet som brukes for å koble til, er det samme som brukes for å koble til Microsoft Office 365-kontoen.  

Innholdspakker krever også at du har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto. Når du angir legitimasjonen, finner vi automatisk Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-leietakerne du har tilgang til. Hvis du ikke har en Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-konto som er lisensiert eller en prøveversjon, vises en feilmelding.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>Nøkkelen samsvarer ikke med en rad i tabellen
Hvis du angir et ugyldige selskapsnavn under tilkoblingen, kan du få du feilmeldingen Nøkkelen samsvarer ikke med en rad i tabellen. Angi riktig selskapsnavn, og prøv å koble til på nytt.

## <a name="see-also"></a>Se også
[Komme i gang med Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI – grunnleggende begreper](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)  
[Forretningsintelligens](bi.md)  
[Komme i gang](product-get-started.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Definere rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)  

