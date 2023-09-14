---
title: Behandle ordrereturer
description: 'Beskriver hvordan du oppretter en ordreretur for å behandle en retur, kansellering eller refusjon for varer eller tjenester du har mottatt betaling for.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 09/08/2021
ms.author: bholtorf
---
# Behandle ordrereturer  

Hvis du trenger mer kontroll over ordrereturprosessen, for eksempel lagerdokumenter for varehåndtering eller bedre oversikt når du mottar varer fra flere salgsdokumenter med en ordreretur, kan du opprette ordrereturer. En ordreretur utsteder automatisk den relaterte salgskreditnotaen, og andre returrelaterte dokumenter, for eksempel en erstatningsordre om nødvendig.

I tillegg til den opprinnelige bokførte salgsfakturaen, kan du bruke salgskreditnotaen eller ordrereturen for andre salgsdokumenter, for eksempel en annen bokført salgsfaktura, fordi kunden også returnerer varer som leveres med denne fakturaen.

## Opprett en ordreretur basert på ett eller flere bokførte salgsdokumenter  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Ordrereturer**, og velg deretter den relaterte koblingen.
2. Velg handlingen **Ny**.  
3. Fyll ut feltene i hurtigfanen **Generelt** etter behov.
4. I **Linjer**-hurtigfanen fyller du ut linjene manuelt, eller kopier informasjon fra andre dokumenter for å fylle ut linjene automatisk:

    - Bruk funksjonen  **Hent bokførte dokumentlinjer som skal tilbakeføres** for å kopiere én eller flere bokførte dokumentlinjer fra ett eller flere bokførte dokumenter. Denne funksjonen tilbakefører alltid kost nøyaktig fra den bokførte dokumentlinjen. Denne funksjonen er beskrevet i følgende fremgangsmåter.    
    - Bruk funksjonen **Kopier fra dokument** til å kopiere et eksisterende dokument til ordrereturen. Bruk denne funksjonen til å kopiere hele dokumentet. Det kan være et bokført dokument eller et dokument som ikke er bokført ennå. Med denne funksjonen er nøyaktig kosttilbakeføring bare mulig hvis det er merket av for **Bruk opprinnelig kostpris** på siden **Salgsoppsett**.  

5. Velg **Prosess**-handling, og velg deretter **Hent bokførte dokumentlinjer som skal tilbakeføres**.
6. Øverst på siden **Bokførte salgsdokumentlinjer** merker du av for **Vis bare reversible linjer** hvis du bare vil se salgslinjer med antall som ennå ikke er tilbakeført. Hvis for eksempel antallet for en bokført salgsfaktura allerede har blitt tilbakeført, kan det hende du ikke vil tilbakeføre det antallet på et nytt ordrereturdokument.

    > [!NOTE]  
    >  Dette feltet fungerer bare for bokførte følgesedler og bokførte fakturalinjer, og ikke for bokførte retur- eller kreditnotalinjer.

    Til venstre på siden vises en oversikt over de ulike dokumenttypene, og nummeret i hakeparenteser viser antall dokumenter som er tilgjengelige for hver enkelt dokumenttype.

7. I feltet **Filter for bilagstype** velger du typen bokførte dokumentlinjer du vil bruke.  
8. Velg linjene du vil kopiere til det nye dokumentet.  

    > [!NOTE]  
    >  Hvis du bruker <kbd>Ctrl</kbd>+<kbd>A</kbd> for å velge alle linjene, kopieres alle linjene med det filteret du har angitt, men filteret **Vis bare reversible linjer** ignoreres. Hvis du for eksempel har filtrert linjene for et bestemt dokumentnummer med to linjer, og en av dem allerede er tilbakeført. Selv om feltet **Vis bare reversible linjer** er valgt, kopieres begge linjene når du velger <kbd>Ctrl</kbd>+<kbd>A</kbd> for å kopiere alle linjene, ikke bare den linjen som ennå ikke er tilbakeført.  

9. Velg **OK**-knappen for å kopiere linjene til det nye dokumentet.  

    Følgende skjer:  

    -   For bokførte dokumentlinjer av typen **Vare** opprettes en ny dokumentlinje som er en kopi av den bokførte dokumentlinjen, med antall som ennå ikke er tilbakeført. Feltet **Utlignet fra-varepost** fylles ut etter behov med tallet på vareposten for den bokførte dokumentlinjen.  

    -   For bokførte dokumentlinjer som ikke er av typen **Vare**, for eksempel varegebyrer, opprettes en ny dokumentlinje som er en kopi av den opprinnelige bokførte dokumentlinjen.  

    -   **Enhetskost (LV)**-feltet beregnes på den nye linjen fra kosten for de tilhørende varepostene.  

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

## Slik oppretter du en erstatningsordre fra en ordreretur:
Du kan bestemme deg for å kompensere en kunde for en vare du har solgt ved å erstatte varen. Du erstatter varen med samme vare, eller med en annen vare. Denne situasjonen kan for eksempel oppstå hvis du ved en feiltakelse leverer feil vare til kunden.  

1. På siden **Ordreretur** for en aktiv returprosess lager du en negativ post på en tom linje for erstatningsvaren ved å sette inn et negativt beløp i **Antall**-feltet.  
2. Velg handlingen **Flytt negative linjer**.
3. På siden **Flytt negative salgslinjer** fyller du ut feltene etter behov.
4. Velg **OK**. Den negative linjen for erstatningsvaren slettes fra ordrereturen, og den settes inn på en ny **Ordre**-side. Hvis du vil ha mer informasjon, kan du se [Selge produkter](sales-how-sell-products.md).

## Slik oppretter du retur-relaterte dokumenter fra en ordreretur:
Du kan opprette erstatningsordrer, bestillingsreturer og erstatningsbestillinger under ordrereturprosessen. Dette er for eksempel nyttig i situasjoner hvor du vil håndtere varer med garantier fra leverandører.

1. På siden **Ordreretur** for en aktiv returprosess velger du handlingen **Opprett retur-relaterte dokumenter**.
2. I **Leverandørnr.**-feltet angir du nummeret til en leverandør hvis du vil opprette leverandørdokumenter automatisk.
3. Hvis en returnert vare må returneres til leverandøren, merker du av for **Opprett bestillingsretur**.
4. Hvis en returnert vare må bestilles fra leverandøren, merker du av for **Opprett bestilling**.
5. Hvis en erstatningsordre må opprettes, merker du av for alternativet **Opprett ordre**.

## Slik oppretter du et returgebyr
Det kan hende du vil belaste kunden med et returgebyr for å dekke kostnader i forbindelse med retur av en vare. Dette er aktuelt hvis kunden for eksempel har bestilt feil vare, eller ombestemt seg etter at han eller hun mottok varen.

Du kan bokføre denne økte kostnaden som et varegebyr i en kreditnota eller en ordreretur, og knytte den til den bokførte følgeseddelen. Det følgende beskriver denne for en ordreretur, men de samme trinnene gjelder en salgskreditnota.

1. Åpne siden **Ordreretur** for en aktiv returprosess.
2. Velg **Gebyr (vare)** i **Type**-feltet på en ny linje.  
3. Fyll ut feltene for en hvilken som helst varegebyrlinje. Hvis du vil ha mer informasjon, kan du se [Bruke varegebyr til å gjøre rede for ekstra handelskostnader](payables-how-assign-item-charges.md).  

Når du bokfører ordrereturen, legges et returgebyr til i det aktuelle salgsbeløpet. Dermed kan du opprettholde en nøyaktig lagerverdisetting.  

## Se relatert [Microsoft-opplæring](/training/paths/return-items-dynamics-365-business-central/)

## Se også

[Salg](sales-manage-sales.md)  
[Sette opp salg](sales-setup-sales.md)  
[Administrere skyldige beløp](payables-manage-payables.md)  
[Send dokumenter i e-post](ui-how-send-documents-email.md)  
[Behandle bestillingsreturer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
