---
title: Opprette nummerserier
description: Finn ut hvordan du definerer nummerserier som tilordner unike ID-koder til konti og dokumenter i Business Central.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'numbers, numbering'
ms.search.form: '456, 457, 458, 459, 460, 461, 21, 22, 26, 27, 31'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="create-number-series"></a>Opprette nummerserier

For hvert selskap som opprettes, må du tilordne unike identifikasjonskoder til elementer som for eksempel hovedbokkontoer, kunde- og leverandørkontoer, fakturaer og andre dokumenter. Nummerering er ikke bare viktig for identifikasjonsformål. Med et godt utformet nummereringssystem er det enklere å styre og analysere selskapet, og antall feil som forekommer ved dataregistrering reduseres.

> [!Important]
> Som standard er det ikke tillatt med mellomrom i nummerserier, fordi den nøyaktige historikken for finanstransaksjoner må være tilgjengelige for revisjon, i henhold til lovgivningen, og må derfor følge en ubrutt sekvens uten slettede numre.
> 
> Hvis du vil tillate hull i visse nummerserier, må du først rådføre deg med revisor eller regnskapssjefen for å være sikker på at du overholder de juridiske kravene i landet/regionen din. Hvis du vil ha mer informasjon, kan du se delen [Tomrom i nummerserier](#gaps-in-number-series).

> [!NOTE]  
> Vi anbefaler at du bruker de samme nummerseriekodene som er oppført på siden **Nummerserieliste** i demoselskapet CRONUS. Koder som *P-INV+* gir kanskje ikke umiddelbar mening for deg, men [!INCLUDE[prod_short](includes/prod_short.md)] har en rekke standardinnstillinger som avhenger av disse nummerseriekodene.

Et nummereringssystem lager du ved å opprette én eller flere koder for hver hoveddatatype eller dokumenttype. Du kan for eksempel opprette én kode for å nummerere kunder, en annen kode for å nummerere salgsfakturaer, og enda en kode for å nummerere dokumenter i finanskladder. Når du har opprettet en kode, må du opprette minst én nummerserielinje. Nummerserielinjen inneholder informasjon som for eksempel første og siste nummer i serien, samt startdato. Du kan opprettet mer enn én nummerserielinje per nummerseriekode, med ulik startdato for hver linje. Seriene brukes i rekkefølge, og hver serie starter på sin respektive startdato.

> [!NOTE]
> Den maksimale lengden på et tall i en nummerserie er 20 tegn. Det finnes noen tilfeller der [!INCLUDE[prod_short](includes/prod_short.md)] vil føye til et nummer med en systemgenerert ID. Når dokumenter som fakturaer for eksempel brukes til å gjennomføre transaksjoner, for eksempel betalinger, genererer [!INCLUDE[prod_short](includes/prod_short.md)] identifikatorer for de utlignede transaksjonene. Identifikatoren består av et tall fra en nummerserie og en systemgenerert ID på seks tegn, for eksempel -12345. Hvis du forventer å behandle mer enn 9999 dokumenter i bank-eller GIRO-kladder, eller innbetalingskladder, kan du definere en nummerserie for disse dokumenttypene for å inkludere færre enn 14 tegn.

Du setter vanligvis opp i nummerserien automatisk skal sette inn neste nummer i rekken på nye kort eller dokumenter du oppretter. Men kan du også definere en nummerserie som tillater at du angir det nye nummeret manuelt. Du angir dette med avmerkingsboksen **Manuelle nr.**

Hvis du vil bruke mer enn én nummerseriekode for én type hoveddata - det vil si hvis du for eksempel vil bruke ulike nummerserier for ulike varekategorier - kan du bruke nummerserieforbindelser.

## <a name="gaps-in-number-series"></a>Tomrom i nummerserier
Ikke alle poster du oppretter i [!INCLUDE[prod_short](includes/prod_short.md)], er finanstransaksjoner som må bruke sekvensiell nummerering. Kundekort, tilbud og lageraktiviteter er eksempler på poster som tilordnes et nummer fra en nummerserie, men som ikke er underlagt revisjon og/eller kan slettes. For slike nummerserier kan du merke av for **Tillat tomrom i nr.** på siden **Nr.serielinjer**. Denne innstillingen kan også endres etter at du har opprettet nummerserien. Hvis du vil ha mer informasjon, kan du se [Opprette en ny nummerserie](ui-create-number-series.md#to-create-a-new-number-series).

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Virkemåte for feltet Nr. på dokumenter og kort

På salgs-, kjøps- og overføringsdokumenter og på alle kort kan **Nr.** feltet kan fylles ut automatisk fra en forhåndsdefinert nummerserie, eller du kan legge den til manuelt. Under visse omstendigheter er feltet **Ant.** er usynlig for å hindre deg i å redigere det.  

**Nr.** -feltet kan fylles ut på tre måter:

1. Hvis det bare finnes én nummerserie for dokumenttypen eller kortet, og feltet **Standardnr.** er valgt og feltet **Manuelle nr**. er ikke valgt for nummerserien, fylles feltet ut automatisk med neste nummer i serien. **Nr.** -feltet vil ikke være synlig på kortet eller dokumentet.  

    Selv om du definerer maler med forskjellige nummerserier for kunder, hvis nummerserien som er definert i siden **Salgsoppsett** er definert på denne måten, er feltet **Nr.** usynlig på kundekortet, uansett hvilken mal du bruker. Det samme gjelder andre typer kort og dokumenter.  

    > [!NOTE]  
    > Hvis nummerserien ikke fungerer, for eksempel fordi den er tom for numre, vil feltet **Nr.** vises, og du kan angi et nummer manuelt eller løse problemene på siden **Nummerserie**.

2. Hvis det finnes flere nummerserier for dokumenttypen eller kortet, og det ikke er merket av for **Standardnr.** for den tilordnede nummerserien, er feltet **Nr.** synlig, og du kan slå opp **Nummerserie**-siden og velge nummerserien du vil bruke. Det neste nummeret i serien settes deretter inn i feltet **Nr.** .

3. Hvis du ikke har definert en nummerserie for typen dokument eller kort, eller hvis det er merket av for **Manuelle nr.** for nummerserien, vises feltet **Nr.** og du må angi et nummer manuelt. Du kan angi opptil 20 tegn, både tall og bokstaver.

Når du åpner et nytt dokument eller kort som det finnes en nummerserie for, åpnes den aktuelle **Oppsett for nummerserie**-siden, slik at du kan definere en nummerserie for denne dokumenttypen eller dette kortet før du går videre med andre dataregistreringer.

> [!NOTE]  
> Hvis du vil aktivere manuell nummerering på for eksempel nye varekort som er opprettet med en dataoverføring som har skjult **Nr.** som standard, går du til siden **Lageroppsett** og velger **Varenr.**-feltet for å åpne og angi den relaterte nummerserien til **Manuelle nr.**.

## <a name="to-create-a-new-number-series"></a>Opprette en ny nummerserie

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Nr.serie**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. Fyll ut feltene etter behov på den nye linjen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Velg handlingen **Linjer**.  
5. På siden **Nr.serielinjer** fyller du ut feltene for å angi faktisk bruk og innhold i nummerserien du opprettet i trinn 2.  
6. Gjenta trinn 5 for så mange typer bruk av nummerserien du trenger. Feltet **Startdato** definerer hvilken nummerserielinje som er aktiv.  

> [!TIP]
> Hvis du vil tillate at brukere angir numre manuelt når de registrerer en ny kunde eller leverandør, kan du for eksempel velge feltet **Manuelle nr.** på selve nummerserien. Hvis du ikke vil tillate manuelt nummer, fjerner du merket i feltet.

Du kan knytte nummerserier til malene du har definert for de ulike typene kunder og leverandører som selger og innkjøpere oftest legger til i [!INCLUDE [prod_short](includes/prod_short.md)]. I dette tilfellet kan du definere de aktuelle nummerseriene, knytte dem til relasjoner og deretter legge til den første nummerserien i den relevante relasjonen på den relevante oppsettsiden. Når en bruker deretter oppretter en kunde, velger de den relevante malen, og den nye kunden får tildelt et nummer fra nummerserien som er definert for denne malen.  

## <a name="to-create-relationships-between-number-series"></a>Slik oppretter du forbindelser mellom nummerserier

Hvis du har opprettet mer enn én nummerseriekode for den samme typen grunnleggende opplysninger eller transaksjoner, kan du opprette forbindelser mellom kodene. Denne funksjonen kan hjelpe deg med å velge mellom koder når du bruker et nummer. Når du definerer et forhold mellom en gruppe med nummerserier, knytter du alle de relaterte seriene til én nummerseriekode. Deretter kan du sette inn koden i et felt på hurtigfanen **Nummerering** på en av de relevante konfigurasjonssidene, for eksempel **Salgsoppsett**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Nr.serie**, og velg deretter den relaterte koblingen.
2. Velg linjen med nummerserien du vil opprette forbindelser for, og velg deretter **Forbindelser**.
3. I **Seriekode**-feltet angir du koden for nummerserien du vil knytte til serien du valgte i trinn 2.
4. Legg til en linje for hver kode du vil knytte til den valgte nummerserien.
5. Lukk siden.

Når du så registrerer noe som trenger et nummer, kan du bruke forbindelsene du har opprettet til å velge mellom nummerseriene som er koblet til hverandre.

## <a name="to-set-up-where-a-number-series-is-used"></a>Slik definerer du der det brukes en nummerserie

Følgende fremgangsmåte viser hvordan du angir nummerseriene for Salg-området. Trinnene er de samme for andre områder.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Salg**, og velg deretter den relaterte koblingen.
2. På siden **Salg** på hurtigfanen **Nummerserie** velger du ønsket nummerserie for hvert salgskort eller dokument.

Det valgte nummeret skal nå brukes til å fylle ut feltet **Nr.** på kortet eller det aktuelle dokumentet, i henhold til innstillingene du gjorde på nummerserielinjen.  

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/number-series-trail-codes-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Konfigurere [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
