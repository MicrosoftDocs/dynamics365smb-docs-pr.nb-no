---
title: Overfør varer mellom lagerlokasjoner
description: 'Finn ut hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 07/08/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# Overfør lager mellom lokasjoner

Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer. Du kan også bruke varereklassifiseringskladden.

> [!NOTE]
> Hvis du vil overføre varer, må du definere lokasjoner og overføringsruter. Hvis du vil vite mer om hvordan du konfigurerer steder, kan du gå til [Konfigurere steder](inventory-how-setup-locations.md). Du kan ikke bruke overføringsordrer for *tomme* lokasjoner.

## Overføringsordrer

Du kan levere en utgående overføring fra en lokasjon og mottar en inngående overføring ved destinasjonen. Du kan:

* Spor et antall i transitt
* Definer kalendere, ruter og inngående og utgående håndteringstider for datoberegning og planlegging. Hvis du vil lære mer om planlegging, går du til [Om planleggingsfunksjonalitet](production-about-planning-functionality.md).
* Bruk forskjellige lagerfunksjoner for inngående og utgående lokasjoner.
* Med enkelte begrensninger kan du bruke overføringsordrer for direkte overføringer.

## Varereklassifiseringskladder

Du kan også bruke siden **Varereklassifiseringskladder** til følgende:

* Direkte overføring av varer mellom lokasjoner.
* Flytt varer mellom hyller. Hvis du vil lære mer om å overføre varer mellom hyller, går du til [Flytt varer som ikke er planlagt, i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)
* Endre et parti- eller serienummer til et nytt parti- eller serienummer. Hvis du vil lære mer om å reklassifisere serie- og partinumre, går du til [Reklassifisering av serie- eller partinumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Endre utløpsdatoen til en ny dato.
* Reklassifiser varer fra en tom lokasjon til en faktisk lokasjon.
* Opprett lagerposter hvis du ikke administrerer lageraktiviteter.

## Slik overfører du varer med en overføringsordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsordrer**, og velg deretter den relaterte koblingen.
2. På siden **Overføringsordrer** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    >   Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** på siden **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.

    Når du fyller ut feltet **Transportørservice**, blir mottaksdatoen for overfør til-lokasjonen beregnet ved at leveringstiden for transportørtjenesten legges til i forsendelsesdatoen.

3. Det er flere måter å fylle inn linjene på:

    |Alternativ  |Beskrivelse  |
    |---------|---------|
    |Manuelt     | På hurtigfanen **Linjer** fyller du ut en linje for en vare eller bruker handlingen **Velg varer** til å velge flere varer.        |
    |Automatisk     | * Velg handlingen **Hent hylleinnhold** for å velge eksisterende varer fra en bestemt hylle på lokasjonen.<br><br>* Velg **Hent mottakslinjer** for å velge varer som du nettopp har mottatt på overfør fra-lokasjonen.        |

    Du kan nå sende varene.
4. Velg **Bokfør**-handlingen, velg **Lever**-alternativet, og velg deretter **OK**-knappen.

    Varene er nå i transitt mellom de angitte lokasjonene i henhold til overføringsruten.

    Som lagermedarbeider på overfør fra-lokasjonen, kan du fortsette å motta varene. Overføringsordrelinjene er de samme som når de sendes, og kan ikke redigeres.
5. Velg **Bokfør**-handlingen, velg **Motta**-alternativet, og velg deretter **OK**-knappen.

### Bokfør flere overføringsordrer samtidig

Fremgangsmåten nedenfor forklarer hvordan du massebokfører overføringsordrer.

1. 1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsordrer**, og velg deretter den relaterte koblingen.  
2. På **Overføringsordrer**-siden velger du ordrene som skal bokføres.
3. I **Nr.** -feltet, åpne hurtigmenyen og velg **Velg flere**.
4. Velg avmerkingsboksen for linjene for hver ordre du vil bokføre.
5. Velg handlingen **Bokfør**, og velg **deretter Massebokfør**.
6. På siden **Massebokfør overføringsordrer** fyller du ut feltene etter behov.

   > [!TIP]
    > For overføringsordrer som bruker en i transitt-lokasjon, kan du velge enten **Lever** eller **Motta**. Gjenta dette trinnet hvis du må gjøre begge deler. For ordrer der **Direkte bokføring** er aktivert, fungerer begge alternativene på samme måte og bokfører ordren fullstendig.

7. Velg **OK**.
8. Du kan vise potensielle problemer ved å åpne siden **Feilmeldingsregister**.

    > [!NOTE]
    > Bokføring av flere dokumenter kan ta litt tid og blokkere andre brukere. Vurder å aktivere bokføring i bakgrunnen. Hvis du vil ha mer informasjon, kan du se [Bruke jobbkøer til å planlegge oppgaver](/dynamics365/business-central/admin-job-queues-schedule-tasks).

### Planlegg en jobbkøoppføring for å bokføre flere dokumenter samtidig

Du kan også bruke jobbkøen til å planlegge at bokføring skal skje på et tidspunkt som passer for organisasjonen. Det kan for eksempel være fornuftig for virksomheten å kjøre visse rutiner etter at det meste av dagens dataregistrering er gjort for dagen.

Følgende fremgangsmåte viser hvordan du konfigurerer rapporten **Massebokfør overføringsordrer** slik at overføringsordrer bokføres direkte automatisk kl. 16:00 på ukedager. Det tidspunktet er bare et eksempel. Trinnene er de samme for andre dokumenter.  

1. Søk etter siden **Prosjektkøoppføringer** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. I feltet **Objekttype som skal kjøres** velger du **Rapport**.  
4. I feltet **Objekt-ID som skal kjøres** velger du **5707, Massebokfør overføringsordrer**.
5. Merk av for **Rapportforespørselsside**.
6. På forespørselssiden **Massebokfør overføringsordrer** velger du **Lever**-alternativet, filtrerer på **Direkte overføring**, og deretter velger du **OK**.

   > [!IMPORTANT]
   > Det er viktig å definere filtre. Hvis ikke bokfører [!INCLUDE [prod_short](includes/prod_short.md)] alle dokumenter, selv om de ikke er klare. Vurder å definere et filter i **Status**-feltet for verdien **Frigitt** og et filter for **Bokføringsdato**-feltet for verdien **..i dag**. Hvis du vil lære mer om filtre, går du til [Sortering, søking og filtrering](/dynamics365/business-central/ui-enter-criteria-filters).

7. Merk av i alle bokser fra **Kjør på mandager** til **Kjør på fredager**.
8. I feltet **Starttidspunkt** angir du **16:00**.
9. Velg **Sett status til Klar**-handlingen.

## Slik overfører du varer med varereklassifiseringskladden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareoverføringskladder** og velg den relaterte koblingen.
2. På siden **Vareoverføringskladder** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.

    > [!NOTE]  
    > Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.
4. I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.
5. Velg handlingen **Bokfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]

## Angre en overføringslevering

Hvis du finner en feil i et antall i en bokført overføringsordre er det enkelt å korrigere antallet så lenge leveringen ikke er mottatt. På siden **Bokfør overføringslevering** oppretter handlingen **Angre levering** korrigerende linjer på følgende måte:

* Verdien i feltet **Levert (antall)** er redusert med antallet du har angret.
* Verdien i feltet **Lever (antall)** er økt med antallet du har angret.
* Det er merket av i **Korrigering** for linjene.

Hvis antallet ble levert i en lagerlevering, opprettes en korrigeringslinje i den bokførte lagerleveringen.

Du fullfører korrigeringen ved å åpne overføringsordren på nytt, angi riktig antall og deretter bokføre ordren. Hvis du bruker lagerlevering til å levere ordren, oppretter og bokfører du en ny lagerlevering.

## Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Konfigurer lokasjoner](inventory-how-setup-locations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
