---
title: Designdetaljer – Behov og forsyning | Microsoft-dokumentasjon
description: Dette emnet introduserer konseptet med behov, som er det vanlige uttrykket som brukes for alle typer bruttobehov, for eksempel en salgsordre og komponentbehov fra en produksjonsordre.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, demand, supply, inventory, planning
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: f808865bd4fc2113dd5c04071f7ba2e8793fe3af
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3185567"
---
# <a name="design-details-demand-at-blank-location"></a>Designdetaljer: Behov på tom lokasjon
Når en bruker oppretter en behovshendelse, for eksempel en salgsordrelinje, tillater programmet at brukeren noen ganger angir en lokasjonskode og andre ganger ikke, dvs. bruker en tom lokasjon.

Når det gjelder behov med eller uten lokasjonskoder, fungerer planleggingssystemet på en enkel måte når følgende er tilfelle:

- Behovslinjer har alltid lokasjonskoder, og systemet bruker LFEer fullt ut, inkludert det relevante lokasjonsoppsettet.
- Behovslinjer har aldri lokasjonskoder, og systemet bruker ikke LFEer eller lokasjonsoppsett (se siste scenario i delen nedenfor).

Hvis behovshendelser imidlertid noen ganger har lokasjonskoder og andre ganger ikke, følger planleggingssystemet visse regler avhengig av oppsettet.

## <a name="demand-at-location"></a>Behov i lokasjon
Når planleggingssystemet oppdager behov i en lokasjon, fungerer det på ulike måter avhengig av tre viktige oppsettverdier. Systemet søker etter tre oppsettsverdier etter tur under en planleggingskjøring, og planlegger i henhold til dem.

1. Er det merket av i feltet **Lokasjon obligatorisk**?

    Hvis ja:

2. Finnes det lagerføringsenhet for varen?

    Hvis ja:

    Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.

    Hvis nei:

3. Inneholder feltet Komponenter ved lokasjon den nødvendige lokasjonskoden?

  Hvis ja:

  Varen planlegges i henhold til planleggingsparametrene på varekortet.

  Hvis nei:

  Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti, Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom, varer som bruker Gjenbestillingsprinsipp = Ordre, fortsetter å bruke Ordre sammen med de andre innstillingene.

> [!NOTE]
> Oppsettet for unntaksplanlegging som avgis som siste reaksjon i trinn 3 ovenfor, kalles "minimumsalternativet" i det følgende. Dette planleggingsoppsettet dekker bare eksakt behov, og alle andre planleggingsparametere ignoreres.

Hvis du vil ha informasjon om variasjoner av planleggingslogikken, kan du se avsnittet nedenfor om scenarier.

## <a name="demand-at-blank-location"></a>Behov i tom lokasjon
Selv om det er merket av i feltet **Lokasjon obligatorisk**, tillater programmet at det opprettes behovslinjer uten en lokasjonskode, også kalt tom lokasjon. Dette er et systemavvik fordi ulike oppsettsverdier er rettet mot lokasjoner (se ovenfor), og planleggingsmotoren vil derfor ikke opprette en planleggingslinje for en slik behovslinje.

Hvis det ikke er merket av for feltet **Lokasjon obligatorisk**, men noen av verdiene for oppsett av lokasjon finnes, blir dette også betraktet som et avvik, og planleggingssystemet vil reagere med å bruke "minimumsalternativet": Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (ordre forblir ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametre = tomme.

## <a name="scenarios"></a>Scenarier
Følgende scenarier beskriver ulike behov på en tom lokasjon og hvordan planleggingssystemet løses til "minimumsalternativet".

### <a name="setup-1"></a>Oppsett 1:
Lokasjon obligatorisk = Ja

LFE er definert for RØD

Komponenter ved lokasjon = BLÅ

#### <a name="case-11-demand-is-at-red-location"></a>Eksempel 1.1: Behovet er i RØD lokasjon
Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.

#### <a name="case-12-demand-is-at-blue-location"></a>Eksempel 1.2: Behovet er i BLÅ lokasjon
Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.

#### <a name="case-13-demand-is-at-green-location"></a>Eksempel 1.3: Behovet er i GRØNN lokasjon
Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.

#### <a name="case-14-demand-is-at-blank-location"></a>Eksempel 1.4: Behovet er i TOM lokasjon
Varen planlegges ikke fordi ingen lokasjon er definert på behovslinjen.

### <a name="setup-2"></a>Oppsett 2:
Lokasjon obligatorisk = Ja

LFE finnes ikke

Komponenter ved lokasjon = BLÅ

#### <a name="case-21-demand-is-at-red-location"></a>Eksempel 2.1: Behovet er i RØD lokasjon
Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.

#### <a name="case-22-demand-is-at-blue-location"></a>Eksempel 2.2: Behovet er i BLÅ lokasjon
Varen planlegges i henhold til planleggingsparametrene på varekortet.

### <a name="setup-3"></a>Oppsett 3:
Lokasjon obligatorisk = Nei

LFE finnes ikke

Komponenter ved lokasjon = BLÅ

#### <a name="case-31-demand-is-at-red-location"></a>Eksempel 3.1: Behovet er i RØD lokasjon
Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.

#### <a name="case-32-demand-is-at-blue-location"></a>Eksempel 3.2: Behovet er i BLÅ lokasjon
Varen planlegges i henhold til planleggingsparametrene på varekortet.

#### <a name="case-33-demand-is-at-blank-location"></a>Eksempel 3.3: Behovet er i TOM lokasjon
Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.

### <a name="setup-4"></a>Oppsett 4:
Lokasjon obligatorisk = Nei

LFE finnes ikke

Komponenter ved lokasjon = TOM

#### <a name="case-41-demand-is-at-blue-location"></a>Eksempel 4.1: Behovet er i BLÅ lokasjon
Varen planlegges slik: Gjenbestillingsprinsipp = Parti for parti (Ordre forblir Ordre), Ta med lagerbeholdning = Ja, alle andre planleggingsparametere = Tom.

#### <a name="case-42-demand-is-at-blank-location"></a>Eksempel 4.2: Behovet er i TOM lokasjon
Varen planlegges i henhold til planleggingsparametrene på varekortet.

Som illustrert i det siste scenariet kan du bare få et riktig resultat for en behovslinje uten lokasjonskode ved å deaktivere alle oppsettsverdier som gjelder lokasjoner. Likeledes kan du bare få stabile planleggingsresultater for behov i lokasjoner ved å bruke LFEer. Hvis selskap ofte planlegger for behov i lokasjoner, anbefales de på det sterkeste å bruke granulen Lagerføringsenheter.

## <a name="see-also"></a>Se også  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)   
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)   
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)
