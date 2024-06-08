---
title: Del kontakter mellom Business Central og Outlook
description: Denne tjenesten er tett integrert med Microsoft 365 slik at du kan dele kontakter mellom Outlook og Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'contacts, Microsoft 365'
ms.search.form: '6700, 5320, 5300, 5301, 5302, 5303, 5304, 5305, 5306, 5307, 5308, 5309, 5310, 5311'
ms.date: 03/17/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisere kontakter i Business Central med kontakter i Microsoft Outlook

Du kan opprette en kontaktsynkronisering slik at kontaktene i [!INCLUDE[prod_short](includes/prod_short.md)] får de samme opplysningene som kontaktene i Microsoft Outlook. Hvis du for eksempel er selger, kan du arbeide i Outlook og [!INCLUDE[prod_short](includes/prod_short.md)] samtidig. Hvis kontaktene er de samme begge steder, er arbeidet mer enkelt.  

Som standard beholdes kontaktene du synkroniserer, i en **Business Central**-mappe i favorittene i Mappe-ruten i Outlook. Business Central-mappen kan gjøre det enklere å identifisere hvilke kontakter du skal synkronisere. Du kan angi at filtre bare skal synkronisere bestemte kontakter fra [!INCLUDE[prod_short](includes/prod_short.md)] til Outlook. Når du har opprettet synkroniseringen, kan du synkronisere manuelt eller automatisere prosessen for å synkronisere etter en tidsplan.  

## <a name="prerequisites"></a>Forutsetninger

- Brukerprofilen i [!INCLUDE[prod_short](includes/prod_short.md)] må angi e-postkontoen for Microsoft 365.

  Du kan kontrollere denne innstillingen i delen **Microsoft 365-godkjenning** av brukerprofilen din i **Brukere**-listen.
- Med [!INCLUDE[prod_short](includes/prod_short.md)] kan du opprette kontaktsynkronisering som beskrevet i [Definer kontaktsynkronisering med Outlook for Business Central On-Premises](admin-contact-sync-setup-onprem.md)

## <a name="set-up-synchronization"></a>Definere synkronisering

Du definerer hvordan du vil synkronisere kontaktene med Outlook på siden **Konfigurasjon av Exchange-synkronisering** i [!INCLUDE[prod_short](includes/prod_short.md)]. 

På siden **Konfigurasjon av Exchange-synkronisering** kan du validere at tilkoblingen til Exchange fungerer, og deretter definere kontaktsynkronisering. Fra siden **Konfigurasjon av Exchange-synkronisering** kan du åpne siden **Oppsett for synkronisering av kontakt** og starte synkroniseringen. Du kan også angi et filter for å angi hvilke kontakter som skal synkroniseres. Du kan for eksempel filtrere på navn, type, selskap og så videre. Du kan også endre standardnavnet på mappen i Outlook som kontaktene skal synkroniseres til.  

Hver av kollegaene kan også konfigurere sin egen Exchange-synkronisering og definere sine egne filtre for kontaktene som skal synkroniseres.  

Når du har opprettet synkronisering, kan du synkronisere endringene i kontakten manuelt, eller du kan automatisere prosessen ved å opprette en prosjektkøpost. Hvis du vil ha mer informasjon om automatisering, kan du se neste avsnitt i denne artikkelen.

### <a name="automate-synchronization"></a>Automatiser synkronisering

Du kan opprette en prosjektkøpost som skal synkronisere kontaktene i henhold til en plan du definerer. Hvis du vil ha mer informasjon, kan du se [Bruk jobbkøer til å planlegge oppgaver](admin-job-queues-schedule-tasks.md). 

Følgende tabell viser innstillingene på siden **Postkort for jobbkø** som er for synkronisering av kontakter:

|Felt|Innstilling for kontaktsynkronisering|
|-----|-----|
|Objekttype som skal kjøres|Kodeenhet|
|Objekt-ID som skal kjøres|6700|

## <a name="synchronize-contacts"></a>Synkronisere kontakter

Hvis du er vant med å arbeide med kontakter i [!INCLUDE[prod_short](includes/prod_short.md)], vil du synes det er enkelt å synkronisere manuelt fra **Kontakter**-listen når det passer deg. Du kan synkronisere kontaktene på to måter:

* **Synkroniser med Microsoft 365**

  Synkroniser alle endringer fra [!INCLUDE[prod_short](includes/prod_short.md)] til Microsoft 365 som ble gjort etter den forrige synkroniseringen, basert på dato med siste endring. Alle nye kontakter fra Microsoft 365 synkroniseres også til [!INCLUDE[prod_short](includes/prod_short.md)]. Denne handlingen er vanligvis raskere enn en fullstendig synkronisering. 

* **Synkroniser fullstendig med Microsoft 365**

  Synkroniser alle kontaktene i begge retninger uavhengig av den siste synkroniseringsdatoen og datoen for siste endring.  

I begge tilfeller synkroniseres bare kontakter fra Outlook hvis de har utfylt de obligatoriske feltene. Obligatoriske felter som skal synkroniseres til Microsoft 365, er **Navn**, **E-postadresse** og kontaktene må være av typen **Person**. [!INCLUDE[prod_short](includes/prod_short.md)] er kilden for kontaktopplysningene, slik at [!INCLUDE[prod_short](includes/prod_short.md)]-kontaktinformasjonen lagres i tilfelle det finnes duplikater.  

> [!NOTE]
> Hvis du sletter en kontakt i Outlook, men beholder den i [!INCLUDE[prod_short](includes/prod_short.md)], gjenopprettes kontakten i Outlook neste gang du synkroniserer. 

## <a name="see-also"></a>Se også

[Bli klar til å gjøre forretninger](ui-get-ready-business.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Innkjøp](purchasing-manage-purchasing.md)  
[Bruk kontakter (personer) i Outlook på Internett](https://support.office.com/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
