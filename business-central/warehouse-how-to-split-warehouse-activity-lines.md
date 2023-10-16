---
title: Dele lageraktivitetslinjer
description: Lær hvordan du deler lageraktivitetslinjer hvis den disponible kapasiteten i en foreslått hylle ikke er tilstrekkelig.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.forms: '931, 9314, 9313, 9315, 9330'
---
# Dele lageraktivitetslinjer

I plasseringer, flyttinger eller plukkinger og i lagerplasseringer og lagerplukkinger foreslås det hyller for plukking eller plassering av varer. Antallet som er faktisk i den foreslåtte hyllen, er kanskje ikke tilstrekkelig, eller det er ikke nok plass i hyllen til å plassere det nødvendige antallet. I slike tilfeller kan du dele linjen slik at varene på en linje blir hentet fra eller plassert i flere enn én hylle.  

Følgende fremgangsmåte gjelder følgende lagerdokumenter:

* Lagerplasseringer
* Lagerflyttinger
* Lagerplukk
* Lagerplasseringer
* Lagerflyttinger
* Lagerplukk  

## Slik deler du lageraktivitetslinjer:  

1. Åpne en lageraktivitetslinje hvor du prøver å håndtere et utilstrekkelig antall.  
2. Angi det reduserte antallet du kan håndtere, i feltet **Ant. som skal håndt.**.  
3. På hurtigfanen **Linjer** velger du handlingen **Handlinger**, **Funksjoner**, og deretter **Del linje**. En ny linje vises. Linjen er en kopi av den opprinnelige linjen, bortsett fra at feltet **Ant. som skal håndt.** inneholder antallet du fjernet fra den opprinnelige linjen.  
4. Tildel en hylle, hvis du bruker lagerstyring, sonen, til den nye linjen, eller fortsett å dele linjen flere ganger til du finner hyller til alle antallene.  

> [!NOTE]  
> Hvis lokasjonen bruker lagerstyring og du deler linjene, må du være kjent med lageret, og du må være i stand til å velge en hylle som samsvarer med lagringskravene for varen, og som oppfyller de generelle kravene i lagerdokumentet. Du bør for eksempel ikke dele en linje i et plukkdokument og plasser noen varer i masselagringen.  

## Se også  

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]