---
title: Om planleggingsfunksjonalitet | Microsoft-dokumentasjon
description: Planleggingssystemet tar hensyn til alle behovs- og forsyningsdata, nettoberegner resultatet og oppretter forslag til å balansere forsyningen slik at den dekker behovet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b6999be84e2fdaca2eefef41c339c366c330a3dc
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3925033"
---
# <a name="about-planning-functionality"></a>Om planleggingsfunksjonalitet

Planleggingssystemet tar hensyn til alle behovs- og forsyningsdata, nettoberegner resultatet og oppretter forslag til å balansere forsyningen slik at den dekker behovet.  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  

> [!NOTE]  
> Les verktøytips for å forstå funksjon for alle feltene i dette emnet. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="demand-and-supply"></a>Behov og forsyning

Planlegging har to elementer: behov og forsyning. Disse må holdes i balanse for å sikre at behovet dekkes i rett tid og på en kosteffektiv måte.  

- Behov er den vanlige betegnelsen som brukes om alle typer bruttobehov, for eksempel en ordre, serviceordre, komponentbehov fra monterings- eller produksjonsordrer, utgående overføring, rammeordre eller prognose. I tillegg til disse tillater programmet andre tekniske typer behov, for eksempel negativ produksjon eller bestilling, negativ beholdning og bestillingsretur.  
- Forsyning er ordet som brukes om alle typer etterfylling, for eksempel beholdning, en bestilling, monteringsordre, produksjonsordre eller inngående overføring. På tilsvarende vis kan det finnes en negativ ordre eller serviceordre, negativt komponentbehov eller ordreretur, og alt dette representerer også på en måte forsyning.  

Et annet mål med planleggingssystemet er å sikre at beholdningen ikke vokser unødvendig. Hvis behovet avtar, foreslår systemet at du utsetter, reduserer antallet i eller annullerer eksisterende etterfyllingsordrer.  

## <a name="planning-calculation"></a>Planleggingsberegning

Planleggingssystemet drives av forventet og faktisk kundebehov samt gjenbestillingsparametere for beholdning. Når du kjører planleggingsberegningen, foreslår programmet bestemte handlinger (handlingsmeldinger) som gjelder mulig etterfylling fra leverandører, overføringer mellom lagre eller produksjon. Hvis det allerede finnes etterfyllingsordrer, kan de foreslåtte handlingene være å øke eller påskynde ordrene for å dekke endringene i behovet.  

Grunnlaget for planleggingsrutinen er i beregningen av brutto til netto. Nettobehov driver planlagte ordrefrigivelser, som planlegges basert på ruteinformasjonen (produserte varer) eller leveringstiden for varekort (kjøpte varer). Antall planlagte ordrefrigivelser er basert på planleggingsberegningen og påvirkes av parameterne som er angitt på de enkelte varekortene.  

## <a name="planning-with-manual-transfer-orders"></a>Planlegge med manuelle overføringsordrer

Som du ser i feltet **Etterfyllingssystem** på et LFE-kort, kan planleggingssystemet konfigureres slik at det opprettes overføringsordrer for å fordele forsyning og behov på tvers av lokasjoner.  

I tillegg til slike automatiske overføringsorder kan det av og til være behov for å foreta en generell flytting av lagerantall til en annen lokasjon, uansett eksisterende behov. Da kan du manuelt opprette en overføringsordre for antallet som skal flyttes. Du må angi Ingen som verdi for **Planleggingsfleksibilitet** på overføringslinjen(e) for å sikre at planleggingssystemet ikke prøver å manipulere denne manuelle overføringsordren.  

Hvis du derimot vil at planleggingssystemet skal justere overføringsordreantallene og datoene til eksisterende behov, må du angi standardverdien Ubegrenset i feltet **Planleggingsfleksibilitet**.

## <a name="planning-parameters"></a>Planleggingsparametere

Planleggingsparameterne kontrollerer når, hvor mye og hvordan etterfylling skal skje, basert på de ulike innstillingene på varekortet (eller lagerføringsenhet - LFE) og produksjonsoppsettet.  

Følgende planleggingsparametre finnes på vare- eller LFE-kortet:  

- Avdempingsperiode  
- Avdempingsantall  
- Gjenbestillingsprinsipp  
- Gjenbestillingspunkt
- Maks. beholdning  
- Overflytnivå  
- Tidsperiode  
- Akkumuleringsperiode for parti  
- Periode for ny planlegging  
- Gjenbestillingsantall  
- Sikkerhetsleveringstid  
- Sikkerhetslagerantall  
- Monteringsprinsipp  
- Produksjonsprinsipp  

Følgende ordremodifikatorer finnes på vare- eller LFE-kortet:  

- Min. bestillingsantall  
- Maks. bestillingsantall  
- Bestillingsfaktor  

Oppsettsfeltene for global planlegging på **Produksjonsoppsett**-siden omfatter følgende:  

- Dynamisk lavnivåkode  
- Gjeldende behovsprognose  
- Bruk prognose på lokasjoner  
- Standard sikkerhetstid  
- Tomt overflytnivå  
- Kombinert MPS/MRP-beregning
- Komponenter ved lokasjon  
- Standard avdempingsperiode  
- Standard avdempingsantall  

Hvis du vil ha mer informasjon, kan du se [Designdetaljer: planleggingsparametere](design-details-planning-parameters.md)  

## <a name="other-important-planning-fields"></a>Andre viktige felt for planlegging

### <a name="planning-flexibility"></a>Planleggingsfleksibilitet

I de fleste forsyningsordrer, for eksempel produksjonsordrer, kan du velge **Ubegrenset** eller **Ingen** i vinduet **Planleggingsfleksibilitet** på linjene.

Dette angir om forsyningen som representeres av produksjonsordrelinjen, vurderes av planleggingssystemet ved beregning av handlingsmeldinger.
Hvis feltet inneholder **Ubegrenset**, tar planleggingssystemet med linjen når handlingsmeldinger beregnes. Hvis feltet inneholder **Ingen**, er linjen fast og uforanderlig, og planleggingssystemet tar den ikke med når handlingsmeldinger beregnes.

### <a name="warning"></a>Advarsel

Informasjonsfeltet **Advarsel** på siden **Planleggingsforslag** informerer deg om eventuelle planleggingslinjer som er opprettet for en uvanlig situasjon med en tekst som brukeren kan velge å få mer informasjon. Følgende typer advarsler finnes:

- Kritisk
- Unntak
- Viktig
- Kritisk

Kritisk-advarselen vises i to situasjoner:

- Beholdningen er negativ på den planlagte startdatoen.
- Det finnes tilbakedatert forsyning eller behov.

Hvis beholdningen for en vare er negativ på den planlagte startdatoen, foreslår planleggingssystemet at det opprettes en kritisk ordre for det negative antallet, med ankomst på den planlagte startdatoen. Advarselsteksten angir startdatoen og antallet på den kritiske ordren.

Dokumentlinjer med forfallsdato før den planlagte startdatoen konsolideres til én kritisk ordre for varen, med ankomst på den planlagte startdatoen.

### <a name="exception"></a>Unntak

Unntak-advarselen vises hvis den beregnede disponible beholdningen faller under sikkerhetslagerantallet.

Planleggingssystemet foreslår at det opprettes en forsyningsordre for å oppfylle behovet på forfallsdatoen. Advarselsteksten angir varens sikkerhetslagerantall og datoen da antallet ble for lavt.

Et for lavt sikkerhetslagernivå anses for å være et unntak fordi det ikke skal forekomme hvis gjenbestillingspunktet er riktig angitt.

> [!NOTE]
> Forsyning på planleggingslinjer med unntaksadvarsler endres vanligvis ikke i henhold til planleggingsparametere. I stedet foreslår planleggingssystemet bare en forsyning for å dekke den nøyaktige behovsmengden. Du kan imidlertid angi planleggingskjøringen for å respektere visse planleggingsparametre for planleggingslinjer med bestemte advarsler. Hvis du vil ha mer informasjon, kan du se beskrivelsen for feltet **Respekter planleggingsparametre for unntaksadvarsler** i artikkelen [Kjøre full planlegging, MPS eller MRP](production-how-to-run-mps-and-mrp.md).

### <a name="attention"></a>Viktig

Tilsyn-advarselen vises i to situasjoner:

- Den planlagte startdatoen er tidligere enn arbeidsdatoen.
- Planleggingslinjen foreslår at en frigitt bestilling eller produksjonsordre endres.

> [!NOTE]
> På planleggingslinjer med advarsler er ikke feltet **Godta handlingsmelding** valgt, fordi planleggeren må undersøke disse linjene ytterligere før planen utføres.

## <a name="planning-worksheets-and-requisition-worksheets"></a>Planleggingsforslag og bestillingsforslag

Som beskrevet i [Planlegging](production-planning.md) kan du velge mellom to forslag for de fleste planleggingsaktivitetene, planleggingsforslaget og bestillingsforslaget. De fleste prosesser er beskrevet basert på planleggingsforslaget, men det finnes et par scenarier der bestillingsforslaget foretrekkes.

### <a name="requisition-worksheet"></a>Bestillingsforslag

Siden **Bestillingsforslag** viser varer du vil bestille. Du kan angi varer i forslaget på følgende måter:

- Angi varene manuelt i bestillingsforslaget, og fyll ut i de aktuelle feltene.

- Bruk kjørselen **Beregn plan**. Den beregner en etterfyllingsplan for varer og lagerføringsenheter som er satt opp med et etterfyllingssystem for **Kjøp** eller **Overføring**. Når du bruker denne kjørselen, fyller programmet automatisk ut feltet **Handlingsmelding** med et forslag til handling for etterfylling av varen. Det kan for eksempel være å øke vareantallet i en eksisterende ordre, eller opprette en ny ordre.

- Hvis du har brukt kjørselen **Beregn plan** på **Planleggingsforslag**-siden til å beregne en etterfyllingsplan, kan du bruke kjørselen **Utfør handlingsmelding** til å kopiere kjøps- og overføringsordreforslag fra planleggingsforslaget til bestillingsforslaget. Dette er nyttig hvis forskjellige brukere har ansvaret for håndtering av produksjonsordrer og kjøps-/overføringsordrer.

- Du kan bruke handlingen **Direkte levering** for å fylle ut bestillingsforslagslinjene. Denne handlingen bruker kjørselen **Hent ordrer** til å finne ordrelinjene du vil angi for en direkte levering.

- Du kan bruke handlingen **Spesialbestilling** for å fylle ut bestillingsforslagslinjene. Denne handlingen bruker kjørselen **Hent ordrer** til å finne ordrelinjene du vil angi for en spesialbestilling.

Bestillingsforslagslinjene inneholder detaljert informasjon om varene som må bestilles. Du kan redigere eller slette linjene for å endre etterfyllingsplanen, og du kan viderebehandle linjene med kjørselen **Utfør handlingsmelding**.

Hvis du vil ha detaljer om planlegging med lokasjoner og overføringer, se [Planlegge med/uten lokasjoner](production-planning-with-without-locations.md).

## <a name="see-also"></a>Se også

[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  
[Planlegging](production-planning.md)  
[Definere produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Lager](inventory-manage-inventory.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
