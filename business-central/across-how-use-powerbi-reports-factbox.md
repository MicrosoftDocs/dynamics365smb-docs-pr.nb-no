---
title: Vis egendefinerte Power BI-rapporter
description: Du kan bruke Power BI-faktaboks til å vise Power BI-rapporter og få ekstra innsikt i postdataene i nøkkellister.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 12/13/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="creating-power-bi-reports-for-displaying-list-data-in-"></a>Opprett Power BI-rapporter for å vise listedata i [!INCLUDE[prod_short](includes/prod_short.md)]

[!INCLUDE[prod_long](includes/prod_long.md)] inkluderer et kontrollelement for en Power BI-faktaboks på mange viktige listesider. Formålet med denne faktaboksen er å vise Power BI-rapporter som er knyttet til poster i listene, og som gir ekstra innsikt i dataene. Poenget er at etter hvert som du flytter mellom radene i listen, oppdateres rapporten for den valgte posten.

[!INCLUDE[prod_long](includes/prod_long.md)] leveres med noen av disse rapportene. Du kan også opprette egendefinerte rapporter som vises i denne faktaboksen. Oppretting av disse rapportene minner om andre rapporter. Det er imidlertid noen få utformingsregler du må følge for å være sikker på at rapportene vises som forventet. Disse reglene forklares i denne artikkelen.

> [!NOTE]
> Hvis du vil ha generell informasjon om hvordan du oppretter og publiserer rapporter for Power BI Business Central, kan du se [Bygge Power BI-rapporter for å vise [!INCLUDE [prod_long](includes/prod_long.md)]-data](across-how-use-financials-data-source-powerbi.md). 

## <a name="prerequisites"></a>Forutsetninger

- En Power BI-konto.
- Power BI Desktop.

<!-- 
For more information about getting started, see [Use [!INCLUDE[prod_short](includes/prod_short.md)] as a Power BI Data Source](across-how-use-financials-data-source-powerbi.md).-->

## <a name="create-a-report-for-a-list-page"></a>Lage en rapport for en listeside

1. Start Power BI Desktop.
2. Velg **Hent data**, og begynn med å velge datakilden for rapporten.

    Angi listesidene for Business Central som inneholder dataene du vil ha med i rapporten. Hvis du for eksempel vil opprette en rapport for **Salgsfakturaer**-listen, tar du med sider som er knyttet til salg.

    Hvis du vil ha mer informasjon, følger du instruksjonene under [Legge til [!INCLUDE[prod_short](includes/prod_short.md)] som en datakilde i Power BI Desktop](across-how-use-financials-data-source-powerbi.md#getdata).

3. Still inn rapportfilteret.

    For å oppdatere dataene til den valgte posten i listen legger du til et filter i rapporten. Filteret må inneholde et felt av datakilden som brukes til entydig identifikasjon av hver post i listen. I utviklersammenheng er dette feltet *prim'rnøkkelen*. I de fleste tilfeller er primærnøkkelen for en liste **Nr.** -feltet.

    Gjør følgende for å stille inn filteret:

    1. I **Filtre** velger du primærnøkkelfeltet fra listen over tilgjengelige felt.
    2. Dra feltet til ruten **Filtre**, og slipp det i boksen **Filtre på alle sider**.
    3. Sett verdien for **Filtertype** til **Grunnleggende filtrering**. Det kan ikke være en side, en visualisering eller et avansert filter.

    ![Angi rapportfilteret for Salgsfaktura-aktivitetsrapporten.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-filter-v3.png)
4. Utform rapportoppsettet.

    Lag oppsettet ved å dra felt og legge til effekter. Hvis du vil ha mer informasjon, kan du se [Arbeide med rapportvisning i Power BI Desktop](/power-bi/create-reports/desktop-report-view) i dokumentasjonen for Power BI.

5. Se de neste avsnittene om å endre størrelse på rapporten og bruke flere sider.

6. Lagre og gi navn til rapporten.

    Gi rapporten et navn som inneholder navnet på listesiden som er knyttet til rapporten, slik det er i klienten. Det skilles imidlertid ikke mellom store og små bokstaver i navnet. La oss si at rapporten er for **Salgsfakturaer**-listesiden. I dette tilfellet tar du med ordet **salgsfakturaer** et sted i navnet, for eksempel **mine salgsfakturaer.pbix** eller **mine_Salgsfakturaer_listen.pbix**.

    Denne navnekonvensjonen er ikke et krav. Den gjør det imidlertid raskere å velge rapporter i [!INCLUDE[prod_short](includes/prod_short.md)]. Når siden for valg av rapport åpnes fra en listeside, brukes et filter automatisk basert på sidenavnet. Filteret har syntaksen `@*<caption>*`, for eksempel `@*Sales Invoices*`. Denne filtreringen utføres for å begrense antall rapporter som vises. Brukere kan fjerne filteret for å få en fullstendig liste over rapporter som er tilgjengelige i Power BI.

7. Når du er ferdig, publiserer du rapporten på vanlig måte.

    Hvis du vil ha mer informasjon, kan du se [Publisere en rapport](across-how-use-financials-data-source-powerbi.md#publish-reports).

8. Test rapporten.

    Når rapporten er publisert på arbeidsområdet, skal den være tilgjengelig fra Power BI-faktaboksen på listesiden i [!INCLUDE[prod_short](includes/prod_short.md)].

    Gjør følgende for å teste det.

    1. Åpne [!INCLUDE[prod_short](includes/prod_short.md)] og gå til listesiden.
    2. Hvis du ikke ser Power BI-faktaboksen, går du til handlingsfeltet og velger **Handlinger** > **Visning** > **Vis/Skjul Power BI-rapporter**.
    3. I Power BI-faktaboksen velger du **Velg rapporter**, merker av for **Aktiver** for rapporten, og velger deretter **OK**.

    Hvis den er utformet riktig, viser rapporten.  

## <a name="set-the-report-size-and-color"></a>Angi rapportstørrelsen og -fargen

Størrelsen på rapporten må settes til 325 x 310 piksler. Denne størrelsen gir riktig skalering av rapporten på den ledige plassen for Power BI-faktabokskontrollen i [!INCLUDE[prod_short](includes/prod_short.md)]. Hvis du vil definere størrelsen på rapporten, fokusere utenfor oppsettsområdet til rapporten, og velg deretter malerrulleikonet.

![Angi bredden og høyden på Salgsfaktura-aktivitetsrapporten.](./media/across-how-use-powerbi-reports-factbox/financials-powerbi-report-sizing-v3.png)

Du kan endre bredden og høyden på rapporten ved å velge **Egendefinert** i **Type**-feltet.

Hvis du vil at bakgrunnen i rapporten skal blandes med bakgrunnsfargen til Power BI-faktabokskontrollen, setter du rapportbakgrunnsfargen til *#FFFFFF* (hvit). 

> [!TIP]
> Bruk [!INCLUDE [prod_short](includes/prod_short.md)]-temafilen til å lage rapporter med de samme farge stilene som [!INCLUDE [prod_short](includes/prod_short.md)]-appene. Hvis du vil ha mer informasjon, kan du se [Bruk [!INCLUDE [prod_short](includes/prod_short.md)]-rapporttemaet](across-how-use-financials-data-source-powerbi.md#theme).

## <a name="reports-with-multiple-pages"></a>Rapporter med flere sider

Du kan opprette én enkelt rapport med flere sider med Power BI. Når det gjelder rapporter som skal vises med listesider, anbefaler vi at de ikke har flere enn én side. Power BI-faktaboksen viser bare den første siden i rapporten.

## <a name="fixing-problems"></a>Løse problemer

Denne delen forklarer hvordan du løser problemer som kan oppstå i når du prøver å vise en Power BI-rapport for en listeside i [!INCLUDE[prod_short](includes/prod_short.md)].  

### <a name="you-cant-see-the-power-bi-factbox-on-a-list-page"></a>Du kan ikke se Power BI-faktaboksen på en listeside

Power BI-faktaboksen er som standard skjult for visning. Hvis du vil vise faktaboksen på en side, velger du **Handlinger** > **Visning** > **Vis/Skjul Power BI-rapporter** i handlingsfeltet.

### <a name="you-cant-see-the-report-in-the-select-report-pane"></a>Du kan ikke se rapporten i ruten Velg rapport

Navnet på rapporten inneholder ikke navnet på listesiden som vises. Fjern filteret for å få en fullstendig liste over tilgjengelige Power BI-rapporter.  

### <a name="report-is-loaded-but-blank-not-filtered-or-filtered-incorrectly"></a>Rapporten er lastet inn, men tom, ikke filtrert eller filtrert feil

Kontroller at rapportfilteret inneholder riktig primærnøkkel. I de fleste tilfeller er dette **Nr.**-feltet, men i **Finanspost**-tabellen, for eksempel, må du bruke **Løpenr.**-feltet.

### <a name="report-is-loaded-but-it-shows-a-page-you-didnt-expect"></a>Rapporten er lastet inn, men den viser en side du ikke forventet

Kontroller at siden du vil vise, er den første siden i rapporten.  

### <a name="report-appears-with-an-unwanted-gray-boarder-or-its-too-small-or-too-large"></a>Rapporten vises med en uønsket grå kantlinje, eller den er for liten eller for stor

Kontroller at størrelsen på rapporten er satt til 325 x 310 piksler. Lagre rapporten, og deretter oppdater listesiden.  

## <a name="see-also"></a>Se også

[Aktiver forretningsdata for Power BI](admin-powerbi.md)  
[Bruk [!INCLUDE[prod_short](includes/prod_short.md)] som en Power BI-datakilde](across-how-use-financials-data-source-powerbi.md)  
[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
