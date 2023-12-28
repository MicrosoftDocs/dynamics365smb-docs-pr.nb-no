---
title: Behandle salgsmuligheter i salgssykluser
description: Dette emnet beskriver de ulike måtene du kan behandle salgsmuligheter på i salgssykluser og flytte en salgsmulighet gjennom fasene i en salgssyklus.
author: jswymer
ms.author: jswymer
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'relationship, prospect'
ms.date: 12/28/2023
ms.custom: bap-template
---
# Behandle salgsmuligheter

Når du oppretter en salgsmulighet, er det flere funksjoner for å behandle salgsmuligheten og fullføre den.

## Vis salgsmuligheter

Eksisterende salgsmuligheter er tilgjengelige på siden **Oversikt over salgsmuligheter**. Tabellen nedenfor beskriver måter å få tilgang til siden på for å behandle salgsmuligheter.

| Vise salgsmuligheter for | Deretter |
| --- | --- |
| Alle selgere og kontakter |Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Oversikt over salgsmuligheter**, og velg deretter den relaterte koblingen. |
| En bestemt selger |Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Selgere**, og velg deretter den relaterte koblingen. Velg selger, velg handlingen **Salgsmuligheter** og velg deretter handlingen **Vis**. |
| En bestemt kontakt |Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Kontakter**, og velg deretter den relaterte koblingen. Velg kontakten fra listen, og velg deretter handlingen **Salgsmuligheter**. |

Hver av disse aktivitetene åpner siden **Oversikt over salgsmuligheter**.

## Lukk salgsmuligheter

Du kan lukke salgsmuligheter når forhandlingene er over. Når du lukker en salgsmulighet, kan du oppgi om den ble vunnet eller mistet og årsaken til at du lukker den. Hvis du vil an angi en årsak, må først definere koder for lukkede salgsmuligheter.

1. På siden **Oversikt over salgsmuligheter** velger du salgsmuligheten og deretter handlingen **Lukk**. Siden **Lukk salgsmulighet** åpnes.
2. Fyll ut de relevante feltene, og klikk deretter **OK**.

   Feltene **Lukk. av salgsmuligh. - kode** og **Lukket den** er obligatoriske og må fylles ut før du velger **Neste**-knappen.

   I feltet **Lukk. av salgsmuligh. - kode** kan du velge fra en av de eksisterende kodene for lukking av salgsmulighet eller legge til en ny kode. Hvis du vil legge til en ny kode fra rullegardinlisten, velger du **Velge fra hele listen** og deretter **ny**. På den nye, tomme linjen fyller du ut feltet **Kode**, **Type** og **Beskrivelse**, og deretter velg du **OK** knappen.

## Opprett tilbud for salgsmuligheter

> [!NOTE]
> Du kan bare opprette tilbud fra salgsmuligheter der kontakttypen er Selskap.

1. På siden **Oversikt over salgsmuligheter** velger du salgsmuligheten og deretter handlingen **Tilordne nytt tilbud**. Siden **Tilbud** åpnes.
2. Fyll ut de aktuelle feltene.

## Opprett ordrer for salgsmuligheter

Du kan opprette ordrer på bakgrunn av tilbudene du har opprettet for salgsmulighetene. Før du kan opprette ordrer for kontaktene, må du opprette kontakten som en kunde. Hvis du vil ha mer informasjon, kan du se [Opprette kontakter](marketing-create-contact-companies.md).

1. På siden **Oversikt over salgsmuligheter** finner du salgsmuligheten du har opprettet et tilbud for.
2. Velg handlingen **Tilordne nytt tilbud**. Siden **Tilbud** åpnes, som viser tilbudet du har tilordnet salgsmuligheten.
3. Fyll ut tilleggsfeltene, og klikk deretter handlingen **Lag ordre**.

Når du håndterer salgsmuligheter, kan det være at du må opprette et tilbud for kontakten som salgsmuligheten er knyttet til.

## Slett salgsmuligheter

Du kan slette salgsmuligheter eksempel etter at du for har inngått en avtale. Du kan imidlertid bare slette lukkede salgsmuligheter. Det er to metoder for å slette lukkede salgsmuligheter. Du kan slette individuelle lukkede salgsmuligheter fra siden **Oversikt over salgsmuligheter**, eller du kan kjøre den satsvise jobben **Slett salgsmuligheter** for å slette flere salgsmuligheter basert på angitte vilkår.

Hvis du vil slette lukkede salgsmuligheter fra siden **Oversikt over salgsmuligheter**, velger du salgsmuligheten og deretter handlingen **Slett**.

Hvis du vil slette lukkede salgsmuligheter ved hjelp av den satsvise jobben **Slett salgsmuligheter**, følger du denne fremgangsmåten:

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Dataadministrasjon**, og velg den relaterte koblingen.
2. Velg handlingen **Slett salgsmuligheter**, og angi filtrene som angir de lukkede salgsmulighetene du vil slette.
3. Velg **OK**-knappen.

Når du har slettet en salgsmulighet, fjernes den fra siden **Oversikt over salgsmuligheter**.

## Flytt en salgsmulighet gjennom salgssyklusfaser

Hvis en salgsmulighet følger en salgssyklus, kan du flytte den til neste eller forrige fase, og til og med hoppe over en fase.

1. På siden **Oversikt over salgsmuligheter** velger du handlingen **Oppdater**. **Oppdater salgsmulighet** åpnes.
2. Bruk feltet **Handlingstype** for å flytte salgsmuligheten gjennom faser i salgssyklusen:
   * **Neste** flytter salgsmuligheten fremover en fase.
   * **Hopp over** flytter salgsmuligheten fremover én eller flere faser i salgssyklusen, som du angir i feltet **Presentasjon**. Du kan bare hoppe over faser som er satt opp slik at de tillater utelatelse.
   * **Forrige** flytter salgsmuligheten bakover en fase.
   * **Hopp** flytter salgsmuligheten bakover én eller flere faser i salgssyklusen, som du angir i feltet **Presentasjon**.
   * **Oppdater** lar deg endre informasjonen (for eksempel endre evalueringen av salgsutsikter og anslåtte verdier) uten å flytte til en annen fase.
3. Fyll ut de andre feltene etter behov, og klikk deretter **OK**.

## Se også

[Salg](sales-manage-sales.md)  
[Opprette og administrere kontakter](marketing-contacts.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]