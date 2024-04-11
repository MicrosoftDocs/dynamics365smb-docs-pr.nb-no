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

Finanskontokategorier forenkler definisjonene i finansrapporter og gjør dem mer robuste mot endringer i kontoplanstrukturen. Finn ut mer under [Bruk finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene](#use-gl-account-categories-to-change-the-layout-of-your-financial-statements).

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

* Navn (kode)
* Description
* Raddefinisjon
* Kolonnedefinisjon

:::image type="content" source="media/financial-reports.png" alt-text="Viser hvordan alle finansrapportene er konstruert ut fra en raddefinisjon og en kolonnedefinisjon." lightbox="media/financial-reports.png":::

> [!NOTE]
> Eksempelfinansrapportene i [!INCLUDE[prod_short](includes/prod_short.md)] er ikke klare til bruk som standard. Avhengig av hvordan du definerer finanskontoer, dimensjoner, finanskontokategorier og budsjetter, må du justere rad- og kolonnedefinisjonene og finansrapportene de brukes i, slik at de samsvarer med oppsettet.

Du kan også bruke formler til å sammenligne to eller flere finansrapporter og kolonnedefinisjoner. Sammenligninger kan gjøre følgende ting:

* Opprette tilpassede finansrapporter.
* Opprette så mange finansrapporter som nødvendig, med unike navn.
* Definere ulike rapportoppsett og skrive ut rapportene med gjeldende tall.

## Læringsbane: Opprett finansrapporter i Microsoft Dynamics 365 Business Central

Vil du lære hvordan du oppretter budsjetter og deretter bruke finansrapporter, dimensjoner og rad- og kolonnedefinisjoner til å generere finansrapportene som vanligvis trengs for de fleste virksomheter?

Begynne å lære på læringsbane: [Opprett finansrapporter i Microsoft Dynamics 365 Business Central](/training/paths/create-financial-reports-dynamics-365-business-central)

## Opprette en ny finansrapport

Du kan bruke finansrapporter til å analysere finanskontoer eller sammenligne finansposter med budsjettposter. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.

Finansrapportene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] passer kanskje ikke til dine forretningsbehov. Hvis du raskt vil opprette dine egne finansrapporter, begynner du med å kopiere en eksisterende, som beskrevet i trinn tre nedenfor.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.  
1. Velg handlingen **Ny** på siden **Finansrapporter** for å opprette et nytt Finansrapportnavn. Hvis du vil bruke innstillinger fra et eksisterende finansrapporter på nytt, velger du handlingen **Kopier finansrapport**.
1. Fyll ut rapportens korte navn (dette kan ikke endres) og beskrivelsen.
1. Velg en raddefinisjon og en kolonnedefinisjon.
1. Du kan eventuelt velge analysevisninger for rad- og kolonnedefinisjonene.
1. Velg **Rediger finansrapport** for å få tilgang til flere egenskaper i finansrapporten.
1. På hurtigfanen **Alternativer** kan du redigere rapportbeskrivelsen, endre rad- og kolonnedefinisjonene og definere hvordan datoer skal vises. Datoer kan være et dag/uke/måned/kvartal/år-hierarki eller bruk regnskapsperioder, Hvis du vil finne ut mer, kan du gå til [Sammenlign regnskapsperioder ved hjelp av periodeformler](#comparing-accounting-periods-using-period-formulas).
1. På hurtigfanen **Dimensjoner** kan du definere dimensjonsfiltre for rapporten.
1. Du kan forhåndsvise rapporten i området under hurtigfanen **Dimensjoner**.

> [!TIP]
> Når du har opprettet en finansrapport, kan du bruke siden **Finansrapport** til å forhåndsvise og validere den. For å åpne siden veger du handlingen **Vis finansrapport**.  

> [!NOTE]
> Når du åpner en finansrapport i visnings- eller redigeringsmodus, er filtreringsruten tilgjengelig. Bruk imidlertid ikke filterruten til å definere filtre for dataene i rapporten. Slike filtre kan føre til feil eller kanskje ikke filtrere dataene. Bruk i stedet feltene på hurtigfanene **Alternativer** og **Dimensjoner** til å definere filtre for rapporten.

### Opprett eller rediger en raddefinisjon

Raddefinisjoner i finansrapporter gir et sted for beregninger som ikke kan utføres direkte i kontoplanen. Du kan for eksempel opprette delsummer for kontogrupper og deretter inkludere denne summen i andre totaler. Du kan også beregne mellomliggende trinn som ikke vises i sluttrapporten.

1. På siden for **Finansrapporter** velger du den relevante finansrapporten, og deretter velger du handlingen **Rediger raddefinisjon**.
1. Velg handlingene **Sett inn finanskontoer**, **Sett inn CF-kontoer** og **Sett inn kostnadstyper** for å opprette en rad for hvert finanselement du vil analysere. Du kan for eksempel ha én rad for aktuelle aktiva og en annen rad for aktiva. For inspirasjon kan du se finansrapporter i demoselskapet CRONUS.

    > [!NOTE]
    > Feltet **Radnr.** viser de 10 første tegnene i en identifikator, for eksempel et kontonummer. Hvis du legger til elementer med identifikatorer som begynner med de samme ti tegnene, vil du ha duplikater fra felte **Radnr.** . Du kan om nødvendig redigere identifikatorer manuelt etter at du har satt inn elementene. De fullstendige identifikatorene vises i feltet **Sammentelling**.

> [!NOTE]
> Kolonnene som du definerer på hver linje i rapportdefinisjonen, representerer kolonner tre og oppover på siden **Finansrapport**. De to første kolonnene, **Radnr.** og **Beskrivelse**, er faste.  

### Opprett eller rediger en kolonnedefinisjon

Bruk kolonnedefinisjoner til å angi kolonnene som skal inkluderes i rapporten. Du kan for eksempel utforme et rapportoppsett for å sammenligne bevegelse og saldo for samme periode i år og i fjor. Du kan ha opptil 15 kolonner i en kolonnedefinisjon. Flere kolonner er for eksempel nyttig for visning av budsjetter for tolv måneder, med en kolonne som viser totalen.

> [!NOTE]
> En utskrifts-/forhåndsvisnings-/lagret versjon av en finansrapport viser maksimalt fem kolonner. Hvis en finansrapporten derimot bare er beregnet for analyse på siden **Finansrapport**, kan du opprette så mange kolonner du vil.

1. På siden for **Finansrapporter** velger du den relevante finansrapprten, og deretter velger du handlingen **Rediger kolonnedefinisjon**.
1. På siden **Kolonnedefinisjon** oppretter du en rad for hver kolonne med finansdata vises etter finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. Velg **OK**.
1. Åpne siden **Finansrapport** med jevne mellomrom for å kontrollere at den nye kolonnedefinisjonen fungerer som forventet.

### Opprett en kolonnedefinisjon for å beregne prosentdeler

Du vil da kanskje ta med en kolonne i en finansrapport for å beregne prosentdeler av en sum. Hvis du for eksempel har rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg i hver rad.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. På siden for **Finansrapporter** velger du en finansrapport.  
1. Velg handlingen **Rediger finansrapport** for å definere en finansrapportrad som skal brukes til å beregne summen prosentene skal baseres på.  
1. legg til en linje like over den første raden som du vil vise en prosentdel for.  
1. Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**. Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet. Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.  
1. Velg handlingen **Rediger kolonnedefinisjon** for å definere en kolonne.  
1. Fyll ut feltene på linjen slik. I **Kolonnetype**-feltet velger du **Formel**. Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av prosenttegnet (%), i **Formel**-feltet. Så hvis kolonnenummeret N inneholder bevegelsen, angir du **N %**.  
1. Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.

## Bruk finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene

Du kan bruke finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene. Etter at du har definert kontokategoriene på siden **Finanskontokategorier** og du velger handlingen Generer kontoskjemaer, kan du for eksempel velge handlingen **Finansrapporter** og oppdatere de underliggende finansrapportene for kjernefinansrapporter. Neste gang du kjører en av disse rapportene, for eksempel **saldoutdrag**, legges nye totaler og underoppføringer til.

En annen fordel med å bruke finanskontokategorier fremfor de rå finanskontoene i raddefinisjonene, er at en endring i kontoplanstrukturen ikke påvirker finansrapportene.

> [!NOTE]
> Kontokategoriene på øverste nivå, for eksempel **Gjeld**-noden, er faste, og du kan ikke legge til dine egne. Du kan imidlertid slette og legge til kontokategorier på lavere nivåer og definere hvordan den tilhørende finansrapporten vises i rapporter.
>
> Du bør opprette og strukturere dine egne finanskontokategorier på lavere nivå fra bunnen av, om nødvendig i et hierarki, i stedet for å prøve å omorganisere de eksisterende. Du kan for eksempel omstrukturere **Gjeld**-noden slik at den inneholder en ny **Egenkapital**-node etterfulgt av nodene **Kortsiktig gjeld** og **Langsiktig gjeld**. Finn ut mer på [Tildel finanskontoer til kontokategorier](finance-general-ledger.md#account-categories).

## Bruk dimensjoner i finansrapporter

I finansanalyse er en dimensjon data du kan legge til i en post som et slags merke. Disse dataene brukes til å gruppere poster med de samme egenskapene, for eksempel kunder, regioner, produkter og selgere, og på en enkel måte få tak i disse gruppene i analyser. Du kan bruke dimensjoner på poster i kladder, dokumenter og budsjetter.

Hver dimensjon beskriver fokuset for analyse. Så en todimensjonal analyse er for eksempel salg per område. Hvis du bruker mer enn to dimensjoner når du oppretter en post, kan du utføre en mer omfattende analyse. Et eksempel på en kompleks analyse er å utforske salg per salgskampanje per kundegruppe per område. Det gir deg større innsikt i forretningsdriften, for eksempel hvordan bra forretningen fungerer, hva som er bra og hva som er dårlig, og hvor du bør tildele flere ressurser. Denne innsikten hjelper deg med å ta mer informerte forretningsbeslutninger. Finn ut mer under [Arbeid med dimensjoner](finance-dimensions.md).

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

## Sammenligne regnskapsperioder ved hjelp av periodeformler

Finansrapporten kan sammenligne resultatene av ulike regnskapsperioder, for eksempel inneværende måned og samme måned i fjor. Dette gjør du ved å åpne **Kolonnedefinisjon**-siden og tilpasse den ved å legge til feltet **Formel - periodesammenligning** som en kolonne. Finn ut mer under [Tilpass arbeidsområdet](ui-personalization-user.md). Deretter kan du sette dette feltet til en periodeformel.  

En regnskapsperiode trenger ikke å samsvare med kalenderen. Regnskapsåret må imidlertid ha samme antall regnskapsperioder, selv om hver periode kan variere i lengde.  

[!INCLUDE[prod_short](includes/prod_short.md)] bruker periodeformelen til å beregne varigheten til sammenligningsperioden, i forhold til perioden som er angitt i datofilteret i rapporten. Sammenligningsperioden er basert på perioden for startdatoen i datofilteret. Periodene forkortes slik:

| Forkortelse | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Periode.                                                                                |
| SP           | Siste periode av et regnskapsår, et halvår eller kvartal.                                   |
| HP           | Inneværende periode av et regnskapsår, et halvår eller kvartal. Bruk IP i formlar for å oppgi perioden som skal starte eller avslutte formelen. For eksempel angir RÅ\[1.. IP\] tiden fra begynnelsen av gjeldende regnskapsår til gjeldende periode.|
| RÅ           | Regnskapsår. Eksempelvis viser RÅ\[1..3\] det første kvartal av inneværende regnskapsår. |

Eksempler på formler:

| Formel         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Inneværende periode.                                                                                  |
| \-1P            | Forrige periode.                                                                                 |
| \-1RÅ\[1..SP\]  | Hele forrige regnskapsår.                                                                     |
| \-1RÅ           | Inneværende periode i forrige regnskapsår.                                                          |
| \-1RÅ\[1..3\]   | Første kvartal av forrige regnskapsår.                                                           |
| \-1RÅ\[1..IP\]  | Fra begynnelsen av forrige regnskapsår til og med inneværende periode i forrige regnskapsår, inkludert begge perioder. |
| \-1RÅ\[IP..SP\] | Fra inneværende periode i forrige regnskapsår til siste periode i forrige regnskapsår, inkludert begge perioder.   |

Hvis du vil beregne etter regelmessige perioder, må du angi en formel i feltet **Datoformel - sammenligning** i stedet. Hvis feltet eksempelvis er satt til -1Å, foretar [!INCLUDE [prod_short](includes/prod_short.md)] en sammenligning med samme periode ett år tidligere.

> [!NOTE]
> Det er ikke alltid gjennomsiktig hvilke perioder du sammenligner, siden du kan angi et datofilter i en rapport som inneholder forskjellige datoer enn regnskapsperiodene som gjenspeiles i kontoplanen. Så hvis du oppretter en finansrapport der du vil sammenligne denne perioden med samme periode i fjor, setter du **Datoformel - sammenligning**-feltet til *-1RÅ*. Deretter kjører du rapporten 28. februar og setter datofilteret til januar og februar. Dermed sammenligner finansrapport januar og februar i år med januar i fjor, som er den eneste fullførte regnskapsperioden av de to for forrige år.  

Lær mer på [Arbeid med kalenderdatoer og klokkeslett](ui-enter-date-ranges.md).

## Skrive ut og lagre finansrapporter

Du kan skrive ut finansrapporter ved hjelp av enhetens utskriftstjenester. [!INCLUDE[prod_short](includes/prod_short.md)] gir også mulighet til å lagre rapporter som Excel-arbeidsbøker, Word-dokumenter, PDF- og XML-filer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. På siden for **Finansrapporter** velger du rapporten som skal skrives ut, og deretter velger du **Skriv ut**-handlingen.
1. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
1. I **Skriver**-feltet velger du enheten som rapporten skal sendes til.
    1. Alternativet **(Håndteres av nettleseren)** angir at det ikke finnes noen tilordnet skriver for rapporten. I dette tilfellet vil nettleseren behandle utskriften og vise standard utskriftstrinn, der du kan velge en lokal skriver som er koblet til enheten. **(Håndteres av nettleseren)** er ikke tilgjengelig i [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen eller appen for Teams.
1. Velg **Skriv ut**-handlingen.

### Planlegge en finansrapport eller lagre som PDF-, Word- eller Excel-dokument

En finansrapport kan lagres som en fil i forskjellige formater, for eksempel PDF, XML, Word eller Excel. [!INCLUDE[prod_short](includes/prod_short.md)] kan eventuelt generere gjentakende finansrapporter:

1. Velg ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. ÅPå siden **Finansrapporter** velger du **Skriv ut**-handlingen.
1. Angi rapporten i henhold til dette, og velg deretter handlingen **Send til**.
1. Velg filformatet eller **Planlegg**-handling, og velg **OK**.
1. Hvis du vil generere en planlagt eller gjentakende finansrapport, fyller du ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].<br><br>For regelmessige finansrapporter angir du feltene **Tidligste startdato/-klokkeslett** og **Utløpsdato/-klokkeslett** med første og siste dato for å generere finansrapporten. Du kan også velge hvilke dager rapporten skal genereres, ved å sette feltet **Datoformel for neste kjøring** etter formatet forklart i delen [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).

## Importer eller eksporter av finansrapportdefinisjoner

Du kan importere og eksportere finansrapporter/raddefinisjoner som RapidStart-konfigurasjonspakker, som er nyttige for å dele informasjon med andre selskaper, for eksempel. Pakken opprettes i en .rapidstart-fil, som komprimerer innholdet.

> [!NOTE]
> Når du importerer finansrapporter/raddefinisjoner, blir eksisterende poster med samme navn som de du importerer, erstattet med de nye definisjonene. Vær oppmerksom på at konfigurasjonspakken for en rapportdefinisjon ikke overskriver eksisterende rad- eller kolonnedefinisjoner som brukes i rapportdefinisjonen.

Hvis du vil importere eller eksportere finansrapportdefinisjoner, gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
1. Velg regnskapsrapporten, og velg deretter **Importer finansrapport** eller **Eksporter finansrapport**, avhengig av hva du vil gjøre.

Hvis du vil importere eller eksportere finansrapportraddefinisjoner, gjør du følgende:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Raddefinisjoner**, og velg deretter den tilknyttede koblingen.
1. Velg raddefinisjonen, og velg deretter **Importer raddefinisjon** eller **Eksporter raddefinisjon**, avhengig av hva du vil gjøre.

## Se også

[Kjør og skriv ut rapporter](ui-work-report.md)  
[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
