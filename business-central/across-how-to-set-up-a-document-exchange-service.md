---
title: Konfigurere en dokumentutvekslingstjeneste | Microsoft-dokumentasjon
description: Du bruker en ekstern tjenesteleverandør til å utveksle elektroniske dokumenter med handelspartnere.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
---
# <a name="set-up-a-document-exchange-service"></a>Konfigurere en dokumentutvekslingstjeneste

Som en del av rammeverket for datautveksling kan du utveksle salgs- og kjøpsdokumenter med handelspartnere uten ekstra trinn, for eksempel knytte sammen dokumenter til e-postmeldinger som PDF-filer. Når du for eksempel er klar til å fakturere en kunde, kan du bokføre fakturaen og sende den til betaling som en fil som kunden kan motta i forretningsadministrasjonsprogrammet. Hvis du vil ha mer informasjon, kan du se [Utveksle data elektronisk](across-data-exchange.md).

> [!NOTE]
> Oppretting av en dokumentutvekslingstjeneste for Business Central on-premises krever noen flere trinn for godkjenning. Hvis du vil ha mer informasjon, se [Innstillinger for Business Central On-Premises](#settings-for-business-central-on-premises).

## <a name="connecting-with-trading-partners"></a>Koble til handelspartnere

Utveksling av elektroniske dokumenter krever en tilkobling til handelspartnerne. For å gjøre det enkelt å opprette en sikker tilkobling er [!INCLUDE[prod_short](includes/prod_short.md)] online konfigurert til å bruke Business Central Integration-appen. Appen er tilgjengelig i Tradeshift App Store, og alt du og alle forretningspartnerne dine trenger å gjøre, er å opprette en Tradeshift-konto og deretter aktivere appen. Business Central Integration-appen leveres i produksjons- og sandkasseversjoner. Hvis du for eksempel bruker sandkasseversjonen, bør du teste dokumentutvekslingen. Du kan bytte mellom produksjons- og sandkasseversjoner ved å aktivere eller deaktivere **Sandkasse** på siden **Oppsett av dokumentutvekslingstjeneste**. Når du gjør dette, oppdateres opplysningene i hurtigfanen **Tjeneste**.

Hvis du vil bruke en annen tjeneste, må du eventuelt angi opplysninger som skal opprette tilkoblingen. Hvis du vil ha mer informasjon, kan du se [Slik kobler du til en dokumentutvekslingstjeneste](across-how-to-set-up-a-document-exchange-service.md#to-connect-to-a-document-exchange-service).

## <a name="to-connect-to-the-business-central-integration-app-on-tradeshift"></a>Slik kobler du til Business Central Integration-appen på Tradeshift

Du kan raskt opprette en Tradeshift-konto og komme i gang med Business Central Integration-appen fra siden **Oppsett av dokumentutvekslingstjeneste**. Velg enten koblingen **Aktiver app** i varslingen eller **URL-adresse for app** for å gå til appen i Tradeshift App Store. På påloggingssiden for Tradeshift kan du enten logge på eller registrere deg.

> [!NOTE]
> Når du har logget deg på Tradeshift-kontoen, kan det hende området ikke tar deg til siden der du aktiverer appen. Dette kan du gjøre ved å klikke koblingen på siden **Oppsett av dokumentutvekslingstjeneste** i Business Central igjen for å gå direkte til appen.

Hvis du vil stanse bruken av Business Central Integration-appen, må du deaktivere den i Tradeshift App Store. 

## <a name="to-connect-to-a-document-exchange-service"></a>Slik kobler du til en dokumentutvekslingstjeneste

Hvis du foretrekker å bruke en annen dokumentutvekslingstjeneste, må du angi opplysninger for å kunne koble til tjenesten.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett av dokumentutvekslingstjeneste**, og velg deretter den relaterte koblingen.  
2. Fyll ut feltene som beskrevet i tabellen nedenfor.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Brukeragent**|Skriv inn tekst som kan brukes til å identifisere firmaet i dokumentutvekslingsprosesser.|  
    |**Aktivert**|Angi om tilkoblingen til tjenesten er aktivert.<br><br> **Obs!** Når du aktiverer tjenesten, opprettes minst to jobbkøposter for å sende og motta elektroniske dokumenter. Når du deaktiverer tjenesten, slettes jobbkøpostene.|  
    |**Sandkasse**|Angi om du kobler til en sandkasseversjon av dokumentutvekslingstjenesten.|
    |**URL-adresse for registrering**|Angi nettsiden der du registrerer deg for dokumentutvekslingstjenesten.|  
    |**URL-adresse for app**|Velg koblingen for å åpne appbutikken og aktivere eller deaktivere Business Central Integration-appen.|
    |**Nettadresse for tjeneste**|Angi adressen til dokumentutvekslingstjenesten, som vil bli kalt når du sender og mottar elektroniske dokumenter.|  
    |**URL-adresse for pålogging**|Angi URL-adressen for siden du bruker til å logge på dokumentutvekslingstjenesten. Dette er siden der du angir firmaets brukernavn og passord.|  
    
    > [!NOTE]  
    > Påloggingslegitimasjonen krypteres automatisk. Du kan ikke deaktivere kryptering.

    > [!NOTE]
    > Hvis du ikke kan koble til dokumentutvekslingstjenesten på grunn av et autorisasjonsproblem, kan det skyldes at [!INCLUDE[prod_short](includes/prod_short.md)] ikke kan fornyes automatisk. Dette kan for eksempel skje hvis du ikke har brukt tjenesten på en stund. Du kan fornye tokenet manuelt ved å bruke handlingen **Forny token**.

## <a name="settings-for-business-central-on-premises"></a>Innstillinger for Business Central On-Premises

Du må opprette en app i Tradeshift App Store for å kunne koble til Business Central on-premises. Når du gjør dette, bruker du URL-adressen for omadressering i feltet **URL-adresse for omadressering** på siden **Oppsett av dokumentutvekslingstjeneste**. Når du har registrert appen, vil Tradeshift tilby en klient-ID og en klienthemmelighet. Under [!INCLUDE[prod_short](includes/prod_short.md)] angir du disse verdiene i hurtigfanen **Autorisasjon** på siden **Oppsett av dokumentutvekslingstjeneste**.

Hvis du foretrekker å lagre app-ID-en og -hemmeligheten på en annen plassering, kan du la feltene klient-ID og klienthemmelighet stå tomme og skrive en utvidelse for å hente ID-en og hemmeligheten fra plasseringen. Du kan gi hemmeligheten under kjøring ved å abonnere på hendelsene OnGetClientId og OnGetClientSecret i codeunit 1410, Administrasjon av dokumentutvekslingstjeneste.

## <a name="see-also"></a>Se også

[Definere datautveksling](across-set-up-data-exchange.md)  
[Utveksle data elektronisk](across-data-exchange.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
