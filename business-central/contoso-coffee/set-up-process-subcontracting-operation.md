---
title: Definer og behandle en underleveranseoperasjon
description: Gjennomgang for å lære hvordan du oppretter og behandler en underleveranseoperasjon i Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Definer og behandle en underleveranseoperasjon

I denne artikkelen tar vi deg gjennom trinnene for å bruke Contoso Coffee-demodataene i underleveranse.

## Scenario

Du er produksjonsplanleggeren hos Contoso Coffee. På grunn av kapasitetsbegrensninger planlegger du å bruke en underleverandør til å produsere varen **SP-SCM1009, Airpot**.

Her oppretter du en ny frigitt produksjonsordre for tolv enheter av vare SP-SCM1009, Airpot, ved hjelp av Rute - SP-SCM1009-SUB-2. Bruk underleveranseforslaget til å generere en bestilling for produksjonen, og deretter full fører du operasjonen ved å motta og fakturere bestillingen.

## Trinn

1. Opprett en ny frigitt produksjonsordre for tolv enheter av varen SP-SCM1009, Airpot.

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Frigitt produksjonsordre**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Ny** og fyll deretter ut feltene som beskrevet i tabellen nedenfor.  

        |Felt  |Verdi  |
        |---------|---------|
        |**Kildetype** |Vare|
        |**Kildenr.** |SP-SCM1009|
        |**Antall** |100|
    3. Velg handlingen **Oppdater produksjonsordre**.  

2. Erstatt ruten til SP-SCM1009-SUB-2 på produksjonsordrelinjen, og oppdater deretter produksjonsordren, men bare for rute.  

    1. Legg til Produksjonsrutenr.-feltet i linjene i den frigitte produksjonsordren.<!--in code, this is marked as visible=false-->

    2. Endre feltet **Rutenr.** fra *SP-SCM1009-SERIAL* til *SP-SCM1009-SUB-2*.  

    3. Velg handlingen **Oppdater produksjonsordre**.  

    4. På forespørselssiden **Forny produksjonsordre** fjerner du feltet **Linjer**og **Komponentbehov** slik at oppgaven bare kjøres for rute, og deretter klikker du på **OK**-knappen.

3. Bruk underleveranseforslaget til å generere en bestilling for underleveranseoperasjonen i produksjonsordren du opprettet i trinn 2.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Underleveranseforslag**, og velg deretter den relaterte koblingen.  

    2. Velg handlingen **Beregn underleveranser**.

    3. Velg **Godta handlingsmelding**-feltet for den nye linjen.

    4. Velg **Utfør handlingsmelding**-handlingen.  

    5. På foresprøselssiden **Utfør handlingsmeld. – forslag**, godtar du alle standardverdier og klikker på **OK**-knappen.

    6. Når kjørselen er ferdig, klikker du på knappen **OK** for å lukke underleveranseforslaget.  

4. Motta og fakturer bestillingen.  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **bestillinger**, og velg deretter den relaterte koblingen.  

    2. På listen **Bestillinger** finner du bestillingen fra leverandøren 82000 underleverandør.

    3. I feltet **Leverandørs fakturanr.** angir du *542349*.

    4. På hurtigfanen **Linjer** velger du linjen og angir feltet **Direkte kostnad** til *18*.

    5. Velg handlingen **Bokfør**.  

    6. I forespørselsmeldingen velger du **Motta og fakturer**-alternativet.  

Avgangen til vare SP-SCM1009 Airpot er nå registrert.

## Se også

[Innføring i demodata for Contoso Coffee](contoso-coffee-intro.md)  
