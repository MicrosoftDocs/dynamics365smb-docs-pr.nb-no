---
title: Forstå elementtyper
description: 'Du kan justere lagerverdien for en vare med lagermetoden FIFO eller Gjennomsnitt, når varekost endres av andre årsaker enn transaksjoner.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: edupont
---
# Om varetyper
I **Type**-feltet på **Varekort**-siden kan du velge hva varen brukes til i virksomheten din, som påvirker i hvilken grad du kan administrere varen på lageret. Tabellen nedenfor viser og beskriver de tre varetypene som er tilgjengelige.

|Alternativ|Vanlig formål|
|------|-----------|
|Lager|Fysiske ting, for eksempel sykler, telefoner og skrivebord, som du ønsker å kunne bruke alle lagerprosessene for. Dette kan også omfatte ikke-fysiske varer, for eksempel programvarelisenser og abonnementer, hvis varene har identifikasjonsnumre, for eksempel serienumre. Du kan fullt ut spore vareverdier og tilgjengelighet på lager.|
|Ikke-lagervarer|Ikke-lagervarer er vanligvis fysiske ting, for eksempel bolter eller penner, som en virksomhet bruker, men ikke vil spore fullt ut på lageret. Årsaken kan for eksempel være at de er lavkostnadsvarer og bare brukes internt.|
|Service|En arbeidstidsenhet, for eksempel en konsulenttime, for begrenset selskapsstøtte.|

> [!NOTE]
> Typene **Service** og **Ikke-lagervarer** støtter ikke sporing av lagerantall og -verdier. Bare utvalgte varetransaksjonstyper og funksjoner støttes.

Tabellen nedenfor viser funksjonene som de tre varetypene støtter.

|Varetype|Salg|Kjøp|Jobbforbruk|Serviceforbruk|Monteringsforbruk|Produksjon Forbruk|Monteringsavgang|Produksjonsavgang|Lokasjon, Overføring|Fysisk opptelling|Revaluering av lager|Beholdning og kostberegning|Varesporing|Reservasjon|Lagerstyring|Planl.|Bestillingsplanlegging|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lager|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Ikke-lager|Ja|Ja|Ja|Ja|Ja|Ja|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Ja|
|Tjeneste|Ja|Ja|Ja|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Ja|

## Lagermetoder for varetyper
Når du bokfører lagertransaksjoner, registreres endringene i antall og verdi på lageret i henholdsvis varepostene og verdipostene. 

For lagervarer registreres kostbeløpet i feltet **Kostbeløp (faktisk)** på **Verdiposter**-siden, og når dette avstemmes til finansposten, vises kostbeløpet i feltet **Bokført kost**. Hvis du vil ha mer informasjon, kan du se [Kostberegning for beholdning](design-details-inventory-costing.md).

For ikke-lagervarer og servicevarer registreres kost i feltet **Kostbeløp (indirekte kost)** på **Verdiposter**-siden. For ikke-lagervarer og servicevarer angis kost i salgs-, monterings- og produksjonsdokumenter og -kladder. Standardkost kan angis i feltet **Enhetskost** på sidene **Varekort** og **Lagerføringsenhet**. Kostnader for denne typen varer er ikke avstemt til finans. 

## Katalog- og servicevarer
Varer som du tilbyr kunder, men som du ikke vil administrere i systemet før du begynner å selge dem, kan defineres som katalogvarer. Katalogvarer må ikke forveksles med vanlige varer av typen Ikke-lagervarer. Hvis du vil ha mer informasjon, kan du se [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).

Kundenes varer som du utfører service på, for eksempel en skriver, kalles servicevarer. Servicevarer har ikke noe å gjøre med vanlige varer eller katalogvarer. Servicekomponentene kan imidlertid være vanlige varer. Hvis du vil ha mer informasjon, se [Definere servicevarer og servicevarekomponenter](service-how-setup-service-items.md).

## Se også
[Registrere nye varer](inventory-how-register-new-items.md)  
[Definere lager](inventory-setup-inventory.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
