---
title: Opprette varekort for varer eller tjenester (inneholder video)
description: Du oppretter varekort for tjenester som du selger som timer og for fysiske produkter. Eksempler er monteringsvarer og ferdige varer som du selger fra lageret.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 09/26/2022
ms.author: edupont
---
# Registrere nye varer

Varer, blant andre produkter, er grunnlaget for virksomheten din, varene eller tjenestene du handler med. Hver vare må være registrert som et varekort.

Varekort inneholder informasjonen som er nødvendig for å kjøpe, lagre, selge, levere og gjøre rede for varer.

Varekortet kan være av typen **Lager**, **Service** eller **Ikke-lagervarer** for å angi om varen er en fysisk lagerenhet, en arbeidstidsenhet eller en fysisk enhet som ikke spores i lagerbeholdningen. Hvis du vil ha mer informasjon, kan du se [Om varetyper](inventory-about-item-types.md).

En vare kan struktureres som en overordnet vare med underliggende underordnede varer i en stykkliste. Finn ut mer om monteringsstykklister og produksjonsstykklister i [Arbeid med stykklister](inventory-how-work-BOMs.md).

Hvis du kjøper den samme varen fra flere leverandører, kan du knytte disse leverandørene til varekortet. Leverandørene vises deretter på siden **Vare/leverandør-katalog**, slik at du enkelt kan velge en annen leverandør.

*Katalogvarer* er varer som du tilbyr kunder, men som du ikke vil administrere i systemet før du begynner å selge dem. Katalogvarer er ikke vanlige varer av typen **Ikke-lagervarer**. Finn ut mer under [Arbeid med katalogvarer](inventory-how-work-nonstock-items.md).  

> [!NOTE]  
> Hvis det finnes varemaler for ulike varetyper, vises en siden når du oppretter et nytt kundekort der du kan velge en passende mal. Hvis det bare finnes én varemal, brukes alltid denne malen i nye varekort.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et varekort fra grunnen av. Du kan også opprette nye varekort ved å kopiere eksisterende varekort. Hvis du vil ha mer informasjon, se [Kopiere eksisterende varer for å opprette nye varer](inventory-how-copy-items.md).  

<br />

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

## Opprette et nytt varekort

[!INCLUDE[create_new_item](includes/create_new_item.md)]

> [!NOTE]
> I feltet **Lagermetode** kan du definere hvordan varens enhetskost beregnes, ved å lage prognoser over vareflyten i selskapet. Fem lagermetoder er tilgjengelige, avhengig av varetypen. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostmetoder](design-details-costing-methods.md).
>
> Hvis du velger **Gjennomsnitt**, blir enhetskosten for en vare beregnet som den gjennomsnittlige enhetskosten på hvert tidspunkt etter et kjøp. Lageret verdisettes basert på antakelsen om at alle beholdninger selges samtidig. Med denne innstillingen kan feltet **Enhetskost** for å vise en historikk over transaksjoner som gjennomsnittskosten beregnes fra, på siden **Oversikt over beregning av gjennomsnittskost**.

Du kan vise eller redigere spesialpriser eller rabatter som du gir, eller som leverandøren gir deg, for varen hvis bestemte kriterier oppfylles, for eksempel kunde, minimumsordreantall eller sluttdato. Dette gjør du ved å velge handlingene **Definer spesialpriser** eller **Definer spesialrabatter**. For eksempel vil hver rad på siden **Salgspriser** representere en spesialpris. Hver kolonne representerer et kriterium som må gjelde for å gi en kunde den spesialprisen du angir i feltet **Enhetspris** på siden **Salgspriser**. Hvis du vil ha mer informasjon, kan du se [Registrere avtaler om salgspris, rabatt og betaling](sales-how-record-sales-price-discount-payment-agreements.md) eller [Registrere spesielle kjøpspriser og rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

Varen er nå registrert, og varekortet er klart til å brukes på kjøps- og salgsdokumenter.

Hvis du vil bruke dette varekortet som en mal når du oppretter nye varekort, kan du lagre det som en mal. Hvis du vil ha mer informasjon, kan du se følgende avsnitt:  

### Lagre varekortet som en mal

1. På siden **Varekort** velger du handlingen **Lagre som mal**. **Varemal**-siden åpnes og viser varekortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner i maler, velger du handlingen **Dimensjoner**. **Dimensjonsmaler**-siden åpnes med alle dimensjonskoder som er definert for varen.
4. Rediger eller angi dimensjonskoder som skal gjelde for nye varekort som opprettes ved hjelp av malen.
5. Når du har fullført den nye varemalen, kan du velge **OK**-knappen.

Varemalen legges til i listen over varemaler, slik at du kan bruke den til å opprette nye varekort.

### Varer som brukes i produksjonsordrer

Hvis du vil registrere varer som brukes i produksjonsordrer, angir du etterfyllingssystemet som *Prod. ordre* i hurtigfanen **Etterfylling**. Hvis du vil ha mer informasjon, kan du se [Om produksjonsordrer](production-about-production-orders.md).  

## Slik definerer du flere leverandører for varer

Hvis du kjøper den samme varen fra flere leverandører, må du angi opplysninger om hver enkelt leverandør av varen, for eksempel priser, leveringstid, rabatter og så videre.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Velg den aktuelle varen, og velg deretter handlingen **Rediger**.  
3. Velg handlingen **Leverandører**.  
4. Velg feltet **Leverandørnr.**, og velg leverandøren du vil definere for varen.  
5. Fyll eventuelt ut de gjenværende feltene.  
6. Gjenta trinn 2 til 5 for hver leverandør som du vil kjøpe varen fra.

Leverandørene vises nå på siden **Vare/leverandør-katalog**, som du åpner fra varekortet, slik at du enkelt kan velge en annen leverandør.

## Konfigurer vareerstatninger

Du kan konfigurere varer slik at de får erstatninger, for eksempel andre varer som kan brukes i stedet for den opprinnelige varen.

### Slik lager du en vareerstatning

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Finn den aktuelle varen, og velg deretter **Varenr.** for å åpne varekortet.  
3. Velg **Relatert**-handlingen, velg **Vare**, og velg deretter **Erstatninger** for å åpne siden **Vareerstatningspost**.  
4. Velg feltet **Erstatningsnr.** og velg deretter erstatningsvaren fra listen.
5. Fyll ut eller endre andre felter på siden etter behov.

Hvis det forespurte antallet overskrider det disponible antallet på lageret, blir det vist en melding for å informere deg om at erstatningsvarer finnes.

> [!NOTE]  
> Vær oppmerksom på at vareerstatninger ikke automatisk fører til at en vare erstattes av en annen vare, for eksempel når du oppretter en ordre eller i en stykkliste. I stedet blir du varslet om at en erstatning er tilgjengelig for deg.

## Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Finn ut mer om varianter under [Administrer av produktvarianter](inventory-item-variants.md).  

## Slette varekort

Hvis du har bokført en transaksjon for en vare, kan du ikke slette kortet, fordi postene kan være nødvendige for å lagervurdering eller -revisjon. Hvis du vil slette varekort med poster, kontakter du Microsoft-partneren for å gjøre det gjennom kode.  

## Håndtere lager på lagre

Når du registrerer en ny vare, vil du se felter som er knyttet til lagerstyring, spesielt på hurtigfanen **Lager**. Hvis organisasjonen ikke bruker lagerstyringsmulighetene i [!INCLUDE [prod_short](includes/prod_short.md)], kan du ignorere disse feltene.  

Hvis organisasjonen senere setter opp lagerstyring, anbefales det at du sørger for at alle eksisterende varer har de riktige opplysningene i de ulike feltene. På denne måten kan lagerprosessene kjøres som forventet. Informasjonen kan omfatte felt som **Lagerklassekode** eller **Plasseringsmalkode**. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

## Planl.

Når selskapet bruker forsyningsplanleggingsprosessene i [!INCLUDE [prod_short](includes/prod_short.md)], må du fylle ut de aktuelle feltene på hurtigfanen **Planlegging**. Se [Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) for å få en innføring i planleggingsområdet.  

Hvis du vil ha eksempler på hvordan du kan bruke feltene på hurtigfanen **Planlegging**, kan du se [Anbefalte fremgangsmåter for oppsett: Planleggingsparametere](setup-best-practices-planning-parameters.md).  

## Se relatert [Microsoft-opplæring](/training/modules/create-items/)

## Se også

[Lager](inventory-manage-inventory.md)  
[Definere enheter](inventory-how-setup-units-of-measure.md)  
[Behandle produktvarianter](inventory-item-variants.md)  
[Definer Intrastat-rapportering](finance-how-setup-report-intrastat.md#other-intrastat-configurations)  
[Avstem lagerkost med finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md)  
[Opprette nummerserier](ui-create-number-series.md)  
[Definere bokføringsgrupper](finance-posting-groups.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Om planleggingsfunksjonalitet](production-about-planning-functionality.md)  
[Anbefalte fremgangsmåter for oppsett: Planleggingsparametere](setup-best-practices-planning-parameters.md)  
[Anbefalte fremgangsmåter for oppsett: Forsyningsplanlegging](setup-best-practices-supply-planning.md)  
[Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)  
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)  
[Designdetaljer: Planleggingsparametere](design-details-planning-parameters.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
