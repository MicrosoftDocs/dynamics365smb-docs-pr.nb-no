---
title: Koble Power BI til Finance and Operations, Business edition | Microsoft-dokumentasjon
description: "Få innsikt, forretningsintelligens og ytelsesindikatorer fra Finance and Operations, Business edition-dataene på en enkel måte med innholdspakkene Power BI og Finance and Operations, Business edition."
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: nb-no
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a>Koble Power BI til Finance and Operations, Business edition-innholdspakker
Få innsikt i Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene på en enkel måte med Power BI og Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-innholdspakkene. Power BI henter dataene, og bygger deretter et forhåndskonfigurert instrumentbord og rapporter basert på dataene.

> [!NOTE]  
>  Du må ha en gyldig konto for Dynamics 365 og Power BI. Du må også laste ned [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).  
>  Power BI-innholdspakker krever tilgang til tabellene der opplysningene hentes fra. Du finner mer informasjon om kravene nedenfor.  

## <a name="how-to-connect"></a>Koble til
1. Velg **Hent data** nederst i navigasjonsruten til venstre.  
![Navigere til Hent data](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. I **Tjenester**-boksen velger du **Hent**. Dette åpner et vindu med **AppSource** og **Apper for Power BI-apper**.  
![Velge innholdspakker fra elektroniske tjenester](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Velg **Apper** fra fanen **Apper for Power BI-apper**, og velg innholdspakken **Microsoft Dynamics 365 for Finance and Operations** som du vil bruke, og velg deretter **Få det nå**.  
![Velg Dynamics 365 for Finance and Operations, Business edition, og velg Få det nå!](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Når du blir spurt, skriver du inn navnet på *selskapet ditt* i [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dette er ikke visningsnavnet.  
![Velg Dynamics 365 for Finance and Operations, Business edition, og velg Få det nå!](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Når du er tilkoblet, lastes det automatisk inn et instrumentbord, en rapport og et datasett i Power BI-arbeidområdet. Når du er ferdig, oppdateres flisene med dataene fra kontoen.
![Velg Dynamics 365 for Finance and Operations, Business edition, og velg Få det nå!](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Hva nå?

- Prøv [å stille et spørsmål i spørsmål og svar-boksen](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) øverst i instrumentbordet.  
- [Endre flisene](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) i instrumentbordet.  
- [Velge en flis](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) for å åpne den underliggende rapporten.  
- Selv om det er planlagt at datasettet ditt oppdateres daglig, kan du endre oppdateringstidsplanen eller prøve å oppdatere den ved behov ved hjelp av **Oppdater nå**.

## <a name="system-requirements"></a>Systemkrav
Hvis du vil importere [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-dataene til Power BI, må du ha tillatelse til å webtjenestene som brukes for å hente data. Webtjenestene som kreves for hver innholdspakke:

**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Sales**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Finance**
- PowerBIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – jobber**
- Prosjektoversikt
- Prosjektplanleggingslinjer
- Prosjektoppgavelinjer

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Kundeoversikt**
- ItemSalesbyCustomer
- Varekjøpsliste_for_Power_BI
- Varesalgsliste_for_Power_BI
- SalesDashboard
- Kundeliste_for_Power_BI
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Vareliste**
- ItemSalesbyCustomer
- Varekjøpsliste_for_Power_BI
- Varesalgsliste_for_Power_BI
- Varer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Leverandørliste**
- ItemSalesbyCustomer
- Varekjøpsliste_for_Power_BI
- Varesalgsliste_for_Power_BI
- Varer
- SalesDashboard
- Kundeliste_for_Power_BI
- ItemSalesbyCustomer
- Leverandørliste_for_Power_BI
- ExcelTemplateViewCompany

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
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  
[Definere rapportering for [!INCLUDE[d365fin](includes/d365fin_md.md)] i Power BI](across-how-use-financials-data-source-powerbi.md)  

