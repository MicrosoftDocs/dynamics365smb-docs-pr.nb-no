---
title: Opprette varekort for varer eller tjenester
description: Du oppretter varekort for tjenester som du selger som timer og for fysiske produkter. Eksempler er monteringsvarer og ferdige varer som du selger fra lageret.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'item, finished good, component, raw material, assembly item, item substitution'
ms.search.form: '30, 5717, 31, 32, 346, 9091, 5718, 5716, 5720, 1384, 1383, 35, 5404, 1378, 5719'
ms.date: 08/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Registrer nye varer

Varer, blant andre produkter, er grunnlaget for virksomheten din, varene eller tjenestene du handler med. Hver vare må være registrert som et varekort.

## Opprette et nytt varekort

Videoen nedenfor viser hvordan du setter opp en vare på Varekort-siden. Du kan imidlertid også sette opp nye varer ved å kopiere eksisterende varer. Hvis du vil ha mer informasjon, kan du gå til [Kopier eksisterende varer for å opprette nye varer](inventory-how-copy-items.md).  

> [!Video https://www.microsoft.com/videoplayer/embed/RE47eLx?rel=0]

[!INCLUDE[create_new_item](includes/create_new_item.md)]

## Bruk varemaler

Hvis du vil bruke innstillinger på nytt for ulike typer varer når du oppretter nye varer, kan du lagre varer som varemaler. Med elementmaler kan du få fart på prosessen med å legge til nye varer og øke konsekvensen i varedataene. Når du registrerer en ny vare, vises en side der du kan velge en mal. Når du har valgt en mal, fylles innstillingene ut for deg for varen du oppretter. Hvis du bare har én varemal, bruker nye varer alltid denne malen. 

### Lagre et varekort som en varemal

1. På siden **Varekort** velger du handlingen **Lagre som mal**. **Varemal**-siden viser varekortet som en mal.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis du vil bruke dimensjoner på nytt i maler, velger du handlingen Relatert **, deretter Vare**  **og deretter** Dimensjoner. **·**  **Standarddimensjoner** for den valgte varen er åpne og viser eventuelle dimensjonskoder som er definert for varen.
4. Rediger eller angi dimensjonskoder som skal gjelde nye varekort som opprettes ved hjelp av malen.
5. Når du fullfører den nye varemalen, kan du velge **OK**-knappen.

Varemalen legges til i listen over varemaler, slik at du kan bruke den til å opprette nye varekort.

## Typer av varer

I **Type**-feltet på **Varekort**-siden kan du velge hva varen brukes til i virksomheten din, som påvirker i hvilken grad du kan administrere varen på lageret.

* **Beholdning** angir at varen er en fysisk enhet som du administrerer og sporer på lageret.
* **Ikke-beholdning** er fysiske enheter som du ikke administrerer eller sporer på lager.
* **Servicevarer** er en arbeidstidsenhet som vanligvis brukes til å registrere, selge eller kjøpe tjenester.

Hvis du vil lære mer om disse typene varer, går du til [Om varetyper](inventory-about-item-types.md).

> [!TIP]
> Det finnes også katalogvarer, som ligner på ikke-lagervarer ved at de er varer du tilbyr til kunder, men ikke administrerer før du selger dem. Hvis du vil ha mer informasjon, kan du gå til [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).  

## Beholdning og kostberegning

I feltet **Lagermetode** kan du definere hvordan varens enhetskost beregnes, ved å lage prognoser over vareflyten i selskapet. Fem lagermetoder er tilgjengelige, avhengig av varetypen. Hvis du vil lære mer om kostberegning, kan du gå til [Designdetaljer: Kostmetoder](design-details-costing-methods.md).

> [!NOTE]
> Hvis du velger **Gjennomsnitt**, blir enhetskosten for en vare beregnet som den gjennomsnittlige enhetskosten på hvert tidspunkt etter et kjøp. Lageret verdisettes basert på antakelsen om at alle beholdninger selges samtidig. Med denne innstillingen kan du velge feltet **Enhetskost** på siden **Oversikt over beregning av gjennomsnittskost** for å vise transaksjonene som ble brukt til å beregne gjennomsnittskost.

## Kategorier, attributter og varianter

[!INCLUDE[inventory_variant](includes/inventory_variant.md)]

Finn ut mer om varianter under [Administrer av produktvarianter](inventory-item-variants.md).  

## Konfigurer vareerstatninger

Du kan konfigurere varer slik at de får erstatninger, for eksempel andre varer som kan brukes i stedet for den opprinnelige varen.

### Slik lager du en vareerstatning

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Finn den aktuelle varen, og velg **deretter Nei.** For å åpne Vare-kort.  
3. Velg **Relatert**-handlingen, velg **Vare**, og velg deretter **Erstatninger** for å åpne siden **Vareerstatningspost**.  
4. Velg feltet **Erstatningsnr.** og velg deretter erstatningsvaren fra listen.
5. Fyll ut eller endre andre felter på siden etter behov.

Når det forespurte antallet overskrider antallet som er tilgjengelig på lageret, vises en melding med informasjon om at det finnes erstatningsvarer.

> [!NOTE]  
> Vær oppmerksom på at vareerstatninger ikke automatisk fører til at en vare erstattes av en annen vare, for eksempel når du oppretter en ordre eller i en stykkliste. I stedet blir du varslet om at en erstatning er tilgjengelig for deg.

## Priser og rabatter

Du kan bruke spesialpriser eller rabatter du gir for varen, basert på bestemte kriterier. Kriterier inkluderer for eksempel kunden, minste bestillingsantall eller sluttdato. Du kan sette opp spesialpriser ved å velge handlingene **Definer spesialpriser** eller **Definer spesialrabatter**. For eksempel vil hver rad på siden **Salgspriser** representere en spesialpris. Hver kolonne representerer et kriterium som må gjelde for å gi en kunde den spesialprisen du angir i feltet **Enhetspris** på siden **Salgspriser**. Hvis du vil lære mer om priser, kan du gå til [Registrere salgspris, rabatt og betalingsavtaler](sales-how-record-sales-price-discount-payment-agreements.md).

## Etterfylling

Du kan angi hvordan varer skal leveres:

* **Bestilling** hvis du vil kjøpe varer.
* **Monteringsordre** eller **produksjonsordre** hvis du produserer varene internt.

Der er andre innstillinger som komplimenterer disse valgene.

### Inkluder varer i stykklister

Du kan strukturere hierarkier som har en hovedvare med underliggende komponentvarer i monterings- og produksjonsstykklister. Hvis du vil ha mer informasjon om stykklister, går du til [Arbeid med stykklister](inventory-how-work-BOMs.md).

### Varer som brukes i produksjonsordrer

Hvis du vil registrere varer du bruker i produksjonsordrer, angir du etterfyllingssystemet som **Prod.ordre** på **hurtigfanen Etterfylling** . Hvis du vil ha mer informasjon, kan du se [Om produksjonsordrer](production-about-production-orders.md).  

### Primære og alternative leverandører

Hvis du kjøper den samme varen fra flere leverandører, kan du knytte disse leverandørene til varen. Bruk handlingen **Leverandører** på **Varekort**-siden til å åpne siden **Vareleverandørkatalog**. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Varer** og velg den relaterte koblingen.  
2. Velg den aktuelle varen, og velg deretter handlingen **Rediger**.  
3. Velg handlingen **Leverandører**.  
4. Velg Nei **.** -feltet, og Velg deretter leverandøren du vil definere for varen.  
5. Fyll eventuelt ut de gjenværende feltene.  
6. Gjenta trinn 2 til 5 for hver leverandør som du vil kjøpe varen fra.

Leverandørene vises på siden **Vare/leverandør-katalog**, som du åpner fra varekortet, slik at du enkelt kan velge en annen leverandør.

Hvis du kjøper den samme varen fra flere leverandører, kan du i tillegg definere rabatter på priser og rabatter.  Hvis du vil ha mer informasjon, kan du se [Registrere spesielle kjøpspriser og -rabatter](purchasing-how-record-purchase-price-discount-payment-agreements.md).

## Håndtere lager på lagre

Når du registrerer en ny vare, ser du felter som er knyttet til lagerstyring, spesielt på hurtigfanen **Lager**. Hvis organisasjonen ikke bruker lagerstyringsmulighetene i [!INCLUDE [prod_short](includes/prod_short.md)], kan du ignorere disse feltene.  

Hvis organisasjonen senere setter opp lagerstyring, anbefales det at du sørger for at alle eksisterende varer har de riktige opplysningene i de ulike feltene. På denne måten kan lagerprosessene kjøres som forventet. Informasjonen kan omfatte felt som **Lagerklassekode** eller **Plasseringsmalkode**. Du finner mer informasjon under [Definere lagerstyring](warehouse-setup-warehouse.md).  

## Planl.

Når selskapet bruker forsyningsplanleggingsprosessene i [!INCLUDE [prod_short](includes/prod_short.md)], må du fylle ut de aktuelle feltene på hurtigfanen **Planlegging**. Se [Designdetaljer: Sentrale begreper for planleggingssystemet](design-details-central-concepts-of-the-planning-system.md) for å få en innføring i planleggingsområdet.  

Hvis du vil ha eksempler på hvordan du kan bruke feltene på hurtigfanen **Planlegging**, kan du se [Anbefalte fremgangsmåter for oppsett: Planleggingsparametere](setup-best-practices-planning-parameters.md).  

## Slett varekort

Hvis du bokfører en transaksjon for en vare, kan du ikke slette kortet, fordi postene kan være nødvendige for å lagervurdering eller -revisjon. Hvis du vil slette varekort med poster, kontakter du Microsoft-partneren for å gjøre det gjennom kode.  

## Se også

[Lager](inventory-manage-inventory.md)    
[Definere enheter](inventory-how-setup-units-of-measure.md)    
[Administrer produktvarianter](inventory-item-variants.md)    
[Definere Intrastat-rapportering](finance-how-setup-report-intrastat.md#other-intrastat-configurations)    
[Avstemme lagerkost mot Finans](finance-how-to-post-inventory-costs-to-the-general-ledger.md)    
[Opprett nummerserie](ui-create-number-series.md)    
[Definere bokføringsgrupper](finance-posting-groups.md)    
[Innkjøp](purchasing-manage-purchasing.md)    
[Salg](sales-manage-sales.md)    
[Om planleggingsfunksjonalitet](production-about-planning-functionality.md)    
[Anbefalte fremgangsmåter for oppsett: planleggingsparametere](setup-best-practices-planning-parameters.md)    
[Anbefalte fremgangsmåter for oppsett: forsyningsplanlegging](setup-best-practices-supply-planning.md)    
[Utformingsdetaljer: Sentrale begreper i planleggingssystemet](design-details-central-concepts-of-the-planning-system.md)    
[Designdetaljer: Balansere behov og forsyning](design-details-balancing-demand-and-supply.md)    
[Utformingsdetaljer: planleggingsparametere](design-details-planning-parameters.md)    
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)    


[!INCLUDE[footer-include](includes/footer-banner.md)]
