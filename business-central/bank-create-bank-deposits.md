---
title: Opprett bankinnbetalinger
description: Du kan foreta innbetalinger for å vedlikeholde en transaksjonspost som inneholder informasjon som kan brukes på utestående fakturaer og kreditnotaer.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Opprett bankinnbetalinger
> [!NOTE]
> Muligheten til å opprette bankinnbetalinger er nytt i Business Central 2022 lanseringsbølge 1 for versjoner i mange land/områder. Hvis du brukte Business Central i USA, Canada eller Mexico før denne utgivelsen, kan det hende du bruker de tidligere funksjonene. Du kan fortsette, men de nye funksjonene vil erstatte de gamle i en fremtidig lansering. Hvis du vil begynne å bruke de nye funksjonene som er beskrevet i denne artikkelen, kan administratoren gå til siden **Funksjonsbehandling** og aktivere **Funksjonsoppdatering: Standardisert bankavstemming og innbetalinger**.  

Bruk siden **Bankinnbetalinger** til å registrere innbetalinger som et enkelt dokument som bokfører en eller flere poster til en bankkonto. Vanligvis brukes bankinnbetalinger til å registrere kontantinnbetalinger. Bankinnbetalinger-siden er tilgjengelig på **Bankstyring**-menyen i rollesenteret for forretningsleder og andre rollesentre som håndterer kontantstyring.

Beløp på bankinnbetalinger kan komme fra flere kilder:

* Salg, ved å bruke en finanskonto for omsetning.
* Kundebetalinger.
* Kontantrefusjoner fra leverandører eller utbetalinger til dem. 

Bankinnbetalingslinjer inneholder opplysninger om enkeltinnbetalinger, for eksempel sjekker fra kunder. Summen av beløpene på linjene må legges sammen med det totale beløpet for innbetalingen.

Når du har fylt ut innbetalingsinformasjonen og -linjene, må du bokføre den. Bokføring vil oppdatere de aktuelle finansene. Disse finansene inkluderer finans og bank-, kunde- og leverandørpostene. Bokførte innbetalinger lagres for fremtidig referanse på siden **Bokførte bankinnbetalinger**.

**Bankinnbetaling**-rapporten viser kunde- og leverandørinnbetalinger med det opprinnelige beløpet, beløpet på innbetalingen som forblir åpent, og beløpet som brukes. Rapporten viser også det totale bokførte innbetalingsbeløpet som skal avstemmes.

## Før du begynner
Det er et par ting du må konfigurere før du kan bruke bankinnbetalinger. Du må ha en nummerserie og en finanskladdemal klar. Du må også angi om bankinnbetalingsbeløp skal bokføres som en engangssum. Det vil si som en sum av alle beløpene på innbetalingslinjene. Ellers bokføres hver linje som en individuell post. Bokføring av en innbetaling som én bankpost kan gjøre det enklere å utføre bankavstemming.

### Nummerserie og engangssuminnbetalinger
Du må definere en nummerserie for bankinnbetalinger, og deretter angi serien i feltet **Bankkontonr.** på siden **Salgsoppsett**. Hvis du vil ha mer informasjon, kan du se [Opprett nummerserier](ui-create-number-series.md). 

Du kan også på **siden Salgsoppsett**, hvis du vil bokføre innbetalinger som engangssummer i stedet for individuelle linjer, aktiverer du alternativet **Bokfør bankinnbetalinger som engangssum**. Bokføring av en innbetaling som en engangssum, som oppretter én bankpost for hele innbetalingsbeløpet, kan gjøre det enklere å utføre bankavstemming.

### Finanskladdemaler for bankinnbetalinger
Du må også opprette en finanskladdemal for innbetalinger. Du bruker finanskladder til å bokføre poster til bank-, kunde-, leverandør-, aktiva- og finanskontoer. Kladdemalene utformer finanskladden slik at den passer til formålet med arbeidet. Det vil si at feltene i kladdemalen er nøyaktig de verdiene du trenger. 

Innbetalingene blir kontaktmottak, så det kan være lurt å bruke nummerseriene for innbetalingskladder på nytt. Hvis du har behov for å skille mellom bankinnbetalings- og innbetalingskladdeposter, bruker du en annen nummerserie.

Du må også opprette en satsvis jobb for malen. Hvis du vil opprette en satsvis jobb, velger du **Kladder** på siden **Finanskladdemaler**. Hvis du vil ha mer informasjon, kan du se [Bruk kladdemaler og kladder](ui-work-general-journals.md#use-journal-templates-and-batches).

## Dimensjoner på bankinnbetalingslinjer
Linjene på bankinnbetalingen bruker automatisk standarddimensjonene du angav i feltene **Avdelingskode** og **Kundegruppekode**. Når du velger **Kunde** eller **Leverandør** i feltet **Kontotype**, vil dimensjonene som er angitt for kunden eller leverandøren, erstatte standardene. Du kan endre dimensjonene på linjene etter behov.

> [!TIP]
> Dimensjon på linjer angis i henhold til standard dimensjonsprioriteter. Linjedimensjoner prioriteres over hodedimensjoner. For å unngå konflikter kan du opprette regler som prioriterer når du skal bruke en dimensjon, avhengig av kilden. Hvis du vil endre hvordan dimensjoner prioriteres, kan du endre rangering på siden **Standard dimensjonsprioriteter**. Hvis du vil ha mer informasjon, kan du se [Slik definerer standard dimensjonsprioriteter](finance-dimensions.md#to-set-up-default-dimension-priorities).

## Opprett en ny bankinnbetaling
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bankinnbetalinger**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å åpne siden **Bankinnbetaling**. 
3. Velg finanskladdemalen du opprettet for bankinnbetalinger.  

    > [!NOTE]
    > Hvis finanskladdemalen har mer enn én kladd, blir du bedt om å velge en.

4. I feltet **Bankkontonr.** velger du bankkontoen du vil foreta innbetalingen.

    > [!TIP]
    > Du kan dobbeltsjekke at du setter opp til riktig konto ved hjelp av handlingene **Kontokort** og **Kontoposter** til å slå opp postene for den valgte bankkontoen. Hvis du for eksempel vil se om like innbetalinger ble gjort på kontoen.

5. I feltet **Totalt innbetalingsbeløp** angir du det totale beløpet for innbetalingen. Denne totalen må være summen av beløpene på alle linjer.
6. Fyll ut feltene som gjenstår, etter behov. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Datoen i feltet **Bokføringsdato** og dimensjonene i feltene **Avdelingskode** og **Kundegruppekode** tildeles linjene du oppretter for bankinnbetalingen. Du kan endre dem ved behov. 

7. Avhengig av om du vil bokføre bankinnbetalingen som engangssum eller hver linje for seg til bankposten, kan du slå av eller på **Bokfør som engangssum**. Standardinnstillingen kommer fra samme veksleknapp på siden **Salgsoppsett**.

    > [!NOTE]
    > Feltet **Valutakode** viser valutaen som er angitt for bankkontoen du velger. Du kan ikke velge en annen valuta.

8. På hurtigfanen **Linjer** oppretter du en ny linje for hver innbetaling du vil sette inn innbetalingen på.
9. I feltet **Kontotype** angir du hvor betalingen kom fra. For bankinnbetalinger er typen vanligvis **kunde** eller **leverandør**. 

    > [!NOTE]
    > Du kan også registrere en innbetaling til en leverandør. Du gjør dette ved å velge **Leverandør** og deretter angi betalingsbeløpet som et negativt tall i feltet **Kreditbeløp** på linjen. 

10. Angi dokumentnummeret til fakturaen som kreditbeløpet stammer fra, i feltet **Dokumentnr.**. Du kan bruke et dokumentnummer for hver linje, eller samme nummer for alle linjer.

    > [!TIP]
    > Vanligvis trenger du ikke å fylle ut feltet **Dokumenttype** for finansposter. Hvis du for eksempel skal sette opp kontanter fra et dags salg, lar du feltet stå tomt. Hvis du skal sette inn kontanter fra en kundebetaling, velger du **Betaling**.

11. Hvis du skal sette inn en innbetaling for en bestemt kundefaktura, velger du handlingen **Utlign poster** og angir deretter fakturanummeret i feltet **Utlignings-ID**. 
12. Hvis du er klar til å bokføre bankinnbetalingen, velger du handlingen **Bokfør**.

    > [!TIP]
    > Før du bokfører innbetalingen, kan du bruke handlingen **Kontrollrapport** til å se gjennom dataene. Rapporten viser om det finnes problemer, for eksempel manglende data, som vil forhindre bokføring.  

## Finn bokførte bankinnbetalinger
På siden **Bokførte bankinnbetalinger** vises en oversikt over selskapets tidligere innbetalinger. I oversikten kan du se gjennom merknadene og dimensjonene som ble angitt for innbetalingene. Du kan åpne bankinnbetalingen for å vise flere detaljer, og derfra kan du undersøke videre. Du kan for eksempel velge handlingen Søk etter poster hvis du vil vise de bokførte bankpostene. Fra bankposten finner du den tilsvarende bokførte finansposten.

Hvis du vil slå opp alle finansposter for de bokførte innbetalingslinjene, går du til **Finansjournal**-siden og bruker **Finans**-handlingen. Der finner du alle finanspostene, inkludert postene for kunder og leverandører.

## Tilbakefør en bokført bankinnbetaling
Hvis du vil tilbakeføre en bokført innbetaling, går du til siden **Finansjournaler**, finner journalen for innbetalingen og velger deretter handlingen **Tilbakefør journal**.

> [!NOTE]
> Du kan bare tilbakeføre en journal som inneholder én type post. Det vil si at journalen bare kan inneholde kundeposter eller leverandørposter, men ikke begge deler. Hvis en journal inneholder både, må du tilbakeføre innbetalingen manuelt.      

## Se også
[Finans](finance.md)  
[Konfigurer finans](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



