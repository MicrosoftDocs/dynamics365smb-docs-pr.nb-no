---
title: Se Planlegge med/uten lokasjoner.
description: 'I dette emnet lærer du om produksjon, inkludert forsyningsplanlegging, i Business Central.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/15/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="planning-with-or-without-locations"></a>Se Planlegge med/uten lokasjoner.

Før du begynner å bruke planleggingsmotoren, anbefales det at du avgjør om du vil bruke lokasjoner. Det finnes to hovedmåter på en enkel måte:

* behovslinjene alltid inneholder lokasjonskoder og systemet fullt ut bruker lagerføringsenheter, inkludert det relevante lokasjonsoppsettet. Finn ut mer på [Behov i lokasjon](#demand-at-location).  
* Behovslinjer inneholder aldri lokasjonskoder og systemet bruker varekortet. Se scenarioet [Behov ved en tom lokasjon](#demand-at-blank-location) nedenfor.

## <a name="demand-at-location"></a>Behov i lokasjon

Når planleggingssystemet oppdager behov i en lokasjon (en linje med en lokasjonskode), fungerer det på ulike måter avhengig av 2 viktige oppsettsverdier.  

Under en kjørsel kontrolleres de 2 oppsettsverdiene etter tur, og planleggingen utføres i tråd med dette:  

1. Finnes det en SKU for varen i den forespurte lokasjonen?  

    Hvis ja:  

    Varen planlegges i henhold til planleggingsparametrene på LFE-kortet.  

    Hvis nei:  

2. Inneholder feltet **Komponenter ved lokasjon** på siden **Produksjonsoppsett** den nødvendige lokasjonskoden?  

    Hvis ja:  

    Varen planlegges i henhold til planleggingsparameterne på varekortet.  

    Hvis nei:  

    Varen planlegges i henhold til minimumsalternativet som dekker det nøyaktige behovet. Planleggingsparameterne er angitt slik: Gjenbestillingsprinsipp = *Parti for parti*, Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme. (Varer som bruker gjenbestillingsprinsippet *Ordre*, fortsetter med å bruke *Ordre* samt de andre innstillingene.)

> [!TIP]
> Hvis du ofte planlegger for behov i ulike lokasjoner, anbefaler vi at du bruker funksjonen for lagerføringsenheter og unngår behov i tom lokasjon. Finn ut mer under [Definer lagerføringsenheter](inventory-how-to-set-up-stockkeeping-units.md)

Se variasjoner i [scenarioene nedenfor](#scenarios).

> [!NOTE]
> Feltet **Komponenter ved lokasjon** på siden **Produksjonsoppsett** er svært viktige når du skal styre hvordan planleggingssystemet håndterer produksjonsbehovlinjer.
>
> For produksjonsbehov bruker [!INCLUDE [prod_short](includes/prod_short.md)] samme lokasjon for delmontering og komponenter som den som er angitt i produksjonsordren. Hvis du fyller ut dette feltet, kan du imidlertid omdirigere delmontering og komponentene til en annen lokasjon.
>
> Du kan også definere dette for en bestemt LFE ved å velge en annen lokasjonskode i feltet **Komponenter ved lokasjon** på LFE-kortet. Vær imidlertid oppmerksom på at dette sjelden gir mening ettersom planleggingslogikken kan bli fordreid når du planlegger for LFE-komponenten.

## <a name="demand-at-blank-location"></a>Behov i tom lokasjon

Når planleggingssystemet oppdager behov i en tom lokasjon (en linje uten lokasjonskode), planlegges varen vanligvis i henhold til planleggingsparameterne på varekortet.

Feltet **Lokasjon obligatorisk** på siden **Lageroppsett** og feltet **Komponenter ved lokasjon** på siden **Produksjonsoppsett** eller lagerføringsenheter som påvirker hvordan planleggingssystemet håndterer behovslinjer med/uten lokasjonskoder. Hvis en av følgende setninger er sanne, er behovet i tom lokasjon også betraktet som et avvik, og planleggingssystemet vil reagere ved å bruke minimumsalternativet: Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* (*ordre* forblir *ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

* Feltet **Komponenter ved lokasjon** på siden **Produksjonsoppsett** har en verdi.
* En lagerføringsenhet finnes for den planlagte varen.
* Feltet **Lokasjon obligatorisk** er valgt.

## <a name="scenarios"></a>Scenarier

Se variasjoner i oppsettsscenariene nedenfor.

### <a name="setup-1"></a>Oppsett 1

* Lokasjon obligatorisk = *Ja*  
* SKU defineres for *VEST*  
* Komponenter ved lokasjon = *ØST*  

#### <a name="case-11-demand-is-at-west-location"></a>Eksempel 1.1: Behovet er i *VEST* lokasjon

Varen planlegges i henhold til planleggingsparametrene på LFE-kortet (inkludert mulig overføring).

#### <a name="case-12-demand-is-at-east-location"></a>Eksempel 1.2: Behovet er i *ØST* lokasjon

Varen planlegges i henhold til planleggingsparameterne på varekortet.

#### <a name="case-13-demand-is-at-main-location"></a>Eksempel 1.3: Behovet er i *HOVED*-lokasjon

Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* ( *Ordre* forblir *Ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

#### <a name="case-14-demand-is-at-blank-location"></a>Eksempel 1.4: Behovet er i *TOM* lokasjon

Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* ( *Ordre* forblir *Ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

### <a name="setup-2"></a>Oppsett 2

* Lokasjon obligatorisk = *Ja*  
* LFE finnes ikke  
* Komponenter ved lokasjon = *ØST*  

#### <a name="case-21-demand-is-at-west-location"></a>Eksempel 2.1: Behovet er i *VEST* lokasjon

Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* ( *Ordre* forblir *Ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

#### <a name="case-22-demand-is-at-east-location"></a>Eksempel 2.2: Behovet er i *ØST* lokasjon

Varen planlegges i henhold til planleggingsparameterne på varekortet.  

### <a name="setup-3"></a>Oppsett 3

* Lokasjon obligatorisk = *Nei*  
* LFE finnes ikke  
* Komponenter ved lokasjon = *ØST*  

#### <a name="case-31-demand-is-at-west-location"></a>Eksempel 3.1: Behovet er i *VEST* lokasjon

Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* ( *Ordre* forblir *Ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

#### <a name="case-32-demand-is-at-east-location"></a>Eksempel 3.2: Behovet er i *ØST* lokasjon

Varen planlegges i henhold til planleggingsparameterne på varekortet.  

#### <a name="case-33-demand-is-at-blank-location"></a>Eksempel 3.3: Behovet er i *TOM* lokasjon

Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* ( *Ordre* forblir *Ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

### <a name="setup-4"></a>Oppsett 4

* Lokasjon obligatorisk = *Nei*  
* LFE finnes ikke  
* Komponenter ved lokasjon = *TOM*  

#### <a name="case-41-demand-is-at-east-location"></a>Eksempel 4.1: Behovet er i *ØST* lokasjon

Varen planlegges slik: Gjenbestillingsprinsipp = *Parti for parti* ( *Ordre* forblir *Ordre*), Ta med lagerbeholdning = *Ja*, alle andre planleggingsparametere = tomme.

#### <a name="case-42-demand-is-at-blank-location"></a>Eksempel 4.2: Behovet er i *TOM* lokasjon

Varen planlegges i henhold til planleggingsparameterne på varekortet.

Som du ser i det siste scenariet, kan du bare få et riktig resultat for en behovslinje uten lokasjonskode ved å deaktivere alle oppsettsverdier som gjelder lokasjoner. På samme måte kan du bare få stabile planleggingsresultater for behov i lokasjoner ved å bruke lagerføringsenheter.  

Hvis du ofte planlegger for behov ved lokasjoner, anbefaler vi derfor at du bruker funksjonen Lagerføringsenheter.

## <a name="see-also"></a>Se også

[Planlegging](production-planning.md)  
[Konfigurer produksjon](production-configure-production-processes.md)  
[Produksjon](production-manage-manufacturing.md)  
[Lager](inventory-manage-inventory.md)  
[Definere lagerføringsenheter](inventory-how-to-set-up-stockkeeping-units.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Designdetaljer: Forsyningsplanlegging](design-details-supply-planning.md)  
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
