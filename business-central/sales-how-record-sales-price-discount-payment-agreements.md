---
title: Registrere spesielle salgspriser og rabatter
description: Beskriver hvordan du definerer pris- og rabattavtaler for salgsdokumenter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 7022, 7024
ms.date: 06/03/2022
ms.author: bholtorf
ms.openlocfilehash: 5560a9a1b5c5eb031136a7c1320019eac75239e0
ms.sourcegitcommit: a9c778b65925435a4099fad45b3611f310e0b203
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9652195"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere spesielle salgspriser og rabatter

> [!NOTE]
> I lanseringsbølge 2 for 2020 lanserte vi nye, effektive fremgangsmåter for å definere og håndtere priser og rabatter. Hvis du er en ny kunde som bruker den nyeste versjonen, bruker du den nye opplevelsen. Hvis du er en eksisterende kunde, vil din bruk av den nye funksjonen avhenge av om administratoren har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Lær mer på [Aktiver kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrasjonsinnholdet.

[!INCLUDE[prod_short](includes/prod_short.md)] støtter forskjellige prisstrategier, for eksempel:

* Én-pris-passer-alle-modeller der en vare alltid selges til samme pris.
* Spesielle prisavtaler med bestemte kunder eller kundegrupper.
* Kampanjer når et salg oppfyller kriteriene for et spesialtilbud. Vilkår kan for eksempel være når en ordre oppfyller et minimumsantall, er før en bestemt dato eller inneholder en bestemt type vare.  

Hvis du vil bruke en grunnleggende prismodell, trenger du bare å angi en enhetspris når du konfigurerer en vare eller ressurs. Denne prisen brukes alltid på salgsdokumenter. For mer avanserte modeller, for eksempel når du vil tilby spesialpriser for en salgskampanje, kan du angi kriterier for det på siden **Enhetspriser**. Du kan gi spesialpriser basert på en kombinasjon av følgende informasjon:  

* Kunde
* Vare
* Måleenhet
* Minimumsantall
* Datoer som definerer perioden som prisene gjelder.

Når du har definert spesialpriser, kan [!INCLUDE[prod_short](includes/prod_short.md)] automatisk beregne de beste prisene for salgs- og kjøpsdokumenter og på prosjekt- og varekladdelinjer. Lær mer under [Best prisberegning](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Du kan konfigurere to typer rabatter for salgsrabatter:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabatt** |Et beløp settes inn på salgslinjer hvis de inneholder en bestemt kombinasjon av kunde, vare, minste antall, enhet, start- og sluttdato finnes. Denne typen fungerer på samme måte som for salgspriser. |
| **Fakturarabatt** |En rabattprosent som trekkes fra dokumenttotalen for salg hvis summen av alle linjer i dokumentet overskrider et bestemt minimumsbeløp. |

> [!TIP]  
> Hvis en vare aldri noensinne skal selges med rabatt, kan du la rabattfeltene på varesiden være tomme, og ikke ta med varen i noen av linjerabattoppsettene.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Definere salgspriser for en kunde

Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse. 

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Priser**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en spesialsalgspris for kunden.

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

Som standard er statusen for nye prislister **Utkast**. Prislister for utkast er ikke inkludert i prisberegninger. Når du er ferdig med å legge til linjer og vil begynne å bruke prisene, kan du endre statusen til **aktiv**.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Salgsprislister**. 
3. Velg **Ny** for å opprette en ny salgsprisliste.
4. Fyll ut feltene i hurtigfanen **Generelt** og **Avgift**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Hvis du vil legge til elementer i oversikten, gjør du en av følgende fremgangsmåte:
   * Hvis du vil legge til mange varer, velger du **Foreslå linjer** og angir deretter filterkriterier for å angi hvilke typer varer du vil legge til. Du kan eventuelt angi andre innstillinger for varene som er spesifikke for prislisten. Du kan endre disse innstillingene senere ved behov.
   * Hvis du vil kopiere varer fra en annen prisliste, velger du **Kopier linjer**, og deretter velger du prislisten du vil kopiere.
   * Hvis du vil legge til varer manuelt i rutenettet i feltet **Produkttype**, velger du produkttypen prislisten gjelder for. Fyll ut resten av feltene etter behov, avhengig av det du har valgt. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Hvis du vil begynne å bruke prislisten, går du til **Status**-feltet og velger **Aktiv**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Bruk av salgs- og kjøpsprislister

> [!NOTE]
> Hvis du bruker prislister, må administratoren ha aktivert funksjonsoppdateringen **Ny salgsprisopplevelse** i **Funksjonsstyring**. Lær mer på [Aktiver kommende funksjoner på forhånd](/dynamics365/business-central/dev-itpro/administration/feature-management) i administrasjonsinnholdet.

Det meste av den nye salgsprisopplevelsen er lik gjeldende erfaring, men det er noen få forskjeller. Disse forskjellene beskrives nedenfor.

I feltene **Gjelder type** og **Gjelder nr.** kan du velge hva en prisliste skal gjelde for, for eksempel kunde eller kundeprisgruppe. Ved å bruke **Vis kolonner for** kan du vise eller skjule kolonner som er relevante for angivelse av priser, rabatter eller priser og rabatter.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Konvertering av eksisterende priser når du aktiverer prisfunksjonsoppdateringen

Når du aktiverer funksjonsoppdateringen **Ny salgsprisopplevelse** på siden **Funksjonsstyring**, åpnes veiledningen **Funksjonsdataoppdatering**. Bruk vekslebryteren **Bruk standardpriser** slik:

* Hvis du vil arbeide med alle prisene på én side, aktiverer du den. Eksisterende priser konverteres til én standard prisliste for hver av disse dokumentene:

    * Salg
    * Innkjøp
    * Prosjektsalg
    * Prosjektkjøp

    Du kan redigere alle prisene for disse områdene på siden **Prisforslag**. Standard prislister blir angitt på sidene **Salgsoppsett**, **Kjøpsoppsett** og **Prosjektoppsett**. 

> [!NOTE]
> Hvis priser bare er angitt for vare- eller ressurskort, vil ikke standard prislister bli fylt ut med disse prisene under dataoppdateringen. Du kan imidlertid åpne en hvilken som helst av standard prislister eller på siden **Prisforslag** og bruke handlingen **Foreslå linjer** til å legge til prisene angitt på vare- eller ressurskort.

* Hvis du vil bruke salgsprislister, deaktiverer du den. Eksisterende priser konverteres til en ny prisliste for hver kombinasjon av følgende ting: 

* Kunde
* Kundegruppe eller -kampanje
* Start- og sluttdatoer
* Valutaer 

Hvis du har mange kombinasjoner, vil du ha mange prislister.

Hvis du allerede har aktivert den nye prisopplevelsen, kan du opprette standard prislister manuelt eller angi en eksisterende prisliste som standard. Hvis du vil angi en eksisterende prisliste som standard, aktiverer du alternativet **Tillat oppdatering av standardverdier** på prislisten. Angi prislisten som standard på sidene **Salgsoppsett**, **Kjøpsoppsett** eller **Prosjektoppsett**.

### <a name="editing-active-price-lists"></a>Redigering av aktive prislister

Hvis du vil la andre redigere priser for aktive prislister for varer, ressurser, kunder, leverandører eller andre enheter som bruker priser, kan du aktivere funksjonen **Tillat redigering av aktiv pris** på sidene **Salgsoppsett** og **Kjøpsoppsett**.

Når alternativet **Tillat redigering av aktiv pris** er deaktivert, for å oppdatere priser i en prisliste, må du endre statusen for prislisten til **Utkast**, foreta endringen og deretter aktivere prislisten på nytt.

Siden **Prisoversikt** gir en oversikt over alle prisene på tvers av prislister. Du kan definere filtre for å begrense listen med priser du vil endre eller legge til. Når du har endret priser, må du bruke handlingen **Bekreft linjer** til å bekrefte prisene mot andre prislistelinjer. Verifisering av priser bidrar til å unngå duplikater og tvetydighet under prisberegningen.

> [!NOTE]
> Når du redigerer en linje i en aktiv prisliste, endres statusen for linjen til **Utkast**, og linjen tas ikke med i prisberegning før du bruker handlingen **Bekreft linjer**. Når du har kontrollert prisen, blir linjens status **Aktiv**, og den vurderes i prisberegninger.

Hvis du vil legge til nye priser, bruker du handlingen **Legg til nye linjer** på siden **Prisoversikt**. Siden **Forslag** åpnes, og du kan legge til prislinjer enten ved å foreslå dem basert på kriterier, kopiere dem fra andre prislister eller angi dem manuelt. Etterpå kan du bruke handlingen **Implementer prisendring** til å sammenligne nye priser med andre prislister for å unngå duplikater og tvetydighet under prisberegning.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Opprett salgsprislinjer basert på salgsprisen

1. På siden **Prisforslag** velger du handlingen **Foreslå linjer**.
2. På siden **Prislinjer – opprett ny** fyller du ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I feltet **Produktfilter** definerer du filtre for den valgte **produkttypen**.
4. Velg feltet **Standarder** for å angi innstillinger som:
   * Hvilke enheter prislisten skal tildeles.
   * Datoer når prisen er gyldig.
   * Valutakoden.
   * Beløpstypefilteret som definerer kolonnene som vises på prislistelinjene.
5. Velg **OK**. Nye linjer blir lagt til på siden **Prisforslag** med de valgte innstillingene og salgsprisene fra varekortene.
6. Rediger de opprettede linjene med de nye salgsprisene eller rabattene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Opprett salgsprislinjer basert på eksisterende prisliser

1. På siden **Prisforslag** velger du handlingen **Kopier linjer**.
2. På siden **Prislinjer – kopier eksisterende** velger du en eksisterende prisliste i feltet **Fra prisliste**.
3. I feltet **Prislinjefilter** definerer du filtre for varene på den valgte prislisten.
4. Velg feltet **Standarder** for å angi innstillinger som:
   * Hvilke enheter prislisten skal tildeles.
   * Datoer når prisen er gyldig.
   * Valutakoden.
   * Beløpstypefilteret som definerer kolonnene som vises på prislistelinjene.
5. Fyll ut de andre feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Velg **OK**. Nye linjer blir lagt til på siden **Prisforslag** med de valgte innstillingene.
7. Rediger de opprettede linjene med de nye salgsprisene eller rabattene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Slik kopierer du salgspriser

Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse.

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)  

Hvis du vil kopiere salgspriser, for eksempel salgsprisen for en enkelt kunde som skal brukes i en kundeprisgruppe, må du utføre kjørselen **Foreslå salgspris i forslag**. kjørselen på siden **Salgspris i forslag**.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå salgspris i forslag.** .  
3. I hurtigfanen **Salgspriser** fyller du ut feltene **Salgstype** og **Salgskode** med de opprinnelige salgsprisene du vil kopiere.  
4. På den øverste delen av forespørselssiden fyller du ut feltene **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.  
5. Hvis du vil at kjørselen skal opprette nye priser, velger du avmerkingsboksen **Opprett nye priser**.  
6. Velg **OK**-knappen for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene, noe som angir at de er gyldige for den valgte salgstypen.  

   > [!NOTE]  
   > Denne kjørselen oppretter forslag, men implementerer ikke de foreslåtte endringene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si legge dem inn på siden **Salgspriser**, velger du handlingen **Implementer prisendringer** på siden **Salgsprisforslag**.

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

Du kan angi om den nye prislisten skal bruke innstillingene fra overskriften på listen du kopierer, eller innstillingene fra den nye listen du kopierer til. Hvis du vil bruke innstillingene fra prislisten du kopierer priser til, slår du på vekslebryteren **Bruk standarder fra mål**.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsprislister**, og velg deretter den relaterte koblingen. 
2. Velg prislisten du vil kopiere, og velg deretter **Kopier linjer**.
3. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > Du kan ikke ha to elementer som har samme innstillinger, men forskjellige priser. Hvis dette skjer, vises en melding når du aktiverer prislisten. Du kan velge hvilken pris som skal brukes, ved å åpne listen og slette den uriktige prisen.  
  
---

## <a name="to-bulk-update-item-prices"></a>Slik samleoppdaterer du varepriser

Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse.

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)

Hvis du vil oppdatere varepriser satsvis, for eksempel øke alle priser med en bestemt prosentdel, kan du fylle ut siden Enhetsprisforslag ved å bruke følgende satsvise jobber:

* **Foreslå salgspris i forslag** foreslår endringer på en av to måter. enten ved å bruke en justeringsfaktor på eksisterende salgspriser, eller ved å kopiere eksisterende salgsprisavtaler til andre kunde, kundeprisgrupper eller salgskampanjer.
* **Foreslå varepris i forslag** foreslår endringer på en av to måter. enten ved å bruke en justeringsfaktor på eksisterende salgspriser på varekort, eller ved å foreslå priser for nye kombinasjoner av valuta, enheter og så videre. Enhetsprisene på varer endres ikke av denne kjørselen.  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Foreslå varepris i forslag** .  
3. I hurtigfanen **Vare** fyller du ut **Nr.** eller **Bokføringsgruppe - lager** eller andre felt med de opprinnelige salgsprisene du vil oppdatere.  
4. På den øverste delen av forespørselssiden fyller du ut **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.
5. Hvis du vil at kjørselen skal justere foreslåtte salgspriser automatisk, kan du angi justeringen i feltet **JUusteringsfaktor**. Du kan for eksempel angi 1,15 i **Justeringsfaktor** for en 15 % økning av vareprisen.  
6. Hvis du vil at kjørselen skal opprette nye priser, slår du på vekslebryteren **Opprett nye priser**.  
7. Velg **OK**-knappen for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene.
8. Når du skal implementere forslagene, bruker du handlingen **Implementer prisendringer**. Den satsvise jobben oppretter forslag, men implementerer dem ikke. 

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)

Hvis du vil oppdatere priser for flere varer, må du opprette en ny prisliste og deretter kopiere linjene fra en eksisterende prisliste. Når du kopierer linjene, kan du bruke filtre til å angi hva som skal kopieres, og du kan angi et heltall eller et desimaltall i feltet **Justeringsfaktor** for å øke eller redusere prisene. Prislisten må være i **Utkast**-status. Om nødvendig kan du deaktivere den gamle prislisten.

> [!NOTE]
> Du kan ikke ha to linjer som har samme innstillinger, men forskjellige priser. Hvis dette skjer, vises en melding når du aktiverer en prisliste. Du kan velge hvilken pris som skal brukes, ved å åpne listen og slette den uriktige prisen.  

---

## <a name="best-price-calculation"></a>Beregning av beste pris

Når du registrerer spesialpriser og linjerabatter for kjøp og salg, beregner [!INCLUDE[prod_short](includes/prod_short.md)] den beste prisen for salgs- og kjøpsdokumenter og på prosjekt- og varekladdelinjer.

Den beste prisen er den lavest prisen med den størst linjerabatten tillatt på denne en gitt dato. [!INCLUDE[prod_short](includes/prod_short.md)] beregner beste priser når det legger til enhetspriser og linjerabattprosentene på dokument- og kladdelinjer.

> [!NOTE]  
> Det følgende beskriver hvordan den beste prisen beregnes for salg. For innkjøp ligner beregningen, men den er basert på de tilgjengelige parameterne. Varerabattgrupper støttes for eksempel ikke støtte for kjøp.

1. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer kombinasjonen av faktura til-kundenr. og varen og beregner deretter den aktuelle prisen/linjerabattprosenten ved hjelp av disse kriteriene:

    * Har kunden en avtale om pris/rabatt, eller tilhører kunden en gruppe som har det?
    * Er varen eller varerabattgruppen på linjen tatt med i noen av disse avtalene om pris/rabatt?
    * Er ordredatoen (eller bokføringsdatoen for fakturaen eller kreditnotaen) innenfor start- og sluttdatoen for avtalen om pris/rabatt?
    * Er det angitt en enhetskode? I så fall kontrollerer [!INCLUDE[prod_short](includes/prod_short.md)] om det finnes priser/rabatter med samme enhetskode, og priser/rabatter uten enhetskode.

2. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer om pris-/rabattavtaler gjelder informasjon på dokumentet eller kladdelinjen. Deretter settes den aktuelle salgsprisen og linjerabattprosenten inn i følgende kriterier:

    * Er det et minimumsbehov i pris/rabatt-avtalen som er oppfylt?
    * Er det et valutabehov i pris/rabatt-avtalen som er oppfylt? I så fall settes den laveste prisen og den høyeste linjerabatten inn for valutaen, selv om NOK gir en bedre pris. Hvis det ikke finnes noen pris/rabatt-avtale for den angitte valutakoden, setter [!INCLUDE[prod_short](includes/prod_short.md)] inn den laveste prisen og den høyeste linjerabatten i lokal valuta.

Hvis ingen spesialpris kan beregnes for varen på linjen, blir enten den siste direkte kostnaden eller salgsprisen fra varekortet satt inn.

## <a name="sales-invoice-discounts-and-service-charges"></a>Salgfakturarabatter og servicegebyrer

Når du bruker fakturarabatter, er totalbeløpet på fakturaen som fastsetter størrelsen på rabatten som gis. På siden **Kundefakturarabatter** kan du også legge til et gebyr i fakturaer som overstiger et bestemt beløp.  

Før du kan bruke fakturarabatter i forbindelse med salg, må du angi bestemte opplysninger. Du må ta følgende beslutninger:  

* Hvilke kunder skal gis denne rabatten?  
* Hvilken rabattprosent vil du bruke?  

Hvis du vil at fakturarabatter skal beregnes automatisk, slår du på vekslebryteren **Beregn fak.rabatt** på siden **Salgsoppsett**.  

Du kan angi om du vil gi fakturarabatter når en faktura oppfyller visse kriterier for hver kunde. Når for eksempel faktura beløpet er stort nok. Fakturarabatter kan være i lokal valuta for innenlandske kunder eller i utenlandsk valuta for utenlandske kunder.  

Du knytter rabattprosentene til bestemte fakturabeløp på siden **Kundefakturarabatter** for hver kunde. Du kan angi den prosentsatsen du vil ha. Hver kunde kan ha en egen side, eller du kan knytte flere kunder til den samme siden.  

I tillegg til, eller i stedet for, en rabattprosent, kan du knytte et gebyrbeløp til et bestemt fakturabeløp.  

> [!TIP]  
> Før du angir disse opplysningene, er det lurt å sette opp en oversikt over hvilken rabattstruktur du vil bruke. Strukturen gjør det enklere å avgjøre hvilke kunder som kan knyttes til den samme fakturarabattsiden. Jo færre sider du må definere, jo raskere kan du angi de grunnleggende opplysningene.

Hvis du vil ha opplæring innen rabatter i salg, kan du se [Definere rabatter for kundene](/training/modules/customer-discounts-dynamics-365-business-central/index).

### <a name="calculating-invoice-discounts-on-sales"></a>Beregning av fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Definere en salgslinjerabatt for en kunde

Denne fremgangsmåten varierer avhengig av om systemansvarlig har aktivert funksjonsoppdateringen **Ny salgsprisopplevelse**. Hvis funksjonsoppdateringen ikke er aktivert, følger du fremgangsmåten i fanen Gjeldende opplevelse.

#### <a name="current-experience"></a>[Nåværende opplevelse](#tab/current-experience/)  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Linjerabatter**.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en salgslinjerabatt for kunden.

> [!NOTE]
> Når du åpner sidene **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, angis feltene **Salgstypefilter** og **Salgskodefilter** for kunden, og de kan ikke endres eller fjernes.
>
> Hvis du vil definere priser eller linjerabatter for alle kunder, en kundeprisgruppe eller en kampanje, må du åpne sidene fra et varekort. Du kan eventuelt bruke siden **Salgsprisforslag** for salgspriser. Finn ut mer under [Slik samleoppdaterer du varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### <a name="new-experience"></a>[Ny opplevelse](#tab/new-experience/)  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Velg kunden, og velg deretter handlingen **Salgsprislister**.
3. Åpne prislisten der du vil angi linjerabatt.
4. Opprett en ny linje, eller velg en eksisterende linje, og fyll deretter ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. I **Definerer**-feltet velger du enten **Pris og rabatt** eller bare **Rabatt**. 
6. Angi rabattprosenten i feltet **Linjerabatt-%**.

    > [!TIP]
    > Hvis du skal redigere en eksisterende linje, kan du filtrere linjene ved å velge et passende alternativ i feltet **Vis kolonner for**.

    > [!NOTE]  
    > Fakturarabattkoder representeres av eksisterende kundekort. Dette lar deg raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene. Hvis du vil definere kundespesifikke fakturarabattbetingelser, angir du feltet **Fakturarabattkode** til kundens kundekode, og deretter går du videre til neste trinn.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Definere en fakturarabatt for en kunde

Når du bestemmer hvilke kunder som skal gis fakturarabatter, angir du fakturarabattkode på sidene Kundekort. Deretter definerer du betingelsene for hver kode.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kundesiden for kunden som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for kunden.

> [!NOTE]  
> Fakturarabattkoder representeres av eksisterende kundekort. Dette lar deg raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene.

Fortsett å definere nye betingelser for salgsfakturarabatt.

1. På siden **Kunder** velger du handlingen **Fakturarabatter**. Siden **Kundefakturarabatter** åpnes.
2. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder. La feltet stå tomt for å definere betingelser for fakturarabatt i LV.
3. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
4. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
5. Gjenta trinn 5 til 7 for hver valuta som kunden vil motta en forskjellig fakturarabatt for.

## <a name="see-related-microsoft-training"></a>Se relatert [Microsoft-opplæring](/training/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også

[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Konfigurering av kundeprisgrupper](sales-how-to-set-up-customer-price-groups.md)  
[Konfigurering av kunderabattgrupper](sales-how-to-set-up-customer-discount-groups.md)  
[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
