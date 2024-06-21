---
title: Spor varekostjusteringer
description: Finn ut hvordan sporing av justeringer av varekost kan hjelpe deg med å holde varekostnadsdataene nøyaktige.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="track-item-cost-adjustments"></a>Spor varekostjusteringer

Det er viktig å holde varekost nøyaktig og forkorte tiden fra du bokfører en post til Finans gjenspeiler kostnaden. Du kan spore ytelsen til kostjusteringer for individuelle justeringskjøringer og varer. Hvis det oppstår feil, kan du identifisere de problematiske elementene og foreta korrigeringer. Du kan for eksempel utelate varene fra beregninger for å sikre at justeringer ikke avbrytes for andre varer. Du kan justere kostnader for enkeltvarer, eller du kan opprette bunker med varer og justere alle samtidig.

## <a name="start-tracking-cost-adjustments"></a>Begynne å spore kostnadsjusteringer

Det er enkelt å komme i gang. På siden **Lageroppsett** har feltet **Loggføring av kostjustering** noen alternativer:

* **Deaktivert** betyr at du ikke logger kjøringer av kostnadsjusteringer.
* **Bare feil** betyr at du logger bare kjøringer som mislyktes.
* **Alle** betyr at du logger alle kjøringer.

> [!NOTE]
> For å minimere størrelsen på loggen loggfører [!INCLUDE [prod_short](includes/prod_short.md)] ikke justeringene som skjer automatisk når noen bokfører et element.

Du må også definere jobbkøposten **Bokfør lagerkost i Finans (1002)**. Denne jobbkøposten justerer automatisk kostnader i henhold til en tidsplan. Hvis du vil finne ut mer om jobbkøposter, kan du gå til [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md).

## <a name="manage-cost-adjustments"></a>Håndtere kostnadsjusteringer

Bruk siden **Lagerkostjustering** til å administrere og overvåke kostnadsjusteringsprosessen. Denne siden viser varer sammen med deres kostnadsparametere og kostnadsjusteringsstatus. Du kan filtrere listen slik at den fokuserer på varer som krever justering eller som er utelatt fra kostnadsjusteringsprosessen.

### <a name="about-item-batches"></a>Om varebunker

Du kan kjøre kostnadsjustering for flere varer ved å gruppere dem i bunker. Bunker gjør det enkelt å justere enkelte varer separat, for eksempel fordi det tar lengre tid å justere dem. Bunker kan også bidra til å identifisere varer som har problemer.

Hvis du vil opprette en bunke, gjør du ett av følgende på siden **Lagerkostjustering**:

* Velg varene i listen, velg **Kjør kostjustering**, og velg deretter **Legg til bunke**.
* Hvis du vil opprette en bunke og kjøre kostjustering umiddelbart, velger du varene i listen, velger **Kjør kostjustering** og velger deretter **Legg til bunke og kjør**.
* Velg **Kjør kostjustering**, velg **Varebunker**, og angi deretter et filter i **Varefilter**-feltet.
  
> [!TIP]
> Hvis du raskt vil opprette en ny bunke for alle varer som ikke allerede er inkludert i en bunke, går du til siden **Kostjustering – varebunker** og velger **Legg til manglende varer**.

Når en kjøring for en bunke er ferdig, har bunken én av følgende statuser på siden **Varebunker**:

* **Vellykket**: Kostnadsjusteringen er vellykket.
* **Mislyktes**: Hvis kostnadsjusteringen mislykkes, identifiserer [!INCLUDE [prod_short](includes/prod_short.md)] varen som forårsaket feilen, og deler deretter gjeldende bunke i to. Én bunke med den problematiske varen og en annen med de gjenstående varene. Kostnadsjustering kjøres på nytt for bunken med de gjenstående varene. Hvis den mislykkes igjen, gjentas prosessen. Du definerer maksimalt antall delinger i feltet **Maks antall nye forsøk**. Standardverdien for nye forsøk er 10, men du kan angi en ny grense.
* **Tidsavbrutt**: Hvis kostnadsjusteringen for en bunke ikke fullføres innen perioden som er angitt i feltet **Tidsavbrudd (minutter)** (fra 1 til 720 minutter), avsluttes økten og endringene rulles tilbake. [!INCLUDE [prod_short](includes/prod_short.md)] deler deretter gjeldende bunke i to og kjører kostnadsjusteringsprosessen på nytt for hver halvdel. Denne prosessen fortsetter til kostnadsjusteringen er vellykket eller til maksimalt antall nye forsøk er nådd.

> [TIPS!] Hver bunke kjøres i en separat økt. Du kan overvåke fremdriften ved å bruke handlingen **Oppdater** .

### <a name="run-cost-adjustment"></a>Kjør kostjustering

Bruk siden **Lagerkostjustering** til å foreta justeringer.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerkostjustering** og velg den relaterte koblingen.
1. Avhengig av hva du vil gjøre, kan du bruke ett av følgende alternativer:

  * For én eller flere varer umiddelbart velger du varene i listen og velger deretter **Kjør kostjustering**.
  * For bunker kan du bruke ett av følgende alternativer:

    * Hvis du vil opprette en bunke og justere kostnader umiddelbart, velger du varene i listen, velger **Kjør kostjustering** og velger deretter **Legg til bunke og kjør**.
    * Hvis du vil kjøre den for alle bunker, velger du **Kjør kostjustering**, **Varebunker**, og velger deretter **Kjør**.
    
    Hvis du vil lære mer om bunker, kan du gå til [Om varebunker](#about-item-batches).

### <a name="explore-item-details"></a>Utforsk varedetaljer

Bruk **Vare**-menyen til å få tilgang til informasjon om kostnadsjusteringer for en valgt vare.

* **Vareposter**: Viser vareposter for varen. Med handlingen **Merk for justering** kan du fremtvinge en ny kjøring av kostjustering for varer som direkte eller indirekte er knyttet til de inngående postene du velger. Det kan være nyttig å fremtvinge en ny kjøring hvis tidligere kjøringer førte til feil kostnader.
* **Verdiposter**: Viser verdiposter for varen.
* **Utgangspunkter for kostjustering**: Åpne siden **Utgangspunkt for justering av gjennomsnittskost**, som du primært bruker til å beregne gjennomsnittskost. Siden viser kombinasjoner av varer, lokasjoner, varianter og verdisettingsdatoer som kostjusteringer kjøres eller må kjøres for.
* **Kostjusteringsordrer**: Åpne siden **Lagerjusteringspost (ordre)**, der du justerer produksjons- og monteringsordrer. Den viser at ordrene er justert eller krever justering.

### <a name="view-the-outcome"></a>Vis resultatet

Bruk menyen **Logg per** til å vise resultatet av kostnadsjusteringer:

* **Kjør**: Vis kostnadsjusteringslogger for hver kjøring. Loggen inneholder data om varefilteret, statusen (Vellykket/Mislyktes/Tidsavbrudd), startdato og sluttdato / klokkeslett, varigheten og kostnadsforskjellene som genereres av kjøringen.
* **Vare**: Vis detaljert informasjon om justeringsprosessen for den valgte varen.

### <a name="include-or-exclude-items-from-adjustments"></a>Inkludere eller utelate varer fra justeringer

Hvis én eller flere varer mislykkes, kan du utelate varene fra justeringskjøringen og deretter inkludere dem i senere kjøringer. Velg ett av følgende på **Funksjoner**-menyen:

* **Utelat vare fra justering** og **Inkluder vare i justering**: Deaktiver midlertidig og aktiver deretter kostnadsjustering for en valgt vare på nytt. Kostjustering fortsetter å holde kostnadene nøyaktige for andre varer mens du undersøker et problem med en bestemt vare.

## <a name="post-adjusted-costs-to-the-general-ledger"></a>Bokfør justerte kostnader til Finans

Vanligvis bokføres nye verdiposter i Finans i henhold til tidsplanen for jobbkøposten **Bokfør lagerkost i Finans (1002)**. Du kan imidlertid bokføre justeringer i Finans umiddelbart fra siden **Lagerkostjustering**. På **Funksjoner**-menyen velger du **Bokfør lagerkost i Finans**.

## <a name="troubleshoot-cost-adjustments"></a>Feilsøking av kostnadsjusteringer

Bruk følgende alternativer på **Diagnostikk**-menyen til å feilsøke kostsjusteringskjøringer.

* **Eksporter varedata**: Eksporter varerelaterte data til en tekstfil. Du kan bruke filen til videre analyse i et sandkassemiljø eller knytte den til en støtteforespørsel når du undersøker problemer med kostnadsberegning.
* **Importer varedata**: Importer den tidligere eksporterte tekstfilen tilbake til databasen. Denne handlingen er bare aktivert i sandkassemiljøer eller evalueringsselskaper.
* **Tilbakestill Kost er justert**: Tilbakestill vekslebryteren **Kost er justert** på varer, produksjonsordrer eller monteringsordrer. Med denne innstillingen kan du fremtvinge ny kjøring av kostnadsjusteringen for dem.
* **Rapport for gjenkjenning av kostberegningsproblemer**: Diagnostiser vanlige dataproblemer som forårsaker beregningsfeil i kostnadsberegningen. Den kontrollerer om varepostene, verdipostene, vareutligningspostene og kapasitetspostene er riktige.
* **Slett varedata**: Fjern alle varerelaterte tabeller i databasen. Denne handlingen er bare tilgjengelig i sandkassemiljøer eller evalueringsselskaper.

## <a name="see-also"></a>Se også

[Juster varekost](inventory-how-adjust-item-costs.md)  
[Utformingsdetaljer: Kostnadsjustering](design-details-cost-adjustment.md)  
