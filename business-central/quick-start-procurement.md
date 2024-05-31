---
title: Hurtigstart for innkjøp (inneholder video)
description: 'Lær hvordan du fyller ut de første kritiske feltene om leverandører i Business Central, slik at du kan starte innkjøp av produkter og tjenester.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: quickstart
ms.search.form: '26, 27, 50, 56'
ms.date: 09/29/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Hurtigstart for innkjøp

For å kunne kjøpe produkter og tjenester må du først definere leverandører. Når dette er gjort, kan du begynne å registrere bestillinger og motta fakturaer.  

## Definer leverandører

I denne videoen får du vite hvordan du definerer en leverandør i [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

### Definer en ny leverandør

[!INCLUDE[create_new_vendor](includes/create_new_vendor.md)]

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du registrerer leverandører, kan du se [Registrer nye leverandører](purchasing-how-register-new-vendors.md).  

## Opprett nye bestillinger

Når du kjøper noe fra en leverandør, har du to alternativer. Den første og enkleste er å bare opprette en kjøpsfaktura. Du må imidlertid bruke bestillinger hvis kjøpsprosessen krever at du registrerer delvise mottak av et bestillingsantall, for eksempel fordi det fullstendige antallet ikke var tilgjengelig hos leverandøren.

I denne videoen får du vite hvordan du oppretter en bestilling i [!INCLUDE[prod_short](includes/prod_short.md)].

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

### Slik oppretter du en bestilling  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 1.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  

2. Velg **Ny**-handlingen på siden **Bestillinger** for å opprette en ny bestilling.

3. I feltet **Leverandørnavn** angir du navnet på en eksisterende leverandør.

    Andre felt på siden **Bestillingshode** fylles nå med standardinformasjon om den valgte leverandøren.  

4. Fyll ut resten av feltene på siden **Bestilling** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du kan nå begynn å fylle ut bestillingslinjene med varer eller ressurser du har kjøpt fra leverandøren.

5. Angi nummeret på en vare eller tjeneste i **Varenr.**-feltet i hurtigfanen **Linjer**.

6. I feltet **Antall** angir du hvor mange varer som skal kjøpes.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Direkte enhetskost** multiplisert med verdien i feltet **Antall**.

7. I feltet **Bestillingsrabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.** nederst på bestillingen.

8. Velg **Bokfør** når du mottar innkjøpte varer eller tjenester.

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du oppretter en bestilling, kan du se [Kjøp](purchasing-manage-purchasing.md).  

## Opprett en kjøpsfaktura  

Du kan opprette en kjøpsfaktura for å registrere kjøpskostnader og spore leverandørgjeld. Oppretting av en kjøpsfaktura fungerer på samme måte som når du oppretter en bestilling.

### Slik oppretter og bokfører du en kjøpsfaktura  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg 3.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. Velg **Ny**-handlingen på siden **Kjøpsfaktur** for å opprette en ny kjøpsfaktura.
3. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.

    Andre felt på siden **Kjøpsfaktura** fylles nå med standardinformasjon for den valgte leverandøren.

4. Fyll ut resten av feltene på siden **Kjøpsfaktura** etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du kan nå begynn å fylle ut kjøpsfakturalinjene med varer eller ressurser du har kjøpt fra leverandøren.

5. Angi nummeret på en vare eller tjeneste i **Varenr.**-feltet i hurtigfanen **Linjer**.
6. I feltet **Antall** angir du hvor mange varer som skal kjøpes.

    Feltet **Linjebeløp** oppdateres for å vise verdien i feltet **Direkte enhetskost** multiplisert med verdien i feltet **Antall**.

7. I feltet **Fakturarabattbeløp** angir du et beløp som skal trekkes fra verdien som vises i feltet **Totalt inkl. mva.** nederst på fakturaen.

8. Velg **Bokfør** når du mottar innkjøpte varer eller tjenester.

Kjøpet gjenspeiles nå i beholdningen, ressursposter og økonomiposter, og leverandørbetalingen aktiveres. Kjøpsfakturaen fjernes fra listen over kjøpsfakturaer og erstattes med et nytt dokument i listen over bokførte kjøpsfakturaer.  

Hvis du vil ha mer informasjon og andre ting du kan gjøre når du oppretter en bestilling, kan du se [Registrer kjøp med kjøpsfakturaer](purchasing-how-record-purchases.md).

## Se også

[Hurtigstart for Business Central](quick-start-business-central.md)  
[Oversikt over kjøp](Purchasing-manage-purchasing.md)  
[Registrer kjøp med kjøpsfakturaer](purchasing-how-record-purchases.md)  
