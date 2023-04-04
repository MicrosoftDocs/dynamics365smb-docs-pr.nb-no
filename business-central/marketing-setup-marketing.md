---
title: Konfigurer markedsføring og kontaktbehandlingsinformasjon
description: Du kan konfigurere markedsføring og kontaktbehandling i Business Central for å optimalisere forholdet til prospekter eller kunder og forbedre kampanjer.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'relationship, prospect, client, customer, campaign, promo'
ms.search.forms: '5172, 5173, 5170, 5094, 429'
ms.date: 04/01/2021
ms.author: edupont
---
# Sette opp forbindelser

Før du begynner å arbeide med kontaktene og markedsføringsinteressene, er det noen beslutninger og trinn du må gjennomføre for å definere hvordan markedsføringsområdet håndterer bestemte aspekter ved kontaktene. Du kan for eksempel avgjøre om du skal synkronisere kontaktkortet med kundekortet, leverandørkortet og bankkontokortet, hvordan tallserier defineres, eller hva standard tiltaleform skal være under skriving til kontaktene dine.

Det å behandle kontaktene og ha en strategi for å identifisere kunder, få kundenes oppmerksomhet og beholde dem vil bidra til å optimalisere bedriften og gjøre kundene mer fornøyde. Bruken av et godt kontaktbehandlingssystem vil også hjelpe deg med å danne og beholde relasjoner med kundene. Kommunikasjon er nøkkelen til disse relasjonene. Det å være i stand til å tilpasse kommunikasjon med potensielle og eksisterende kunder, leverandører og forretningspartner i henhold til behovene, er nødvendig for at bedrifter skal lykkes. Utvikling av en strategi og definering av hvordan bedriften bruker kontaktinformasjon er et grunnleggende trinn. Disse opplysningene vil bli vist av mange forskjellige grupper i bedriften, så alle vil bli mer produktive hvis du har et godt system etablert.

Du definerer markedsførings- og kontakthåndtering fra siden **Markedsføringsoppsett**. Du åpner siden **Markedsføringsoppsett** ved å velge ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Markedsføringsoppsett** og velg den relaterte koblingen.

## Automatisk kopiere spesifikk informasjon fra kontaktselskapene til kontaktpersonene
Noen opplysninger om kontaktselskaper er identiske med opplysningene om kontaktpersonene som arbeider i disse selskapene, for eksempel opplysninger om adresse. I inndelingen **Arv** på siden **Markedsføringsoppsett** kan du angi at programmet automatisk kopiere bestemte felt fra kortet for kontaktselskapet til kortet for kontaktpersonen hver gang du oppretter en kontaktperson for et kontaktselskap. Du kan for eksempel velge for å kopiere selgerkoden, adresseopplysninger (adresse, adresse 2, poststed, postnummer og fylke), kommunikasjonsdetaljer (telefaksnummer, teleks (tilbakesvar) og telefonnummer) og mer.

Når du endrer ett av disse feltene på kortet for kontaktselskapet, endres automatisk feltet på kortet for kontaktpersonen (med mindre du har endret feltet manuelt på dette kortet).

Hvis du vil ha mer informasjon, kan du se [Opprett kontakter](marketing-create-contact-companies.md).

## Bruk forhåndsdefinerte standarder på nye kontakter
Du kan angi at hver gang du oppretter en ny kontakt, skal det automatisk tilordnes en bestemt språkkode, distriktskode, selgerkode og lands-/regionkode som standard. Du kan også angi en standard salgssykluskode som automatisk tilordnes hver nye salgsmulighet du oppretter.

Arv av felt overskriver standardverdiene du har definert. Hvis du for eksempel har definert norsk som standardspråk, men ett av kontaktselskapene bruker tysk, tildeles automatisk tysk som språkkode for de kontaktpersonene som står registrert for dette selskapet.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## Registrere samhandlinger automatisk
[!INCLUDE[prod_short](includes/prod_short.md)] kan automatisk registrere salgs- og kjøpsdokumenter som samhandlinger (for eksempel ordrer, fakturaer, mottak og så videre), men også e-post, telefonsamtaler og følgebrev.

Hvis du vil ha mer informasjon, kan du se [Automatisk registrere samhandlinger med kontakter](marketing-auto-record-interactions.md).

## Synkronisere kontakter med kunder og mer
Når du skal synkronisere kontaktkortet med kundekortet, leverandørkortet og bankkontokortet, må du velge en kode for forretningsforbindelse for kunder, leverandører og bankkonti. Du kan for eksempel knytte en kontakt til en eksisterende kunde bare hvis du har valgt en kode for forretningsforbindelse for kunder på siden **Markedsføringsoppsett**.

Hvis du vil ha mer informasjon, kan du se [Synkronisere kontaktene med kunder, leverandører og bankkonti](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-employees-and-bank-accounts).  

## Tilordne en nummerserie til kontakter og salgsmuligheter
Du kan definere en nummerserie for kontakter og salgsmuligheter. Hvis du har definert en nummerserie for kontakter, og du oppretter en kontakt og trykker <kbd>Enter</kbd> i Nr. -feltet på kontaktkortet, angir programmet automatisk neste tilgjengelige kontaktnummer.

Hvis du vil ha mer informasjon om nummerserie, kan du se [Opprette nummerserie](ui-create-number-series.md).

## Søke etter duplikatkontakter når kontakter opprettes
Du kan angi at programmet skal foreta automatisk søk etter duplikater hver gang du oppretter et kontaktselskap, eller du kan velge å søke manuelt etter at du har opprettet kontakter. Du kan også angi at programmet skal oppdatere søkestrengene automatisk hver gang du endrer kontaktopplysninger eller oppretter en kontakt. Du kan selv bestemme søketreffprosenten, det vil si hvor høy prosentandel to kontakter må ha av like strenger før de betraktes som duplikater.

## Se også
[Administrere kontakter](marketing-contacts.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]