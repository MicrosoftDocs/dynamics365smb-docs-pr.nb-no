---
title: Definere lokasjoner slik at de bruker hyller
description: Hyller representerer den enkle lagerstrukturen og brukes til å komme med forslag om plasseringen av varer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Definere lokasjoner slik at de bruker hyller

Hyller representerer den grunnleggende lagerstrukturen, og du kan bruke dem til å foreslå hvor varene skal plasseres. Når du har opprettet hyllene, kan du definere innholdet, eller la de fungere som mobile hyller uten angitt innhold.

Hvis du vil bruke hyllefunksjonaliteten i en lokasjon, må du slå på vekslebryteren **Hylle obligatorisk** på kortet **Lokasjon**. Når du har aktivert vekslebryteren, er feltene **Hyllekode** og **Sonekode** tilgjengelige i følgende dokumenter:

* Lagermottakshode
* Lagermottakslinjer
* Plasseringslinjer
* Lagerfølgeseddelhode
* Lagerfølgeseddellinjer
* Plasseringslinjer

Det neste trinnet er å utforme vareflyten på lokasjonen ved å angi hyllekoder i oppsettsfeltene som representerer ulike flyter.  

> [!NOTE]  
> Du må opprette hyllekoder før du kan angi dem for lokasjonen. Hvis du vil ha mer informasjon, kan du se [Opprette hyller](warehouse-how-to-create-individual-bins.md).  

## Sette opp en lokasjon til å bruke hyller

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2. Velg lokajonen der du vil bruke hyller.  
3. Velg handlingen **Rediger**.  
4. På hurtigfanen **Lager** merker du av for **Hylle obligatorisk**.  
5. Hvis du ikke bruker lagerstyring for lokasjonen, velger metoden du vil at [!INCLUDE [prod_short](includes/prod_short.md)] skal bruke til å tildele en standardhylle til en vare, i feltet **Standard hyllevalg**.  
6. Åpne kortet for lokasjonen du vil konfigurere hyller for.
7. På hurtigfanen **Hyller** velger du de hyllene du vil bruke som standard for mottak og leveringer og inngående, utgående og åpne produksjonshyller.  

    De hyllekodene du angir, vises automatisk i hodene og linjene i ulike lagerdokumenter. Standardhyllene definerer alle start- og sluttplasseringer for varene i lageret.  
8. Hvis du bruker lagerstyring, velger du en hylle til lagerjusteringer. Hyllekoden i feltet **Justeringshyllekode** definerer den virtuelle hyllen der det skal registreres avvik i beholdning:

    * Når du observerer avvik som er registrert i lagervarekladden
    * Avvik beregnet når du registrerer en lageropptelling  
9. Valgfritt: Fyll ut feltene på hurtigfanen **Hyllepolicyer**. De viktigste feltene er **Hyllekapasitetsprinsipp**, **Tillat anbrekk** og **Plasseringsmal - kode**.  
10. På hurtigfanen **Lager** fyller du ut feltene **Utgående lagerhåndteringstid**, **Inngående lagerhåndteringstid** og **Hovedkalenderkode**. Hvis du vil ha mer informasjon om ressurser, går du til [Definer hovedkalendere](across-how-to-assign-base-calendars.md).

## Fyll ut forbrukshyllen

Følgende flytdiagram viser hvordan **Hyllekode**-feltet på produksjonsordrekomponentlinjer fylles ut i henhold til lokasjonsoppsettet.

:::image type="content" source="media/binflow.png" alt-text="Hyllekodefeltet på produksjonsordrekomponentlinjer.":::

## Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
