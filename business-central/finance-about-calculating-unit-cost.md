---
title: Om beregning av enhetskost
description: Lær hvordan lagermetoden og andre faktorer påvirker Enhetskost-feltet på varekortet.
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: a-reishima
---
# <a name="about-unit-cost-calculation"></a>Om beregning av enhetskost

Hver vare har en enhetskost som beregnes på bakgrunn av selskapets lagermetode og andre faktorer. Som en regel, med lagermetoden *Standard*, er verdien i **Enhetskost**-feltet basert på standardkost for varen. For alle andre lagermetoder (*FIFU*, *LIFO*, *Serienummer* og *Gjennomsnitt*) beregnes enhetskosten på grunnlag av gjennomsnittlig enhetskost i løpet av en tidsperiode.  

Hvis du vil ha mer informasjon, kan du se [Administrere lagerkostnader](finance-manage-inventory-costs.md).  

## <a name="when-is-the-unit-cost-field-updated"></a>Når enhetskostfeltet oppdateres

Den valgte lagermetoden påvirker når **Enhetskost**-feltet oppdateres.

Når lagermetoden er definert som *Standard*, oppdateres **Enhetskost**-feltet hver gang standardkostnaden endres, og brukerne kan ikke redigere feltet **Enhetskost**. Hvis du vil ha mer informasjon, kan du se [Oppdatering av standardkost](finance-how-to-update-standard-costs.md).

Hvis lagermetoden er *FIFU*, *LIFO*, *Serienummer* eller *Gjennomsnitt*, oppdateres **Enhetskost** i følgende tilfeller:

* Når varen er kostnadsjustert, automatisk eller ved hjelp av en [Juster kostverdi](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually)-oppgave.
* Under bokføring av kjøpsfakturaer, avgang eller positiv justering hvis en av følgende betingelser er oppfylt:
  * Fakturert beholdning for varen endres fra negativ eller null til positiv.
  * Nåværende enhetskost er null.

Hvis en av disse betingelsene er oppfylt, oppdateres **Enhetskost**-feltet med verdien i feltet **Siste direkte kostnad** på varekortet.

> [!NOTE]
> **Enhetskost**-feltet oppdateres ikke hvis nåværende enhetskost er høyere enn null og den nye enhetskosten er null. En enhetskost på null anses for å være et unntak fra vanlig handel. Nåværende enhetskost beholdes derfor for å gi den siste kjente, relevante verdien. Dette unntaket gjelder selv om det eksisterende lageret er revaluert til null.

I feltet **Enhetskost** på varekortet kan du drille ned for å vise historikken over transaksjoner som gjennomsnittlig enhetskosten tilgjengelig beregnes fra, i vinduet **Oversikt over beregning av gjennomsnittskost**.

## <a name="unit-cost-calculation-for-purchases"></a>Beregning av enhetskost for kjøp

Når du kjøper varer, blir verdien i feltet **Siste direkte kostnad** på varekortet kopiert til feltet **Direkte enhetskost** på en bestillingslinje eller til **Enhetsbeløp**-linjen på en varekladdelinje.

Det du velger i **Lagermetode**-feltet, har innvirkning på hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner innholdet i **Enhetskost**-feltet på linjene.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Lagermetoden FIFU, LIFO, Serienummer eller Gjennomsnitt

[!INCLUDE[prod_short](includes/prod_short.md)] beregner innholdet i feltet **Enhetskost LV** på bestillingslinjen, eller innholdet i feltet **Enhetskost** på varekladdelinjen etter følgende formel:

*Enhetskost (LV) = (Direkte enhetskost - (Rabattbeløp / Antall)) x (1 + Indirekte kost-% / 100) + Sats for indirekte kostnader*

### <a name="costing-method-standard"></a>Standard lagermetode

Feltet **Enhetskost (LV)** på bestillingslinjen eller feltet **Enhetskost** fylles ut på varekladdelinjen ved å kopiere verdien i feltet **Enhetskost** på varekortet. Ved å angi lagermetoden som *Standard*, er denne verdien alltid basert på standardkosten.

Når du bokfører kjøpet, bruker [!INCLUDE[prod_short](includes/prod_short.md)] enhetskosten fra bestillingslinjen eller varekladdelinjen til kjøp/varefakturaposten. Du kan se det i postoversikten for varen.

### <a name="all-costing-methods"></a>Alle lagermetoder

Enhetskosten fra kildedokumentlinjen brukes til å beregne innholdet i feltet **Kostbeløp faktisk**, eller feltet **Kostbeløp forventet**, hvis det er aktuelt, som er tilknyttet denne vareposten, uavhengig av lagermetoden for varen.

## <a name="unit-cost-calculation-for-sales"></a>Beregning av enhetskost for salg

Når du selger varer, kopieres enhetskosten fra feltet **Enhetskost** på varekortet til salgslinjen eller varekladdelinjen.

Ved bokføring kopieres enhetskosten til salgsfakturaposten, og den kan dermed ses på varens postoversikt. [!INCLUDE[prod_short](includes/prod_short.md)] bruker enhetskosten til å beregne innholdet i feltet **Kostbeløp faktisk**, eller feltet **Kostbeløp forventet**, hvis det brukes, i verdiposten som er knyttet til denne vareposten.

## <a name="see-also"></a>Se også

[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Registrering av nye varer](inventory-how-register-new-items.md)  
[Om lagerkost](finance-learn-about-costing.md)  
[Lager](inventory-manage-inventory.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Anbefalte fremgangsmåter for oppsett: lagermetode](setup-best-practices-costing-method.md)  
[Designdetaljer: Lagermetoder](design-details-costing-methods.md)  
[Designdetaljer: Kostjustering](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
