---
title: Integrer med Microsoft Dataverse via datasynkronisering
description: Innføring i hvordan du integrerer og bruker Microsoft Dataverse og styrer komponentene for å koble til andre Dynamics 365-programmer.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.date: 06/28/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Integrer med Microsoft Dataverse via datasynkronisering

Forretningsapper bruker ofte data fra mer enn én kilde. [!INCLUDE[prod_short](includes/cds_long_md.md)] kombinerer data til et logisk sett som gjør det enklere å koble [!INCLUDE[prod_short](includes/prod_short.md)] til andre Dynamics 365-apper. For eksempel [!INCLUDE[crm_md](includes/crm_md.md)] eller ditt eget program bygd på [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du vil vite mer om [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du gå til [Hva er Dataverse?](/powerapps/maker/common-data-service/data-platform-intro).

Følgende fremgangsmåte gir en oversikt over hvordan du integrerer [!INCLUDE[prod_short](includes/cds_long_md.md)] med [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Disse oppgavene krever **Systemansvarlig**-sikkerhetsrolle i [!INCLUDE[prod_short](includes/cds_long_md.md)] og [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Tilordne lisenser for [!INCLUDE[prod_short](includes/cds_long_md.md)] til [!INCLUDE[prod_short](includes/prod_short.md)]-brukere som skal bruke de integrerte appene.

2. Konfigurere en tilkobling til [!INCLUDE[prod_short](includes/cds_long_md.md)] Hvis du vil ha mer informasjon, kan du se [Koble til Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Synkronisere data mellom apper. Hvis du vil ha mer informasjon, kan du se [Synkronisere Business Central og Dataverse](admin-synchronizing-business-central-and-sales.md). 

## Kom i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)]

Hvis du vil komme i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)], trenger du en Microsoft Power Apps-konto. Hvis du ikke allerede har en Power Apps-konto, kan du få en kostnadsfritt ved å gå til [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) og klikke koblingen **Komme i gang vederlagsfritt**. Hvis du vil ha mer informasjon om hvordan du kommer i gang med [!INCLUDE[prod_short](includes/cds_long_md.md)], kan du gå til modulen [Kom i gang med Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) i Microsoft-opplæring.

## Toveis eller enveis datasynkronisering

Du kan synkronisere data til eller fra én Dynamics 365-forretningsapp til en annen, eller i begge retninger i nær sanntid via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Hvis du for eksempel integrerer [!INCLUDE[prod_short](includes/prod_short.md)] med [!INCLUDE[crm_md](includes/crm_md.md)], kan en selger opprette en salgsordre i [!INCLUDE[crm_md](includes/crm_md.md)], og ordren synkroniseres med [!INCLUDE[prod_short](includes/prod_short.md)]. I [!INCLUDE[crm_md](includes/crm_md.md)] kan selgeren i motsetning kontrollere tilgjengeligheten av varen i ordren i [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Standard og egendefinerte enheter

[!INCLUDE[prod_short](includes/cds_long_md.md)] lagrer data på en sikker måte i et sett med tabeller. Dette er sett med poster som ligner på hvordan en tabell lagrer data i en database. [!INCLUDE[prod_short](includes/cds_long_md.md)] inneholder et grunnleggende sett med standardtabeller som dekker vanlige scenarier, men du kan også opprette egendefinerte tabeller som er spesifikke for organisasjonen. I [!INCLUDE[prod_short](includes/prod_short.md)] kan du vise standard og egendefinerte tabeller som synkroniseres på siden Tilordninger for integreringstabell.

## Om den grunnleggende integreringsløsningen for Business Central

Den grunnleggende integreringsløsningen er en viktig del av integreringen. Løsningen legger til nødvendige roller og tilgangsnivåer for brukerkontoene for integreringen, og det opprettes tabeller som kreves for å tilordne [!INCLUDE[prod_short](includes/prod_short.md)]-firmaer til konsernet i [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Som standard importerer den assisterte oppsettsveiledningen **Konfigurer [!INCLUDE[prod_short](includes/cds_long_md.md)]-tilkobling** løsningen. For å gjøre dette bruker oppsettveiledningen en administratorbrukerkonto du angir. Denne kontoen må være en gyldig bruker i [!INCLUDE[prod_short](includes/cds_long_md.md)] med sikkerhetsrollen **Systemadministrator**.  

Hvis du vil vite mer om brukerkontoer, går du til følgende artikler:

* [Sette opp brukerkontoer for integrasjon med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Opprett brukere i Microsoft Dynamics 365 (online) og tildel sikkerhetsroller](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Administratorkontoen brukes bare én gang i oppsettet for konfigurasjonsendringene som den grunnleggende integreringsløsningen gjør i [!INCLUDE[prod_short](includes/cds_long_md.md)]. Når løsningen er importert, er kontoen ikke lenger nødvendig. Integrasjonen fortsetter å bruke brukerkontoen som automatisk er opprettet spesielt for integrasjonen.

I tillegg til å tilpasse [!INCLUDE [cds_long_md](includes/cds_long_md.md)], oppretter løsningen også en sikkerhetsrolle i [!INCLUDE [cds_long_md](includes/cds_long_md.md)] for integreringen:

* **Business Central Dataverse-integrering** – lar deg administrere tilkoblingen mellom [!INCLUDE [prod_short](includes/prod_short.md)] og [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Denne rollen tildeles vanligvis bare til brukerkontoen som ble automatisk opprettet for synkronisering. Hvis du vil finne ut mer om denne rollen, kan du gå til [Konfigurer brukerkontoer for integrering med [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Når du konfigurerer tilkoblingen, oppretter du integreringstabelltildelingene som du trenger for å synkronisere data. Enheter i [!INCLUDE[prod_short](includes/cds_long_md.md)] blir tildelt til tabeller og tabellfelter i [!INCLUDE [prod_short](includes/prod_short.md)] via integreringstabeller. Hvis du vil lære mer om tildelinger, går du til [Standard enhetstildeling for synkronisering](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Håndter forskjeller i lokale valutaer og standardtransaksjonsvalutaer

Du kan koble til et [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljø som har en annen standardvaluta enn den lokale valutaen i [!INCLUDE[prod_short](includes/prod_short.md)]. Du oppretter tilkoblingen i [!INCLUDE[prod_short](includes/prod_short.md)] på siden **Dataverse-tilkoblingsoppsett** eller ved å bruke veiledningen for det assisterte oppsettet **Konfigurer tilkobling til Dataverse**.

Hvis du vil koble til, må du kontrollere at innstillingen i [!INCLUDE[prod_short](includes/cds_long_md.md)] for standardtransaksjonsvalutaen er valutaen som er angitt på siden **Valutaer** i [!INCLUDE [prod_short](includes/prod_short.md)], og at minst én valutakurs er angitt for valutaen på siden **Valutakurser**.

Her er et eksempel. Du kobler [!INCLUDE[prod_short](includes/cds_long_md.md)] til euro (EUR) angitt som lokal valuta på siden **Finansoppsett** til et [!INCLUDE[prod_short](includes/cds_long_md.md)]-miljø som har en standardvaluta for valuta angitt til amerikanske dollar (USD). Du må ha USD på siden **Valutaer** i [!INCLUDE [prod_short](includes/prod_short.md)] og riktig valutakurs. 

Når du aktiverer tilkoblingen til [!INCLUDE[prod_short](includes/cds_long_md.md)], legger [!INCLUDE [prod_short](includes/prod_short.md)] til den lokale valutaen i enheten **Valuta** i [!INCLUDE[prod_short](includes/cds_long_md.md)] med valutakursen fra feltet **Valutafaktor** på siden **Valutakurser**.

Valutasynkronisering er enveis, fra [!INCLUDE [prod_short](includes/prod_short.md)] til [!INCLUDE [!INCLUDE[prod_short](includes/cds_long_md.md)], pengebeløp konverteres og synkroniseres på følgende måte:

* Beløp i [!INCLUDE[prod_short](includes/cds_long_md.md)] standardvalutaen konverteres til [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta basert på den siste valutakursen som er synkronisert fra [!INCLUDE [prod_short](includes/prod_short.md)].
* Beløp i [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta synkroniseres med [!INCLUDE [prod_short](includes/prod_short.md)] lokal valuta i en av de andre (ikke-standard) valutaene i [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Se også

[Dataeierskapsmodeller](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
