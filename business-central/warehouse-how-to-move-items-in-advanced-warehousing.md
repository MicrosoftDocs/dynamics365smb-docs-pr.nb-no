---
title: Flytt varer i lagre som bruker lagerstyring
description: Denne artikkelen forklarer hvordan du flytter varer på lokasjoner som bruker lagerstyring.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7351,'
ms.service: dynamics-365-business-central
---

# Flytt varer i avanserte lageroppsett som bruker lagerstyring

Du kan flytte varer mellom hyller uten behov fra et kildedokument. Det kan for eksempel være at du vil gjøre dette som en del av følgende aktiviteter:

* Organiser lageret på nytt.
* Overføre varer til et inspeksjonsområde.
* Ta varer tas ut av plukkhyller midlertidig, for eksempel for å tjene som demonstrasjonsmodeller i en salgspresentasjon.
* Flytt ekstra varer til produksjonsområde for komponenter som er konfigurert med enkelte trekkmetoder.
* Flytt produserte eller monterte varer fra produksjons- eller monteringsområde til lager.
* Flytt varer fra masselagringsområdet til hyllene du bruker til plukking.

Hvordan du flytter varer avhenger av hvordan lageret er definert som lokasjon. Finn ut mer under [Definer lagerstyring](warehouse-setup-warehouse.md).

I lageroppsett der **Lagerstyring**-vekslebryteren er aktivert for lokasjoner kan du registrere ikke-planlagte flyttinger på følgende sider:  

* Flytteforslag
* Internt lagerplukk
* Intern lagerplassering
* Lagerreklassifiseringskladd

Sidene **Flytteforslag**, **Internt lagerplukk** og **Intern lagerplassering** fungerer på samme måte. Bruk sidene til å klargjøre lageraktiviteter for de lageransatte. Forskjellen er i de avanserte funksjonene som er knyttet til hver side, og de ulike typene lageraktiviteter som sannsynligvis utføres av ulike ansatte:

* Flytteforslag lar deg fylle opp plukkhyller med høy rangering med varer fra andre hyller
* Plassering bruker plasseringer maler
* Plukk bruker hylleprioritering og tilgjengelighet

## Lagerflytteforslag

### Flytte varer med lagerflytteforslaget

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Flytteforslag**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene på forslagslinjene manuelt, eller bruk en av følgende handlinger til å fylle ut linjene automatisk:

    * **Hent hylleinnhold** fyller ut forslagslinjene med innholdet i hyllen eller hyllene du angir.
    * **Beregn hylleetterfylling** bruker hylleprioriteringene til å foreslå etterfylling fra hyller med lav prioritet til hyller med høy.

    > [!NOTE]  
    > Hvis varen oppfyller kriteriene i oversikten nedenfor, er feltene **Fra sone** og **fra hylle** tomme. [!INCLUDE [prod_short](includes/prod_short.md)] beregner fra hvor varene skal flyttes til bare når du bruker handlingen **Opprett flytting**.  
    >  
    > * Varen har en utløpsdato.  
    > * Vekslebryteren **Plukk i henhold til FEFO** er slått på for lokasjonen.  
    > * Du bruker funksjonen **Beregn etterfylling av hyller**  

3. Velg **Opprett flytting**-handling for å opprette flyttingen. Når flyttingen er fullført, kan du registrere den på nytt.  

### Slik registrerer du lagerflyttingen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Flyttinger**, og velg deretter den relaterte koblingen.  
2. Åpne flyttedokuementet du vil registrere.  
3. På **Plasser**-linjene angir du hvor, hvilke, og etter når den aktuelle varen skal flyttes ved å velge verdier feltene **Sonekode**, **Hyllekode**, **Ant. som skal håndt.** eller **Forfallsdato**.  
4. På **Hent**-linjer i feltet **Ant. som skal håndt.** angir du antallet av hylleinnholdet som du vil flytte. Du kan bare redigere dette feltet på **Hent**-linjer. 

    > [!NOTE]
    > Hvis du må plukke eller plassere varene for én linje i mer enn én hylle, for eksempel fordi den angitte hyllen er full, bruker du handlingen **Del linje** i hurtigfanen **Linjer**. Handlingen oppretter en linje der restantallet skal håndteres.
 
5. Hvis du vil registrere alle foreslåtte antall som er angitt i **Antall**-feltet, velger du handlingen **Autoutfyll ant som skal håndt**.  
6. Velg handlingen **Registrer**.  

> [!NOTE]  
> For lokasjoner som bruker lagerstyring, kan du ikke manuelt flytte varer i hyller av typen **MOTTA** fordi de ennå ikke anses som tilgjengelig lager. Du må plassere varene i disse hyllene før de er tilgjengelige for flytting.

## Internt plukk  

### Opprette en intern plukking  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Intern plukk**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltet **Nr.** feltet **Lokasjonskode** og **Til hylle-kode** i hurtigfanen **Generelt**. Feltet **Til hylle-kode** angir hyllen der du vil plassere de plukkede varene. Til produksjonsformål ville denne hyllen være den inngående produksjonshyllen eller den åpne produksjonshyllen. Til andre formål velger du en hyllekode for en hylletype som ikke brukes til plukking, sannsynligvis en hylle for oppsamling, levering eller spesielle formål.  
4. Velg en vare i feltet **Varenr.**, og fyll ut antallene du vil plukke.  
5. Velg handlingen **Opprett plukk**. En plukkinstruksjon er nå klar til utføring av en lageransatt. Du kan også velge **Frigi**-handlingen og opprette lagerplukk ved hjelp av **Plukkforslag**-siden. Hvis du vil ha mer informasjon om plukkforslag, går du til [Opprett plukkdokumenter i bulk med plukkforslaget](warehouse-how-to-pick-items-for-warehouse-shipment.md#to-create-pick-documents-in-bulk-with-the-pick-worksheet).
6. Når plukkingen er fullført, kan du registrere den på nytt.  

### Slik registrerer du lagerplukk

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angir **Plukking** og velger den relaterte koblingen.  

    Hvis du arbeider på en bestem plukking, velger du plukkingen fra oversikten eller filtrerer oversikten for å finne plukkingene som er tilordnet til deg.  
2. Hvis feltet **Tildelt bruker-ID** er tomt, angir du om nødvendig ID-en for å identifisere deg selv.  
3. Plukke varene.  

    Siden lageret er definert til å bruke lagerstyring, fastslåt hylleprioriteringen hyllene å plukke fra. Hyllene foreslås på plukklinjene. Instruksjonene inneholder minst to separate linjer for handlingene Hent og Plasser.  

4. Når du har utført plukkingen og plassert varene i leveringsområdet eller leveringshyllen, velger du **Registrer plukk**-handlingen.  

## Intern plassering  

### Opprette en intern plassering  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og skriv inn **Interne lagerplasseringer**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.
3. Fyll ut feltet **Nr.** og **Lokasjonskode**-felter.
4. Fyll ut en linje for hver vare du vil flytte til lageret. Feltet **Varenr.** og **Antall**-feltene er obligatoriske.

    > [!NOTE]  
    > Når du velger en vare i feltet **Varenr.**, åpnes siden **Hylleinnhold** i stedet for **Varer**-siden. Denne siden åpnes fordi du plasserer en vare som er tildelt til en bestemt hylle – *hylleinnhold* – ikke bare en vare, og du vet allerede hvilken hylle varen skal tas fra. Hvis du fyller ut feltet **Fra-hyllekode**, blir hylleinnholdet filtrert etter denne verdien.

5. Hvis du vil fylle ut linjene med hele hylleinnholdet eller det filtrerte innholdet i hyller i lokasjonen, velger du handlingen **Hent hylleinnhold**.  
6. Velg handlingen **Opprett plassering**. En plasseringsinstruksjon er nå klar for en lageransatt. Du kan også velge **Frigi**-handlingen og opprette lagerplasseringer ved hjelp av siden **Plasseringsforslag**. Hvis du vil ha mer informasjon om plasseringsforslag, går du til [Opprett plasseringsdokumenter i bulk med plasseringsforslaget](warehouse-how-to-put-items-away-with-warehouse-put-aways.md#to-create-put-away-documents-in-bulk-with-the-put-away-worksheet).
6. Når plasseringen er fullført, kan du registrere den på nytt.  

### Slik registrerer du lagerplasseringen

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Plasseringer** og velg den relaterte koblingen.
2. Åpne lagerplasseringen som er klar til å håndtere.  
3. Angi bruker-ID-en når du begynner å arbeide med en plassering, om nødvendig.  

    Når du skal optimalisere plasseringsprosessen, kan du sortere plasseringslinjene etter ulike kriterier. For eksempel etter vare, hyllenummer eller forfallsdato.

    * Hvis Hent- og Plasser-linjene for hvert mottak ikke følger umiddelbart etter hverandre, og du vil at de skal gjøre det, kan du sortere linjene ved å velge **Vare** i feltet **Sorteringsmetode**.  
    * Hvis hylleprioriteringen gjenspeiler det fysiske oppsettet av lageret, kan du bruke sorteringsmetoden **hylleprioriteringen** til å organisere de midlertidige løsningene på hyllene.  

4. Utfør plasseringen.

    Hver interne plasseringslinje er blitt til mist to linjer i plasseringen.  

    * Den første linjen, med **Hent** i **Handlingstype**-feltet, angir hvor varene er plassert i mottaksområdet. Du kan ikke endre sonen og hyllen på denne linjen.  
    * Den neste linjen, med **Plasser** i **Handlingstype**-feltet, viser hvor du skal plassere varene i lageret. Hvis du mottar et stort antall varer på én mottakslinje, kan det hende du må plassere varene i flere hyller, det finnes derfor en Plass-linje for hver hylle.  

5. Når du har plassert alle varene i hyller i henhold til instruksjonen, velger du handlingen **Registrer plassering**.  

## Slik registrerer du en flytting som allerede har skjedd

Hvis du må registrere at varer allerede er flyttet til andre hyller uten plassering, plukking eller flytting, kan du bruke siden **Lagervarereklassifiseringskladd** for å registrere flyttingen.

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerreklassifiseringskladd** og velg den relaterte koblingen.  
2. Fyll ut feltene **Varenr.**, **Fra sone-kode**, **Fra hylle-kode**, **Til sone-kode**, **Til hylle-kode**.  
3. Velg handlingen **Registrer**.  

## Se også

[Oversikt over lagerstyring](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Definer lagerstyring](warehouse-setup-warehouse.md)  
[Monteringsstyring](assembly-assemble-items.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
