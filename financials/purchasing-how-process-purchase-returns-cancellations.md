---
title: "Bruke kjøpskreditnotaer til å behandle returer eller annulleringer | Microsoft-dokumentasjon"
description: "Forklarer hvordan du oppretter og bokfører en kjøpskreditnota når du vil returnere varer til en leverandør eller annullere kjøpte tjenester."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cancel, undo, correct
ms.date: 08/03/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: aa56764b5f3210229ad21eae6891fb201462209c
ms.openlocfilehash: 114448607d8b99252573912d2df08f91e1d27c76
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="how-to-process-purchase-returns-or-cancellations"></a>Behandle bestillingsreturer eller annulleringer
Hvis du vil returnere varer til leverandøren eller avbryte tjenester du har kjøpt, kan du opprette og bokføre en kjøpskreditnota som angir den ønskede endringen med hensyn til den opprinnelige kjøpsfakturaen. For å inkludere den riktige kjøpsfakturainformasjonen kan du opprette kjøpskreditnotaen direkte fra den bokførte kjøpsfakturaen, eller du kan opprette en ny kjøpskreditnota med kopiert fakturainformasjon.

Hvis du trenger mer kontroll over returprosessen, for eksempel lagerdokumenter for varehåndtering eller bedre oversikt ved tilbakelevering av varer fra flere kjøpsdokumenter med én bestillingsretur, kan du opprette bestillingsreturer. En bestillingsretur utsteder automatisk den relaterte kjøpskreditnotaen. Hvis du vil ha mer informasjon, kan du se delen "Opprette en bestillingsretur basert på ett eller flere bokførte kjøpsdokumenter".

> [!NOTE]  
>   Hvis en bokført kjøpsfaktura ennå ikke er betalt, kan du bruke funksjonen **Korriger** eller **Annuller** på den bokførte kjøpsfakturaen til å reversere de involverte transaksjonene automatisk. Disse funksjonene fungerer bare for ubetalte fakturaer, og de støtter ikke delvise returer eller annulleringer. Hvis du vil ha mer informasjon, kan du se [Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Vanligvis oppretter du en kjøpskreditnota eller bestillingsretur i relasjon til en kreditnota du har mottatt fra en leverandør. Kjøpskreditnotaen eller bestillingsreturen fungerer som intern dokumentasjon av kreditnotaprosessen for regnskapsformål eller for å kontrollere leveringen av de aktuelle varene.

Endringen kan relateres til alle produktene på den opprinnelige kjøpsfakturaen eller bare noen av produktene. Du kan derfor delvis returnere mottatte varer eller kreve delvis refusjon av mottatte tjenester. I så fall må du redigere opplysningene på linjene på kjøpskreditnotaen eller bestillingsreturen.

I tillegg til den opprinnelige bokførte kjøpsfakturaen, kan du bruke kjøpskreditnotaen eller bestillingsreturen for andre kjøpsdokumenter, for eksempel en annen bokført kjøpsfaktura, fordi du også returnerer varer som leveres med denne fakturaen.

Bokføringen av kreditnotaen tilbakefører også eventuelle varegebyr som var tilordnet det bokførte dokumentet, slik at varens verdiposter er de samme som før varegebyret ble tilordnet.

## <a name="inventory-costing"></a>Beholdning og kostberegning
For å beholde riktig lagerverdi vil du vanligvis plukke returvarer fra lageret med enhetskosten som de er solgt på, ikke på gjeldende enhetskost. Dette kalles opprinnelig kostpris.

Det finnes to funksjoner du kan bruke til å tilordne opprinnelig kosttilbakeføring automatisk.  

|Funksjon|Beskrivelse|  
|------------------|---------------------------------------|  
|Funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** i vinduet **Bestillingsretur**|Kopierer linjer i en eller flere bokførte dokumenter som skal tilbakeføres til bestillingsreturen. Hvis du vil ha mer informasjon, kan du se delen "Opprette en bestillingsretur og relatert kjøpskreditnota for en eller flere bokførte kjøpsfakturaer".|  
|**Kopier dokument**-funksjonen i vinduene **Kjøpskreditnota** og **Bestillingsretur**|Kopierer både hodet og linjene i et bokført bilag som skal tilbakeføres.<br /><br /> Krever at du merker av for **Bruk opprinnelig kostpris** i vinduet **Kjøpsoppsett**.|

For å tilordne opprinnelig kostpris manuelt, må du velge feltet **Utlignet fra-varepost** på alle typer returdokumentlinjer, og deretter velge nummeret på den opprinnelige kjøpsposten. Dermed knyttes kjøpskreditnotaen eller bestillingsreturen til den opprinnelige kjøpsposten, og verdien av varen fastsettes til opprinnelig enhetskost.

Hvis du vil ha mer informasjon, kan du se [Kostberegning for beholdning](design-details-inventory-costing.md).

## <a name="to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice"></a>Opprette en kjøpskreditnota fra en bokført kjøpsfaktura
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bokførte kjøpsfakturaer**, og velg deretter den relaterte koblingen.  
2. I vinduet Bokførte **Kjøpsfakturaer** velger du den bokførte kjøpsfakturaen som du vil tilbakeføre, og deretter velger du handlingen **Opprett korrigerende kreditnota**.

    De fleste feltene på kjøpskreditnotahodet fylles ut med informasjon fra den bokførte kjøpsfakturaen. Du kan redigere alle feltene, for eksempel med ny informasjon som gjenspeiler returavtalen.
3. Redigere informasjonen på linjene i henhold til avtalen, for eksempel antall varer som returneres, eller beløpet som skal refunderes.
4. Velg handlingen **Utlign poster**.
5. I vinduet **Utlign leverandørposter** velger du linjen med det bokførte kjøpsdokumentet du vil utligne kjøpskreditnotaen mot, og deretter velger du handlingen **Utlignings-ID**. Nummeret på kjøpskreditnotaen settes inn i feltet **Utlignings-ID**.
6. I feltet **Beløp som skal utlignes** skriver du inn beløpet som du vil utligne hvis mindre enn det opprinnelige beløpet.

    Nederst i vinduet **Utlign leverandørposter** kan du se det totale beløpet som skal utlignes for å tilbakeføre alle involverte poster, nemlig når verdien i **Saldo** -feltet er null.
7. Velg **OK**. Når du bokfører kjøpskreditnotaen, brukes den på de angitte bokførte kjøpsdokumenter.

    Når du har opprettet eller redigert nødvendige kjøpskreditnotalinjer og ett eller flere programmer er angitt, kan du fortsette med å bokføre kjøpskreditnotaen.
8. Velg handlingen **Bokfør**.

De bokførte kjøpsfakturaene du utligner kreditnotaen mot, er nå tilbakeført. Hvis du allerede har betalt den opprinnelige fakturaen, skal leverandøren nå refundere betalingen til deg. Hvis kreditnotaen bare er en del av produktet på den opprinnelige fakturaen, kan du bare betale det resterende beløpet på den opprinnelige kjøpsfakturaen for å lukke den.

Kjøpskreditnotaen fjernes og erstattes med et nytt dokument i listen over bokførte kjøpskreditnotaer.

## <a name="to-create-a-purchase-credit-memo-by-copying-a-posted-purchase-invoice"></a>Opprette en ny kjøpskreditnota ved å kopiere en bokført kjøpsfaktura
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kjøpskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom kjøpskreditnota.
3. I feltet **Leverandør** angir du navnet på en eksisterende leverandør.
4. Velg handlingen **Kopier dokument**.
5. Velg **Bokført faktura** i feltet **Dokumenttype** i vinduet **Kopier kjøpsdokument**.
6. Velg feltet **Bilagsnr.** for å åpne vinduet **Bokførte kjøpsfakturaer**, og velg deretter den bokførte kjøpsfakturaen som inneholder linjer du vil tilbakeføre.
7. Merk av for  **Gjenberegn linjer**  hvis du vil at de kopierte bokførte kjøpsfakturalinjene skal oppdateres med endringer i varepris og enhetskost etter at fakturaen er bokført.
8. Velg **OK**. De kopierte fakturalinjene settes inn i kjøpskreditnotaen.
9. Fullføre kjøpskreditnotaen som forklart i den avsnittet "Opprette en kjøpskreditnota fra en bokført kjøpsfaktura" i dette emnet.

## <a name="to-create-a-purchase-return-order-based-on-one-or-more-a-posted-purchase-documents"></a>Opprette en bestillingsretur basert på ett eller flere bokførte kjøpsdokumenter
1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Bestillingsreturer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
4. I **Linjer**-hurtigfanen fyller du ut linjene manuelt, eller kopier informasjon fra andre dokumenter for å fylle ut linjene automatisk:

    - Bruk funksjonen  **Hent bokførte dokumentlinjer som skal tilbakeføres** for å kopiere én eller flere bokførte dokumentlinjer fra ett eller flere bokførte dokumenter. Denne funksjonen tilbakefører alltid kost nøyaktig fra den bokførte dokumentlinjen. Denne funksjonen er beskrevet i følgende fremgangsmåter.    
    - Bruk funksjonen **Kopier dokument** til å kopiere et eksisterende dokument til ordrereturen. Bruk denne funksjonen til å kopiere hele dokumentet. Det kan være et bokført dokument eller et dokument som ikke er bokført ennå. Med denne funksjonen er nøyaktig kosttilbakeføring bare mulig hvis det er merket av for **Bruk opprinnelig kostpris** i vinduet **Salgsoppsett**.  

4. Velg handlingen **Hent bokførte dokumentlinjer som skal tilbakeføres**.
5. Øverst i vinduet **Bokførte kjøpsdokumentlinjer** merker du av for **Vis bare reversible linjer** hvis du bare vil se salgslinjer med antall som ennå ikke er tilbakeført. Hvis for eksempel antallet for en bokført kjøpsfaktura allerede har blitt tilbakeført, kan det hende du ikke vil inkludere det antallet på et nytt bestillingsreturdokument.

    > [!NOTE]  
    >  Dette feltet fungerer bare for bokførte mottak og bokførte fakturalinjer, og ikke for bokførte retur- eller kreditnotalinjer.  

    På venstre side av vinduet vises en oversikt over de ulike dokumenttypene, og nummeret i parentes viser antall dokumenter som er tilgjengelig for hver enkelt dokumenttype.

6. I feltet **Filter for bilagstype** velger du typen bokførte dokumentlinjer du vil bruke.  
7. Velg linjene du vil kopiere til det nye dokumentet.  

    > [!NOTE]  
    >  Hvis du bruker Ctrl+A for å velge alle linjene, kopieres alle linjene med det filteret du har angitt, men filteret **Vis bare reversible linjer** ignoreres. Hvis du for eksempel har filtrert linjene for et bestemt dokumentnummer med to linjer, og en av dem allerede er tilbakeført. Selv om feltet **Vis bare reversible linjer** er valgt, kopieres begge linjene når du trykker CTRL+A for å kopiere alle linjene, ikke bare den linjen som ennå ikke er tilbakeført.  

8. Velg **OK**-knappen for å kopiere linjene til det nye dokumentet.  

    Følgende skjer:  

    -   For bokførte dokumentlinjer av typen **Vare** opprettes en ny dokumentlinje som er en kopi av den bokførte dokumentlinjen, med antall som ennå ikke er tilbakeført. Feltet **Utlignet til-varepost** fylles ut etter behov med tallet på vareposten for den bokførte dokumentlinjen.  

    -   For bokførte dokumentlinjer som ikke er av typen **Vare**, for eksempel varegebyrer, opprettes en ny dokumentlinje som er en kopi av den opprinnelige bokførte dokumentlinjen.  

    -   **Enhetskost (NOK)**-feltet beregnes på den nye linjen fra kosten for de tilhørende varepostene.  

    -   Hvis det kopierte dokumentet er en bokført følgeseddel, et bokført mottak, en bokført returseddel eller en bokført returforsendelse, beregnes salgsprisen fra varekortet.  

    -   Hvis det kopierte dokumentet er en bokført faktura eller kreditnota, kopieres salgsprisen, fakturarabatter og linjerabatter fra den bokførte dokumentlinjen.  

    -   Hvis den bokførte dokumentlinjen inneholder varesporingslinjer, fylles feltet **Utlignet til-varepost** ut på varesporingslinjene med relevant varepostnummer fra de bokførte varesporingslinjene.  

     Når du kopierer fra en bokført faktura eller bokført kreditnota, kopieres alle relevante fakturarabatter og linjerabatter som er gyldige på bokføringstidspunktet for det dokumentet, fra den bokførte dokumentlinjen til den nye dokumentlinjen. Vær imidlertid oppmerksom på at hvis alternativet **Beregn fakturarabatt** er aktivert i vinduet **Kjøpsoppsett**, vil fakturarabatten bli beregnet på nytt når du bokfører den nye dokumentlinjen. Det kan derfor hende at linjebeløpet for den nye linjen er forskjellig fra linjebeløpet på den bokførte dokumentlinjen, avhengig av den nye beregningen av fakturarabatten.  

    > [!NOTE]  
    >  Hvis en del av antallet for den bokførte dokumentlinjen allerede er tilbakeført (returnert) eller solgt eller forbrukt, opprettes en linje bare for antallet som gjenstår på lageret, eller som ikke har blitt returnert. Hvis hele antallet for den bokførte dokumentlinjen allerede er tilbakeført, opprettes det ikke en ny dokumentlinje.  
    >   
    >  Hvis vareflyten i det bokførte dokumentet er den samme som vareflyten i det nye dokumentet, opprettes det ganske enkelt en kopi av den opprinnelige bokførte dokumentlinjen i det nye dokumentet. Feltet **Utlignet fra-varepost** fylles ikke ut fordi nøyaktig kosttilbakeføring ikke er mulig i dette tilfellet. Hvis du for eksempel bruker funksjonen **Hent bokførte dokumentlinjer som skal tilbakeføres** for å hente en bokført kjøpskreditnotalinje for en ny kjøpskreditnota, kopieres bare den opprinnelige bokførte kreditnotalinjen til den nye kreditnotaen.  

8. I vinduet **Bestillingsretur** i feltet **Returårsakskode** velger du årsaken til returen på hver linje.
9. Velg handlingen **Bokfør**.

## <a name="to-create-a-replacement-purchase-order-from-a-purchase-return-order"></a>Slik oppretter du en erstatningsbestilling fra en bestillingsretur
Det kan hende du avtaler med leverandøren at de kompenserer deg for en kjøpt vare ved å erstatte varen. Erstatningsvaren kan være samme eller en annen vare. Denne situasjonen kan oppstå hvis leverandøren ved en feiltakelse leverer feil vare.  
1.  I vinduet **Bestillingsretur** for en aktiv returprosess lager du en negativ post på en tom linje for erstatningsvaren ved å sette inn et negativt beløp i **Antall**-feltet.  
2. Velg handlingen **Flytt negative linjer**.  
3. I vinduet **Flytt negative kjøpslinjer** fyller du ut feltene etter behov.
4. Velg **OK**. Den negative linjen slettes fra bestillingsreturen, og en ny bestilling opprettes. Hvis du vil ha mer informasjon, kan du se [Registrere kjøp](purchasing-how-record-purchases.md).  

## <a name="to-create-a-purchase-allowance"></a>Slik oppretter du en kjøpsrabatt  
Hvis leverandøren sender deg varer som du ikke er fornøyd med, på grunn av at de for eksempel er lettere skadet, har feil farge eller feil størrelse, kan det hende leverandøren tilbyr deg en kjøpsrabatt.  

Du kan bokføre denne reduserte kjøpskostnaden som et varegebyr i en kreditnota eller bestillingsretur og knytte den til det bokførte mottaket. Det følgende beskriver den for en bestillingsretur, men de samme trinnene gjelder en kjøpskreditnota.

1. Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kjøpskreditnotaer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny** for å åpne en ny, tom kjøpskreditnota.  
3.  Fyll ut kreditnotahodet med opplysninger om leverandøren som sendte kjøpsrabatten til deg.  
4. På hurtigfanen **Linjer**, i **Type**-feltet, velger du **Gebyr (vare)**.  
5.  I feltet **Nr.** -feltet velger du den aktuelle varegebyrverdien.  

    Det kan hende du vil opprette et eget varegebyrnummer for å dekke kjøpsrabatter.  
6.  I feltet **Antall** angir du **1**.  
7.  I feltet **Direkte enhetskost** angir du beløpet i kjøpsrabatten.  
8.  Tilordne kjøpsrabatten som et varegebyr til varene i det bokførte mottaket. Hvis du vil ha mer informasjon, kan du se [Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md). Når du har tilordnet rabatten, går du tilbake til **Kjøpskreditnota**-vinduet.

Når du bokfører bestillingsreturen, legges kjøpsrabatten til i det aktuelle kjøpsbeløpet. Dermed kan du opprettholde en nøyaktig lagerverdisetting.  

## <a name="to-combine-return-shipments"></a>Slik kombinerer du returforsendelser  
Hvis du vil returnere varer som dekkes av forskjellige bestillingsreturer, til samme leverandør, kan du bruke funksjonen **Kombiner returforsendelser**.  

Når du leverer varene, bokfører du de tilknyttede bestillingsreturene som levert, og dermed opprettes det bokførte bestillingsreturforsendelser.  

Når du er klar til å fakturere disse varene, kan du i stedet for å fakturere hver enkelt bestillingsretur separat, opprette en kjøpskreditnota og automatisk kopiere de bokførte bestillingsreturforsendelseslinjene til dette dokumentet. Deretter kan du bokføre kjøpskreditnotaen og helt enkelt fakturere alle åpne bestillingsreturer samtidig.  

Når returforsendelser kombineres i en kreditnota og bokføres, opprettes det en bokført kjøpskreditnota for de fakturerte linjene. **Fakturert (antall)**-feltet på den opprinnelige bestillingsreturen oppdateres basert på det fakturerte antallet. Denne opprinnelige bestillingsreturen slettes imidlertid ikke, selv om den er fullstendig mottatt og fakturert, og derfor må du slette bestillingsreturen manuelt.

> [!NOTE]  
> Denne fremgangsmåten forutsetter at det finnes flere bestillingsreturer for leverandøren, og at de er bokført som levert.     

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Kjøpskreditnotaer**, og velg deretter den relaterte koblingen.  
2.  Velg handlingen **Ny**.  
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.  
4. Velg handlingen **Hent returforsendelseslinjer**.  
5.  Velg flere returforsendelseslinjer du vil inkludere på fakturaen.  

    Hvis feil returforsendelseslinje ble merket eller du vil begynne på nytt, kan du ganske enkelt slette linjene i kjøpskreditnotaen og deretter bruke funksjonen **Hent returforsendelseslinjer** på nytt.  
6.  Velg handlingen **Bokfør**.  

### <a name="to-remove-open-purchase-return-orders-after-combined-return-shipment-posting"></a>Fjerne åpne bestillingsreturer etter kombinert returforsendelsesbokføring  

1.  Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Slett fakturerte ordrereturer**, og velg deretter den relaterte koblingen.  
2.  Fyll ut feltene etter behov, og klikk deretter **OK**.  
3.  Du kan også slette individuelle bestillingsreturer manuelt.

## <a name="see-also"></a>Se også
[Innkjøp](purchasing-manage-purchasing.md)  
[Registrere kjøp](purchasing-how-record-purchases.md)  
[Korrigere eller annullere ubetalte kjøpsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

