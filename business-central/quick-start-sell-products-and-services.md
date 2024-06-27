---
title: Hurtigstart for salg
description: 'Lær hvordan du fyller ut de første kritiske feltene for produkter og kunder i Business Central, slik at du kan starte salgsprosessene.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Hurtigstart for salg

For å kunne selge produkter og tjenester må du først definere varer og kunder. Når dette er gjort, kan du begynne å registrere ordrer og sende ut fakturaer.

## Definer varer som skal selges

Denne videoen viser hvordan du definerer en vare som skal selges, i [!INCLUDE[prod_short](includes/prod_short.md)].

<br>

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE47eLx?rel=0]

### Definer en ny vare

[!INCLUDE[create_new_item](includes/create_new_item.md)]

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du oppretter varer, kan du se [Registrer nye varer](inventory-how-register-new-items.md).  

## Definer kunder

Denne videoen viser hvordan du oppretter en ny kunde i [!INCLUDE[prod_short](includes/prod_short.md)].  

<br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

### Definer en ny kunde

[!INCLUDE[create_new_customer](includes/create_new_customer.md)]

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du oppretter kunder, kan du se [Registrer nye kunder](sales-how-register-new-customers.md)

## Opprett en ordre  

Når du selger noe til en kunde, har du to alternativer. Den første og enkleste er å bare opprette en salgsfaktura. Hvis imidlertid salgsprosessen er mer sammensatt, for eksempel hvis du har situasjoner der du bare leverer deler av et ordreantall, bruker du en ordre.

### Opprette en ordre  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 10.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrer**, og velg deretter den relaterte koblingen.
2. Velg **Ny** for å opprette en ny post.
3. I feltet **Kunde** angir du navnet på en eksisterende kunde.

    Andre felt på siden **Ordre** fylles nå med standardinformasjon for den valgte kunden.  

4. Fyll ut resten av feltene på siden **Ordre** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden med salgslinjen.

6. I **Nr.** -feltet, angir du nummeret for en lagervare eller service.

7. I feltet **Antall** angir du hvor mange varer som skal selges.

8. I feltet **Linjerabatt-%** angir du en prosent hvis du vil gi kunden en rabatt på produktet.

9. Hvis du vil legge til en kommentar om ordrelinjen som kunden kan se på ordreutskriften, skriver du en kommentar i **Beskrivelse**-feltet på en tom linje.

10. Gjenta trinn 5 til 9 for hver vare som du vil selge til kunden.

11. Hvis du vi sende bare en del av ordreantallet, kan du angi antallet i den feltet **Levere (antall)**. Verdien kopieres til feltet **Fakturer (antall)**.

12. Hvis du vi fakturere bare en del av det sendte antallet, kan du angi antallet i den feltet **Fakturer (antall)**. Antallet må være lavere enn verdien i feltet **Levere (antall)**.

13. Når ordrelinjene er fullført, kan du velge handlingen **Bokfør og send**.

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du oppretter kundeordrer, kan du se [Selg produkter med en kundeordre](sales-how-sell-products.md).  

## Opprett en salgsfaktura

Når du oppretter og bokfører en salgsfaktura, oppretter du ikke bare fakturadokumentet du sender til kunden, du oppretter også relaterte antall og verdiposter i [!INCLUDE[prod_short](includes/prod_short.md)].

### Slik oppretter og bokfører du en salgsfaktura  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 20.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsfakturaer**, og velg deretter den relaterte koblingen.  

2. Velg **Ny** for å opprette en ny post.

3. I feltet **Kunde** angir du navnet på en eksisterende kunde.

4. Fyll ut resten av feltene på siden **Salgsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

5. På **Linjer**-hurtigfanen i **Type**-feltet velger du typen produkt, tillegg eller transaksjon som du vil legge til for kunden med salgslinjen.

6. I **Nr.** velger du en post skal bokføres, i henhold til verdien i **Type**-feltet.

7. I **Antall**-feltet angir du hvor mange enheter av produktet, gebyret eller transaksjonen som linjen skal registrere for kunden.  

8. Hvis du vil gi en rabatt, skriver du inn en prosentandel i feltet **Linjerabatt-%**. Verdien i feltet **Linjebeløp** oppdateres tilsvarende.  

9. Gjenta trinn 5 til 8 for hver hvert produkt eller gebyr som du vil fakturere kunden for.  

10. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.**.

11. Når salgsfakturalinjene er fullført, kan du velge handlingen **Bokfør og send**.  

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du oppretter kundesalgsfakturaer, kan du se [Fakturasalg](sales-how-invoice-sales.md)

## Se også

[Hurtigstart for Business Central](quick-start-business-central.md)  
[Oversikt over salg](sales-manage-sales.md)  
[Selg produkter med en kundeordre](sales-how-sell-products.md)  
[Fakturere salg](sales-how-invoice-sales.md)  
