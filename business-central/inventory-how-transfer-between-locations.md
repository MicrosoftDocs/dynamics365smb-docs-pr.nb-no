---
title: Overfør varer mellom lagerlokasjoner
description: 'Finn ut hvordan du flytter beholdning fra ett sted eller lager til et annet, enten med reklassifiseringskladden eller overføringsordrer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 08/12/2024
ms.custom: bap-template
ms.search.keywords: 'move, warehouse'
ms.search.forms: '5746, 5745, 5759, 5753, 5743, 5758, 5752, 5744, 5749, 5740, 5741, 5742, 5757, 5748, 5747, 9285, 5756, 5755'
ms.service: dynamics-365-business-central
---

# <a name="transfer-inventory-between-locations"></a>Overfør lager mellom lokasjoner

Du kan overføre lagervarer mellom lokasjoner ved å opprette overføringsordrer. Du kan også bruke varereklassifiseringskladden.

> [!NOTE]
> Hvis du vil overføre varer, må du definere lokasjoner og overføringsruter. Hvis du vil vite mer om hvordan du konfigurerer steder, kan du gå til [Konfigurere steder](inventory-how-setup-locations.md). Du kan ikke bruke overføringsordrer for *tomme* lokasjoner.

## <a name="transfer-orders"></a>Overføringsordrer

Du kan levere en utgående overføring fra en lokasjon og mottar en inngående overføring ved destinasjonen. Du kan:

* Spore et antall i transitt.
* Definer kalendere, ruter og inngående og utgående håndteringstider for datoberegning og planlegging. Hvis du vil lære mer om planlegging, går du til [Om planleggingsfunksjonalitet](production-about-planning-functionality.md).
* Bruk forskjellige lagerfunksjoner for inngående og utgående lokasjoner.
* Med enkelte begrensninger kan du bruke overføringsordrer for direkte overføringer.

## <a name="item-reclassification-journals"></a>Varereklassifiseringskladder

Du kan også bruke siden **Varereklassifiseringskladder** til følgende:

* Direkte overføring av varer mellom lokasjoner.
* Flytte varer mellom hyller. Hvis du vil lære mer om overføring av varer mellom hyller, kan du gå til [Flytte varer som ikke er planlagt i grunnleggende lagerkonfigurasjoner](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).
* Endre et parti- eller serienummer til et nytt parti- eller serienummer. Hvis du vil lære mer om å reklassifisere serie- og partinumre, går du til [Reklassifisering av serie- eller partinumre](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).
* Endre utløpsdatoen til en ny dato.
* Reklassifiser varer fra en tom lokasjon til en faktisk lokasjon.
* Opprett lagerposter hvis du ikke administrerer lageraktiviteter.

## <a name="to-transfer-items-with-a-transfer-order"></a>Slik overfører du varer med en overføringsordre

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Overføringsordrer**, og velg deretter den relaterte koblingen.
2. På siden **Overføringsordrer** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du har fylt ut feltene **I transitt-kode**, **Transportørkode** og **Transportørservice** på siden **Spesif. av overføringsrute** når du definerer overføringsruten, fylles de tilsvarende feltene i overføringsordren ut automatisk.

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

### <a name="undo-a-transfer-shipment"></a>Angre en overføringslevering

Hvis du finner en feil i et antall i en bokført overføringsordre er det enkelt å korrigere antallet så lenge leveringen ikke er mottatt. På **siden Bokført overføringsseddel** oppretter handlingen **Angre forsendelse** korrigerende linjer på følgende måte:

* Verdien i feltet **Levert (antall)** er redusert med antallet du har angret.
* Verdien i feltet **Lever (antall)** er økt med antallet du har angret.
* Det er merket av i **Korrigering** for linjene.

Hvis antallet som er levert i en lagerlevering, opprettes det en korreksjonslinje i den bokførte lagerfølgeseddelen.

Du fullfører korrigeringen ved å åpne overføringsordren på nytt, angi riktig antall og deretter bokføre ordren. Hvis du bruker lagerlevering til å levere ordren, oppretter og bokfører du en ny lagerlevering.

### <a name="post-multiple-transfer-orders-in-a-batch"></a>Bokfør flere overføringsordrer samtidig

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

### <a name="schedule-a-job-queue-entry-to-post-multiple-documents-in-a-batch"></a>Planlegg en jobbkøoppføring for å bokføre flere dokumenter samtidig

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

### <a name="comparison-of-different-settings-for-transfer-orders"></a>Sammenligning av ulike innstillinger for overføringsordrer

Du kan bokføre overføringsordrer i forskjellige moduser, med eller uten transittlokasjon. Deaktiver veksleknappen Direkte overføring **, og Velg den midlertidige lokasjonen** i feltet I transitt-kode **på siden Overføringsordre**  **.**  Når du bokfører leveringen av en overføringsordre som bruker transittlokasjonen, er ikke varene på linjen lenger tilgjengelige på en av lokasjonene dine fordi de er i transitt. Direkte bokføring sikrer at et sted i transitt ikke brukes, og at forsendelsen og mottaket behandles samtidig. Den nøyaktige virkemåten til direkte bokføring kan være forskjellig basert på verdien som er valgt i **feltet Bokføring** av direkte overføring på **siden Lageroppsett** .

Tabellen nedenfor beskriver hvordan kombinasjonene er forskjellige.

|Funksjon|Feltet **Direkte overføring** er deaktivert på **siden Overføringsordre** |**Direkte overføring** er aktivert på **siden Overføringsordre** </br>**Direkte overføringsbokføring** er satt til **Direkte overføring** på **siden Lageroppsett** |**Direkte overføring** er aktivert på **siden Overføringsordre** </br>**Direkte overføringsbokføring** settes til **Mottak og levering** på **siden Lageroppsett** |
|---|---|---|---|
|Bruk sted i transitt|Ja|Nei|Nei|
|Kan bokføre mottak uten forsendelse.</br>Kan bruke **Angre mottak**.|Ja|Nei|Nei|
|Delvis bokføring|Ja|Nei|Ja|
|Vareposter|4:</br>Overfør fra From-Location,</br>Overføring til I transitt,</br>Overføring fra i transitt,</br>Overfør til lokasjon.|2:</br>Overfør fra From-Location,</br>Overfør til lokasjon.|4:</br>Overfør fra From-Location,</br>Overfør til *tomt*,</br>Overfør fra *tomt*,</br>Overfør til lokasjon.|
|bokførte dokumenter|Bokført overføringsforsendelse,</br>Bokført overføringsmottak.|Bokført direkte overføring|Bokført overføringsforsendelse,</br>Bokført overføringsmottak.|
|Reservasjon: inngående og utgående|Ja|Ja|Ja|
|Varegebyr – tilordne til bokført overføringsmottak|Ja|Nei|Ja|
|Lagerhåndtering|Full|Nei|Begrenset, se nedenfor|

Matrise for lagerhåndtering for konfigurasjon: **Direkte overføring** er aktivert på siden Overføringsordre **,** og **Direkte overføringsbokføring** er satt til **Direkte overføring** på **siden Lageroppsett** .

|Fra \ Til|Til: Ingen lagerhåndtering|Til: Lagermottak|Til: Lagerplassering|Til: Regissert plassering og plukking|
|-|-|-|-|-|
|**Fra: Ingen lagerhåndtering**|1|Støttes ikke|1, 4|Støttes ikke|
|**Fra: Lagerlevering**|1, 2|Støttes ikke|1,2,4|Støttes ikke|
|**Fra: Lagerplassering**|1, 3|Støttes ikke|1,3,4|Støttes ikke|
|**Fra: Regissert plassering og plukking**|2|Støttes ikke|2|Støttes ikke|

Tallene i cellene viser bokføringsalternativene som støttes.

1. Bokfør fra overføringsordre. For enkelte kombinasjoner må du kanskje fylle ut **feltet Levere** (antall).
2. Opprette og bokføre en lagerlevering.
3. Opprette og bokføre en lagerplukking.
4. Opprette og bokføre en lagerplassering. For enkelte kombinasjoner må du kanskje fylle ut **feltet Levere** (antall).

Uansett metode utføres forsendelses- og mottakstransaksjonene. Du kan for eksempel opprette en overføringsordre fra en lokasjon som krever lagerplukking, til en lokasjon som krever lagerplassering. Du kan opprette og bokføre lagerplasseringen, og både leverings- og mottakstransaksjonen opprettes. Du kan også bokføre slike dokumenter fra en overføringsordre eller fra en lagerplukking.  

Hvis du vil ha mer informasjon om lagerhåndtering, kan du se [Oversikt](design-details-warehouse-management.md) over lagerstyring.

## <a name="to-transfer-items-with-the-item-reclassification-journal"></a>Slik overfører du varer med varereklassifiseringskladden

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Vareoverføringskladder** og velg den relaterte koblingen.
2. På siden **Vareoverføringskladder** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I **Lokasjonskode**-feltet angir du lokasjonen der varene er lagret.

    > [!NOTE]  
    > Hvis du vil overføre varer uten lokasjonskode, lar du **Lokasjonskode**-feltet være tomt.
4. I feltet **Ny lokasjonskode** angir du lokasjonen du vil overføre varene til.
5. Velg handlingen **Bokfør**.

    [!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]


## <a name="see-also"></a>Se også

[Håndtere lager](inventory-manage-inventory.md)  
[Konfigurer lokasjoner](inventory-how-setup-locations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Endre hvilke funksjoner som vises](ui-experiences.md)  
[Generelle forretningsfunksjoner](ui-across-business-areas.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
