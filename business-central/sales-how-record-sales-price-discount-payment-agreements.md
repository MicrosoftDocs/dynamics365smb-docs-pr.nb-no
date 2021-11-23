---
title: Definer salgspriser og rabatter for kunder | Microsoft-dokumentasjon
description: Beskriver hvordan du definerer og bruker pris- og rabattavtaler for salgsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 8b7943caba8482e39217307be904f368f0ec31c0
ms.sourcegitcommit: a9e2aaee735870af566db68532cfa697347d68e0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752433"
---
# <a name="record-sales-prices-and-discounts"></a>Registrer salgspriser og rabatter
> [!NOTE]
> I lanseringsbølge 2 i 2020 lanserte vi strømlinjeformede prosesser for å definere og håndtere priser og rabatter. Hvis du er en ny kunde som bruker denne versjonen, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] støtter forskjellige prisstrategier, som går fra modeller med én pris som passer alle modeller der en vare alltid selges med samme pris, til spesielle prisavtaler med bestemte kunder, kundegrupper eller spesialtilbud når du kjører en salgskampanje. Du kan for eksempel tilby en spesialpris på en ordre under følgende betingelser:

* når det gjelder et minimumsantall
* det gjelder en bestemt type vare  
* hvis den opprettes under en bestemt tidsperiode

Hvis du vil bruke en grunnleggende prismodell, trenger du bare å angi en salgspris for en vare eller ressurs. Denne prisen brukes alltid på salgsdokumenter. For mer avanserte modeller, for eksempel når du kjører en salgskampanje og vil tilby spesialpriser, kan du angi kriterier for det på siden **Salgspriser**. Du kan gi spesialpriser basert på kombinasjoner av følgende: 

* Kunde
* Vare
* Måleenhet
* Minimumsantall
* Datointervaller som angir når prisene er gyldige

Når du har definert spesialpriser, kan [!INCLUDE[prod_short](includes/prod_short.md)] i tillegg automatisk beregne den beste prisen for salgs- og kjøpsdokumenter og på prosjekt- og varekladdelinjer. Du finner mer informasjon under [Beregning av beste pris](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

For salgsrabatter kan du opprette og bruke følgende typer:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabatt** |Et beløp som brukes på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start- og sluttdato finnes. Disse kombinasjonene fungerer på samme måte som for salgspriser. |
| **Fakturarabatt** |En rabattprosent som trekkes fra dokumenttotalen for salg hvis summen av alle linjer i dokumentet overskrider et bestemt minimumsbeløp. |

> [!TIP]  
> Hvis en vare aldri noensinne skal selges med rabatt, kan du la rabattfeltene på varesiden være tomme, og ikke ta med varen i noen av linjerabattoppsettene.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Definere salgspriser for en kunde

Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse. 

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Priser**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en spesialsalgspris for kunden.

---

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  
Som standard er statusen for nye prislister Utkast. Prislister for utkast er ikke inkludert i prisberegninger. Når du er ferdig med å legge til linjer og vil begynne å bruke prisene, kan du endre statusen til aktiv.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Kunder** og velger den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Salgsprislister**. 
3. Velg **Ny** for å opprette en ny salgsprisliste.
4. Fyll ut feltene i hurtigfanen **Generelt** og **Avgift**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Du kan legge til varer i listen på følgende måter:
   * Hvis du vil legge til mange varer, velger du **Foreslå linjer** og angir deretter filterkriterier for å angi hvilke typer varer du vil legge til. Du kan eventuelt angi andre innstillinger for varene. Disse innstillingene gjelder bare prislisten. Du kan endre dem senere ved behov.
   * Hvis du vil kopiere varer fra en annen prisliste, velger du **Kopier linjer**, og deretter velger du prislisten du vil kopiere.
   * Hvis du vil legge til varer manuelt i feltet **Produkttype** på en linje, velger du produkttypen prislisten gjelder for. Fyll ut resten av feltene etter behov, avhengig av det du har valgt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynne å bruke prislisten, går du til **Status**-feltet og velger **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Bruk av salgs- og kjøpsprislister
> [!NOTE]
> Hvis du bruker prislister, må administratoren ha aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Hvis du vil ha mer informasjon, kan du se [Aktivering av kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management).

I feltene **Gjelder type** og **Gjelder nr.** kan du velge hva en prisliste skal gjelde for, for eksempel kunde eller kundeprisgruppe. Bruk feltet **Vis kolonner for** for å vise kolonner som bare er relevante for angivelse av priser, rabatter eller priser og rabatter.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertering av eksisterende priser når du aktiverer prisfunksjonsoppdateringen
Når du aktiverer funksjonsoppdateringen **Ny salgsprisopplevelse** på siden **Funksjonsstyring**, åpnes veiledningen **Funksjonsdataoppdatering**. Bruk vekslebryteren **Bruk standardpriser** slik:

* Hvis du vil arbeide med alle prisene på én side, aktiverer du den. Eksisterende priser konverteres til én standard prisliste for hver av disse:

    * Salg
    * Innkjøp
    * Prosjektsalg
    * Prosjektkjøp 

    Etterpå kan du redigere alle prisene for disse områdene på siden **Prisforslag**. Standard prislister angis på sidene **Salgsoppsett**, **Kjøpsoppsett** og **Prosjektoppsett**. 

    > [!NOTE]
    > Hvis priser bare er angitt for vare- eller ressurskort, vil ikke standard prislister bli fylt ut med disse prisene under dataoppdatering. Du kan imidlertid åpne en hvilken som helst av standard prislister eller på siden Prisforslag og bruke handlingen **Foreslå linjer** til å legge til prisene angitt på vare- eller ressurskort. 

* Hvis du vil bruke salgsprislister, deaktiverer du den. Eksisterende priser blir konvertert til en ny prisliste for hver kombinasjon av kunde, kundegruppe eller kampanje, og start- og sluttdatoer og valuta. Hvis du har mange kombinasjoner, vil du ha mange prislister.

Hvis du allerede har aktivert den nye prisopplevelsen, kan du opprette standard prislister manuelt eller angi en eksisterende prisliste som standard. Hvis du vil angi en eksisterende prisliste som standard, aktiverer du alternativet **Tillat oppdatering av standardverdier** på prislisten. Angi prislisten som standard på sidene **Salgsoppsett**, **Kjøpsoppsett** eller **Prosjektoppsett**.

### <a name="editing-active-price-lists"></a>Redigering av aktive prislister
Hvis du vil la andre redigere priser for aktive prislister for varer, ressurser, kunder, leverandører eller andre enheter som bruker priser, kan du aktivere funksjonen **Tillat redigering av aktiv pris** på sidene **Salgsoppsett** og **Kjøpsoppsett**. 

Når alternativet **Tillat redigering av aktiv pris** er deaktivert, for å oppdatere priser i en prisliste, må du endre statusen for prislisten til **Utkast**, foreta endringen og deretter aktivere prislisten på nytt.

Siden **Prisoversikt** gir en oversikt over alle prisene på tvers av prislister. Du kan angi filtre for å begrense listen. Når du har endret priser, må du bruke handlingen **Bekreft linjer** til å bekrefte prisene mot andre prislistelinjer. Hvis du for eksempel kontrollerer prisene, unngår du duplikater eller avvikende priser. 

> [!NOTE]
> Når du redigerer en linje i en aktiv prisliste, endres statusen for linjen til Utkast, og linjen tas ikke med i prisberegninger før du bruker handlingen **Bekreft linjer**. Når du har kontrollert prisen, aktiveres linjens status, og den brukes i prisberegninger.

Hvis du vil legge til nye priser, bruker du handlingen **Legg til nye linjer** på siden **Prisoversikt**. Siden **Prisforslag** åpnes, der du legger til prislinjer på følgende måter:

* Ved å foreslå dem basert på kriterier
* Kopiere dem fra andre prislister
* Angi dem manuelt. 

Etterpå kan du bruke handlingen **Implementer prisendring** til å sammenligne nye priser med andre prislister for å unngå duplikater.

## <a name="to-copy-sales-prices"></a>Slik kopierer du salgspriser
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse.

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

---

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsprislister**, og velg deretter den relaterte koblingen. 
2. Velg prislisten du vil kopiere, og velg deretter **Kopier linjer**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan ikke ha to linjer som har samme innstillinger, men forskjellige priser. Hvis dette skjer, vises en melding når du aktiverer en prisliste. Du kan velge hvilken pris som skal brukes, ved å åpne listen og slette den uriktige prisen.  
  
---

## <a name="to-bulk-update-item-prices"></a>Slik samleoppdaterer du varepriser
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse.

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)

Hvis du vil oppdatere varepriser satsvis, for eksempel øke alle varepriser med en bestemt prosentdel, kan du fylle ut **Salgsprisforslag** ved å bruke følgende satsvise jobber:

* **Foreslå varepris i forslag** foreslår endringer ved å bruke en justeringsfaktor på eksisterende salgspriser, eller ved å kopiere eksisterende salgsprisavtaler til andre kunde, kundeprisgrupper eller salgskampanjer.
* **Foreslå varepris i forslag** foreslår endringer ved å bruke en justeringsfaktor på eksisterende salgspriser på varekort, eller ved å foreslå priser for nye kombinasjoner av valuta, enheter og så videre. Enhetsprisene på varer endres ikke.    

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå varepris i forslag** .  
3. I hurtigfanen **Vare** fyller du ut **Nr.** eller **Bokføringsgruppe - lager** eller andre felt med de opprinnelige salgsprisene du vil oppdatere.  
4. På den øverste delen av forespørselssiden fyller du ut **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.
5. Hvis du vil at kjørselen skal justere foreslåtte salgspriser automatisk, kan du angi justeringen i feltet **JUusteringsfaktor**. Du kan for eksempel angi **1,15** i **Justeringsfaktor** for **15 %** økning av vareprisen.  
6. Hvis du vil at kjørselen skal opprette nye priser, slår du på vekslebryteren **Opprett nye priser**.  
7. Velg **OK** for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene.
8. Når du skal implementere forslagene, bruker du handlingen **Implementer prisendringer**. Den satsvise jobben oppretter forslag, men implementerer dem ikke.

---

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)

Hvis du vil oppdatere priser for flere varer, må du opprette en ny prisliste og deretter kopiere linjene fra en eksisterende prisliste. Når du kopierer linjene, kan du bruke filtre til å angi hva som skal kopieres, og du kan angi et heltall eller et desimaltall i feltet **Justeringsfaktor** for å øke eller redusere prisene. Prislisten må være i **Utkast**-status. Om nødvendig kan du deaktivere den gamle prislisten.

> [!NOTE]
> Du kan ikke ha to linjer som har samme innstillinger, men forskjellige priser. Hvis dette skjer, vises en melding når du aktiverer en prisliste. Du kan velge hvilken pris som skal brukes, ved å åpne listen og slette den uriktige prisen.  

## <a name="sales-invoice-discounts-and-service-charges"></a>Salgfakturarabatter og servicegebyrer
Når du bruker fakturarabatter, er totalbeløpet på fakturaen som fastsetter størrelsen på rabatten som gis. På siden **Kundefakturarabatter** kan du også legge til et gebyr i fakturaer som overstiger et bestemt beløp.  

Hvis du vil at fakturarabatter skal beregnes automatisk, slår du på vekslebryteren **Beregn fak.rabatt** på siden **Salgsoppsett**.  

For hver kunde kan du angi om du vil tilby fakturarabatter hvis kriteriene oppfylles. Hvis for eksempel faktura beløpet er stort nok. Du kan definere betingelsene for fakturarabatten i NOK for innenlandske kunder, og i fremmed valuta for kunder i utlandet.  

Du knytter rabattprosentene til bestemte fakturabeløp på siden **Kundefakturarabatter** for hver kunde. Du kan angi den prosentsatsen du vil ha. Hver kunde kan ha en egen side, eller du kan knytte flere kunder til den samme siden.  

I tillegg til, eller i stedet for, en rabattprosent, kan du knytte et gebyrbeløp til et bestemt fakturabeløp.  

Hvis du vil ha opplæring innen rabatter i salg, kan du se [Definere rabatter for kundene](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

---

### <a name="calculating-invoice-discounts-on-sales"></a>Beregne fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Definere en salgslinjerabatt for en kunde
Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse.

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Linjerabatter**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en salgslinjerabatt for kunden.

> [!Note]
> Når du åpner sidene **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, angis feltene **Salgstypefilter** og **Salgskodefilter** for kunden, og de kan ikke endres eller fjernes.
>
> Hvis du vil definere priser eller linjerabatter for alle kunder, en kundeprisgruppe eller en kampanje, må du åpne sidene fra et varekort. Du kan eventuelt bruke siden **Salgsprisforslag** for salgspriser. Hvis du vil ha mer informasjon, se [Slik samleoppdaterer du varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

---

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Salgsprislister**.
3. Åpne prislisten der du vil angi linjerabatt.
4. Opprett en ny linje, eller velg en eksisterende linje, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. I **Definerer**-feltet velger du enten **Pris og rabatt** eller bare **Rabatt**. 
6. Angi rabattprosenten i feltet **Linjerabatt-%**.

    > [!TIP]
    > Du kan filtrere linjene ved å velge et passende alternativ i feltet **Vis kolonner for**.
    > [!NOTE]  
    > Fakturarabattkoder representeres av eksisterende kundekort. Ved å bruke kundenavn og koder kan du raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene. Hvis du vil definere kundespesifikke fakturarabattbetingelser, angir du feltet **Fakturarabattkode** til kundens kundekode, og deretter går du videre til neste trinn.
---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Definere en fakturarabatt for en kunde
Når du har bestemt hvilke kunder som skal gis fakturarabatter, angir du fakturarabattkode på kundekortet og definerer betingelsene for hver kode.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kundesiden for kunden som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for kunden. 

> [!NOTE]  
> Fakturarabattkoder representeres av eksisterende kundekort. Ved å bruke kundenavn og koder kan du raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene.

Nå kan du definere nye betingelser for salgsfakturarabatt.

1. På siden **Kunder** velger du handlingen **Fakturarabatter**. Siden **Kundefakturarabatter** åpnes.
2. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i NOK.
3. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
4. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
5. Gjenta trinn 5 til 7 for hver valuta som kunden vil motta en forskjellig fakturarabatt for.

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