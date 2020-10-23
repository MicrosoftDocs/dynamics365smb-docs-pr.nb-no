---
title: Koble til Common Data Service | Microsoft Docs
description: Du kan integrere andre apper med Business Central via Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 51f04f690483fd5b0c3f093ac5f8e2694ca3fdd9
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3924631"
---
# <a name="connect-to-common-data-service"></a>Koble til Common Data Service

Dette emnet beskriver hvordan du setter opp en tilkobling mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Vanligvis oppretter selskaper tilkoblingen for å integrere og synkronisere data med en annen Dynamics 365-forretningsapp, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du begynner

Før du oppretter tilkoblingen, er det noen få opplysninger du må ha klar:  

* URL-adressen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljøet du vil koble til. Hvis du bruker den assisterte oppsettsveiledningen for **Konfigurasjon for CDS-tilkobling** til å opprette tilkoblingen, finner du miljøene, men du kan også angi URL-adressen til et annet miljø i leieren.  
* Brukernavnet og passordet for en konto som har administratorrettigheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  

> [!Note]
> Følgende trinn beskriver fremgangsmåten for den elektroniske versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)].
> Hvis du bruker Business Central lokalt og ikke bruker Azure Active Directory-kontoen til å koble til [!INCLUDE [cds_long_md](includes/cds_long_md.md)], må du også angi brukernavn og passord for en brukerkonto for integrasjonen. Denne kontoen kalles kontoen for "integrasjonsbruker". Hvis du bruker en Azure Active Directory-konto, er ikke brukerkontoen for integrasjon nødvendig eller vist. Brukeren for integrasjon konfigureres automatisk og krever ikke en lisens.

## <a name="set-up-a-connection-to-cds_long_md"></a>Konfigurere en kobling til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

For andre godkjenningstyper enn Microsoft 365-godkjenning definerer du en tilkobling til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på siden **Konfigurasjon for CDS-tilkobling**. For Microsoft 365-godkjenning anbefales det å bruke den assisterte oppsettsveiledningen for **Konfigurasjon for Common Data Service-tilkobling**. Veiledningen gjør det enklere å opprette tilkoblingen og angi avanserte funksjoner, for eksempel eierskapsmodell og første synkronisering.  

> [!IMPORTANT]
> Under oppsettet av tilkoblingen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] blir administrator bedt om å gi følgende tillatelse til å registrere Azure-programmet kalt [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrering til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]:
>
> * Tillatelse for **tilgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)] som deg** kreves, slik at [!INCLUDE[d365fin](includes/d365fin_md.md)], på vegne av administrator, automatisk kan opprette ikke-interaktive ulisensierte programbruker for [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjon, tilordne sikkerhetsroller til denne brukeren og distribuere den grunnleggende løsningen for [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrering til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. Denne tillatelsen brukes bare én gang under oppsett av kobling til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
> * Tillatelse for å **ha full tilgang til Dynamics 365 [!INCLUDE[d365fin](includes/d365fin_md.md)]** kreves, slik at den automatisk opprettede programbrukeren for [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrering har tilgang til [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som skal synkroniseres.  
> * Tillatelse for å **logge på og lese profilen din** kreves for å bekrefte at brukeren som logger på, faktisk har sikkerhetsrollen for systemansvarlig tilordnet i [!INCLUDE[cds_long_md](includes/cds_long_md.md)].  
>
> Ved å gi samtykke på vegne av organisasjonen, gir administrator det registrerte Azure-programmet som kalles [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrering med [!INCLUDE[cds_long_md](includes/cds_long_md.md)], rett til å synkronisere data ved hjelp av automatisk opprettet legitimasjon for programbruker for [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrering.

### <a name="to-use-the-set-up-common-data-service-connection-assisted-setup-guide"></a>Slik bruker du den assisterte oppsettsveiledningen for Konfigurasjon for Common Data Service-tilkobling

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Assistert oppsett**, og velg deretter den relaterte koblingen.
2. Velg **Konfigurasjon for Common Data Service-tilkobling** for å starte assistert oppsettsveiledning.
3. Fyll ut feltene etter behov.

### <a name="to-create-or-maintain-the-connection-manually"></a>Opprette eller vedlikeholde tilkoblingen manuelt

Følgende fremgangsmåte beskriver hvordan du konfigurerer tilkoblingen manuelt på siden **Konfigurasjon for CDS-tilkobling**. Dette er også siden der du kan håndtere innstillingene for integrasjonen.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjon for CDS-tilkobling**, og velg deretter den relaterte koblingen.
2. Skriv inn følgende informasjon for tilkoblingen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[cds_long_md](includes/cds_long_md.md)].

    |Felt|Beskrivelse|
    |-----|-----|
    |**URL-adresse for miljø**|Hvis du eier miljøer i [!INCLUDE[cds_long_md](includes/cds_long_md.md)], finner vi de for deg når du kjører installasjonsveiledningen. Hvis du vil koble til et annet miljø i en annen leier, kan du angi administratorlegitimasjon for miljøet slik at vi kan finne disse. |
    |**Aktivert**|Begynn å bruke integrasjonen. Hvis du ikke aktiverer tilkoblingen nå, lagres tilkoblingsinnstillingene, men brukerne vil ikke ha tilgang til [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gå tilbake til denne siden og aktivere tilkoblingen senere.  |

3. I feltet **Eierskapsmodell** velger du om du vil ha en teamenhet i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] til egne nye poster, eller én eller flere bestemte brukere. Hvis du velger **Person**, må du angi hver bruker. Hvis du velger **Team**, vil standard forretningsenhet, kalt BCI_Company, vises i feltet **Koblet konsern**.

    <!--Need to verify the details in this table, are these specific to Sales maybe?-->
    Angi følgende avanserte innstillinger.

    |Felt|Beskrivelse|
    |-----|-----|
    |**[!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere må samordne med CDS-brukere**|Hvis du bruker personeierskapsmodellen, angir du om [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukerkontoer må ha en samsvarende brukerkonto i [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. **E-postadresse for godkjenning for Microsoft 365** for [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukeren må være den samme som **Primær-e-postadresse** til [!INCLUDE[crm_md](includes/crm_md.md)]-brukeren.<br /><br /> Hvis du angir verdien til **Ja**, vil [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere som ikke har en tilsvarende [!INCLUDE[crm_md](includes/crm_md.md)]-brukerkonto, ikke ha [!INCLUDE[d365fin](includes/d365fin_md.md)]-integrasjonsfunksjonene i brukergrensesnittet. Tilgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data direkte fra [!INCLUDE[d365fin](includes/d365fin_md.md)] er utført på vegne av [!INCLUDE[crm_md](includes/crm_md.md)]-brukerkontoen.<br /><br /> Hvis du angir verdien til **Nei**, vil alle [!INCLUDE[d365fin](includes/d365fin_md.md)]-brukere ha [!INCLUDE[crm_md](includes/crm_md.md)]-integrasjonsfunksjonene i brukergrensesnittet. Tilgang til [!INCLUDE[crm_md](includes/crm_md.md)]-data gjøres på vegne av [!INCLUDE[crm_md](includes/crm_md.md)]-tilkoblings(integrerings)bruker.|
    |**Gjeldende Business Central-selger er tilordnet til en bruker**|Angir om brukerkontoen er tilordnet til en konto i [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field-->|

4. Hvis du vil teste tilkoblingsinnstillingene, velger du **Tilkobling** og deretter **Test tilkobling**.  

    > [!NOTE]  
    > Hvis datakryptering ikke er aktivert i [!INCLUDE[d365fin](includes/d365fin_md.md)], får du bli spurt om du vil aktivere den. Hvis du vil aktivere datakryptering, velger du **Ja** og angir nødvendig informasjon. Ellers velger du **Nei**. Du kan aktivere datakryptering senere. Hvis du vil ha mer informasjon, kan du se [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data) i hjelpen for utviklere og administrasjon.  

5. Hvis [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-synkronisering ikke allerede er satt opp, vil du bli spurt om du vil bruke standard synkroniseringsoppsett. Avhengig av om du vil beholde postene som er justert i [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du **Ja** eller **Nei**.

## <a name="show-me-the-process"></a>Vis prosessen

Den følgende videoen viser hvordan du kobler [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[cds_long_md](includes/cds_long_md.md)]. <br>
  
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ArlP]

## <a name="connecting-on-premises-versions"></a>Koble til lokale versjoner

Hvis du vil koble [!INCLUDE[d365fin](includes/d365fin_md.md)] lokalt til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], må du angi informasjon på siden **Tilkoblingsoppsett for Common Data Service**.

Hvis du vil koble til ved hjelp av en Azure Active Directory-konto (Azure AD), må du registrere et program i Azure AD og angi program-ID, hemmelighet for nøkkelhvelv og nettadressen som skal brukes til omdirigering. Nettadressen for omdirigering er forhåndsutfylt og skal fungere for de fleste installasjoner. Du må konfigurere installasjonen til å bruke HTTPS. Hvis du vil ha mer informasjon, kan du se [Konfigurere SSL for å sikre nettklienttilkoblingen for Business Central](/dynamics365/business-central/dev-itpro/deployment/configure-ssl-web-client-connection). Hvis du konfigurerer serveren slik at den har en annen hjemmeside, kan du endre nettadressen når som helst. Klienthemmeligheten vil bli lagret som en kryptert streng i databasen.  

### <a name="to-register-an-application-in-azure-ad-for-connecting-from-business-central-to-common-data-service"></a>Slik registrerer du et program i Azure AD for tilkobling fra Business Central til Common Data Service

Fremgangsmåten nedenfor forutsetter at du bruker Azure AD til å administrere identiteter og tilgang. Hvis du vil ha mer informasjon om hvordan du registrerer et program i Azure AD, kan du se [Hurtigstart: Registrere et program i Microsoft Identity Platform](/azure/active-directory/develop/quickstart-register-app). Hvis du ikke bruker Azure AD, kan du se [Bruke en annen identitet og tjeneste for administrasjon av tilgang](admin-how-to-set-up-a-dynamics-crm-connection.md#using-another-identity-and-access-management-service).  

1. Velg **Godkjenning** i Azure-portalen under **Behandle** i navigasjonsruten.  
2. Under **nettadresser for omdirigering** legger du til nettadressen for omdirigering som foreslås på siden **Tilkoblingsoppsett for Common Data Service** i [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Velg **API-tillatelser** under **Behandle**.
4. Under **Konfigurerte tillatelser** velger du **Legg til tillatelse**, og deretter legger du til delegerte tillatelser i kategorien **Microsoft API-er** på følgende måte:
    * For Business Central legger du til tillatelsene **Financials.ReadWrite.All**.
    * For Dynamics CRM legger du til tillatelsene **user_impersonation**.  

    > [!NOTE]
    > Navnet på Dynamics CRM-API-et kan endres.

5. Under **Behandle** velger du **Sertifikater og hemmeligheter**, og deretter oppretter du en ny hemmelighet for appen. Du bruker hemmeligheten i [!INCLUDE[d365fin](includes/d365fin_md.md)], i feltet **Klienthemmelighet** på siden **Tilkoblingsoppsett for Common Data Service**, eller du lagrer på en sikker lagringsplass og angir det i et hendelsesabonnent, som beskrevet tidligere i dette emnet.
6. Velg **Oversikt**, og finn deretter verdien **ID (klient) for programmet**. Dette er klient-ID-en for programmet. Du må angi den på siden **Tilkoblingsoppsett for Common Data Service** i feltet **Klient-ID**, eller lagre den på en sikker lagringsplass og angi den i et hendelsesabonnent.
7. I [!INCLUDE[d365fin](includes/d365fin_md.md)], på siden **Tilkoblingsoppsett for Common Data Service** i feltet **Nettadresse for miljø**, angir du nettadressen for [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljøet.
8. Hvis du vil aktivere tilkoblingen til [!INCLUDE[cds_long_md](includes/cds_long_md.md)], aktiverer du alternativet **Aktivert**.
9. Logg på med administratorkontoen din for Azure Active Directory (denne kontoen må ha en gyldig lisens for [!INCLUDE[cds_long_md](includes/cds_long_md.md)] og være administrator i ditt [!INCLUDE[cds_long_md](includes/cds_long_md.md)]-miljø). Når du har logget på, blir du bedt om å tillate at det registrerte programmet kan logge på [!INCLUDE[cds_long_md](includes/cds_long_md.md)] på vegne av organisasjonen. Du må gi samtykke for å fullføre oppsettet.

   > [!NOTE]
   > Hvis du ikke blir bedt om å logge på med administratorkontoen, skyldes det trolig at popup-vinduer er blokkert. Hvis du vil logge på, må du tillate popup-vinduer fra `https://login.microsoftonline.com`.

#### <a name="using-another-identity-and-access-management-service"></a>Bruke en annen identitet og tjeneste for administrasjon av tilgang

Hvis du ikke bruker Azure Active Directory til å administrere identiteter og tilgang, trenger du litt hjelp fra en utvikler. Hvis du foretrekker å lagre app-ID-en og -hemmeligheten på en annen plassering, kan du la feltene klient-ID og klienthemmelighet stå tomme og skrive en utvidelse for å hente ID-en og hemmeligheten fra plasseringen. Du kan gi hemmeligheten under kjøring ved å abonnere på hendelsene OnGetCDSConnectionClientId og OnGetCDSConnectionClientSecret i kodeenhet 7201, CDS Integration Impl.

### <a name="to-disconnect-from-cds_long_md"></a>For å koble fra [!INCLUDE[cds_long_md](includes/cds_long_md.md)]

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjon for CDS-tilkobling**, og velg deretter den relaterte koblingen.
2. På siden **Konfigurasjon for CDS-tilkobling** deaktiverer du alternativet **Aktivert**.  

## <a name="see-also"></a>Se også

[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  
