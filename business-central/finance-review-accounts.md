---
title: Gå gjennom finanskontoer
description: Du kan spore fremdriften når du gjennomgår beløp i finanskontoer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/28/2023
ms.custom: bap-template
ms.search.form: '22207,'
ms.service: dynamics-365-business-central
---

# <a name="review-amounts-in-general-ledger-accounts"></a>Gå gjennom beløp i finanskontoer

Du har kanskje finanskontoer du ofte holder øye med. Eller kanskje du vil øke gjennomgangsprosessen raskere på slutten av måneden. Hvis du trenger hjelp med å holde oversikt over hva du har gjort og gjøre gjennomganger raskere, bruker du handlingen **Se gjennom poster** på **Kontoplan** eller **Finanskontokort**-siden for hver konto. 

## <a name="set-up-accounts-for-reviews"></a>Definer kontoer for gjennomganger

På siden **Finanskontokort** for hver konto angir du hvordan du vil tillate gjennomganger i feltet **Gå gjennom policy**.

|Gå gjennom policy  |Beskrivelse  |
|---------|---------|
|Ingen     | Du kan ikke merke oppføringer for kontoen som kontrollert. Du kan for eksempel bruke dette alternativet for kontoer, for eksempel leverandører, salg og bankkontoer, hvor det finnes andre måter å gå gjennom beløpene på.        |
|Tillat gjennomgang     | Du trenger ikke inkludere oppføringer i en gjennomgang, og beløpene for debet- og kreditoppføringer må ikke balansere. Du fjerner en gjennomgang, for eksempel hvis du har gjort en feil.        |
|Tillat gjennomgang og samsvar saldo     | Det totale beløpet for debet- og kreditoppføringer i gjennomgangen må samsvare. **Debet**- og **Kredit**-feltene viser disse beløpene, og **Saldo**-feltet viser totalen. Med denne innstillingen kan du også fjerne en gjennomgang. Når du fjerner en gjennomgang fra en eller flere oppføringer, må debet- og kreditoppføringer fremdeles være i balanse.        |

## <a name="mark-entries-as-reviewed"></a>Merk oppføringer som gjennomgått

Velg oppføringene du har gjennomgått, og bruk deretter handlingen **Angi som gjennomgått**. Hver gang du merker for en eller flere oppføringer som kontrollert, får oppføringene samme nummer som i kolonnen **Gjennomgått identifikator**. Gjennomgangsidentifikatoren er en hendig måte å holde oversikt over oppføringene som ble gjennomgått samtidig. [!INCLUDE [prod_short](includes/prod_short.md)] registrerer også brukeren som utførte gjennomgangen, og når brukeren gjorde det.

Hvis du merker oppføringer som gjennomgått, men angrer, bruker  du handlingen **Angi som ikke kontrollert**.

* Hvis den Gjennomgang tillatt-policyen er tildelt kontoen, tilbakestiller handlingen den korrekturleste identifikatoren til 0 og fjerner personen og datoen og klokkeslettet for gjennomgangen. 
* Hvis Gjennom tillatt-policyen og policy for samsvar saldo er tildelt, må kredit og debet være i balanse. Hvis for eksempel en av oppføringene i en gjennomgang er en feil, kan du velge en annen oppføring med riktig verdi. Erstatningsoppføringen trenger ikke ha samme gjennomgått identifikator.

> [!TIP]
> En rask måte å velge flere oppføringer på, er å holde nede CTRL eller SKIFT mens du velger oppføringene. Med CTRL kan du velge bestemte oppføringer, og deretter velger du alle oppføringer mellom første og siste oppføring du velger.

## <a name="review-accounts-that-have-old-entries"></a>Gå gjennom kontoer som har gamle oppføringer

Du kan ha oppføringer fra tidligere perioder som du allerede har gjennomgått, eller bare trenger en gjennomgang. Du vil bare begynne å se gjennom oppføringer fra, for eksempel begynnelsen av året eller regnskapsperioden. Du kan la oppføringene være som de er. Hvis du imidlertid vil analysere data i Excel eller ved hjelp av analysemodus, merker du oppføringene som gjennomgått. Hvis du vil ha mer informasjon om å analysere oppføringer, går du til [Analyser oppføringer](#analyze-entries). Hvis du vil merke oppføringer som gjennomgått, legger du til et filter i filtrerruten for å vise bare oppføringene, og deretter velger du handlingen **Merk valgte oppføringer som gjennomgått**.

## <a name="filter-entries"></a>Filtrer oppføringer

For å få et klarere bilde er det flere måter å filtrere oppføringer på på siden **Se gjennom finansposter**.

* Bruk handlingene **Vis gjennomgåtte poster** og **Skjul gjennomgåtte poster** til å vise bare de postene du har eller ikke har gjennomgått. Hvis du vil fjerne filtrene, bruker du handlingen **Vis alle poster**.
* Bruk filtreringsruten. Du kan for eksempel filtrere etter kontonummer eller, hvis du har eldre poster og vil markere alle som gjennomgått, etter en bokføringsdato.

## <a name="analyze-entries"></a>Analyser oppføringer

Det finnes flere måter å analysere finansposter du har gjennomgått på.

* Aktiver analysemodus, for eksempel for å gruppere poster i henhold til gjennomgått identifikator. Hvis du vil lære mer om analysemodus, går du til [Analyser listesidedata ved hjelp av analysemodus](analysis-mode.md).
* Eksporter oppføringene til Excel.

## <a name="see-also"></a>Se også

[Forstå finans og kontoplanen](finance-general-ledger.md)  
[Definere eller endre kontoplanen](finance-setup-chart-accounts.md)  
