---
title: Definere spesielle salgspriser og rabatter for kunder | Microsoft-dokumentasjon
description: Beskriver hvordan du kan definere alternative priser og rabattavtaler du vil bruke i salgsdokumenter når du selger til ulike kunder.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 6d358afec4689a3543245295427d5fae992dd680
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/08/2021
ms.locfileid: "6436779"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere spesielle salgspriser og rabatter
> [!NOTE]
> I lanseringsbølge 2 i 2020 lanserte vi strømlinjeformede prosesser for å definere og håndtere priser og rabatter. Hvis du er en ny kunde som bruker denne versjonen, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

Pris- og rabattavtalene som gjelder ved salg til kunder, må defineres slik at de avtalte reglene og verdiene brukes på salgsdokumenter.

Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[prod_short](includes/prod_short.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer. Du finner mer informasjon under [Beregning av beste pris](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Når det gjelder priser, kan du sette inn en spesialsalgspris på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start-/sluttdato finnes. Hvis du vil ha mer informasjon, kan du se delene [Definere salgspriser for en kunde](#to-set-up-a-sales-price-for-a-customer) og [Beregning av beste pris](#best-price-calculation).  

Når det gjelder rabatter, kan du opprette og bruke to typer salgsrabatter:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabatt** |Et rabattbeløp som settes inn på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start-/sluttdato finnes. Dette fungerer på samme måte som for salgspriser. |
| **Fakturarabatt** |En rabattprosent som trekkes fra dokumenttotalen for salg hvis summen av alle linjer i dokumentet overskrider et bestemt minimumsbeløp. |

Ettersom salgspriser og salgslinjerabatter er basert på en kombinasjon av vare og kunde, kan du også utføre denne konfigurasjon fra varesiden for varen der reglene og verdiene skal brukes.

> [!TIP]  
> Hvis en vare aldri noensinne skal selges med rabatt, kan du la rabattfeltene på varesiden være tomme, og ikke ta med varen i noen av linjerabattoppsettene.

I feltene **Gjelder type** og **Gjelder nr.** kan du velge hva denne prislisten skal gjelde for, for eksempel kunde eller kundeprisgruppe. Ved å bruke **Vis kolonner for** kan du vise eller skjule kolonner som er relevante for angivelse av priser, rabatter eller priser og rabatter.

Du kan konfigurere prislistelinjer manuelt, eller du kan for eksempel bruke handlingen **Foreslå linjer** til å opprette nye priser for utvalgte varer, varerabattgrupper, ressurser og andre produkttyper. Hvis du velger Foreslå linjer, kan du på siden Prislinjer - Opprett ny definere filtre for å velge produkter som du vil opprette nye prislistelinjer for. Du kan også angi om du vil ta hensyn til et minimumsantall ved beregning av priser, justeringsfaktoren som skal brukes for nye prislistelinjer, og avrundingsmetoden som skal brukes for priser. Med **Kopier linjer**-handlingen kan du kopiere eksisterende prislistelinjer mellom prislister.

Som standard er statusen for nye prislister Utkast. Når du er ferdig med å legge til linjer og vil at prisberegningsmotoren skal inkludere den, kan du endre statusen til aktiv.

Hvis du vil gå gjennom prislister og priser som gjelder for bestemte kunder eller leverandører, går du til siden **Kunde** og velger **Salgsprislister**, eller du går til siden **Leverandør** og velger **Kjøpsprislister**. Du kan vise prislistelinjer i diverse prislister ved å velge **Salgspriser** eller **Kjøpspriser** på sidene **Vare** og **Ressurs**.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Definere salgspriser for en kunde

Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonensoppdateringen **Ny salgsprisopplevelse**.  

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Priser**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en spesialsalgspris for kunden.

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Salgsprislister**. 
3. Velg **Ny** for å opprette en ny salgsprisliste.
4. Fyll ut feltene i hurtigfanen **Generelt** og **Avgift**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Hvis du vil legge til elementer i oversikten, gjør du ett av følgende:
   * Hvis du vil legge til mange varer, velger du **Foreslå linjer** og angir deretter filterkriterier for å angi hvilke typer varer du vil legge til. Du kan eventuelt også angi tilleggsinnstillinger for varene som er spesifikke for prislisten. Du kan endre disse senere ved behov.
   * Hvis du vil kopiere varer fra en annen prisliste, velger du **Kopier linjer**, og deretter velger du prislisten du vil kopiere.
   * Hvis du vil legge til varer manuelt i rutenettet i feltet **Produkttype**, velger du produkttypen prislisten gjelder for. Fyll ut resten av feltene etter behov, avhengig av det du har valgt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynne å bruke prislisten, går du til **Status**-feltet og velger **Aktiv**.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Salgfakturarabatter og servicegebyrer
Når du bruker fakturarabatter, er totalbeløpet på fakturaen som fastsetter størrelsen på rabatten som gis. På siden **Kundefakturarabatter** kan du også legge til et gebyr i fakturaer som overstiger et bestemt beløp.  

Før du kan bruke fakturarabatter i forbindelse med salg, må du angi bestemte opplysninger. Du må bestemme følgende:  

- hvilke kunder som skal gis denne rabatten  
- hvilken rabattprosent du vil bruke  

Hvis du vil at fakturarabatter skal beregnes automatisk, angir du dette på siden **Salgsoppsett**.  

For hver kunde kan du angi om du vil gi fakturarabatter hvis kravene er innfridd (det vil si hvis fakturabeløpet er stort nok). Du kan definere betingelsene for fakturarabatten i NOK for innenlandske kunder, og i fremmed valuta for kunder i utlandet.  

Du knytter rabattprosentene til bestemte fakturabeløp på siden **Kundefakturarabatter** for hver kunde. Du kan angi den prosentsatsen du vil ha. Hver kunde kan ha en egen side, eller du kan knytte flere kunder til den samme siden.  

I tillegg til (eller i stedet for) en rabattprosent, kan du knytte et gebyrbeløp til et bestemt fakturabeløp.  

> [!TIP]  
> Før du angir disse opplysningene, er det lurt å sette opp en oversikt over hvilken rabattstruktur du vil bruke. Dermed er det enklere å se hvilke kunder som kan knyttes til den samme fakturarabattsiden. Jo færre sider du må definere, jo raskere kan du angi de grunnleggende opplysningene.

Hvis du vil ha opplæring innen rabatter i salg, kan du se [Definere rabatter for kundene](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

### <a name="calculating-invoice-discounts-on-sales"></a>Beregne fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Definere en salgslinjerabatt for en kunde
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonensoppdateringen **Ny salgsprisopplevelse**. 

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Linjerabatter**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en salgslinjerabatt for kunden.

> [!Note]
> Når du åpner sidene **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, angis feltene **Salgstypefilter** og **Salgskodefilter** for kunden, og de kan ikke endres eller fjernes.
>
> Hvis du vil definere priser eller linjerabatter for alle kunder, en kundeprisgruppe eller en kampanje, må du åpne sidene fra et varekort. Du kan eventuelt bruke siden **Salgsprisforslag** for salgspriser. Hvis du vil ha mer informasjon, se [Slik samleoppdaterer du varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Salgsprislister**.
3. Åpne prislisten der du vil angi linjerabatt.
4. Slå på **Tillat linjerabatt**.
5. Opprett en ny linje, eller velg en eksisterende linje, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. I **Definerer**-feltet velger du enten **Pris og rabatt** eller bare **Rabatt**. 
7. Angi rabattprosenten i feltet **Linjerabatt-%**.

    > [!TIP]
    > Hvis du skal redigere en eksisterende linje, kan du filtrere linjene ved å velge et passende alternativ i feltet **Vis kolonner for**.

    > [!NOTE]  
    > Fakturarabattkoder representeres av eksisterende kundekort. Dette lar deg raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene. Hvis du vil definere kundespesifikke fakturarabattbetingelser, angir du feltet **Fakturarabattkode** til kundens kundekode, og deretter går du videre til neste trinn.

8. På siden **Kundekort** velger du handlingen **Fakturarabatter**. Siden **Kundefakturarabatter** åpnes.
9. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i den lokale valutaen.
10. I **Minimumsbeløp**-feltet kan du eventuelt angi hva som er minstebeløpet for at det skal gis rabatt i en faktura.
11. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
12. Gjenta trinn 5 til 7 for hver valuta som kunden vil motta en forskjellig fakturarabatt for.

Fakturarabatten er nå definert og tilordnet til kunden. Når du velger kundekoden i **Fakturarabattkode**-feltet på andre kundekort, tilordnes den samme fakturarabatten til kundene.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Definere en fakturarabatt for en kunde
Når du har bestemt hvilke kunder som skal gis fakturarabatter, angir du fakturarabattkode på kundekortet og definerer betingelsene for hver kode.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Åpne kundesiden for kunden som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for kunden. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Fakturarabattkoder representeres av eksisterende kundekort. Dette lar deg raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene.

Fortsett å definere nye betingelser for salgsfakturarabatt.

1. På siden **Kunder** velger du handlingen **Fakturarabatter**. Siden **Kundefakturarabatter** åpnes.
2. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i den lokale valutaen.
3. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
4. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
5. Gjenta trinn 5 til 7 for hver valuta som kunden vil motta en forskjellig fakturarabatt for.

## <a name="to-copy-sales-prices"></a>Slik kopierer du salgspriser
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonensoppdateringen **Ny salgsprisopplevelse**. 

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)  

Hvis du vil kopiere salgspriser, for eksempel salgsprisen for en enkelt kunde som skal brukes i en kundeprisgruppe, må du utføre kjørselen **Foreslå salgspris i forslag**. kjørselen på siden **Salgspris i forslag**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå salgspris i forslag.** .  
3. I hurtigfanen **Salgspriser** fyller du ut feltene **Salgstype** og **Salgskode** med de opprinnelige salgsprisene du vil kopiere.  
4. På den øverste delen av forespørselssiden fyller du ut feltene **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.  
5. Hvis du vil at kjørselen skal opprette nye priser, velger du avmerkingsboksen **Opprett nye priser**.  
6. Velg **OK**-knappen for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene, noe som angir at de er gyldige for den valgte salgstypen.  

   > [!NOTE]  
   > Denne kjørselen oppretter forslag, men implementerer ikke de foreslåtte endringene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si legge dem inn på siden **Salgspriser**, velger du handlingen **Implementer prisendringer** på siden **Salgsprisforslag**.

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

Statusen for prislistelinjen må være **Utkast**. 

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsprislister**, og velg deretter den relaterte koblingen. 
2. Velg prislisten du vil kopiere, og velg deretter **Kopier linjer**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan ikke ha to linjer som har samme innstillinger, men forskjellige priser. Hvis dette skjer, vises en melding når du aktiverer en prisliste. Du kan velge hvilken pris som skal brukes, ved å åpne listen og slette den uriktige prisen.  
  
---

## <a name="to-bulk-update-item-prices"></a>Slik samleoppdaterer du varepriser
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonensoppdateringen **Ny salgsprisopplevelse**. 

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)

Hvis du vil oppdatere varepriser satsvis, for eksempel øke alle varepriser med en bestemt prosentdel, må du kjøre **Foreslå varepris i forslag** Kjørselen . Du finner en kobling til den satsvise jobben på siden **Salgsprisforslag**.  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå varepris i forslag** .  
3. I hurtigfanen **Vare** fyller du ut **Nr.** eller **Bokføringsgruppe - lager** eller andre felt med de opprinnelige salgsprisene du vil oppdatere.  
4. På den øverste delen av forespørselssiden fyller du ut **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.
5. Hvis du vil at kjørselen skal justere foreslåtte salgspriser automatisk, kan du angi justeringen i feltet **JUusteringsfaktor**. Du kan for eksempel angi 1,15 i **Justeringsfaktor** for 15 % økning av vareprisen.  
6. Hvis du vil at kjørselen skal opprette nye priser, velger du feltet **Opprett nye priser**.  
7. Velg **OK**-knappen for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene, noe som angir at de er gyldige for den valgte **Vare**.  

> [!NOTE]
> Denne kjørselen oppretter forslag, men implementerer ikke de foreslåtte endringene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si legge dem inn i tabellen **Salgspriser**, kan du bruke kjørselen **Implementer prisendringer**, som du finner i fanebladet **Handlinger**, i gruppen **Funksjoner**, på siden **Salgsprisforslag**.

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)

Hvis du vil oppdatere priser for flere varer, må du opprette en ny prisliste og deretter kopiere linjene fra en eksisterende prisliste. Når du kopierer linjene, kan du bruke filtre til å angi hva som skal kopieres, og du kan angi et heltall eller et desimaltall i feltet **Justeringsfaktor** for å øke eller redusere prisene. Prislisten må være i **Utkast**-status. Om nødvendig kan du deaktivere den gamle prislisten.

> [!NOTE]
> Du kan ikke ha to linjer som har samme innstillinger, men forskjellige priser. Hvis dette skjer, vises en melding når du aktiverer en prisliste. Du kan velge hvilken pris som skal brukes, ved å åpne listen og slette den uriktige prisen.  

---

## <a name="best-price-calculation"></a>Beregning av beste pris
Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[d365fin](includes/d365fin_md.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer.

Den beste prisen er den lavest tillatte prisen med den størst tillatte linjerabatten på denne en gitt dato. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner dette automatisk når det setter inn salgsprisen og linjerabattprosenten for varer på nye dokument- og kladdelinjer.

> [!NOTE]  
> Det følgende beskriver hvordan den beste prisen beregnes for salg. Beregningen er den samme for kjøp.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer kombinasjonen av faktura til-kundenr. og varen og beregner deretter den aktuelle prisen/linjerabattprosenten ved hjelp av disse kriteriene:

    - Har kunden en avtale om pris/rabatt, eller tilhører kunden en gruppe som har det?
    - Er varen eller varerabattgruppen på linjen tatt med i noen av disse avtalene om pris/rabatt?
    - Er ordredatoen (eller bokføringsdatoen for fakturaen eller kreditnotaen) innenfor start- og sluttdatoen for avtalen om pris/rabatt?
    - Er det angitt en enhetskode? I så fall kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)] om det finnes priser/rabatter med samme enhetskode, og priser/rabatter uten enhetskode.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer om avtaler om pris/rabatt gjelder for informasjon om dokument- eller journallinjen, og setter deretter inn den aktuelle enhetsprisen og rabattprosent, ved hjelp av følgende kriterier:

    - Er det et minimumsbehov i pris/rabatt-avtalen som er oppfylt?
    - Er det et valutabehov i pris/rabatt-avtalen som er oppfylt? I så fall settes den laveste prisen og den høyeste linjerabatten inn for valutaen, selv om NOK gir en bedre pris. Hvis det ikke finnes noen pris/rabatt-avtale for den angitte valutakoden, setter [!INCLUDE[d365fin](includes/d365fin_md.md)] inn den laveste prisen og den høyeste linjerabatten i NOK.

Hvis ingen spesialpris kan beregnes for varen på linjen, blir enten den siste direkte kostnaden eller salgsprisen fra varekortet satt inn.

## <a name="see-related-training-at-microsoft-learn"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]