---
title: Gjennomgang – Motta og plassere i grunnleggende lageroppsett
description: Lær om de ulike måtene å håndtere inngående prosesser på for mottak og plassering.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
---
# Gjennomgang: Mottak og plassering i grunnleggende lageroppsett

I [!INCLUDE[prod_short](includes/prod_short.md)] mottar du varer og plasserer dem ved å bruke en av fire metoder, som beskrevet i tabellen nedenfor.

|Prinsipp|Inngående prosess|Krev kvitteringer|Krev plasseringer|Kompleksitetsnivå (Finn ut mer under [Oversikt over Warehouse Management](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Bokføre mottak og plassering fra ordrelinjen|||Ingen dedikert lageraktivitet.|  
|B|Bokføre mottak og plassering fra et lagerplasseringsdokument||Slått på|Grunnleggende: ordre for ordre.|  
|U|Bokføre mottak og plassering fra et lagermottaksdokument|Slått på||Grunnleggende: konsolidert mottak/levering for flere ordrer.|  
|D|Bokføre mottak fra et lagermottaksdokument og bokføre plassering fra et lagerplasseringsdokument|Slått på|Slått på|Avansert|  

Finn ut mer under [Inngående lagerflyt](design-details-inbound-warehouse-flow.md).

Følgende gjennomgangen demonstrerer metoden B i forrige tabell.  

## Om denne gjennomgangen  

I enkle lageroppsett hvor lokasjonen er definert til å kreve plasseringsbehandling, men ikke mottaksbehandling, bruker du siden **Lagerplassering** til å registrere og bokføre plasserings- og mottaksopplysninger for de inngående kildedokumentene. Følgende dokumenter er inngående kildedokumenter:

* Bestilling
* Ordreretur
* Inngående overføringsordre
* Produksjonsordre med avgang som er klar for plassering

> [!NOTE]
> Selv om innstillingene kalles **Plukk nødv.** og **Plassering nødv.**, kan du bokføre mottak og leveringer direkte fra kildedokumenter for firma på lokasjoner der du velger disse avmerkingsboksene.  

Denne gjennomgangen viser følgende oppgaver:  

* Definer SØLV-plassering for lagerplasseringer.  
* Definer SØLV-plassering for hyllehåndtering.  
* Definer en standardhylle for varen LS-81. (LS-75 er allerede er satt opp i CRONUS.)  
* Opprett en bestilling for leverandør 10000 for 40 høyttalere.  
* Verifiser at plasseringshyllene er forhåndsinnstilt i oppsettet.  
* Frigi bestillingen for lagerhåndtering.  
* Opprett en lagerplassering basert på et frigitt kildedokument.  
* Verifiser at plasseringshyllene er arvet fra bestillingen.  
* Registrer lagerflyttingen til lageret og bokfør mottaket for kildebestillingen.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

## Roller  

Følgende brukerroller utføre oppgaver som denne gjennomgangen viser:  

* Lagerleder  
* Innkjøper  
* Lagermedarbeider  

## Forutsetninger  

For å fullføre denne gjennomgangen må du gjøre følgende:  

* CRONUS International Ltd.-data  
* Være en lageransatt på SØLV-lokasjon. Konfigurer deg selv ved å følge disse trinnene:  

    1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lageransatte**, og velg deretter den relaterte koblingen.  
    2. Velg feltet **Bruker-ID**, og velg brukerkontoen på siden **Brukere**.  
    3. Velg **SØLV** i feltet **Lokasjonskode**.  
    4. Merk av for **Standard**.  

## Hovedscenario  

Ellen, lagerlederen hos CRONUS Norge AS, oppretter en bestilling for 10 enheter av varen LS-75 og 30 enheter av varen LS-81 fra leverandør 10000 som skal leveres til SØLV-lageret. Når leveringen ankommer til lageret, plasserer lagermedarbeideren John varene i standardhyller definert for varene. Når John bokfører plasseringen, bokføres varene som mottatt på lageret og tilgjengelig for salg eller andre behov.  

## Definer lokasjon  

Innstillinger på siden **Lokasjonskort** definerer selskapets lagerflyter.  

### Slik definerer du lokasjonen  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lokasjoner**, og velg deretter den relaterte koblingen.  
2. Åpne lokasjonskortet SØLV.  
3. Slå på vekslebryteren **Plassering nødv.**.  

    Sett opp en standardhylle for de to varenumrene for å kontrollere hvor de er plassert.  

4. Velg handlingen **Hyller**.  
5. Merk den første raden, hylle **S-01-0001**, og velg **Innhold**.  

    Legg merke til at på siden **Hylleinnhold** er varen **LS-75** allerede definert som innhold i hyllen S-01-0001.  

6. Velg handlingen **Ny**.  
7. Velg feltene **Fast** og **Standard**.  
8. Angi **LS-81** i feltet **Varenr.**.  

## Opprett bestillingen  

Bestillinger er den vanligste typen inngående kildedokument.  

### Slik oppretter du bestillingen:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Bestillinger**, og velg deretter den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Opprett en bestilling for leverandør 10000 på arbeidsdatoen (23. januar) med følgende bestillingslinjer.  

    |Vare|Lokasjonskode|Hyllekode|Antall|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SØLV|S-01-0001|10|  
    |LS-81|SØLV|S-01-0001|30|  

    > [!NOTE]  
    > Hyllekoden angis automatisk i samsvar med oppsettet du opprettet i delen [Definer plassering](#setting-up-the-location).  

    Varsle deretter lageret om at bestillingen er klar for håndtering av lageret når leveringen ankommer.  

4. Velg handlingen **Frigi**.  

    Leveringen av høyttalere fra leverandør 10000 er ankommet på SØLV-lageret, og John fortsetter med å plassere dem.  

## Motta og plasser varene  

Bruk siden **Lagerplassering** til å håndtere alle inngående lageraktiviteter for et bestemt kildedokument, for eksempel en bestilling.  

### Slik mottar og plasserer du varene:  

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Lagerplasseringer** og velg den relaterte koblingen.  
2. Velg handlingen **Ny**.  
3. Velg feltet **Kildedokument**, og velg deretter **Bestilling**.  
4. Velg feltet **Kildenr.**, velg linjen for kjøp fra leverandør 10000, og velg deretter **OK**-knappen.  

    Velg eventuelt **Hent kildedokument**-handlingen, og velg deretter bestillingen.  

5. Velg handlingen **Autoutfyll ant som skal håndt**.  

    Du kan også skrive inn 10 og 30 i de to lagerplasseringslinjene i feltet **Ant. som skal håndt.**.  

6. Velg **Bokfør**-handlingen, velg **Motta og fakturer**, og velg deretter **OK**-knappen.  

    40 høyttalere er nå registrert som plassert i hyllen S-01-0001, og det opprettes en positiv varepost som gjenspeiler det bokførte kjøpsmottaket.  

## Se også  

[Plassere varer med lagerplasseringer](warehouse-how-to-put-items-away-with-inventory-put-aways.md)  
[Opprette grunnleggende lagre med operasjonsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Plukke for produksjon eller montering](warehouse-how-to-pick-for-production.md)  
[Flytte varer ad hoc i enkle lageroppsett](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Designdetaljer: Inngående lagerflyt](design-details-inbound-warehouse-flow.md)  
[Gjennomgang av forretningsprosesser](walkthrough-business-process-walkthroughs.md)  
[Arbeid med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]