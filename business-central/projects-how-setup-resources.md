---
title: 'Definere prosjektressurskostpriser, priser og kapasitet'
description: 'For å bruke ressurser og forenkle prosjektstyring angir du kostnadene og prisene for individuelle ressurser eller ressursgrupper, og angir ressurskapasiteten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'project management, capacity, staff'
ms.search.form: '72, 76, 77, 203, 204'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Definer ressurser for prosjekter

For å behandle ressursaktiviteter på riktig måte må du definere ressursene og de relaterte kostnadene og prisene. De prosjektrelaterte prisene, rabattene og kostfaktorreglene er definert på prosjektkortet. Du kan angi kostnadene og prisene for individuelle ressurser, ressursgrupper eller alle tilgjengelige ressurser for firmaet.

Når ressurser brukes eller selges i et prosjekt, hentes de tilknyttede prisene og kostnadene fra informasjonen du definerer.

Du angir standardbeløpet per time når ressursen opprettes. Hvis du for eksempel bruker en bestemt maskin i fem timer på et prosjekt, beregnes prosjektet basert på beløpet per time.

> [!NOTE]
> Du kan kjøpe eksterne ressurser, for eksempel for å fakturere en leverandør for arbeid som er levert. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).<br /><br />
> For eksterne ressurser anbefaler vi at du gir navn til eller grupperer dem slik at de angir forveksles med de interne ressursene.
>  
> Hvis du bokfører konserninterne transaksjoner, selv om du kan gi en ressurs til en linje på en salgsordre, hvis du konverterer salgsordren til en bestilling på mottakersiden, inkluderes ikke ressursen. Hvis du vil bruke ressurser i konserninterne transaksjoner, bruker du feltet **Finanskontonr. for KI-partnerkjøp** på ressurskortet for å angi hvilken konto utgiftene skal bokføres til.

## Slik konfigurerer du en ressurs

Opprette et kort for hver ressurs du vil bruke i prosjekter.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## Slik definerer du en ressursgruppe

Du kan kombinere flere ressurser i én ressursgruppe. Alle kapasiteter og budsjetter for ressursgrupper akkumuleres fra de enkelte ressursene. Det er også mulig å angi kapasiteter for ressursgrupper, enten uavhengig av akkumulerte verdier eller i tillegg til disse.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressursgrupper**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.
3. Fyll ut feltene etter behov.

## Angi kapasiteten til en ressurs

Hvis du vil beregne hvor mye tid en ressurs kan bruke på prosjekter, må deres kapasitet først defineres som tilgjengelig tid per periode i arbeidskalenderen. Dette oppsettet brukes når du fyller ut prosjetplanleggingslinjer som inneholder ressursen. Hvis du vil ha mer informasjon, kan du se [Opprette prosjekter](projects-how-create-jobs.md).

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.
2. Åpne det aktuelle ressurskortet, og velg deretter handlingen **Ressurskapasitet**.
3. På siden **Ressurskapasitet** i **Vis etter**-feltet, angir du lengden på perioden, for eksempel **Dag**, som vises i kolonner i hurtigfanen **Matrise for ressurskapasitet**.
4. For hver ressurs på en linje angir du for hver periode i kolonnene antall timer som ressursen er tilgjengelig.
5. Hvis du vil angi detaljer om ressursens ukentlige kapasitet innenfor en start- og sluttdato, kan du også velge handlingen **Angi kapasitet**.
6. På siden **Innstillinger for ressurskapasitet** fyller du ut feltene på en linje etter behov.
7. Velg handlingen **Oppdater kapasitet**. Siden **Ressurskapasitet** oppdateres med den angitte kapasiteten.
8. Lukk siden.

## Slik definerer du alternative ressurskostpriser

I tillegg til kostprisen som er angitt på ressurskortet, kan du definere alternative kostpriser for hver ressurs. Hvis du for eksempel betaler ansatte en høyere timesats for overtid, kan du definere en ressurskostpris for overtidssatsen. Den alternative kostprisen du definerer for ressursen, overstyrer kostprisen på ressurskortet når du bruker ressursen i ressurskladden.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.  
2. Velg ressursen som du vil definere ett eller flere alternative kostpriser for, og velg deretter handlingen **Kostpriser**.  
3. På siden **Ressurskostpriser** fyller du ut feltene på en linje etter behov.  
4. Gjenta trinn 3 for hvert alternativ ressurskostpris du vil definere.

**Merk**. Hvis du vil definere ressurskostpriser som skal gjelde for alle ressurser og ressursgrupper, åpner du siden **Ressurskostpriser** og fyller ut feltene.

## Slik definerer du alternative ressurspriser

I tillegg til prisen som er angitt på ressurskortet, kan du definere alternative priser for hver ressurs. Disse alternative prisene kan være betinget. De kan være avhengig av at ressursen brukes med et bestemt prosjekt eller arbeidstype.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Ressurser** og velg den relaterte koblingen.
2. Velg ressursen som du vil definere ett eller flere alternative priser for, og velg deretter handlingen **Priser**.
3. På siden **Ressurspriser** fyller du ut feltene på en linje etter behov.
4. Gjenta trinn 3 for hvert alternativ ressurspris du vil definere.

## Se også

[Konfigurer prosjektstyring](projects-setup-projects.md)  
[Prosjektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
