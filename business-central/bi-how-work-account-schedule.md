---
title: Bygge finansrapporter ved hjelp av finansdata og kontokategorier
description: Beskriver hvordan du bruker finansrapporter til å opprette ulike visninger og rapporter for å analysere økonomiske resultatdata.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI, account schedule, financial report
ms.search.form: 103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766
ms.date: 08/12/2022
ms.author: edupont
ms.openlocfilehash: 3b71bec5ca7f1c903913b4244eb176dbf1c53c86
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2022
ms.locfileid: "9605249"
---
# <a name="prepare-financial-reporting-with-financial-data-and-account-categories"></a>Klargjøre Financial Reporting med finansdata og kontokategorier

Finansrapporter gir deg innsikt i finansdataene som er lagret i kontoplanen. Finansrapporter analyserer tall på finanskonti og sammenligner finansposter med budsjettposter. Resultatet vises i diagrammer og rapporter i rollesenteret, for eksempel ut kontantstrømdiagrammet og rapportene resultatregnskap og balanse.

Du får tilgang til disse to rapportene for eksempel med handlingen **Årsregnskap** i rollesentrene for forretningsleder og regnskapsfører.  

[!INCLUDE[prod_short](includes/prod_short.md)] inneholder eksempelfinansrapporter som du kan bruke umiddelbart. Du kan også opprette dine egne rader og kolonner for å angi tallene som skal sammenlignes. Du kan for eksempel opprette finansrapporter for å beregne fortjenestemarginer ved hjelp av dimensjoner som avdelinger eller kundegrupper. Antall egendefinerte regnskapsrapporter du kan opprette, er ubegrenset.  

Oppretting av finansrapporter krever en forståelse av de økonomiske dataene i kontoplanen. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene, men det krever at du har opprettet budsjetter. Lære mer om [Opprette finansbudsjetter](finance-how-create-budgets.md).

## <a name="financial-reports"></a>Finansrapporter

Finansrapporter ordner kontoer fra kontoplanen din på måter som gjør det enkelt å presentere data. Du kan definere ulike oppsett for å velge hvilken informasjon du vil trekke ut fra kontoplanen. Finansrapporter gir et sted for beregninger som ikke kan utføres direkte i kontoplanen. Du kan for eksempel opprette delsummer for kontogrupper og deretter inkludere denne summen i andre totaler. Et annet eksempel er å beregne fortjenestemarginer for dimensjoner som avdelinger eller kundegrupper. I tillegg kan du filtrere finansposter og budsjettposter, for eksempel etter bevegelse eller debetbeløp.

Du kan også sammenligne to eller flere finansrapporter og kolonnedefinisjoner ved hjelp av formler, slik at du kan gjøre følgende:

* Opprette tilpassede finansrapporter.
* Opprette så mange finansrapporter som nødvendig, med unike navn.
* Definere ulike rapportoppsett og skrive ut rapportene med gjeldende tall.

## <a name="gl-account-categories"></a>Finanskontokategorier

Du kan bruke finanskontokategoriene til å endre oppsettet for regnskapsoppgjørene. Når du har definert kontokategoriene på siden **Finanskontokategorier** og du velger handlingen Generer kontoskjemaer, kan du for eksempel velge handlingen **Finansrapporter** og oppdatere de underliggende finansrapportene for kjernefinansrapporter. Neste gang du kjører en av disse rapportene, for eksempel **saldoutdrag**, legges nye totaler og underoppføringer til.

> [!NOTE]
> Kontokategoriene på øverste nivå, for eksempel **Gjeld**-noden, er faste, og du kan ikke legge til dine egne. Du kan imidlertid slette og legge til kontokategorier på lavere nivåer og definere hvordan den tilhørende finansrapporten vises i rapporter.
>
> Du bør opprette og strukturere dine egne finanskontokategorier på lavere nivå fra bunnen av, om nødvendig i et hierarki, i stedet for å prøve å omorganisere de eksisterende. Du kan for eksempel omstrukturere **Gjeld**-noden slik at den inneholder en ny **Egenkapital**-node etterfulgt av nodene **Kortsiktig gjeld** og **Langsiktig gjeld**.

## <a name="create-a-new-financial-report"></a>Opprette en ny finansrapport

Du kan bruke finansrapporter til å analysere finanskontoer eller sammenligne finansposter med budsjettposter. Du kan for eksempel vise finansposter som en prosentandel av budsjettpostene.

Finansrapportene i standardversjonen av [!INCLUDE[prod_short](includes/prod_short.md)] passer kanskje ikke til dine forretningsbehov. Hvis du raskt vil opprette dine egne finansrapporter, begynner du med å kopiere en eksisterende, som beskrevet i trinn tre nedenfor.

> [!TIP]
> Når du har opprettet en finansrapport, kan du bruke siden **Finansrapport** til å forhåndsvise og validere den nylig definerte finansrapporten. For å åpne siden veger du handlingen **Rediger finansrapport**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny** på siden **Finansrapporter** for å opprette et nytt Finansrapportnavn.
3. Hvis du vil bruke innstillinger fra et eksisterende finansrapporter på nytt, velger du handlingen **Kopier finansrapport**.
4. Fyll ut feltene etter behov. Velg en eksisterende definisjon i **Kolonnedefinisjon**-feltet, som du senere kan redigere hvis du vil.

    Kolonnedefinisjoner angir parameterne som finansielle data i radene vises etter. Et kolonnedefinisjon kan for eksempel inneholde fire kolonner du kan bruke til å sammenligne bevegelse og saldo for samme periode i år og i fjor. Lær mer i delen [Redigere en kolonnedefinisjon](bi-how-work-account-schedule.md#edit-a-column-definition).

5. Velg handlingen **Rediger raddefinisjon**.
6. Velg handlingene **Sett inn finanskontoer**, **Sett inn CF-kontoer** og **Sett inn kostnadstyper** for å opprette en rad for hvert finanselement du vil analysere. Du kan for eksempel ha én rad for aktuelle aktiva og en annen rad for aktiva. For inspirasjon kan du se finansrapporter i demoselskapet CRONUS.

    > [!NOTE]
    > Feltet **Radnr.** viser de 10 første tegnene i en identifikator, for eksempel et kontonummer. Hvis du legger til elementer med identifikatorer som begynner med de samme ti tegnene, vil du ha duplikater fra felte **Radnr.** . Du kan om nødvendig redigere identifikatorer manuelt etter at du har satt inn elementene. De fullstendige identifikatorene vises i feltet **Sammentelling**.

7. På siden for **Finansrapporter** velger du **Rediger økonomisk rapport** for å vise den resulterende finansrapporten.
8. På siden **Finansrapport** i feltet **Kolonnedefinisjon** velger du en annen kolonnedefinisjon for å utforske finansdataene etter andre parametere.
9. Velg **OK**.

Du har nå definert grunnlaget for finansrapporten, radene med økonomiske data som skal vises, og et eksisterende kolonneoppsett for å vise dataene i radene ved hjelp av egendefinerte parametere. Hvis standardkolonnedefinisjonen du valgte i trinn 4, ikke dekker behovet ditt, følger du fremgangsmåten nedenfor.

### <a name="edit-a-column-definition"></a>Redigere en kolonnedefinisjon

Du bruker kolonnedefinisjoner til å angi kolonnene som var inkludert i den resulterende rapporten. Du kan for eksempel sammenligne bevegelse og saldo for samme periode i år og i fjor. Du kan ha opptil 15 kolonner, som være nyttig for eksempelvis visning av budsjetter for tolv måneder, med en kolonne som viser totalen.

> [!NOTE]
> En utskrifts-/forhåndsvisnings-/lagret versjon av en finansrapport viser maksimalt fem kolonner. Hvis en finansrapporten derimot bare er beregnet for analyse på siden **Finansrapport**, kan du opprette så mange kolonner du vil.

1. På siden for **Finansrapporter** velger du den relevante finansrapprten, og deretter velger du handlingen **Rediger kolonnedefinisjon**.
2. På siden **Kolonnedefinisjon** oppretter du en rad for hver kolonne med finansdata vises etter finansrapporten. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Velg **OK**.
4. Åpne siden **Finansrapport** med jevne mellomrom for å kontrollere at den nye kolonnedefinisjonen fungerer som forventet.

> [!NOTE]
> Kolonnene som du definerer på hver rad, representerer kolonner tre og oppover på **Finansrapport**-siden. De to første kolonnene, **Radnr.** og **Beskrivelse**, er faste.  

### <a name="create-a-column-that-calculates-percentages"></a>Opprette en kolonne som beregner prosentdeler

Noen ganger vil du kanskje ta med en kolonne i en finansrapport for å beregne prosentdeler av en sum. Hvis du for eksempel har rader som bryter ned salg etter dimensjon, vil du kanskje ta med en kolonne som angir hvor stor prosentdel av totalt salg i hver rad.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 2.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
2. På siden for **Finansrapporter** velger du en finansrapport.  
3. Velg handlingen **Rediger finansrapport** for å definere en finansrapportrad som skal brukes til å beregne summen prosentene skal baseres på.  
4. Sett inn en linje like over den første raden som du vil vise en prosentdel for.  
5. Fyll ut feltene på linjen som følger: I feltet **Sammentellingstype** angir du **Angi grunnlag for prosent**. Skriv inn en formel for summen som prosentdelen skal være basert på, i **Sammentelling**-feltet. Hvis rad 11 for eksempel inneholder totalt salg, angir du **11**.  
6. Velg handlingen **Rediger kolonnedefinisjon** for å definere en kolonne.  
7. Fyll ut feltene på linjen som følger: I feltet **Kolonnetype** velger du **Formel**. Skriv inn en formel for beløpet du vil beregne en prosent for, fulgt av prosenttegnet (%), i **Formel**-feltet. Så hvis kolonnenummeret N inneholder bevegelsen, angir du **N %**.  
8. Gjenta trinn 4 til og med 7 for hver gruppe med rader du vil bryte ned i prosentdeler.

## <a name="set-up-financial-reports-with-overviews"></a>Definere finansrapporter med oversikter

Du kan bruke en finansrapport til å opprette en oppgave som sammenligner finanstall og budsjettall.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
2. På siden for **Finansrapporter** velger du en finansrapport.  
3. Velg handlingen **Rediger raddefinisjon**  
4. Velg standard finansrapportnavn i **Navn**-feltet på **Raddefinisjon**-siden.
5. Velg handlingen **Sett inn finanskontoer**.  
6. Velg kontiene du vil ta med i oppgaven og velg deretter **OK**.

    Kontiene settes nå inn i finansrapport. Hvis du vil, kan du også endre kolonnedefinisjon  
7. Velg handlingen **Rediger finansrapport**.  
8. På hurtigfanen **Dimensjoner** på **Finansrapport**-siden setter du budsjettfilteret til filternavnet du vil bruke.  
9. Velg **OK**.  

Du kan nå kopiere og lime inn budsjettoppgaven i et regneark.  

## <a name="comparing-accounting-periods-using-period-formulas"></a>Sammenligne regnskapsperioder ved hjelp av periodeformler

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

## <a name="print-and-save-financial-reports"></a>Skrive ut og lagre finansrapporter

Du kan skrive ut finansrapporter ved hjelp av enhetens utskriftstjenester. [!INCLUDE[prod_short](includes/prod_short.md)]gir også mulighet til å lagre rapporter som Microsoft Excel-arbeidsbøker, Microsoft Word-dokumenter, PDF- og XML-filer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
2. På siden for **Finansrapporter** velger du rapporten som skal skrives ut, og deretter velger du **Skriv ut**-handlingen.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. I **Skriver**-feltet velger du enheten som rapporten skal sendes til.
    1. Alternativet **(Håndteres av nettleseren)** angir at det ikke finnes noen tilordnet skriver for rapporten. I dette tilfellet vil nettleseren behandle utskriften og vise standard utskriftstrinn, der du kan velge en lokal skriver som er koblet til enheten. **(Håndteres av nettleseren)** er ikke tilgjengelig i [!INCLUDE[prod_short](includes/prod_short.md)]-mobilappen eller appen for Microsoft Teams.
5. Velg **Skriv ut**-handlingen.

### <a name="schedule-a-financial-report-or-save-as-a-pdf-word-or-excel-document"></a>Planlegge en finansrapport eller lagre som PDF-, Word- eller Excel-dokument

En finansrapport kan lagres som en fil i forskjellige formater, for eksempel PDF, XML, Word eller Excel. Du kan eventuelt angi at [!INCLUDE[prod_short](includes/prod_short.md)] skal generere gjentakende finansrapporter:

1. Velg ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
2. ÅPå siden **Finansrapporter** velger du **Skriv ut**-handlingen.
3. Angi rapporten i henhold til dette, og velg deretter handlingen **Send til**.
4. Velg filformatet eller **Planlegg**-handling, og velg **OK**.
5. Hvis du vil generere en planlagt eller gjentakende finansrapport, fyller du ut feltene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
   * For regelmessige finansrapporter angir du feltene **Tidligste startdato/-klokkeslett** og **Utløpsdato/-klokkeslett** med første og siste dato for å generere finansrapporten. Du kan også velge hvilke dager rapporten skal genereres, ved å sette feltet **Datoformel for neste kjøring** etter formatet forklart i delen [Bruk datoformler](ui-enter-date-ranges.md#use-date-formulas).

## <a name="importing-or-exporting-financial-reports"></a>Importere eller eksportere finansrapporter

Du kan importere og eksportere finansrapporter som RapidStart-konfigurasjonspakker, som er nyttige for å dele informasjon med andre selskaper, for eksempel. Pakken opprettes i en .rapidstart-fil, som komprimerer innholdet.

### <a name="import-and-export-financial-reports"></a>Importere og eksportere finansrapporter

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 4.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Finansrapporter**, og velg deretter den relaterte koblingen.
2. Velg regnskapsrapporten, og velg deretter **Importer finansrapport** eller **Eksporter finansrapport**, avhengig av hva du vil gjøre.

> [!NOTE]
> Når du importerer finansrapporter, vil eksisterende poster med samme navn som de du importerer, slettes.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/configure-financial-reports-dynamics-365-business-central/index).

## <a name="see-also"></a>Se også

[Kjør og skriv ut rapporter](ui-work-report.md)  
[Finansforretningsanalyse](bi.md)  
[Finans](finance.md)  
[Konfigurere finans](finance-setup-finance.md)  
[Finans og kontoplanen](finance-general-ledger.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
