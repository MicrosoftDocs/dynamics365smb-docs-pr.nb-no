---
title: Definere spesielle salgspriser og rabatter for kunder | Microsoft-dokumentasjon
description: "Beskriver hvordan du kan definere alternative priser og rabattavtaler du vil bruke i salgsdokumenter når du selger til ulike kunder."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3bb16f6f192e3a3ca29911cf6215fe1f00bfcb68
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Registrere spesielle salgspriser og rabatter
De ulike pris- og rabattavtalene som gjelder ved salg til ulike kunder, må defineres slik at de avtalte reglene og verdiene brukes på salgsdokumenter du oppretter for kundene.

Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[d365fin](includes/d365fin_md.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer. Du finner mer informasjon under «Beregning av beste pris».

Når det gjelder priser, kan du sette inn en spesialsalgspris på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start-/sluttdato finnes.

Når det gjelder rabatter, kan du opprette og bruke to typer salgsrabatter:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabatt** |Et rabattbeløp som settes inn på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start-/sluttdato finnes. Dette fungerer på samme måte som for salgspriser. |
| **Fakturarabatt** |En prosentrabatt som trekkes fra dokumenttotalen hvis beløpet for alle linjer på et salgsdokument overskrider et bestemt minimumsbeløp. |

Ettersom salgspriser og salgslinjerabatter er basert på en kombinasjon av vare og kunde, kan du også utføre denne konfigurasjon fra varekortet for varen der reglene og verdiene skal brukes.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Definere salgspriser for en kunde
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Priser**.

    Feltet **Salgstype** er forhåndsutfylt med **Kunde**, og feltet **Salgskode** er forhåndsutfylt med kundenummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en spesialsalgspris for kunden.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Definere en salgslinjerabatt for en kunde
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Linjerabatter**.

    Feltet **Salgstype** er forhåndsutfylt med **Kunde**, og feltet **Salgskode** er forhåndsutfylt med kundenummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en salgslinjerabatt for kunden.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Definere en fakturarabatt for en kunde
Når du har bestemt hvilke kunder som skal gis fakturarabatter, angir du fakturarabattkode på kundekortet og definerer betingelsene for hver kode.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kundekortet for kunden som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for kunden.

    > [!NOTE]  
>   Fakturarabattkoder representeres av eksisterende kundekort. Dette lar deg raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene.

    Fortsett å definere nye betingelser for salgsfakturarabatt.
4. I vinduet **Kundekort** velger du handlingen **Fakturarabatter**. Vinduet **Kundefakturarabatter** åpnes.
5. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i USD.
6. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
7. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
8. Gjenta trinn 5 til 7 for hver valuta som kunden vil motta en forskjellig fakturarabatt for.

Fakturarabatten er nå definert og tilordnet til den aktuelle kunden. Når du velger kundekoden i **Fakturarabattkode**-feltet på andre kundekort, tilordnes den samme fakturarabatten til kundene.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Arbeide med salgfakturarabatter og servicegebyrer
Når du bruker fakturarabatter, er det størrelsen på fakturabeløpet som fastsetter størrelsen på rabatten som gis.  

I vinduet **Kundefakturarabatter** kan du også legge til et gebyr i fakturaer som overstiger et bestemt beløp.  

Før du kan bruke fakturarabatter i forbindelse med salg, må du angi bestemte opplysninger i programmet. Du må angi:  

- hvilke kunder som skal gis denne rabatten.  
- hvilken rabattprosent du vil bruke.  

Hvis du vil at fakturarabatter skal beregnes automatisk, angir du dette i vinduet **Salgsoppsett**.  

For hver kunde kan du angi om du vil gi fakturarabatter hvis kravene er innfridd (det vil si hvis fakturabeløpet er stort nok). Du kan definere betingelsene for fakturarabatten i NOK for innenlandske kunder, og i fremmed valuta for kunder i utlandet.  

Du knytter rabattprosentene til bestemte fakturabeløp i vinduene **Kundefakturarabatter**. Du kan angi den prosentsatsen du vil ha i hvert vindu. Hver kunde kan ha et eget vindu, eller du kan knytte flere kunder til det samme vinduet.  

I tillegg til (eller i stedet for) en rabattprosent, kan du knytte et gebyrbeløp til et bestemt fakturabeløp.  

> [!TIP]  
>  Før du angir disse opplysningene i programmet, er det lurt å sette opp en oversikt over hvilken rabattstruktur du vil bruke. Dermed er det enklere å se hvilke kunder som kan knyttes til det samme fakturarabattvinduet. Jo færre vinduer du må definere, jo raskere kan du angi de grunnleggende opplysningene.  

## <a name="best-price-calculation"></a>Beregning av beste pris
Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[d365fin](includes/d365fin_md.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer.

Den beste prisen er den lavest tillatte prisen med den størst tillatte linjerabatten på denne en gitt dato. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner dette automatisk når det setter inn salgsprisen og linjerabattprosenten for varer på nye dokument- og kladdelinjer.

> [!NOTE]  
>   Det følgende beskriver hvordan den beste prisen beregnes for salg. Beregningen er den samme for kjøp.

1. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer kombinasjonen av faktura til-kuindenr. og varen og beregner deretter den aktuelle prisen/linjerabattprosenten ved hjelp av disse kriteriene:

    - Har kunden en avtale om pris/rabatt, eller tilhører kunden en gruppe som har det?
    - Er varen eller varerabattgruppen på linjen tatt med i noen av disse avtalene om pris/rabatt?
    - Er ordredatoen (eller bokføringsdatoen for fakturaen eller kreditnotaen) innenfor start- og sluttdatoen for avtalen om pris/rabatt?
    - Er det angitt en enhetskode? I så fall kontrollerer [!INCLUDE[d365fin](includes/d365fin_md.md)] om det finnes priser/rabatter med samme enhetskode, og priser/rabatter uten enhetskode.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer om avtaler om pris/rabatt gjelder for informasjon om dokument- eller journallinjen, og setter deretter inn den aktuelle enhetsprisen og rabattprosent, ved hjelp av følgende kriterier:

    - Er det et minimumsbehov i pris/rabatt-avtalen som er oppfylt?
    - Er det et valutabehov i pris/rabatt-avtalen som er oppfylt? I så fall settes den laveste prisen og den høyeste linjerabatten inn for valutaen, selv om NOK gir en bedre pris. Hvis det ikke finnes noen pris/rabatt-avtale for den angitte valutakoden, setter [!INCLUDE[d365fin](includes/d365fin_md.md)] inn den laveste prisen og den høyeste linjerabatten i NOK.

Hvis ingen spesialpris kan beregnes for varen på linjen, blir enten den siste direkte kostnaden eller salgsprisen fra varekortet satt inn.

## <a name="to-copy-sales-prices"></a>Slik kopierer du salgspriser  
Hvis du vil kopiere salgspriser, for eksempel salgsprisen for en enkelt kunde som skal brukes i en kundeprisgruppe, må du utføre kjørselen **Foreslå salgspris i forslag**. Kjørselen . Du finner kjørselen i vinduet **Salgspris i forslag**.    

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Foreslå salgspris i forslag.** .  
3.  I hurtigfanen **Salgspriser** fyller du ut feltene **Salgstype** og **Salgskode** med de opprinnelige salgsprisene du vil kopiere.  
4.  I den øverste delen av forespørselsvinduet fyller du ut **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.  
5.  Hvis du vil at kjørselen skal opprette nye priser, velger du feltet **Opprett nye priser**.  
6.  Velg **OK**-knappen for å fylle ut linjene i vinduet **Salgsprisforslag** med de foreslåtte nye prisene, noe som angir at de er gyldige for den valgte **salgstypen**.  

> [!NOTE]  
>  Denne kjørselen oppretter forslag, men implementerer ikke de foreslåtte endringene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si legge dem inn i tabellen **Salgspriser**, kan du bruke kjørselen **Implementer prisendringer**, som du finner i fanebladet **Handlinger**, i gruppen **Funksjoner**, i vinduet **Salgsprisforslag**.

## <a name="see-also"></a>Se også
[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

