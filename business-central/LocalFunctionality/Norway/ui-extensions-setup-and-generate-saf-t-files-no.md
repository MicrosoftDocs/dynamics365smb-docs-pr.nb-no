---
title: Installere og generere SAF-T-filer
description: Bruk denne utvidelsen til å konfigurere og generere SAF-T-filer for de norske myndighetene, i Business Central.
author: sorenfriisalexandersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, saf-t, authorities, export, compliance
ms.search.form: 10690, 10674, 10673, 10675, 10677, 10679, 10670, 10680,
ms.date: 04/01/2021
ms.author: soalex
ms.openlocfilehash: b0ab173b274a7ee9ac5c5061ccd8c147f3610804
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2022
ms.locfileid: "8135523"
---
# <a name="standard-audit-files---tax"></a>Standard revisjonsfiler – avgift

Fra januar 2020 må selskaper i Norge rapportere finansdata og angi et sett med Standard revisjonsfiler – avgift (SAF-T) til de norske myndighetene på forespørsel. Med denne utvidelsen er det enkelt å sette opp, generere og eksportere Standard revisjonsfiler – avgift i [!INCLUDE[prod_short](../../includes/prod_short.md)]. De eksporterte SAF-T-filene vil automatisk bli komprimert som en zip-fil som er klar til å lastes opp av brukeren på webområdet til Skatteetaten, de norske skattemyndighetene.  

## <a name="what-does-this-extensions-handle"></a>Hva håndterer denne utvidelsen?
Denne utvidelsen gir følgende funksjoner:
* Oppsett og tilordning av kontoplan til SAF-T-standardkontoer
* Tilordne mva-oppsett til SAF-T-mva-koder
* Styre i hvilket omfang dimensjoner eksporteres i SAF-T-filer
* Eksporter SAF-T-filer, enten direkte eller ved hjelp av jobbkøen. Ved hjelp av Jobbkø kan du planlegge at eksporten skal skje i rolige perioder, som er nyttig for potensielt store datasett.

## <a name="setup-of-the-norwegian-saf-t-extension"></a>Oppsett av norsk SAF-T-utvidelse
Konfigurer SAF-utvidelsen ved hjelp av assistert oppsett, som gir en enkel, trinnvis veiledning for å komme i gang med SAF-T i [!INCLUDE[prod_short](../../includes/prod_short.md)]. Om nødvendig kan du kjøre guiden flere ganger til du er ferdig med oppsettet.

1. I [!INCLUDE[prod_short](../../includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Assistert oppsett** og velger **Assistert oppsett**.  
2. Velg **Angi SAF-T**.
3. Den første siden i installasjonsveiledningen forklarer hva du er i ferd med å konfigurere. Velg **Neste**.
4. I feltet **Tilordningstype** velger du Kontoplan-typen du vil bruke for SAF-T-kontoer, og deretter velger du **Neste**. 

   > [!Note]
   > Hvis du bruker den lokale versjonen av [!INCLUDE[prod_short](../../includes/prod_short.md)], finnes det noen flere trinn. 
   > 1. Last ned og importer kildefiler med SAF-T-kontoer. Last ned SAF-T-tilordningsfilene fra [Skatteetatens repo på Github](https://github.com/Skatteetaten/saf-t).
   > 2. Velg **Importer kildefilene for tilordning**.
   > 3. Importer alle nødvendige filer. Hvis du definerer tilordningen for importfiler for resultatregnskapet, må du huske å importere tilordningskoder for alle poster med **Resultatregnskap** i kolonnen **Kildetype**.
   > 4. For hver importerte fil velger du **Oppdater tilordningskodene fra filen**.

5. Hvis du vil definere perioden for første SAF-T-rapportering, velger du **Regnskapsperiode**, bekrefter dataområdet og velger **Neste**.

   Dette gjøres vanligvis for en bestemt regnskapsperiode, men du kan også definere et datointervall uten å angi en regnskapsperiode.
6. Hvis du vil knytte kontoplanen til SAF-T-kontoene, velger du **Åpne oppsettssiden for å definere finanskontotilordninger**. Linjer der finanskontonr. er merket med grønt, angir at her er transaksjoner på kontoen innenfor det datointervallet som er angitt i forrige trinn, og må da tilordnes. Andre finanskonti kan hoppes over. Når du er ferdig, lukker du **Oppsettkort for SAF-T-tilordning** og velger **Neste** i oppsettsveiledningen.
7. Du tilordner mva-bokføringsoppsettet til standard salgs- og kjøpskoder for SAF-T ved å velge **Åpne oppsettssiden for å definere en tilordning for mva-bokføringsoppsett**.  Når du er ferdig, lukker du **Oppsettkort for SAF-T-bokføring** og velger **Neste** i oppsettsveiledningen.
8. Norske myndigheter anbefaler at du eksporterer dimensjoner for finanstransaksjoner. I enkelte situasjoner kan det imidlertid hende du ikke vil eksportere dimensjoner, for eksempel hvis du har interne dimensjoner som gir verdi til revisorer. Dette alternativet lar deg åpne Dimensjoner-listen og velge hvilke dimensjoner du vil eksportere. Velg verdien i feltet **Eksporter til SAF-T**, og velg deretter **Lukk**.
9. Hvis du vil angi hvilken ansatt som er SAF-kontakt i selskapet, velger du den ansatte i feltet **Ansattnr.** -feltet. Dette er nyttig når norske myndigheter har spørsmål om SAF-T-filene. Velg **Neste** når du er ferdig.
10. Oppsettet av SAF-T er nå ferdig. Velg **Fullfør**.

> [!Note] 
> Tilordningene er bundet til datointervallet du har angitt. Du kan opprette flere tilordninger for andre perioder uten å endre tilordningen du allerede har opprettet. Du kan også kopiere tilordninger fra tidligere oppgitte oppsett. Dette er for å sikre at du kan rapportere SAF-T for ulike perioder når du håndterer endringer i kontoplanen.

## <a name="exporting-saf-t-files"></a>Eksportere SAF-T-filer
Når du skal eksportere SAF-T-filer fra [!INCLUDE[prod_short](../../includes/prod_short.md)], må du først opprette og konfigurere en **SAF-T-eksport** for å definere tilordningsområdet. Du kan for eksempel definere en tilordning og eksportere hele 2019-året, og en annen tilordning for bare måneden april 2019 hvis du blir bedt om å oppgi disse dataene spesifikt.

### <a name="to-create-an-export-of-saf-t-files"></a>Opprette eksport av SAF-T-filer  
1. I [!INCLUDE[prod_short](../../includes/prod_short.md)] velger du ikonet ![Lyspære som åpner funksjonen Fortell meg.](../../media/ui-search/search_small.png) Fortell meg hva du vil gjøre), skriv inn **SAF-T-eksporter**, og velg deretter **SAF-T-eksporter**.  
2. På siden **SAF-T-eksporter** velger du **Opprett**.
3. På siden **SAF-T-eksport**, i feltet **Tilordningsområdekode**, velger du tilordningsområdet du vil definere en eksport for.
5. Hvis du vil starte SAF-T-eksport, gjør du ett av følgende: 
   * Velg **Start** hvis du vil eksportere umiddelbart.
   * Hvis du vil planlegge at eksporten skal håndteres av jobbene i jobbkøen, velger du **Parallell behandling**. Eksport av finansposter kan ta tid. For å øke hastigheten på prosessen må du vurdere å angi hvor mange jobber som skal kjøres parallelt. 
6. Du kan kontrollere statusen for SAF-T-filgenerering ved å se på **Linjer**-delen nederst på siden. 
7. Når alle filer er generert, velger **Last ned fil** for å laste ned en zip-fil som inneholder SAF-T-filene. Denne filen kan lastes opp til Skatteetaten.

### <a name="saf-t-files-and-data-quality"></a>SAF-T-filer og datakvalitet
Du kan konfigurere [!INCLUDE[prod_short](../../includes/prod_short.md)] med ekstra valideringskontroller for datakvalitet som bidrar til å sikre at SAF-filene kan valideres av Skatteetaten. SAF-T-filer kan for eksempel bare valideres når det finnes bestemt informasjon for relevante poster i [!INCLUDE[prod_short](../../includes/prod_short.md)]. For å sikre datakvaliteten for SAF-T kan du aktivere flere aktive kontroller i hurtigfanen **Datakvalitet** på siden **SAF-T-oppsett**. I tillegg bruker du handlingen **Datakontroll** til å kontrollere datakvaliteten før du eksporterer filen, på **SAF-T-eksport**-kortsiden.

> [!NOTE]
> SAF-T-eksporter genererer som standard én fil med hoveddata og separate filer for hver måned som er inkludert i det valgte tilordningsområdet. Vurder transaksjonsbeløpet i den valgte perioden, og juster **Maks. antall prosjekter** tilsvarende på siden for SAF-T-eksport. Som en generell anbefaling starter du med tre parallelle jobber for å tillate parallell eksport og likevel beholde ressurser for andre [!INCLUDE[prod_short](../../includes/prod_short.md)]-brukere. I tillegg kan du angi en delt nettverksressurs i **Mappebane** lokalt for å generere SAF-T-filene direkte på en delt nettverksressurs i stedet for i databasen. For elektroniske versjoner av [!INCLUDE[prod_short](../../includes/prod_short.md)] er dette alltid tilfellet. Hvis du angir **Mappenavn**, vil den genererte zip-filen bli plassert her. 


> [!IMPORTANT]
> På grunn av måten eksport av transaksjoner fungerer på, påvirker eksport av SAF-T-filer ytelsen til [!INCLUDE[prod_short](../../includes/prod_short.md)].

Det er et par ting du kan gjøre for å forbedre ytelsen:

* Alternativet **Del etter dato**

   Denne fremgangsmåten samler inn finansposter etter dato i stedet for måned, som er standarden, med bedre ytelse som resultat. 
   
* **XML-alternativet**

   Når det gjelder [!INCLUDE[prod_short](../../includes/prod_short.md)] lokalt, kan du la være å generere ZIP-filer fra eksporten. Dermed eksporteres de rå XML-filene, som bare er mulig når det finnes en **Mappebane** å eksportere til. Brukeren kan deretter komprimere filene manuelt, som gjør at du sparer serverressurser. SAF-T-filer kan være store, og det kan ta en stor mengde serverressurser å komprimere dem til en ZIP-fil. 
   
* Alternativet **Opprett flere ZIP-filer**

Når det gjelder både Online og lokalt, kan du også bruke alternativet for å opprette flere ZIP-filer for svært store eksporter med mange transaksjoner. Dette er nyttig hvis enkeltfiler per måned er svært store, eller antallet filer per dato er for stort. Bruk dette alternativet når den ene store ZIP-filen ikke kan valideres på myndighetenes nettsted, for eksempel på grunn av størrelsen. Når du bruker denne funksjonen, deles eksporten inn i flere ZIP-filer, opptil 10 i samsvar med kravene som er angitt i den generelle SAF-T-dokumentasjonen. Siden **SAF-T-eksporterte filer** åpnes alltid når du bruker handlingen **Last ned fil**. Her kan du se hvor mange filer som ble generert, og laste dem ned én etter én.  

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[prod_short](../../includes/prod_short.md)] ved hjelp av utvidelser](../../ui-extensions.md)  
[Bli klar til å gjøre forretninger](../../ui-get-ready-business.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]