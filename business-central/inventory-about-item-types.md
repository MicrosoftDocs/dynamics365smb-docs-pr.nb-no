---
title: Forstå varetyper
description: 'Lær om varentypene du kan administrere i beholdningen, og innvirkningen til typene. Du kan justere lagerverdien for en vare med lagermetoden FIFO eller Gjennomsnitt, når varekost endres av andre årsaker enn transaksjoner.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Om varetyper

I **Type**-feltet på **Varekort**-siden kan du velge hva varen brukes til i virksomheten din, som påvirker i hvilken grad du kan administrere varen på lageret. Tabellen nedenfor viser og beskriver de tre varetypene som er tilgjengelige.

|Alternativ|Vanlig formål|
|------|-----------|
|Lager|Fysiske ting, for eksempel sykler, telefoner og skrivebord, som du ønsker å kunne bruke alle lagerprosessene for. Beholdningsvarer kan også omfatte ikke-fysiske varer, for eksempel programvarelisenser og abonnementer, hvis varene har identifikasjonsnumre, for eksempel serienumre. Du kan fullt ut spore vareverdier og tilgjengelighet på lager.|
|Ikke-lager|Ikke-lagervarer er vanligvis fysiske ting, for eksempel bolter eller penner, som virksomheten din bruker, men ikke sporer fullstendig på lageret. Årsaken kan for eksempel være at de er lavkostnadsvarer og bare brukes internt.|
|Tjeneste|En arbeidstidsenhet, for eksempel en konsulenttime, for begrenset selskapsstøtte.|

> [!NOTE]
> Typene **Service** og **Ikke-lagervarer** støtter ikke sporing av lagerantall og -verdier. Bare utvalgte varetransaksjonstyper og funksjoner støttes. Tabellen nedenfor viser funksjonene som de tre varetypene støtter.

|Varetype|Salg|Kjøp|Jobbforbruk|Serviceforbruk|Monteringsforbruk|Produksjon Forbruk|Monteringsavgang|Produksjonsavgang|Lokasjon, Overføring|Fysisk opptelling|Revaluering av lager|Beholdning og kostberegning|Varesporing|Reservasjon|Lagerstyring|Planl.|Bestillingsplanlegging|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Lager|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Ikke-lager|Ja|Ja|Ja|Ja|Ja|Ja|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Ja|
|Tjeneste|Ja|Ja|Ja|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Nei|Ja|

## Lagermetoder for varetyper

Når du bokfører lagertransaksjoner, registreres endringene i antall og verdi på lageret i henholdsvis varepostene og verdipostene.

Du registrerer kostnaden for lagervarer i feltet **Kostbeløp (faktisk)** på **Verdiposter**-siden. Når du avstemmer posten mot økonomimodulen, vises kostbeløpet i feltet **Bokført kost til finans**. Hvis du vil lære mer om kostberegning for beholdning, kan du gå til [Designdetaljer: Kostberegning for beholdning](design-details-inventory-costing.md).

For ikke-lagervarer og servicevarer registreres kost i feltet **Kostbeløp (indirekte kost)** på **Verdiposter**-siden. For ikke-lagervarer og servicevarer angis kost i salgs-, monterings- og produksjonsdokumenter og -kladder. Angi standardkost i feltet **Enhetskost** på sidene **Varekort** og **Lagerføringsenhet**. Kostnader for denne typen varer er ikke avstemt til finans.

## Katalog- og servicevarer

Du kan definere varer som du tilbyr kunder, men som du ikke administrerer i systemet før du selger dem, som katalogvarer. Selv om katalogvarer ligner på vanlige varer av typen **Ikke-lager** i denne sammenhengen, må du ikke forveksle disse to fordi det er forskjeller. Hvis du vil ha mer informasjon, kan du gå til [Arbeide med katalogvarer](inventory-how-work-nonstock-items.md).

Kundevarer som du utfører service på, for eksempel en skriver, kalles servicevarer. Servicevarer har ikke noe å gjøre med vanlige varer eller katalogvarer. Servicekomponentene kan imidlertid være vanlige varer. Hvis du vil ha mer informasjon, kan du gå til [Definere servicevarer og servicevarekomponenter](service-how-setup-service-items.md).

## Se også

[Registrer nye varer](inventory-how-register-new-items.md)  
[Definere lager](inventory-setup-inventory.md)  
[Administrere lagerkostnader](finance-manage-inventory-costs.md)  
[Lager](inventory-manage-inventory.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
