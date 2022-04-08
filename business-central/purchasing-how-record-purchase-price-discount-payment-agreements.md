---
title: Registrere spesielle kjøpspriser og rabatter
description: Du kan definere ulike eller alternative priser og rabattavtaler og bruke dem i kjøpsdokumenter for leverandører.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 26, 1346, 7012, 7014, 7017, 7018, 7189, 7190, 9307
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 85445267dac39103ed9851604182f09cc9819ea0
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2022
ms.locfileid: "8522671"
---
# <a name="record-special-purchase-prices-and-discounts"></a>Registrere spesielle kjøpspriser og rabatter
> [!NOTE]
> I lanseringsbølge 2 i 2020 lanserte vi strømlinjeformede prosesser for å definere og håndtere priser og rabatter. Hvis du er en ny kunde som bruker denne versjonen, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

De forskjellige pris- og rabattavtaler som gjelder når du kjøper fra forskjellige leverandører, må defineres slik at avtalte regler og verdier brukes på kjøpsdokumenter du oppretter for leverandørene.

Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[prod_short](includes/prod_short.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer. Du finner mer informasjon under [Beregning av beste pris](purchasing-how-record-purchase-price-discount-payment-agreements.md#best-price-calculation).

Når det gjelder priser, kan du sette inn en spesialkjøpspris på bestillingslinjer hvis en bestemt kombinasjon av leverandør, vare, minste antall, enhet, eller start-/sluttdato finnes.

Når det gjelder rabatter, kan du opprette og bruke to typer kjøpsrabatter:

| Rabattype | Beskrivelse |
| --- | --- |
| **Bestillingslinjerabatt** |Et rabattbeløp som settes inn på bestillingslinjer hvis en bestemt kombinasjon av leverandør, vare, minste antall, enhet, eller start-/sluttdato finnes. Dette fungerer på samme måte som for innkjøpspriser. |
| **Fakturarabatt** |En prosentrabatt som trekkes fra dokumenttotalen hvis beløpet for alle linjer på et kjøpsdokument overskrider et bestemt minimumsbeløp. |

Ettersom bestillingslinjerabatter og kjøpspriser er basert på en kombinasjon av vare og leverandør, kan du også angi denne konfigurasjonen fra varekortet, der regler og verdier er definert. Hvis du vil ha mer informasjon, kan du se [Registrere nye varer](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Definere en spesialkjøpspris for en leverandør

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience)  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne det aktuelle leverandørkortet, og velg deretter handlingen **Priser**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fylle ut en linje for hver kombinasjon som leverandøren gir deg en bestillingslinjerabatt for.

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience)  
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Velg leverandøren, og velg deretter handlingen **Salgsprislister**. 
3. Velg **Ny** for å opprette en ny kjøpsprisliste.
4. Fyll ut feltene i hurtigfanen **Generelt** og **Avgift**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Hvis du vil legge til elementer i oversikten, gjør du ett av følgende:
   * Hvis du vil legge til mange varer, velger du **Foreslå linjer** og angir deretter filterkriterier for å angi hvilke typer varer du vil legge til. Du kan eventuelt også angi tilleggsinnstillinger for varene som er spesifikke for prislisten. Du kan endre disse senere ved behov.
   * Hvis du vil kopiere varer fra en annen prisliste, velger du **Kopier linjer**, og deretter velger du prislisten du vil kopiere.
   * Hvis du vil legge til varer manuelt i rutenettet i feltet **Produkttype**, velger du produkttypen prislisten gjelder for. Fyll ut resten av feltene etter behov, avhengig av det du har valgt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynne å bruke prislisten, går du til **Status**-feltet og velger **Aktiv**.

---

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Definere en linjerabatt for en leverandør
1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne det aktuelle leverandørkortet, og velg deretter handlingen **Linjerabatter**.

    **Kjøpstype**-feltet er forhåndsutfylt med **Leverandør**, og **Kjøpskode**-feltet er forhåndsutfylt med leverandørnummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Fylle ut en linje for hver kombinasjon som leverandøren gir deg en bestillingslinjerabatt for.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Definere en fakturarabatt for en leverandør
Når leverandøren har informert deg om hvilke linjerabatter som gis, angir du fakturarabattkoden på leverandørkortet og definerer betingelsene for hver kode.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Leverandører** og velger den relaterte koblingen.
2. Åpne leverandørkortet for leverandøren som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for leverandøren.

    > [!NOTE]  
    >   Fakturarabattkoder representeres av eksisterende leverandørkort. Dette lar deg raskt tilordne fakturarabattbetingelsene til leverandører ved å velge navnet på en annen leverandører som har de samme betingelsene.

    Fortsett å definere nye betingelser for kjøpsfakturarabatt.
4. På siden **Leverandørkort** velger du handlingen **Fakturarabatter**. Siden **Levrd./fakt.-rabatter** åpnes.
5. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i LV.
6. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
7. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
8. Gjenta trinn 5 til 7 for hver valuta som leverandøren vil motta en forskjellig fakturarabatt for.

Fakturarabatten er nå definert og tilordnet til den aktuelle leverandøren. Når du velger leverandørkoden i **Fakturarabattkode**-feltet på andre leverandørkort, tilordnes den samme fakturarabatten til leverandøren.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Slik velger du et prinsipp for bokføring av kjøpsrabatter  
Når du bokfører en kjøpsfaktura som inneholder én eller flere rabatter, kan du velge mellom to prinsipper for bokføring av rabattbeløp. Du kan bokføre rabatter separat, eller du kan trekke fra rabatter på fakturarabatter.  

Før du kan gjøre dette, må du definere de nødvendige kontiene for å kunne bokføre rabattbeløp i kontoplanen. Kontroller også at du har angitt riktige kontonumre i det generelle bokføringsoppsettet i feltene **Best.linjerabattkonto** og **Kjøpsfakturarabattkonto**.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kjøpsoppsett**, og velg deretter den relaterte koblingen.
2. I feltet **Rabattbokføring** velger du ett av følgende prinsipper for bokføring av rabatter.

|**Prinsipp for rabattbokføring**|**Fakturarabatt**|**Linjerabatt**|  
|------------------------------------|--------------------------|-----------------------|  
|**Alle rabatter**|Bokført separat|Bokført separat|  
|**Fakturarabatt**|Bokført separat|Trukket fra|  
|**Linjerabatt**|Trukket fra|Bokført separat|  
|**Ingen rabatt**|Trukket fra|Trukket fra|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Kjøpsfakturarabatter og servicegebyrer
Hvis du har faste betingelser for fakturarabatter fra leverandører, kan du angi betingelsene for disse leverandørene. Når du fyller ut en kjøpsfaktura, beregnes rabatten.  

 Før du kan bruke fakturarabatter i forbindelse med kjøp, må du angi hvilke leverandører du mottar rabattene fra.  

 Du knytter rabattprosentene til bestemte fakturabeløp på sidene **Levrd./fakt.-rabatter**. Du kan angi den prosentsatsen du vil ha på hver side. Hver leverandør kan ha en egen side, eller du kan knytte flere leverandører til den samme siden.  

 I tillegg til (eller i stedet for) en rabattprosent, kan du koble et gebyrbeløp til et bestemt fakturabeløp.  

 Du kan definere betingelsene for fakturarabatten i LV for innenlandske leverandører, og i fremmed valuta for utenlandske leverandører.  

 Du kan la [!INCLUDE[prod_short](includes/prod_short.md)] automatisk beregne fakturarabattene for forespørsler, rammebestillinger, bestillinger, fakturaer eller kreditnotaer.  

> [!TIP]  
>  Før du angir disse opplysningene, er det lurt å sette opp en oversikt over hvilken rabattstruktur du vil bruke. Dermed er det enklere å se hvilke leverandører som kan knyttes til den samme fakturarabattsiden. Jo færre sider du må definere, jo raskere kan du angi de grunnleggende opplysningene.

## <a name="best-price-calculation"></a>Beregning av beste pris
Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[prod_short](includes/prod_short.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer.

Den beste prisen er den lavest tillatte prisen med den størst tillatte linjerabatten på denne en gitt dato. [!INCLUDE[prod_short](includes/prod_short.md)] beregner dette automatisk når det setter inn salgsprisen og linjerabattprosenten for varer på nye dokument- og kladdelinjer.

> [!NOTE]  
>   Det følgende beskriver hvordan den beste prisen beregnes for salg. Beregningen er den samme for kjøp.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer kombinasjonen av faktura til-kundenr. og varen og beregner deretter den aktuelle prisen/linjerabattprosenten ved hjelp av disse kriteriene:

    - Har kunden en avtale om pris/rabatt, eller tilhører kunden en gruppe som har det?
    - Er varen eller varerabattgruppen på linjen tatt med i noen av disse avtalene om pris/rabatt?
    - Er ordredatoen (eller bokføringsdatoen for fakturaen eller kreditnotaen) innenfor start- og sluttdatoen for avtalen om pris/rabatt?
    - Er det angitt en enhetskode? I så fall kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)] om det finnes priser/rabatter med samme enhetskode, og priser/rabatter uten enhetskode.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer om avtaler om pris/rabatt gjelder for informasjon om dokument- eller journallinjen, og setter deretter inn den aktuelle enhetsprisen og rabattprosent, ved hjelp av følgende kriterier:

    - Er det et minimumsbehov i pris/rabatt-avtalen som er oppfylt?
    - Er det et valutabehov i pris/rabatt-avtalen som er oppfylt? I så fall settes den laveste prisen og den høyeste linjerabatten inn for valutaen, selv om LV gir en bedre pris. Hvis det ikke finnes noen pris/rabatt-avtale for den angitte valutakoden, setter [!INCLUDE[prod_short](includes/prod_short.md)] inn den laveste prisen og den høyeste linjerabatten i LV.

Hvis ingen spesialpris kan beregnes for varen på linjen, blir enten den siste direkte kostnaden eller salgsprisen fra varekortet satt inn.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/set-up-prices-discounts-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Definere kjøp](purchasing-setup-purchasing.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]