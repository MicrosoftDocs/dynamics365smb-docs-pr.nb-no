---
title: Justere kostnadene for varer manuelt
description: 'Du kan justere lagerverdien for en vare med lagermetoden FIFO eller Gjennomsnitt, når kostnadene på produkter endres.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: 'cost adjustment, cost forwarding, costing method, inventory valuation, costing'
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Juster varekost

Kostnaden for en vare (lagerverdien) som du kjøper og senere selger, kan endres i løpet av levetiden, for eksempel fordi en fraktkostnader er lagt til innkjøpskostnaden etter at du har solgt varen. Kostjustering er spesielt relevant i situasjoner der du selger varer før du fakturerer kjøpet av varene. Hvis du alltid vil vite riktig lagerverdi, bør du justere varekostnader regelmessig. Korrekte kostnader sikrer at salgs- og fortjenestestatistikk er oppdatert og at økonomiske KPI-er er riktige. Hvis du vil ha mer informasjon, kan du se [Designdetaljer: Kostjustering](design-details-cost-adjustment.md).

Verdien i **Enhetskost**-feltet på varekortet er basert på standardkost for varer med lagermetoden Standard. For varer med andre lagermetoder er verdien basert på beregning av tilgjengelig lagerbeholdning (fakturerte kostnader og forventede kostnader) delt på aktuell beholdning. Du finner flere opplysninger i [Forstå beregning av enhetskost](inventory-how-adjust-item-costs.md#understanding-unit-cost-calculation).

I [!INCLUDE[prod_short](includes/prod_short.md)] justeres varekostnader automatisk hver gang det oppstår en lagertransaksjon, for eksempel når du bokfører en kjøpsfaktura for en vare.

Du kan også justere kostnadene for en eller flere varer manuelt. Manuelle justeringer er for eksempel nyttig når du vet at varekostnader er endret av andre grunner enn varetransaksjoner.

Varekost justeres med lagermetoden FIFO eller Gjennomsnitt, avhengig av hva du valgte i den assisterte oppsettsveiledningen **Konfigurere Mitt selskap** eller i feltet **Lagermetode** på varekortet. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).  

For FIFO-lagermetoden er enhetskosten for en vare den faktiske verdien for alle mottak av varen. Lageret verdisettes basert på antakelsen om at de første varene som plasseres på lager, selges først.

Hvis du bruker lagermetoden Gjennomsnitt, blir enhetskosten for en vare beregnet som den gjennomsnittlige enhetskosten på hvert tidspunkt etter et kjøp. Lageret verdisettes basert på antakelsen om at alle beholdninger selges samtidig. For varer som bruker denne lagermetoden, kan du velge feltet **Enhetskost** på varekortet for å vise en historikk over transaksjoner som gjennomsnittskosten beregnes fra

Kostnadsjustering behandler bare verdiposter som ikke er justert. I en situasjon der endrede inngående kostnader må videresendes til relaterte utgående poster, opprettes det nye justeringsverdiposter. Justeringsverdipostene er basert på informasjonen i de opprinnelige verdipostene, men inneholder justeringsbeløpet. Funksjonen for kostnadsjustering bruker bokføringsdatoen for den opprinnelige verdiposten i justeringsposten hvis denne datoen ikke er i en lukket lagerperiode. I så tilfelle bruker programmet startdatoen for den neste åpne lagerperioden. Hvis lagerperioder ikke brukes, styrer datoen i feltet **Bokf. tillatt fra** på siden **Finansoppsett** når justeringsposten bokføres.

## Justere varekost manuelt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Juster kostverdi – vareposter**, og velg deretter den tilknyttede koblingen.
2. På siden **Juster kostverdi - vareposter** angir du hvilke varer du vil justere kostnader for.
3. Velg **OK**.

## Slik gjør du generelle endringer i direkte enhetskost

Hvis du må endre direkte enhetskost for flere varer, kan du bruke kjørselen **Juster varekost/priser**.  

Kjørselen endrer innholdet i **Salgspris**-feltet på varekortet. Innholdet endres på samme måte for alle varene eller for utvalgte varer. Kjørselen multipliserer verdien i feltet med en justeringsfaktor som du angir.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Juster varekost/priser**, og velg deretter den tilknyttede koblingen.  
2. I feltet **Juster felt** angir du hvilket vare- eller LFE-kortfelt du vil justere.  
3. Angi faktoren som verdien skal justeres med, i **Justeringsfaktor**-feltet. Angi for eksempel **1,5** for å øke verdien med 50 %.  
4. På hurtigfanen **Vare** definerer du filtre til å angi, for eksempel, hvilke varer kjørselen skal behandle.  
5. Velg **OK**-knappen.  

## Forstå beregning av enhetskost

Verdien i **Enhetskost**-feltet på varekortet er basert på standardkost for varer med lagermetoden Standard. For varer med andre lagermetoder er verdien basert på beregning av tilgjengelig lagerbeholdning (fakturerte kostnader og forventede kostnader) delt på aktuell beholdning.  

Hvordan innholdet i feltet **Lagermetode** påvirker beregningen av enhetskosten for kjøp og salg, er beskrevet mer inngående i delene nedenfor.  

## Beregning av enhetskost for kjøp  

Når du kjøper varer, blir verdien i feltet **Siste direkte kostnad** på varekortet kopiert til feltet **Direkte enhetskost** på en bestillingslinje eller til **Enhetsbeløp**-linjen på en varekladdelinje.  

Det du velger i **Lagermetode**-feltet, har innvirkning på hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner innholdet i **Enhetskost**-feltet på linjene.  

### Lagermetodene FIFU, LIFO, Serienummer eller Gjennomsnitt  

[!INCLUDE[prod_short](includes/prod_short.md)] bruker følgende formel til å beregne innholdet i feltet **Enhetskost LV** på bestillingslinjen, eller innholdet i feltet **Enhetskost** på varekladdelinjen:  

Enhetskost (LV) = (Direkte enhetskost - (Rabattbeløp / Antall)) x (1 + Indirekte kost-% / 100) + Sats for indirekte kostnader  

### Standard lagermetode  

Feltet **Enhetskost (LV)** på bestillingslinjen eller feltet **Enhetskost** fylles ut på varekladdelinjen ved å kopiere verdien i feltet **Enhetskost** på varekortet. Hvis du bruker lagermetoden Standard, er verdien alltid basert på standardkosten.  

Når du bokfører et kjøp, kopieres enhetskosten fra bestillingslinjen eller varekladdelinjen til kjøp/varefakturaposten. Dette vises i postoversikten for varen.  

### Alle lagermetoder  

Enhetskosten fra linjen i kildedokumentet brukes til å beregne innholdet i feltet **Kostbeløp faktisk**, eller feltet **Kostbeløp forventet**, hvis det brukes, som er knyttet til denne vareposten. Kostnaden tas med i beregningen uavhengig av varens lagermetode.  

## Beregning av enhetskost for salg  

Når du selger varer, kopieres enhetskosten fra feltet **Enhetskost** på varekortet til salgslinjen eller varekladdelinjen.  

Ved bokføring kopieres enhetskosten til salgsfakturaposten, og den kan dermed ses på varens postoversikt. [!INCLUDE[prod_short](includes/prod_short.md)] bruker enhetskosten til å beregne innholdet i feltet **Kostbeløp faktisk**, eller feltet **Kostbeløp forventet**, hvis det brukes, i verdiposten som er knyttet til denne vareposten.  

## Spor varekostjusteringer

Varekost kan endres av mange årsaker, så det er viktig at du kan holde oversikt over kostnadsjusteringer. Bruk siden **Lagerkostjustering** til å administrere og overvåke kostnadsjusteringsprosessen. Denne siden viser varer sammen med deres kostnadsparametere og kostnadsjusteringsstatus. Du kan filtrere listen slik at den fokuserer på varer som krever justering eller som er utelatt fra kostnadsjusteringsprosessen. Hvis du vil ha mer informasjon om sporing av kostjusteringer, kan du gå til [Spor varekostjusteringer](finance-track-inventory-costs.md).

## Se også

[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]