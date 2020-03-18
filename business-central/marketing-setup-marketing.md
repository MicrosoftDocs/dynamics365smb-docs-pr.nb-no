---
title: Konfigurere markedsføring og kontaktbehandlingsinformasjon | Microsoft-dokumentasjon
description: Du kan konfigurere markedsføring og kontaktbehandling i Business Central for å optimalisere forholdet til prospekter eller kunder og forbedre kampanjer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, client, customer, campaign, promo
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: da0ef3338a32e797c9ebe21b051fb8cc8babcc6d
ms.sourcegitcommit: d0dc5e5c46b932899e2a9c7183959d0ff37738d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076856"
---
# <a name="setting-up-relationship-management"></a>Sette opp forbindelser
Før du begynner å arbeide med kontaktene og markedsføringsinteressene, er det noen beslutninger og trinn du må gjennomføre for å definere hvordan markedsføringsområdet håndterer bestemte aspekter ved kontaktene. Du kan for eksempel avgjøre om du skal synkronisere kontaktkortet med kundekortet, leverandørkortet og bankkontokortet, hvordan tallserier defineres, eller hva standard tiltaleform skal være under skriving til kontaktene dine.

Det å behandle kontaktene og ha en strategi for å identifisere kunder, få kundenes oppmerksomhet og beholde dem vil bidra til å optimalisere bedriften og gjøre kundene mer fornøyde. Bruken av et godt kontaktbehandlingssystem vil også hjelpe deg med å danne og beholde relasjoner med kundene. Kommunikasjon er nøkkelen til disse relasjonene. Det å være i stand til å tilpasse kommunikasjon med potensielle og eksisterende kunder, leverandører og forretningspartner i henhold til behovene, er nødvendig for at bedrifter skal lykkes. Utvikling av en strategi og definering av hvordan bedriften bruker kontaktinformasjon er et grunnleggende trinn. Disse opplysningene vil bli vist av mange forskjellige grupper i bedriften, så alle vil bli mer produktive hvis du har et godt system etablert.

Du definerer markedsførings- og kontakthåndtering fra siden **Markedsføringsoppsett**. Du åpner siden **Markedsføringsoppsett** ved å velge ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Markedsføringsoppsett** og deretter velge den relaterte koblingen.

## <a name="automatically-copying-specific-information-from-contact-companies-to-contact-persons"></a>Automatisk kopiere spesifikk informasjon fra kontaktselskapene til kontaktpersonene
Noen opplysninger om kontaktselskaper er identiske med opplysningene om kontaktpersonene som arbeider i disse selskapene, for eksempel opplysninger om adresse. I inndelingen **Arv** på siden **Markedsføringsoppsett** kan du angi at programmet automatisk kopiere bestemte felt fra kortet for kontaktselskapet til kortet for kontaktpersonen hver gang du oppretter en kontaktperson for et kontaktselskap. Du kan for eksempel velge for å kopiere selgerkoden, adresseopplysninger (adresse, adresse 2, poststed, postnummer og fylke), kommunikasjonsdetaljer (telefaksnummer, teleks (tilbakesvar) og telefonnummer) og mer.

Når du endrer ett av disse feltene på kortet for kontaktselskapet, endres automatisk feltet på kortet for kontaktpersonen (med mindre du har endret feltet manuelt på dette kortet).

Hvis du vil ha mer informasjon, kan du se [Opprette kontakter](marketing-create-contact-companies.md).

## <a name="using-predefined-defaults-on-new-contacts"></a>Bruke forhåndsdefinerte standarder på nye kontakter
Du kan angi at hver gang du oppretter en ny kontakt, skal det automatisk tilordnes en bestemt språkkode, distriktskode, selgerkode og lands-/regionkode som standard. Du kan også angi en standard salgssykluskode som automatisk tilordnes hver nye salgsmulighet du oppretter.

Arv av felt overskriver standardverdiene du har definert. Hvis du for eksempel har definert norsk som standardspråk, men ett av kontaktselskapene bruker tysk, tildeles automatisk tysk som språkkode for de kontaktpersonene som står registrert for dette selskapet.

<!--You can also setup a default salutation that application automatically assigns to your contacts. You can use these salutations in your interaction template attachments (for example, Microsoft Word documents). When setting up a default salutation, you can enter a salutation text and a salutation format. For example, if the salutation text is Dear, and the salutation format is Salutation Text + Title + Name, application will automatically enter Dear Mr. John Smith as a salutation for a contact called John Smith.-->

## <a name="automatically-recording-interactions"></a>Registrere samhandlinger automatisk
[!INCLUDE[d365fin](includes/d365fin_md.md)] kan automatisk registrere salgs- og kjøpsdokumenter som samhandlinger (for eksempel ordrer, fakturaer, mottak og så videre), men også e-post, telefonsamtaler og følgebrev.

Hvis du vil ha mer informasjon, kan du se [Automatisk registrere samhandlinger med kontakter](marketing-auto-record-interactions.md).

## <a name="synchronizing-contacts-with-customers-and-more"></a>Synkronisere kontakter med kunder og mer
Når du skal synkronisere kontaktkortet med kundekortet, leverandørkortet og bankkontokortet, må du velge en kode for forretningsforbindelse for kunder, leverandører og bankkonti. Du kan for eksempel knytte en kontakt til en eksisterende kunde bare hvis du har valgt en kode for forretningsforbindelse for kunder på siden **Markedsføringsoppsett**.

Hvis du vil ha mer informasjon, kan du se [Synkronisere kontaktene med kunder, leverandører og bankkonti](marketing-synchronize-contacts-customers-vendors-bank-accounts/Synchronizing Contacts With Customers, Vendors, and Bank Accounts).

## <a name="assigning-a-number-series-to-contacts-and-opportunities"></a>Tilordne en nummerserie til kontakter og salgsmuligheter
Du kan definere en nummerserie for kontakter og salgsmuligheter. Hvis du har definert en nummerserie for kontakter, og du oppretter en kontakt og trykker Enter i Nr. -feltet på kontaktkortet, angir programmet automatisk neste tilgjengelige kontaktnummer.

Hvis du vil ha mer informasjon om nummerserie, kan du se [Opprette nummerserie](ui-create-number-series.md).

## <a name="searching-for-duplicate-contacts-when-contacts-are-created"></a>Søke etter duplikatkontakter når kontakter opprettes
Du kan angi at programmet skal foreta automatisk søk etter duplikater hver gang du oppretter et kontaktselskap, eller du kan velge å søke manuelt etter at du har opprettet kontakter. Du kan også angi at programmet skal oppdatere søkestrengene automatisk hver gang du endrer kontaktopplysninger eller oppretter en kontakt. Du kan selv bestemme søketreffprosenten, det vil si hvor høy prosentandel to kontakter må ha av like strenger før de betraktes som duplikater.

## <a name="see-also"></a>Se også
[Administrere kontakter](marketing-contacts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
