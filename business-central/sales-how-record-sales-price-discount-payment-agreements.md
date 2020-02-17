---
title: Definere spesielle salgspriser og rabatter for kunder | Microsoft-dokumentasjon
description: Beskriver hvordan du kan definere alternative priser og rabattavtaler du vil bruke i salgsdokumenter når du selger til ulike kunder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 02/04/2020
ms.author: sgroespe
ms.openlocfilehash: 820439f8b18026d8a92a07dfe320423381847cb7
ms.sourcegitcommit: 0cb8a646dcba8f6d6336ebd008587874d25f4629
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030271"
---
# <a name="record-special-sales-prices-and-discounts"></a>Registrere spesielle salgspriser og rabatter
De ulike pris- og rabattavtalene som gjelder ved salg til ulike kunder, må defineres slik at de avtalte reglene og verdiene brukes på salgsdokumenter du oppretter for kundene.

Når du har registrert spesielle priser og linjerabatter for salg og innkjøp, sikrer [!INCLUDE[d365fin](includes/d365fin_md.md)] at din fortjeneste på varehandel alltid er optimal ved automatisk å beregne den beste prisen på salgs- og kjøpsdokumenter og på prosjekt- og varekladdlinjer. Du finner mer informasjon under [Beregning av beste pris](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Når det gjelder priser, kan du sette inn en spesialsalgspris på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start-/sluttdato finnes.

Når det gjelder rabatter, kan du opprette og bruke to typer salgsrabatter:

| Rabattype | Beskrivelse |
| --- | --- |
| **Salgslinjerabatt** |Et rabattbeløp som settes inn på salgslinjer hvis en bestemt kombinasjon av kunde, vare, minste antall, enhet, eller start-/sluttdato finnes. Dette fungerer på samme måte som for salgspriser. |
| **Fakturarabatt** |En prosentrabatt som trekkes fra dokumenttotalen hvis beløpet for alle linjer på et salgsdokument overskrider et bestemt minimumsbeløp. |

Ettersom salgspriser og salgslinjerabatter er basert på en kombinasjon av vare og kunde, kan du også utføre denne konfigurasjon fra varekortet for varen der reglene og verdiene skal brukes.

> [!NOTE]  
> Hvis du ikke vil at en vare noen sinne selges til redusert pris, kan du la rabattfeltene på varekortet være tomme, og ikke ta med varen i noen av linjerabatt-oppsettene.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Definere salgspriser for en kunde
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Priser**.

    På siden **Salgspriser** er feltet **Salgstype** forhåndsutfylt med **Kunde**, og feltet **Salgskode** er forhåndsutfylt med kundenummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en spesialsalgspris for kunden.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Definere en salgslinjerabatt for en kunde
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne det aktuelle kundekortet, og velg deretter handlingen **Linjerabatter**.

    På siden **Salgslinjerabatter** er feltet **Salgstype** forhåndsutfylt med **Kunde**, og feltet **Salgskode** er forhåndsutfylt med kundenummeret.
3. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Fyll ut en linje for hver kombinasjon som gir en salgslinjerabatt for kunden.

> [!Note]
> Når du åpner vinduene **Salgspriser** og **Salgslinjerabatter** fra en bestemt kunde, angis feltene **Salgstypefilter** og **Salgskodefilter** for kunden, og de kan ikke endres eller fjernes, angitt av den grå verdien i feltet **Salgskodefilter**.<br /><br />
> Hvis du vil definere priser eller linjerabatter for alle kunder, en kundeprisgruppe eller en kampanje, må du åpne vinduene fra et varekort. Du kan eventuelt bruke siden **Salgsprisforslag** for salgspriser. Hvis du vil ha mer informasjon, se [Slik samleoppdaterer du varepriser](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Definere en fakturarabatt for en kunde
Når du har bestemt hvilke kunder som skal gis fakturarabatter, angir du fakturarabattkode på kundekortet og definerer betingelsene for hver kode.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kunder**, og velg deretter den relaterte koblingen.
2. Åpne kundekortet for kunden som skal ha fakturarabatter.
3. I feltet **Fakturarabattkode** velger du en kode for de aktuelle fakturarabattbetingelsene som skal brukes til å beregne fakturarabatter for kunden.

> [!NOTE]  
>   Fakturarabattkoder representeres av eksisterende kundekort. Dette lar deg raskt tilordne fakturarabattbetingelsene til kunder ved å velge navnet på en annen kunde som har de samme betingelsene.

Fortsett å definere nye betingelser for salgsfakturarabatt.

1. På siden **Kundekort** velger du handlingen **Fakturarabatter**. Siden **Kundefakturarabatter** åpnes.
2. I feltet **Valutakode** angir du koden til en valuta som fakturarabattbetingelsene på linjen gjelder for. La feltet stå tomt for å definere betingelser for fakturarabatt i NOK.
3. I **Minimumsbeløp**-feltet angir du hva som er minstebeløpet for at det skal gis rabatt i en faktura.
4. I **Rabatt-%**-feltet angir du fakturarabatten prosentvis av fakturabeløpet.
5. Gjenta trinn 5 til 7 for hver valuta som kunden vil motta en forskjellig fakturarabatt for.

Fakturarabatten er nå definert og tilordnet til den aktuelle kunden. Når du velger kundekoden i **Fakturarabattkode**-feltet på andre kundekort, tilordnes den samme fakturarabatten til kundene.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Arbeide med salgfakturarabatter og servicegebyrer
Når du bruker fakturarabatter, er det størrelsen på fakturabeløpet som fastsetter størrelsen på rabatten som gis.  

På siden **Kundefakturarabatter** kan du også legge til et gebyr i fakturaer som overstiger et bestemt beløp.  

Før du kan bruke fakturarabatter i forbindelse med salg, må du angi bestemte opplysninger i programmet. Du må angi:  

- hvilke kunder som skal gis denne rabatten.  
- hvilken rabattprosent du vil bruke.  

Hvis du vil at fakturarabatter skal beregnes automatisk, angir du dette på siden **Salgsoppsett**.  

For hver kunde kan du angi om du vil gi fakturarabatter hvis kravene er innfridd (det vil si hvis fakturabeløpet er stort nok). Du kan definere betingelsene for fakturarabatten i NOK for innenlandske kunder, og i fremmed valuta for kunder i utlandet.  

Du knytter rabattprosentene til bestemte fakturabeløp på sidene **Kundefakturarabatter**. Du kan angi den prosentsatsen du vil ha på hver side. Hver kunde kan ha en egen side, eller du kan knytte flere kunder til den samme siden.  

I tillegg til (eller i stedet for) en rabattprosent, kan du knytte et gebyrbeløp til et bestemt fakturabeløp.  

> [!TIP]  
>  Før du angir disse opplysningene, er det lurt å sette opp en oversikt over hvilken rabattstruktur du vil bruke. Dermed er det enklere å se hvilke kunder som kan knyttes til den samme fakturarabattsiden. Jo færre sider du må definere, jo raskere kan du angi de grunnleggende opplysningene.

Hvis du vil ha mer informasjon om rabatter i salg, kan du se [Definere rabatter for kundene](/learn/modules/customer-discounts-dynamics-365-business-central/index) på Microsoft Learn.  

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
Hvis du vil kopiere salgspriser, for eksempel salgsprisen for en enkelt kunde som skal brukes i en kundeprisgruppe, må du utføre kjørselen **Foreslå salgspris i forslag**. kjørselen, som du starter fra siden **Salgsprisforslag**.    

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsprisforslag**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Foreslå salgspris i forslag.** .  
3.  I hurtigfanen **Salgspriser** fyller du ut feltene **Salgstype** og **Salgskode** med de opprinnelige salgsprisene du vil kopiere.  
4.  På den øverste delen av forespørselssiden fyller du ut feltene **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.  
5.  Hvis du vil at kjørselen skal opprette nye priser, velger du avmerkingsboksen **Opprett nye priser**.  
6.  Velg **OK**-knappen for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene, noe som angir at de er gyldige for den valgte salgstypen.  

> [!NOTE]  
>  Denne kjørselen oppretter forslag, men implementerer ikke de foreslåtte endringene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si legge dem inn på siden **Salgspriser**, velger du handlingen **Implementer prisendringer** på siden **Salgsprisforslag**.

## <a name="to-bulk-update-item-prices"></a>Slik samleoppdaterer du varepriser   
Hvis du vil oppdatere varepriser satsvis, for eksempel øke alle varepriser med en bestemt prosentdel, må du kjøre **Foreslå varepris i forslag** Kjørselen . Du finner en kobling til den satsvise jobben på siden **Salgsprisforslag**.     

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgsprisforslag**, og velg deretter den relaterte koblingen.   
2.  Velg handlingen **Foreslå varepris i forslag** .   
3.  I hurtigfanen **Vare** fyller du ut **Nr.** eller **Bokføringsgruppe - lager** eller andre felt med de opprinnelige salgsprisene du vil oppdatere.   
4.  På den øverste delen av forespørselssiden fyller du ut **Salgstype** og **Salgskode** med type og navn du vil at salgsprisene skal kopieres til.
5.  Hvis du vil at kjørselen skal justere foreslåtte salgspriser automatisk, kan du angi justeringen i feltet **JUusteringsfaktor**. Du kan for eksempel angi 1,15 i **Justeringsfaktor** for 15 % økning av vareprisen.  
6.  Hvis du vil at kjørselen skal opprette nye priser, velger du feltet **Opprett nye priser**.   
7.  Velg **OK**-knappen for å fylle ut linjene på siden **Salgsprisforslag** med de foreslåtte nye prisene, noe som angir at de er gyldige for den valgte **Vare**.   

> [!NOTE]   
>  Denne kjørselen oppretter forslag, men implementerer ikke de foreslåtte endringene. Hvis du er tilfreds med forslagene og vil implementere dem, det vil si legge dem inn i tabellen **Salgspriser**, kan du bruke kjørselen **Implementer prisendringer**, som du finner i fanebladet **Handlinger**, i gruppen **Funksjoner**, på siden **Salgsprisforslag**.

## <a name="see-related-training-at-microsoft-learnlearnmodulesmanage-sales-prices-dynamics-365-business-centralindex"></a>Se relatert opplæring på [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Se også
[Sette opp salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
