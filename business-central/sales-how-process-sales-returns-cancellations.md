---
title: Behandle ordrereturer eller annulleringer | Microsoft-dokumentasjon
description: Beskriver hvordan du oppretter en salgskreditnota, direkte eller via en ordreretur, for å behandle en retur, kansellering eller refusjon for varer eller tjenester du har mottatt betaling for.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 249c38574c2f5ff1babc17df25bf33679a6b6764
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316407"
---
# <a name="process-sales-returns-or-cancellations"></a>Behandle ordrereturer eller annulleringer
Hvis en kunde vil returnere varer eller bli refundert for varer eller tjenester du har solgt og mottatt betaling for, må du opprette og bokføre en salgskreditnota som angir den ønskede endringen. For å inkludere den riktige salgsfakturainformasjonen kan du opprette salgskreditnotaen direkte fra den bokførte salgsfakturaen, eller du kan opprette en ny salgskreditnota kopiert fakturainformasjon.

Hvis du trenger mer kontroll over ordrereturprosessen, for eksempel lagerdokumenter for varehåndtering eller bedre oversikt når du mottar varer fra flere salgsdokumenter med en ordreretur, kan du opprette ordrereturer. En ordreretur utsteder automatisk den relaterte salgskreditnotaen, og andre returrelaterte dokumenter, for eksempel en erstatningsordre om nødvendig. Hvis du vil ha mer informasjon, kan du se [Opprette en ordreretur basert på ett eller flere bokførte salgsdokumenter](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).

> [!NOTE]  
>   Hvis en bokført salgsfaktura ennå ikke er betalt, kan du bruke funksjonen **Korriger** eller **Annuller** på den bokførte salgsfakturaen for å tilbakeføre transaksjonene. Disse funksjonene fungerer bare for ubetalte fakturaer, og de støtter ikke delvise returer eller annulleringer. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md).

En returnert vare eller refusjon kan være knyttet til bare noen av varene eller tjenestene på den opprinnelige salgsfakturaen. I så fall må du redigere opplysningene på linjene på salgskreditnotaen eller ordrereturen. Når du bokfører salgskreditnotaen eller ordrereturen, tilbakeføres salgsdokumentene som påvirkes av endringen og en refusjonsbetaling kan opprettes for kunden. Hvis du vil ha mer informasjon, kan du se [Utføre betalinger](payables-make-payments.md).  

I tillegg til den opprinnelige bokførte salgsfakturaen, kan du bruke salgskreditnotaen eller ordrereturen for andre salgsdokumenter, for eksempel en annen bokført salgsfaktura, fordi kunden også returnerer varer som leveres med denne fakturaen.

Du kan sende den bokførte salgskreditnotaen til kunden for å bekrefte returen eller annulleringen, og formidle at den tilknyttede verdien blir refundert, for eksempel når varene returneres.

Bokføringen av kreditnotaen tilbakefører også eventuelle varegebyr som var tilordnet det bokførte dokumentet, slik at varens verdiposter er de samme som før varegebyret ble tilordnet.

## <a name="inventory-costing"></a>Beholdning og kostberegning
For å beholde riktig lagerverdi vil du vanligvis sette returnerte varene tilbake i lageret med enhetskosten som de er solgt på, ikke på gjeldende enhetskost. Dette kalles opprinnelig kostpris.

Det finnes to funksjoner du kan bruke til å tilordne opprinnelig kosttilbakeføring automatisk.   

|Funksjon|Description|  
|------------------|---------------------------------------|  
|Funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** på siden **Ordreretur**|Kopierer linjer i en eller flere bokførte dokumenter som skal tilbakeføres til ordrereturen. Hvis du vil ha mer informasjon, kan du se [Opprette en ordreretur basert på ett eller flere bokførte salgsdokumenter](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents).|  
|**Kopier dokument**-funksjonen på sidene **Salgskreditnota** og **Ordreretur**|Kopierer både hodet og linjene i et bokført bilag som skal tilbakeføres.<br /><br /> Krever at du merker av for **Bruk opprinnelig kostpris** på siden **Salgsoppsett**.|

For å tilordne opprinnelig kostpris manuelt, må du velge feltet **Utlignet fra-varepost** på alle typer returdokumentlinjer, og deretter velge nummeret på den opprinnelige salgsposten. Dermed knyttes salgskreditnotaen eller ordrereturen til den opprinnelige salgsposten, og verdien av varen fastsettes til opprinnelig enhetskost.

Hvis du vil ha mer informasjon, kan du se [Kostberegning for beholdning](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Opprette en ny salgskreditnota fra en bokført salgsfaktura
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte salgsfakturaer**, og velg deretter den relaterte koblingen.  
2. På siden **Bokførte salgsfakturaer** velger du den bokførte salgsfakturaen som du vil tilbakeføre, og deretter velger du **Opprett korrigerende kreditnota**.

    For salgskreditnotahodet inneholder noen opplysninger fra den bokførte salgsfakturaen. Du kan redigere dette, for eksempel med ny informasjon som gjenspeiler returavtalen.  
3. Redigere informasjonen på linjene i henhold til avtalen, for eksempel antall varer som returneres, eller beløpet som skal refunderes.
4. Velg handlingen **Utlign poster**.
5. På siden **Utlign kundeposter** velger du linjen med det bokførte salgsdokumentet du vil utligne salgskreditnotaen mot, og deretter velger du handlingen **Utlignings-ID**.

    ID-en på salgskreditnotaen vises i feltet **Utlignings-ID**.
6. I feltet **Beløp som skal utlignes** skriver du inn beløpet som du vil utligne hvis mindre enn det opprinnelige beløpet.  

    Nederst på siden **Utlign kundeposter** kan du se det totale beløpet som skal utlignes for å tilbakeføre alle involverte poster, nemlig når verdien i **Saldo**-feltet er null.
7. Velg **OK**. Når du bokfører salgskreditnotaen, brukes den på de bokførte salgsdokumentene.

    Når du har opprettet eller redigert salgskreditnotalinjene, og ett eller flere programmer er angitt, kan du fortsette med å bokføre salgskreditnotaen.   
8. Velg handlingen **Bokfør og send**.  

Dialogboksen **Bokfør og send bekreftelse** åpnes, og viser den foretrukne sendemetoden for kunden. Du kan endre sendemetoden ved å velge oppslagsknappen for feltet **Send dokument til**. Hvis du vil ha mer informasjon, kan du se [Definere en profil for dokumentsending](sales-how-setup-document-send-profiles.md).  

De bokførte salgsdokumentene som du utlignet kreditnotaen mot, tilbakeføres, og en refusjonsbetaling kan opprettes for kunden. Salgskreditnotaen fjernes og erstattes med et nytt dokument i listen over bokførte salgskreditnotaer.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Opprette en salgskreditnota ved å kopiere en bokført salgsfaktura
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom salgskreditnota.
3. I feltet **Kunde** angir du navnet på en eksisterende kunde.
4. Velg handlingen **Kopier dokument**.
5. Velg **Bokført faktura** i **Bilagstype**-feltet på siden **Kopier salgsdokument**.
6. Velg feltet **Bilagsnr.** for å åpne siden **Bokførte salgsfakturaer**, og velg deretter den bokførte salgsfakturaen som inneholder linjer du vil tilbakeføre.
7. Merk av for  **Gjenberegn linjer**  hvis du vil at de kopierte bokførte salgsfakturalinjene skal oppdateres med endringer i varepris og enhetskost etter at fakturaen er bokført.
8. Velg **OK**. De kopierte fakturalinjene settes inn i salgskreditnotaen.
9. Fullfør salgskreditnotaen som forklart i [Opprette en salgskreditnota fra en bokført salgsfaktura](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Opprette en ordreretur basert på ett eller flere bokførte salgsdokumenter
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Ordrereturer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
4. I **Linjer**-hurtigfanen fyller du ut linjene manuelt, eller kopier informasjon fra andre dokumenter for å fylle ut linjene automatisk:

    - Bruk funksjonen  **Hent bokførte dokumentlinjer som skal tilbakeføres** for å kopiere én eller flere bokførte dokumentlinjer fra ett eller flere bokførte dokumenter. Denne funksjonen tilbakefører alltid kost nøyaktig fra den bokførte dokumentlinjen. Denne funksjonen er beskrevet i følgende fremgangsmåter.    
    - Bruk funksjonen **Kopier dokument** til å kopiere et eksisterende dokument til ordrereturen. Bruk denne funksjonen til å kopiere hele dokumentet. Det kan være et bokført dokument eller et dokument som ikke er bokført ennå. Med denne funksjonen er nøyaktig kosttilbakeføring bare mulig hvis det er merket av for **Bruk opprinnelig kostpris** på siden **Salgsoppsett**.  

5. Velg handlingen **Hent bokførte dokumentlinjer som skal tilbakeføres**.
6. Øverst på siden **Bokførte salgsdokumentlinjer** merker du av for **Vis bare reversible linjer** hvis du bare vil se salgslinjer med antall som ennå ikke er tilbakeført. Hvis for eksempel antallet for en bokført salgsfaktura allerede har blitt tilbakeført, kan det hende du ikke vil tilbakeføre det antallet på et nytt ordrereturdokument.

    > [!NOTE]  
    >  Dette feltet fungerer bare for bokførte følgesedler og bokførte fakturalinjer, og ikke for bokførte retur- eller kreditnotalinjer.

    Til venstre på siden vises en oversikt over de ulike dokumenttypene, og nummeret i hakeparenteser viser antall dokumenter som er tilgjengelige for hver enkelt dokumenttype.

7. I feltet **Filter for bilagstype** velger du typen bokførte dokumentlinjer du vil bruke.  
8. Velg linjene du vil kopiere til det nye dokumentet.  

    > [!NOTE]  
    >  Hvis du bruker Ctrl+A for å velge alle linjene, kopieres alle linjene med det filteret du har angitt, men filteret **Vis bare reversible linjer** ignoreres. Hvis du for eksempel har filtrert linjene for et bestemt dokumentnummer med to linjer, og en av dem allerede er tilbakeført. Selv om feltet **Vis bare reversible linjer** er valgt, kopieres begge linjene når du trykker CTRL+A for å kopiere alle linjene, ikke bare den linjen som ennå ikke er tilbakeført.  

9. Velg **OK**-knappen for å kopiere linjene til det nye dokumentet.  

    Følgende skjer:  

    -   For bokførte dokumentlinjer av typen **Vare** opprettes en ny dokumentlinje som er en kopi av den bokførte dokumentlinjen, med antall som ennå ikke er tilbakeført. Feltet **Utlignet fra-varepost** fylles ut etter behov med tallet på vareposten for den bokførte dokumentlinjen.  

    -   For bokførte dokumentlinjer som ikke er av typen **Vare**, for eksempel varegebyrer, opprettes en ny dokumentlinje som er en kopi av den opprinnelige bokførte dokumentlinjen.  

    -   **Enhetskost (NOK)**-feltet beregnes på den nye linjen fra kosten for de tilhørende varepostene.  

    -   Hvis det kopierte dokumentet er en bokført følgeseddel, et bokført mottak, en bokført returseddel eller en bokført returforsendelse, beregnes salgsprisen fra varekortet.  

    -   Hvis det kopierte dokumentet er en bokført faktura eller kreditnota, kopieres salgsprisen, fakturarabatter og linjerabatter fra den bokførte dokumentlinjen.  

    -   Hvis den bokførte dokumentlinjen inneholder varesporingslinjer, fylles feltet **Utlignet fra-varepost** ut på varesporingslinjene med relevant varepostnummer fra de bokførte varesporingslinjene.  

     Når du kopierer fra en bokført faktura eller bokført kreditnota, kopieres alle relevante fakturarabatter og linjerabatter som er gyldige på bokføringstidspunktet for det dokumentet, fra den bokførte dokumentlinjen til den nye dokumentlinjen. Legg merke til at hvis alternativet **Beregn. fakt.rab.** er aktivert på siden **Salgsoppsett**, blir fakturarabatten beregnet på nytt når du bokfører linjen for det nye dokumentet. Det kan derfor hende at linjebeløpet for den nye linjen er forskjellig fra linjebeløpet på den bokførte dokumentlinjen, avhengig av den nye beregningen av fakturarabatten.  

     > [!NOTE]  
     >  Hvis en del av antallet for den bokførte dokumentlinjen allerede er tilbakeført (returnert) eller solgt eller forbrukt, opprettes en linje bare for antallet som gjenstår på lageret, eller som ikke har blitt returnert. Hvis hele antallet for den bokførte dokumentlinjen allerede er tilbakeført, opprettes det ikke en ny dokumentlinje.  
     >   
     >  Hvis vareflyten i det bokførte dokumentet er den samme som vareflyten i det nye dokumentet, opprettes det ganske enkelt en kopi av den opprinnelige bokførte dokumentlinjen i det nye dokumentet. Feltet **Utlignet fra-varepost** fylles ikke ut fordi nøyaktig kosttilbakeføring ikke er mulig i dette tilfellet. Hvis du for eksempel bruker funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** for å hente en bokført salgskreditnotalinje for en ny salgskreditnota, kopieres bare den opprinnelige bokførte kreditnotalinjen til den nye kreditnotaen.  

10. På siden **Ordreretur** i feltet **Returårsakskode** velger du årsaken til returen på hver linje.
11. Velg handlingen **Bokfør**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Slik oppretter du en erstatningsordre fra en ordreretur:
Du kan bestemme deg for å kompensere en kunde for en vare du har solgt ved å erstatte varen. Du erstatter varen med samme vare, eller med en annen vare. Denne situasjonen kan for eksempel oppstå hvis du ved en feiltakelse leverer feil vare til kunden.  

1. På siden **Ordreretur** for en aktiv returprosess lager du en negativ post på en tom linje for erstatningsvaren ved å sette inn et negativt beløp i **Antall**-feltet.  
2. Velg handlingen **Flytt negative linjer**.
3. På siden **Flytt negative salgslinjer** fyller du ut feltene etter behov.
4. Velg **OK**. Den negative linjen for erstatningsvaren slettes fra ordrereturen, og den settes inn på en ny **Ordre**-side. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Slik oppretter du retur-relaterte dokumenter fra en ordreretur:
Du kan opprette erstatningsordrer, bestillingsreturer og erstatningsbestillinger under ordrereturprosessen. Dette er for eksempel nyttig i situasjoner hvor du vil håndtere varer med garantier fra leverandører.

1. På siden **Ordreretur** for en aktiv returprosess velger du handlingen **Opprett retur-relaterte dokumenter**.
2. I **Leverandørnr.**-feltet angir du nummeret til en leverandør hvis du vil opprette leverandørdokumenter automatisk.
3. Hvis en returnert vare må returneres til leverandøren, merker du av for **Opprett bestillingsretur**.
4. Hvis en returnert vare må bestilles fra leverandøren, merker du av for **Opprett bestilling**.
5. Hvis en erstatningsordre må opprettes, merker du av for alternativet **Opprett ordre**.

## <a name="to-create-a-restock-charge"></a>Slik oppretter du et returgebyr
Det kan hende du vil belaste kunden med et returgebyr for å dekke kostnader i forbindelse med retur av en vare. Dette er aktuelt hvis kunden for eksempel har bestilt feil vare, eller ombestemt seg etter at han eller hun mottok varen.

Du kan bokføre denne økte kostnaden som et varegebyr i en kreditnota eller en ordreretur, og knytte den til den bokførte følgeseddelen. Det følgende beskriver den for en ordreretur, men de samme trinnene gjelder en salgskreditnota.

1. Åpne siden **Ordreretur** for en aktiv returprosess.
2. Velg **Gebyr (vare)** i **Type**-feltet på en ny linje.  
3. Fyll ut feltene for en hvilken som helst varegebyrlinje. Hvis du vil ha mer informasjon, kan du se [Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md).  

Når du bokfører ordrereturen, legges et returgebyr til i det aktuelle salgsbeløpet. Dermed kan du opprettholde en nøyaktig lagerverdisetting.  

## <a name="to-create-a-sales-allowance"></a>Slik oppretter du en salgsrabatt
Du kan sende en kunde en kreditnota med prisreduksjon hvis kunden har mottatt ukurante varer eller har mottatt varene for sent.  
Du kan bokføre den reduserte prisen som et varegebyr i en kreditnota eller en ordreretur, og knytte den til den bokførte følgeseddelen. Det følgende beskriver den for en salgskreditnota, men de samme trinnene gjelder en ordreretur.

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom salgskreditnota.
3. Fyll ut kreditnotahodet med aktuelle opplysninger om kunden du vil gi salgsrabatt til.  
4. På hurtigfanen **Linjer**, i **Type**-feltet, velger du **Gebyr (vare)**.  
5.  I feltet **Nr.** -feltet velger du den aktuelle varegebyrverdien.  
     Det kan hende du vil opprette et eget varegebyrnummer for å dekke salgsrabatter.  
6.  I feltet **Antall** angir du **1**.  
7.  I feltet **Salgspris** angir du beløpet i salgsrabatten.  
8.  Du kan  tilordne salgsrabatten som et varegebyr til varene i den bokførte leveringen. Hvis du vil ha mer informasjon, kan du se [Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md). Når du har tilordnet rabatten, går du tilbake til **Salgskreditnota**-siden.  

Når du bokfører ordrereturen, legges salgsrabatten til i det aktuelle salgsbeløpet. Dermed kan du opprettholde en nøyaktig lagerverdisetting.

## <a name="to-combine-return-receipts"></a>Slå sammen retursedler
Du kan slå sammen retursedler hvis kunden returnerer flere varer som dekkes av ulike ordrereturer.  

Når du mottar varene på lageret, bokfører du de aktuelle ordrereturene som mottatt. Dette oppretter bokførte returmottak.  

Når du er klar til å fakturere denne kunden, kan du i stedet for å fakturere hver enkelt ordreretur separat, opprette en salgskreditnota og automatisk kopiere de bokførte returmottakslinjene til dette dokumentet. Deretter kan du bokføre salgskreditnotaen, og helt enkelt fakturere alle åpne ordrereturer samtidig.  

Du kombinerer retursedler ved å merke av for **Opprett samlefaktura** på siden **Kundekort**.  

### <a name="to-manually-combine-return-receipts"></a>Slik slår du sammen retursedler manuelt  

1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Salgskreditnota**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.  
4. Velg handlingen **Hent returmottakslinjer**.  
5. Velg returmottakslinjene du vil ta med i kreditnotaen:  

    -   Du setter inn alle linjene ved å merke dem og velge **OK**.  

    -   Du setter inn bestemte linjer ved å merke dem og velge **OK**.  

6.  Hvis du valgte en feil følgeseddellinje, eller du vil starte på nytt, kan du ganske enkelt slette linjene på kreditnotaen og kjøre funksjonen **Hent returseddellinjer** på nytt.  
7.  Bokfør fakturaen.  

### <a name="to-automatically-combine-return-receipts"></a>Slik slår du sammen retursedler automatisk:  
Du kan slå sammen retursedler automatisk og velge å bokføre kreditnotaene automatisk ved hjelp av funksjonen **Slå sammen retursedler**.  

1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slå sammen retursedler**, og velg deretter den relaterte koblingen.
2. På siden **Slå sammen retursedler** fyller du ut feltene for å velge de aktuelle returmottakene.
3. Merk av for **Bokfør kreditnotaer**. Hvis ikke må du manuelt bokføre de endelige kjøpskreditnotaene.
4.  Velg **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Slik fjerner du mottatte og fakturerte ordrereturer  
Når du fakturerer retursedler på denne måten, eksisterer fortsatt ordrereturene som retursedlene ble bokført fra, selv om de er fullstendig mottatt og fakturert.  

Når retursedler slås sammen på en kreditnota og bokføres, opprettes en bokført salgskreditnota for den eller de krediterte linjene. **Fakturert (antall)**-feltet på den opprinnelige ordrereturen oppdateres ut fra det fakturerte antallet.   
1.  Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Slett fakturerte ordrereturer**, og velg deretter koblingen.  
2.  Angi hvilke ordrer som skal slettes, i **Nr.** -filterfeltet.  
3.  Velg **OK**-knappen.  

Du kan også slette individuelle ordrereturer manuelt.   

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
