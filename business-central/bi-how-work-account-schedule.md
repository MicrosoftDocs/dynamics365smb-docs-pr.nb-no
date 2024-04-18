---
title: Bygge finansrapporter ved hjelp av finansdata og kontokategorier
description: Beskriver hvordan du bruker finansrapporter til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 03/27/2024
ms.custom: bap-template
ms.search.keywords: 'bi, power BI, analysis, KPI, account schedule, financial report'
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
ms.service: dynamics-365-business-central
---
# Klargjør finansrapportering med finansdata og kontokategorier

Funksjonen **Finansrapporter** gir deg innsikt i finansdataene som vises i kontoplanen. Du kan konfigurere finansrapporter til å analysere tall på finanskontoer og sammenligner finansposter med budsjettposter. Resultatet vises i diagrammer og rapporter i rollesenteret, for eksempel ut Kontantstrøm-diagrammet og rapportene Resultatregnskap og Balanse. Du får tilgang til disse to rapportene for eksempel med handlingen **Årsregnskap** på startsidene for forretningsleder og regnskapsfører.  

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder eksempelfinansrapporter som du kan bruke umiddelbart som maler. Du kan også opprette dine egne rapporter for å angi tallene som skal sammenlignes. Du kan for eksempel opprette finansrapporter for å beregne fortjenestemarginer ved hjelp av dimensjoner som avdelinger eller kundegrupper. Antall finansrapporter du kan opprette, er ubegrenset og krever ingen involvering av en utvikler.  

## Forutsetninger for finansrapportering

Oppretting av finansrapporter krever en forståelse av strukturen til kontoplanen. Det er tre nøkkelbegreper du sannsynligvis må være oppmerksom på før du utformer finansrapportene:

- Tildel finansbokføringskontoer til finanskontokategorier.
- Utform hvordan du bruker dimensjoner.
- Konfigurer finansbudsjetter.

Finanskontokategorier forenkler definisjonene i finansrapporter og gjør dem mer robuste mot endringer i kontoplanstrukturen. Finn ut mer under [Bruk finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene](bi-row-definitions.md#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

Ved å definere dimensjoner kan du dele opp finansdataene på måter som gir mening for organisasjonen. Finn ut mer under [Arbeide med dimensjoner](finance-dimensions.md). 

Hvis du vil vise finansposter som prosentandeler av budsjettpostene, må du opprette finansbudsjetter. Lære mer om [Opprette finansbudsjetter](finance-how-create-budgets.md).

## Finansrapporter

Finansrapporter ordner kontoer fra kontoplanen din på måter som gjør det enkelt å presentere data. Du kan definere ulike oppsett for å velge hvilken informasjon du vil trekke ut fra kontoplanen. Finansrapporter gir også et sted for beregninger som ikke kan utføres direkte i kontoplanen. Du kan for eksempel opprette delsummer for kontogrupper og deretter inkludere denne summen i andre totaler. Et annet eksempel er å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper. I tillegg kan du filtrere finansposter og budsjettposter, for eksempel etter bevegelse eller debetbeløp.

> [!NOTE] 
> Tenk matematisk på en finansrapport som definert av to ting:
>
> - en vektor av raddefinisjoner som definerer hva som må beregnes
> - en vektor av kolonnedefinisjoner som definerer dataene for beregningen
>
> Finansrapporten er da det ytre produktet av disse to vektorene, der hver celleverdi beregnes i henhold til formelen i raden som brukes på datadefinisjonen fra kolonnen.

:::image type="content" source="media/financial-report-definition.svg" alt-text="Viser hvordan en finansrapport er konstruert ut fra en raddefinisjon og en kolonnedefinisjon." lightbox="media/financial-report-definition.svg":::

Siden **Finansrapporter** viser hvordan alle finansrapporter følger et mønster som består av følgende attributter:

- Navn (kode)
- Description
- Raddefinisjon
- Kolonnedefinisjon

:::image type="content" source="media/financial-reports.png" alt-text="Viser hvordan alle finansrapportene er konstruert ut fra en raddefinisjon og en kolonnedefinisjon." lightbox="media/financial-reports.png":::

> [!NOTE]
> Eksempelfinansrapportene i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke klare til bruk som standard. Avhengig av hvordan du definerer finanskontoer, dimensjoner, finanskontokategorier og budsjetter, må du justere rad- og kolonnedefinisjonene og finansrapportene de brukes i, slik at de samsvarer med oppsettet.

Du kan også bruke formler til å sammenligne to eller flere finansrapporter og kolonnedefinisjoner. Sammenligninger kan gjøre følgende ting:

- Opprette tilpassede finansrapporter.
- Opprette så mange finansrapporter som nødvendig, med unike navn.
- Definere ulike rapportoppsett og skrive ut rapportene med gjeldende tall.

## Læringsbane: Opprett finansrapporter i Microsoft Dynamics 365 Business Central

Vil du lære hvordan du oppretter budsjetter og deretter bruke finansrapporter, dimensjoner og rad- og kolonnedefinisjoner til å generere finansrapportene som virksomheter vanligvis trenger?

Begynn på følgende læringsbane: [Opprett finansrapporter i Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central).

## Opprette en ny finansrapport

Du kan bruke finansrapporter til å analysere finanskontoer eller sammenligne finansposter med budsjettposter. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.

Finansrapportene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] passer kanskje ikke til dine forretningsbehov. Hvis du raskt vil opprette dine egne finansrapporter, begynner du med å kopiere en eksisterende, som beskrevet i trinn tre nedenfor.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.  
1. Velg handlingen **Ny** på siden **Finansrapporter** for å opprette et nytt Finansrapportnavn. Hvis du vil bruke innstillinger fra et eksisterende finansrapporter på nytt, velger du handlingen **Kopier finansrapport**.
1. Fyll ut rapportens korte navn (du kan ikke endre navnet senere) og beskrivelsen.
1. Velg en raddefinisjon og en kolonnedefinisjon.
1. Du kan eventuelt velge analysevisninger for rad- og kolonnedefinisjonene.
1. Velg **Rediger finansrapport** for å få tilgang til flere egenskaper i finansrapporten.
1. På hurtigfanen **Alternativer** kan du redigere rapportbeskrivelsen, endre rad- og kolonnedefinisjonene og definere hvordan datoer skal vises. Datoer kan være et dag/uke/måned/kvartal/år-hierarki eller bruk regnskapsperioder. Hvis du vil finne ut mer, kan du gå til [Sammenlign regnskapsperioder ved hjelp av periodeformler](bi-column-definitions.md#comparing-accounting-periods-using-period-formulas).
1. På hurtigfanen **Dimensjoner** kan du definere dimensjonsfiltre for rapporten.
1. Du kan forhåndsvise rapporten i området under hurtigfanen **Dimensjoner**.

> [!TIP]
> Når du har opprettet en finansrapport, kan du bruke siden **Finansrapport** til å forhåndsvise og validere den. For å åpne siden veger du handlingen **Vis finansrapport**.  

> [!NOTE]
> Når du åpner en finansrapport i visnings- eller redigeringsmodus, er filtreringsruten tilgjengelig. Bruk imidlertid ikke filterruten til å definere filtre for dataene i rapporten. Slike filtre kan føre til feil eller kanskje ikke filtrere dataene. Bruk i stedet feltene på hurtigfanene **Alternativer** og **Dimensjoner** til å definere filtre for rapporten.

### Opprett eller rediger en raddefinisjon

Raddefinisjoner i finansrapporter gir et sted for beregninger som ikke kan utføres direkte i kontoplanen. Du kan for eksempel opprette delsummer for kontogrupper og deretter inkludere denne summen i andre totaler. Du kan også beregne mellomliggende trinn som ikke vises i sluttrapporten.

Hvis du vil ha mer informasjon, kan du gå til [Raddefinisjoner i finansrapportering](bi-row-definitions.md).

### Opprett eller rediger en kolonnedefinisjon

Bruk kolonnedefinisjoner til å angi kolonnene som skal inkluderes i rapporten. Du kan for eksempel utforme et rapportoppsett for å sammenligne bevegelse og saldo for samme periode i år og i fjor. Du kan ha opptil 15 kolonner i en kolonnedefinisjon. Flere kolonner er for eksempel nyttig for visning av budsjetter for tolv måneder, med en kolonne som viser totalen.

Hvis du vil ha mer informasjon, kan du gå til [Kolonnedefinisjoner i finansrapportering](bi-column-definitions.md).

## Bruk dimensjoner i finansrapporter

I finansanalyse er en dimensjon data du kan legge til i en post som et slags merke. Disse dataene brukes til å gruppere poster med de samme egenskapene, for eksempel kunder, regioner, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Du kan bruke dimensjoner på poster i kladder, dokumenter og budsjetter.

Hver dimensjon beskriver fokuset for analyse. Så en todimensjonal analyse er for eksempel salg per område. Hvis du bruker mer enn to dimensjoner når du oppretter en post, kan du utføre en mer omfattende analyse. Et eksempel på en kompleks analyse er å utforske salg per salgskampanje per kundegruppe per område. Det gir deg større innsikt i forretningsdriften, for eksempel hvordan bra forretningen fungerer, hva som er bra og hva som er dårlig, og hvor du bør tildele flere ressurser. Denne innsikten hjelper deg med å ta mer informerte forretningsbeslutninger. Hvis du vil ha mer informasjon, kan du gå til [Arbeide med dimensjoner](finance-dimensions.md).

## Definere finansrapporter med oversikter

Du kan bruke en finansrapport til å opprette en oppgave som sammenligner finanstall med budsjettall.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. På siden for **Finansrapporter** velger du en finansrapport.  
1. Velg handlingen **Rediger raddefinisjon**  
1. Velg standard finansrapportnavn i **Navn**-feltet på **Raddefinisjon**-siden.
1. Velg handlingen **Sett inn finanskontoer**.  
1. Velg kontiene du vil ta med i oppgaven og velg deretter **OK**.

    Kontoene settes nå inn i finansrapporten. Hvis du vil, kan du også endre kolonnedefinisjon  
1. Velg handlingen **Rediger finansrapport**.  
1. På hurtigfanen **Dimensjoner** på **Finansrapport**-siden setter du budsjettfilteret til filternavnet du vil bruke.  
1. Velg **OK**.  

Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.  

## Skrive ut og lagre finansrapporter

Du kan skrive ut finansrapporter ved hjelp av enhetens utskriftstjenester. [!INCLUDE[prod_short](includes/prod_short.md)] gir også mulighetene til å lagre rapporter som Excel-arbeidsbøker, Word-dokumenter, PDF- og XML-filer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. På siden for **Finansrapporter** velger du rapporten som skal skrives ut, og deretter velger du **Skriv ut**-handlingen.
1. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. I **Skriver**-feltet velger du enheten som rapporten sendes til.
    1. Alternativet **(Håndteres av nettleseren)** angir at det ikke finnes noen tilordnet skriver for rapporten. I dette tilfellet vil nettleseren behandle utskriften og vise standard utskriftstrinn, der du kan velge en lokal skriver som er koblet til enheten. **(Håndteres av nettleseren)** er ikke tilgjengelig i [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen eller appen for Teams.
1. Velg **Skriv ut**-handlingen.

### Planlegge en finansrapport eller lagre som PDF-, Word- eller Excel-dokument

Du kan lagre en finansrapport i filformater som PDF, XML, Word eller Excel. [!INCLUDE[prod_short](includes/prod_short.md)] kan også generere gjentakende finansrapporter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. ÅPå siden **Finansrapporter** velger du **Skriv ut**-handlingen.
1. Angi rapporten i henhold til dette, og velg deretter handlingen **Send til**.
1. Velg filformatet eller **Planlegg**-handling, og velg **OK**.
1. Hvis du vil generere en planlagt eller gjentakende finansrapport, fyller du ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>For regelmessige finansrapporter angir du feltene **Tidligste startdato/-klokkeslett** og **Utløpsdato/-klokkeslett** med første og siste dato for å generere finansrapporten. Du kan også velge hvilke dager rapporten skal genereres, ved å sette feltet **Datoformel for neste kjøring** etter formatet forklart i delen [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).

## Anbefalte fremgangsmåter for arbeid med finansrapportdefinisjoner

Finansrapportdefinisjoner versjonskontrolleres ikke. Når du endrer en rapportdefinisjon, erstattes den gamle versjonen når endringen lagres i databasen. Listen nedenfor inneholder noen anbefalte fremgangsmåter for å arbeide med finansrapportdefinisjoner:

- Hvis du legger til rapportdefinisjoner, velger du en god kode og fyller ut beskrivelsesfeltet med en meningsfull tekst mens du fortsatt vet hva du bruker rapporten til. Denne informasjonen hjelper kollegene dine (og ditt fremtidige jeg) med å arbeide med rapporten og kanskje endre rapportdefinisjonen.
- Før du endrer en rapportdefinisjon, bør du vurdere å ta en kopi av den som en sikkerhetskopi, i tilfelle endringen ikke fungerer som forventet. Du kan enten bare kopiere definisjonen (gi den et bra navn), eller eksportere den. Hvis du vil finne ut mer, kan du gå til [Importer eller eksporter finansrapportdefinisjoner](#import-or-export-financial-report-definitions).
- Hvis du trenger en ny kopi av en definisjon som [!INCLUDE[prod_short](includes/prod_short.md)] gir, er det enkelt å opprette et nytt selskap som bare inneholder oppsettsdata. Deretter eksporterer du definisjonen og importerer den til selskapet der definisjonen trenger en oppdatering.

## Importer eller eksporter finansrapportdefinisjoner

Du kan importere og eksportere finansrapportdefinisjoner som RapidStart-konfigurasjonspakker. Konfigurasjonspakker er for eksempel nyttig for deling av informasjon med andre selskaper. Pakken opprettes i en .rapidstart-fil, som komprimerer innholdet.

> [!NOTE]
> Når du importerer finansrapportdefinisjoner, blir eksisterende poster med samme navn som de du importerer, erstattet med de nye definisjonene. Konfigurasjonspakken for en rapportdefinisjon overskriver ikke eksisterende rad- eller kolonnedefinisjoner som brukes i rapportdefinisjonen.

Hvis du vil importere eller eksportere finansrapportdefinisjoner, gjør du følgende:

1. Velg ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. Velg regnskapsrapporten, og velg deretter **Importer finansrapport** eller **Eksporter finansrapport**, avhengig av hva du vil gjøre.

Hvis du vil lære mer om hvordan du importerer eller eksporterer rad- eller kolonnedefinisjoner for finansrapporter, kan du gå til følgende artikler: 

- [Importer eller eksporter av raddefinisjoner for finansrapport](bi-row-definitions.md#import-or-export-financial-reporting-row-definitions) eller
- [Importer eller eksporter av kolonnedefinisjoner for finansrapport](bi-column-definitions.md#import-or-export-financial-report-column-definitions)

## Se også

[Raddefinisjoner i finansrapportering](bi-row-definitions.md)  
[Kolonnedefinisjoner i finansrapportering](bi-column-definitions.md)  
[Kjør og skriv ut rapporter](ui-work-report.md)  
[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
