---
title: Arbeide med servicekontrakter og servicekontrakttilbud | Microsoft-dokumentasjon
description: Du kan opprette servicekontrakter manuelt eller fra et servicekontrakttilbud. Du kan opprette en kontrakt basert på et servicekontrakttilbud.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 9cfb99319510b76843e7c94adedb66835023c55d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775303"
---
# <a name="work-with-service-contracts-and-service-contract-quotes"></a>Arbeide med servicekontrakter og servicekontrakttilbud
Du kan opprette servicekontrakter manuelt eller fra et servicekontrakttilbud. Du kan bruke et servicekontrakttilbud som en forløper til en servicekontrakt der selskapet kommer med et tilbud overfor kunden, og som får godkjenning fra kunden før du kan konvertere tilbudet til en servicekontrakt. Prosedyrene for oppretting av servicekontrakt og servicekontrakttilbud er like.  

## <a name="to-create-a-service-contract-or-service-contract-quote"></a>Slik oppretter du en servicekontrakt eller et servicekontrakttilbud  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakter** eller **Servicekontrakttilbud**, og velg deretter den relaterte koblingen.  
2. Opprett en ny servicekontrakt eller et servicekontrakttilbud.  
3. Fyll ut feltet **Nr.** . Det vises en dialogboks med forespørsel om du vil fylle den ut med vanlige data fra en kontraktmal. Hvis du vil opprette en slik servicekontrakt eller et slikt servicekontrakttilbud, velger du **Ja**-knappen. Siden **Oversikt over servicekontraktmaler** åpnes.  
4. Velg den relevante malen, og velg deretter **OK** for å bruke den til å opprette servicekontrakten eller servicekontrakttilbudet.  
5. I feltet **Kundenr.** Velg kunde.  
6. Hvis du ikke vil at en årlig beløpsdifferanse skal fordeles automatisk, velger merker du av for **Tillat beløp som ikke er i balanse**. Verdiene i feltene **Årlig beløp** og **Beregnet årlig beløp** blir ikke automatisk utlignet. Hvis du vil at programmet automatisk skal distribuere årlig beløpsdifferanse som kan oppstå basert på en endring i servicekontrakten, fjerner du merket for **Tillat beløp som ikke er i balanse**.  
7. Legg til kontraktlinjer til servicekontrakten eller servicekontrakttilbudet.  
8. Fyll ut de resterende feltene ved behov.  

## <a name="to-convert-a-service-contract-quote-to-service-contract"></a>Slik konverterer du et servicekontrakttilbud til en servicekontrakt  
Når en kunde har godkjent et servicekontrakttilbud, konverterer du det til en servicekontrakt. Du kan samtidig opprette en servicefaktura for startperioden til kontrakten hvis startdatoen til kontrakten er før begynnelsen av neste fakturaperiode.

Når du har fullført fremgangsmåten nedenfor, opprettes det en servicekontrakt med statusen **Signert**. Hvis en servicefaktura opprettes for startperioden til kontrakten, beregnes det fakturerte beløpet på følgende måte, avhengig av om kontrakten er detaljert eller ikke.  

Når det gjelder detaljerte kontrakter, beregnes det fakturerte beløpet slik:  

* Fakturert beløp = summen av det fakturerte beløpet for hver enkelt kontraktlinje.  
* Fakturert beløp for hver enkelt kontraktlinje = ((tilbudsverdi ÷ 12) × antall måneder i startperioden) + ((tilbudsverdi ÷ antall dager i året) × antall dager igjen i startperioden).  
* Hvis kontraktlinjen utløper før startperioden er avsluttet, blir utløpsdatoen sluttdatoen til startperioden for linjen.  

Når det gjelder kontrakter som ikke er detaljerte, beregnes det fakturerte beløpet slik:  

* Fakturert beløp = (årlig beløp ÷ antall dager i året) × antall dager i startperioden.  
* Hvis kontrakten utløper før startperioden er avsluttet, blir utløpsdatoen sluttdatoen til startperioden.    

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakttilbud**, og velg deretter den relaterte koblingen.  
2. Åpne servicekontrakttilbudet du vil konvertere til en servicekontrakt.  
3. Velg handlingen **Lag kontrakt**.  
4. Hvis kontraktens startdato er før begynnelsen av neste fakturaperiode, blir du spurt om du vil opprette en faktura for kontraktens startperiode. Velg **Ja**.  

 Servicefakturaen bokføres til servicekontoen for kontrakten, uavhengig av om kontrakten er forhåndsbetalt.

## <a name="to-create-contract-service-credit-memos"></a>Slik oppretter du servicekreditnotaer for kontrakter
Du kan bruke en servicekreditnota for kontrakter når en kunde avbryter en forhåndsbetalt servicekontrakt, eller fjerner en servicevare fra en forhåndsbetalt kontrakt. Du kan dessuten bruke den til å korrigere en feilaktig servicefaktura.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Service – kreditnotaer**, og velg deretter den relaterte koblingen.  
2. Opprett en servicekreditnota.  
3. Fyll ut feltet **Nr.** .  
4. I feltet **Kundenr.** angir du nummeret på kunden i servicekontrakten.  

     Hurtigfanen **Fakturering** viser flere opplysninger som er kopiert fra **Kunde**-kortet. Hvis du vil bokføre kreditnotaen til en annen kunde enn den som er angitt på hurtigfanen **Generelt**, angir du nummeret på den kunden i feltet **Faktura til-kundenr.**. .  

    > [!NOTE]  
    >  Du kan sammenligne kreditnotaen med det opprinnelige bokførte dokumentet på siden **Bokførte servicefakturaer**. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokførte servicefakturaer**, og velg deretter den relaterte koblingen.  

5. Fyll ut feltene **Bokføringsdato** og **Dokumentdato**.  
6. På kreditnotalinjene angir du opplysninger om varene som er returnert eller fjernet, eller om rabatten som skal sendes. Du kan også bruke kjørselen **Hent forh.bet. kontraktposter**.  

 Hvis du vil automatisk opprette en kreditnota når kontraktslinjer fjernes i en servicekontrakt på siden **Servicekontrakt** på hurtigfanen **Fakturadetaljer**, merker du av for **Automatiske kreditnotaer**.  

 Hvis du vil opprette en kreditnota manuelt når kontraktlinjer fjernes fra en servicekontrakt, velger du **Kreditnotat** på siden **Servicekontrakt**.  

## <a name="updating-and-evaluating-contracts"></a>Oppdatere og evaluere kontrakter
Noen ganger må du endre betingelsene i en kontrakt etter at den er opprettet. I de fleste tilfeller åpner du den aktuelle kontrakten på **Servicekontrakt**-siden og endrer den.  

Du kan endre kontraktens status, som til å begynne med er satt til **Låst**, legge til og fjerne kontraktlinjer og kansellere en kontrakt. Hvis du vil se hvordan forretningen gjør det, målt i agio og disagio, kan du foreta en rask forretningsanalyse ved hjelp av funksjonen Kontrakt - Trendscape.

## <a name="to-add-a-contract-line-to-a-service-contract-or-contract-quote"></a>Slik legger du til en kontraktlinje i en servicekontrakt eller et kontrakttilbud  
Når en kunde kjøper en ny vare og vil inkludere den i den eksisterende servicekontrakten eller kontrakttilbudet, kan du registrere varen som en servicevare, og deretter legge den til som en ny kontraktlinje i kontrakten eller kontrakttilbudet.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakter**, og velg deretter den relaterte koblingen.  
2. Åpne servicekontrakten eller servicekontrakttilbudet du vil legge til en ny kontraktlinje for.  
3. Velg handlingen **Åpne kontakt** for å åpne servicekontrakten eller servicekontrakttilbudet for redigering.  
4. På hurtigfanen **Fakturadetaljer** velger du feltet **Tillat beløp som ikke er i balanse** hvis du vil endre årlig beløp og fordele differansen i årlig beløp manuelt på kontraktlinjene. Ellers fjerner du merket for **Tillat beløp som ikke er i balanse**. Dette vil fordele differansen i årlig beløp automatisk på kontraktlinjene når du har endret årlig beløp.  
5. På hurtigfanen **Linjer** legger du til en servicevare eller vare, eller tekstbeskrivelse, på hver kontraktlinje. Du kan også legge til kontrakttilbudslinjer. Legg merke til at du kan opprette flere kontrakter for hver servicevare, slik at varen tas med i forskjellige kontrakter eller kontrakttilbud samtidig.  
6. Kontroller og rett tallene i feltene **Linjerabatt-%**, **Linjerabattbeløp**, **Responstid**, **Serviceperiode** og andre felt etter behov.

## <a name="to-remove-contract-lines"></a>Slik fjerner du kontraktlinjer  
Du kan bli nødt til å fjerne kontraktlinjer fra servicekontrakten etter hvert som du fjerner tilsvarende servicevarer fra servicekontrakten. Vanligvis fjerner du kontraktlinjer som er utløpt eller tilsvarer servicevaren som er ødelagt.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakter**, og velg deretter den relaterte koblingen.  
2. Åpne servicekontrakten du vil fjerne kontraktlinjer fra.  
3. Velg handlingen **Åpne kontakt** for å åpne servicekontrakten for redigering.  
4. Velg kontraktlinjen du vil fjerne. Fyll ut feltet **Kontraktens utløpsdato** med datoen da du vil fjerne linjen. Det kan for eksempel angi datoen da servicevaren sluttet å virke.  
5. Velg handlingen **Fjern kontraktlinjer**. Siden **Fjern linjer fra kontrakt** åpnes.  
6. Fyll ut standardfiltrene: **Kontraktnr.**, **Servicevarenr.** og **Kontrakttype**. Om nødvendig kan du bruke flere filtre eller endre de eksisterende.  
7. Fyll ut feltene i hurtigfanen **Alternativer**, og velg deretter **Slett linjer**.  

> [!NOTE]  
>  Hvis kontrakten ikke er detaljert, må du oppdatere verdien i **Årlig beløp**-feltet på hurtigfanen **Fakturadetaljer** på **Servicekontrakt**-siden, som gjenspeiler tapet av servicevaren fra kontrakten.  
>   
>  Hvis kontrakten er detaljert og forhåndsbetalt og du har bokført fakturaer for kontrakten, kan du opprette en kreditnota for kontrakten. Velg handlingen **Opprett kreditnota**. Dette er unødvendig hvis avmerkingsboksen i feltet **Automatiske kreditnotaer** på hurtigfanen **Fakturadetaljer** er valgt. I dette tilfellet opprettes en kreditnota automatisk når du fjerner en kontraktlinje.

## <a name="service-line-cost-and-value"></a>Kostnadene på servicelinjen og verdi
På en servicekontraktlinje beregnes beløpene i **Linjekostnad** og **Linjeverdi** som beskrevet i tabellen nedenfor.

| Alternativer for linjekostnad | Beskrivelse|
|----------------------------------|---------------------------------------|  
|**Servicevare** | Kostnaden hentes automatisk fra feltet **Standard kontraktkost** i tabellen **Servicevare**, og kopieres til feltet **Linjekostnad**. Følgende formel brukes ved beregning av Linjekostnad:<br /><br /> Enhetskost - salg × Kontraktverdi % ÷ 100|  
|**Vare** | Kostnaden hentes automatisk fra feltet **Enhetskost** i tabellen **Vare**, og fra feltet **Kontraktverdi-%** i tabellen **Serviceoppsett**. Følgende formel brukes ved beregning av Linjekostnad:<br /><br /> Enhetskost × Kontraktverdi-% ÷ 100|  
|**Tekstbeskrivelse** | Verdien i **Linjekostnad**-feltet er satt til null.|  

| Alternativer for linjeverdi | Beskrivelse|
|----------------------------------|---------------------------------------|  
|**Servicevare** | Prisen hentes automatisk fra feltet **Standard kontraktverdi** i tabellen **Servicevare**, og kopieres til feltet **Linjeverdi**.|  
|**Vare** | Avhengig av verdien i feltet **Beregn.måte for kontraktverdi** i tabellen **Serviceoppsett** hentes beløpet fra feltet **Salgspris** eller **Enhetskost** i **Vare**-tabellen. Deretter multipliseres verdien med innholdet i feltet **Kontraktverdi-%** i tabellen **Serviceoppsett**, og divideres med 100. Dette beløpet kopieres til feltet Linjeverdi. Dette beløpet kopieres inn i **Linjeverdi**-feltet.<br /><br /> **OBS!** Hvis **Ingen** er angitt i feltet **Beregn.måte for kontraktverdi**, beregnes ikke innholdet i feltet **Linjeverdi**.|  
|**Tekstbeskrivelse** | Innholdet i feltet **Linjeverdi** settes til null.|  

## <a name="to-add-a-contract-discount-to-service-contract-quotes"></a>Slik legger du til en kontraktrabatt for et servicekontrakttilbud  
Du kan legge til kontraktrabatter på tjenester for kontrakttilbud og servicekontrakter. Rabattene kan gjelde for reservedeler i bestemte servicevaregrupper, for ressurstimer for ressurser i bestemte ressursgrupper, og for bestemte servicekostnader.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakttilbud**, og velg den relaterte koblingen.  
2. Velg tilbudet å legge til rabatter for.  
3. Velg handlingen **Servicerabatter**. Siden **Kontrakt-/servicerabatter** åpnes.  
4. Hvis du vil opprette en ny kontraktrabatt, velger du handlingen **Ny**.  
5. Fyll ut feltene på linjen etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].  

> [!Tip]  
>  Hvis du vil legge til kontraktrabatter direkte i en servicekontrakt, bruker du tilsvarende fremgangsmåte på siden **Servicekontrakt**.  

## <a name="to-change-the-owner-of-a-service-contract"></a>Slik skifter du eieren av en servicekontrakt  
Det kan hende du må skifte eieren av en servicekontrakt. Hvis en servicevare i en servicekontrakt er registrert i flere kontrakter som ikke er annullert, og som eies av samme kunde, endres eier automatisk for alle servicekontrakter hvor denne servicevaren er inkludert, og for alle andre servicevarer som er inkludert i disse kontraktene.  

> [!NOTE]  
>  I dette tilfellet behandles bare kontrakter som ikke er annullert. Det tas ikke hensyn til status for kontrakttilbud.  

> [!IMPORTANT]  
>  Servicevarer og kontrakter kan være relaterte. Skifte av eier av en servicekontrakt kan påvirke disse relasjonene.  
>   
>  La oss for eksempel si at servicevarenr. 8 er med både i kontrakt SC00003 og SC00015. Kontrakt SC00015 har med servicevarenr. 15, som også er med i kontrakt SC00080. I dette tilfellet blir eieren for alle tre kontrakter og servicevarer endret.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakter**, og velg deretter den relaterte koblingen. Åpne den aktuelle servicekontrakten som du vil endre eier av.  
2. Velg handlingen **Åpne kontakt** for å åpne kontrakten for redigering.  
3. Velg handlingen **Skift kunde**. Siden **Skift kunde i kontrakt** åpnes.  
4. I feltene **Kontraktnr.** og **Servicevarenr.** ser du nummeret på kontrakten og servicevaren som eies av den valgte kunden. Hvis kunden eier flere kontrakter med flere servicevarer, blir verdien i disse feltene **Flere**. Hvis du vil se listen over relaterte kontrakter eller servicevarer, kan du velge disse feltverdiene.  
5. Velg den nye kunden i feltet **Nytt kundenr.** velger du ny kunde.  
6. Velg adresse i **Ny lever til-kode**-feltet.  
7. Velg **OK**-knappen for å endre kunden og lever til-koden i servicekontraktene.  
8. Velg handlingen **Lås kontrakt** for å låse kontrakten og for å sørge for at endringene blir en del av kontraktene.  

## <a name="to-update-a-service-contract-price"></a>Slik oppdaterer du en servicekontraktpris:  
Du kan oppdatere prisene på servicekontrakter ved å angi en prisoppdateringsprosent.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppdater servicekontraktpriser**, og velg deretter den relaterte koblingen.
2. Velg servicekontrakten.  
3. Angi en dato i feltet **Oppdater t.o.m. den**. Kjørselen oppdaterer priser for kontrakter med neste prisoppdateringsdatoer på eller før denne datoen.  
4. I feltet **Prisoppdaterings-%** angir du prosenten du vil oppdatere prisene med.  
5. I **Handling**-feltet velger du **Oppdater kontraktpriser**.  

## <a name="to-post-prepaid-contract-entries"></a>Slik bokfører du forhåndsbetalte kontraktposter  
Hvis du arbeider med forhåndsbetalte servicekontrakter, må du regelmessig bokføre forhåndsbetalte kontraktposter, og dermed overføre de forhåndsbetalte innbetalingene fra forhåndsbetalingskontiene for kontrakten til de vanlige kontraktkontiene.  

Før du kan bokføre forhåndsbetalte kontraktposter må du angi en nummerserie i feltet **Bilagsnr. for bokf. forh.betal.** på **Serviceoppsett**-siden.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bokf. forh.bet. kontraktposter**, og velg deretter den relaterte koblingen.  
2. Angi en dato i feltet **Bokfør t.o.m. den** . Kjørselen bokfører forhåndsbetalte serviceposter med bokføringsdatoer frem til denne datoen.  
4. I **Bokføringsdato**-feltet angir du datoen du vil bruke som bokføringsdato på finanskladdelinjen.  
5. I **Handling**-feltet velger du **Bokf. forhåndsbet. transaksjoner**.  
6. Velg **OK** for å bokføre postene.

## <a name="changing-the-service-contract-status"></a>Endrer status for servicekontrakten
Når servicekontrakten er undertegnet, settes verdien i feltet **Endringsstatus** automatisk til **Låst**. Hvis du vil endre opplysningene i servicekontrakten eller servicekontrakttilbudet, må du først endre status for kontrakten eller kontrakttilbudet, fra **Låst** til **Åpen**. Merk at du ikke kan opprette servicefakturaer for servicekontrakten med endringsstatus **Åpen**. Når kontrakten eller kontrakttilbudet er endret, må du endre status tilbake til **Låst**, slik at det igjen blir mulig å opprette servicefakturaer og finansposter for servicekontrakten, som inkluderer de endringene du foretok.  

> [!NOTE]  
>  Feltet **Endre status** er ikke relatert til **Frigivelsesstatus**-feltet på serviceordrehodet, som styrer lagerhåndteringen av servicevarer.  

## <a name="to-cancel-a-service-contract"></a>Slik annullerer du en servicekontrakt  
Du kan bli nødt til å annullere en servicekontrakt når den er utløpt eller er annullert av deg eller kunden.  

> [!NOTE]  
>  Du kan ikke åpne en kontrakt etter at den er kansellert.  

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Servicekontrakter**, og velg deretter den relaterte koblingen.  
2. Åpne servicekontrakten du vil kansellere.  
3. Velg handlingen **Åpne kontakt** for å åpne servicekontrakten for redigering.  
4. I feltet **Kanselleringsårsakskode** velger du den aktuelle feilårsakskoden. Hvis du vil legge til flere årsakskoder, velger du handlingen **Avansert**.  

     Hvis det er merket av for **Bruk kontraktavbruddsårsak** på siden **Serviceoppsett**, må du angi en kanselleringsårsakskode når kontrakten skal kanselleres.  

5. I feltet **Status** velger du **Kansellert**.  
6. Hvis det finnes fakturaer, kreditnotaer eller åpnede betalte poster for kontrakten, vises en bekreftelsesmelding. Velg **Nei** i meldingsboksen for å gå tilbake til kontrakten for å bokføre dokumentene, eller på **Ja** for å fortsette annulleringsprosessen.  

## <a name="filing-a-service-contract-or-contract-quote"></a>Arkivere en servicekontrakt elle et kontrakttilbud  
Du kan når som helst arkivere servicekontrakter og kontrakttilbud for å registrere og arkivere en kopi av kontrakten eller kontrakttilbudet. [!INCLUDE[prod_short](includes/prod_short.md)] arkiverer servicekontrakter automatisk når du konverterer kontrakttilbud til servicekontrakter eller avbryter servicekontrakter. Du kan arkivere en kontrakt eller et tilbud selv ved å velge handlingen **Arkiver kontrakt** på siden **Servicekontrakter** eller **Servicekontrakttilbud**. Hvis du vil vise de arkiverte kontraktene for tilbud ved å søke etter **Arkiverte kontrakter**.

## <a name="see-also"></a>Se også  
[Definere servicekontrakter](service-how-setup-service-contracts.md)  
[Servicebehandling](service-service.md)  
[Konvertere servicekontrakter som inkluderer mva-beløp](service-how-to-convert-service-contracts.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]