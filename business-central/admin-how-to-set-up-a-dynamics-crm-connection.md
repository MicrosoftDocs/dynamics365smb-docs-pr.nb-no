---
title: Koble til Dynamics 365 Sales | Microsoft Docs
description: Du kan integrere andre apper med Business Central via Common Data Service.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 3375db0208d1a0275011f0efbfce4a13102c522e
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196642"
---
# <a name="connect-to-common-data-service"></a>Koble til Common Data Service
Dette emnet beskriver hvordan du setter opp en tilkobling mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)]. Vanligvis oppretter selskaper tilkoblingen for å integrere og synkronisere data med en annen Dynamics 365-forretningsapp, for eksempel [!INCLUDE[crm_md](includes/crm_md.md)].  

## <a name="before-you-start"></a>Før du begynner
Før du oppretter tilkoblingen, er det noen få opplysninger du må ha klar:  

* URL-adressen til [!INCLUDE[d365fin](includes/cds_long_md.md)]-miljøet du vil koble til. Hvis du bruker den assisterte oppsettsveiledningen for **Konfigurasjon for CDS-tilkobling** til å opprette tilkoblingen, finner du miljøene, men du kan også angi URL-adressen til et annet miljø i leieren.  
* Et brukernavn og passord til en brukerkonto som bare brukes for integrasjonen. Denne kontoen kalles kontoen for "integrasjonsbruker". 
* Brukernavnet og passordet for en konto som har administratorrettigheter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[d365fin](includes/cds_long_md.md)].  

> [!Note]
> Følgende trinn beskriver fremgangsmåten for den elektroniske versjonen av [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="set-up-a-connection-to-d365fin"></a>Konfigurere en kobling til [!INCLUDE[d365fin](includes/cds_long_md.md)]  
For andre godkjenningstyper enn Office 365-godkjenning definerer du en tilkobling til [!INCLUDE[d365fin](includes/cds_long_md.md)] på siden **Konfigurasjon for CDS-tilkobling**. For Office 365-godkjenning anbefales det å bruke den assisterte oppsettsveiledningen for **Konfigurasjon for CDS-tilkobling**. Veiledningen gjør det enklere å opprette tilkoblingen og angi avanserte funksjoner, for eksempel kobling mellom poster.  

### <a name="to-use-the-cds-connection-setup-assisted-setup-guide"></a>Slik bruker du den assisterte oppsettsveiledningen for Konfigurasjon for CDS-tilkobling 
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Assistert oppsett**, og velg deretter den relaterte koblingen.
2. Velg **Konfigurer primær integreringstilkobling for CDS** for å starte den assisterte oppsettsveiledningen.
3. Fyll ut feltene etter behov.

> [!Note]
> Den assisterte oppsettsveiledningen for **Konfigurasjon for CDS-tilkobling** tilordner automatisk sikkerhetsrollene **Integrasjonsadministrator** og **Integrasjonsbruker** til brukerkontoen som brukes for integrasjon, og setter tilgangsmodusen for kontoen til **ikke-interaktiv**.

### <a name="to-create-or-maintain-the-connection-manually"></a>Opprette eller vedlikeholde tilkoblingen manuelt
Følgende fremgangsmåte beskriver hvordan du konfigurerer tilkoblingen manuelt på siden **Konfigurasjon for CDS-tilkobling**. Dette er også siden der du kan håndtere innstillingene for integrasjonen.

1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjon for CDS-tilkobling**, og velg deretter den relaterte koblingen.
2. Skriv inn følgende informasjon for tilkoblingen fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[d365fin](includes/cds_long_md.md)].

|Felt|Beskrivelse|
|-----|-----|
|**URL-adresse for miljø**|Hvis du eier miljøer i [!INCLUDE[d365fin](includes/cds_long_md.md)], finner vi de for deg når du kjører installasjonsveiledningen. Hvis du vil koble til et annet miljø i en annen leier, kan du angi administratorlegitimasjon for miljøet slik at vi kan finne disse. |
|**Brukernavn** og **Passord**|Legitimasjon for brukerkontoen som er reservert for integreringen. Hvis du vil ha mer informasjon, se [Sette opp brukerkontoer for integrasjon med [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).|
|**Aktivert**|Begynn å bruke integrasjonen. Hvis du ikke aktiverer tilkoblingen nå, lagres tilkoblingsinnstillingene, men brukerne vil ikke ha tilgang til [!INCLUDE[d365fin](includes/cds_long_md.md)]-data fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan gå tilbake til denne siden og aktivere tilkoblingen senere.  |

3. I feltet **Eierskapsmodell** velger du om du vil ha en teamenhet i [!INCLUDE[d365fin](includes/cds_long_md.md)] til egne nye poster, eller én eller flere bestemte brukere. Hvis du velger **Person**, må du angi hver bruker. Hvis du velger **Team**, vil standard forretningsenhet, kalt BCI_Company, vises i feltet **Koblet konsern**.

<!--Need to verify the details in this table, are these specific to Sales maybe?
Enter the following advanced settings.

|Field|Description|
|-----|-----|
|**[!INCLUDE[d365fin](includes/d365fin_md.md)] Users Must Map to CDS Users**|If you are using the Person ownership model, specify whether [!INCLUDE[d365fin](includes/d365fin_md.md)] user accounts must have a matching user accounts in [!INCLUDE[d365fin](includes/cds_long_md.md)]. The **Office 365 Authentication Email** of the [!INCLUDE[d365fin](includes/d365fin_md.md)] user must be the same as the **Primary Email** of the [!INCLUDE[crm_md](includes/crm_md.md)] user.<br /><br /> If you set the value to **Yes**, [!INCLUDE[d365fin](includes/d365fin_md.md)] users who do not have a matching [!INCLUDE[crm_md](includes/crm_md.md)] user account will not have [!INCLUDE[d365fin](includes/d365fin_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data directly from [!INCLUDE[d365fin](includes/d365fin_md.md)] is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] user account.<br /><br /> If you set the value to **No**, all [!INCLUDE[d365fin](includes/d365fin_md.md)] users will have [!INCLUDE[crm_md](includes/crm_md.md)] integration capabilities in the user interface. Access to [!INCLUDE[crm_md](includes/crm_md.md)] data is done on behalf of the [!INCLUDE[crm_md](includes/crm_md.md)] connection (integration) user.|
|**Current Business Central Salesperson is Mapped to a User**|Indicates whether your user account is mapped to an account in [!INCLUDE[crm_md](includes/crm_md.md)] <!--double check the name of this field|-->

4. Hvis du vil teste tilkoblingsinnstillingene, velger du **Tilkobling** og deretter **Test tilkobling**.  

    > [!NOTE]  
    >  Hvis datakryptering ikke er aktivert i [!INCLUDE[d365fin](includes/d365fin_md.md)], får du bli spurt om du vil aktivere den. Hvis du vil aktivere datakryptering, velger du **Ja** og angir nødvendig informasjon. Ellers velger du **Nei**. Du kan aktivere datakryptering senere. Hvis du vil ha mer informasjon, kan du se [Kryptere data i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-encrypting-data.md) i hjelpen for utviklere og IT-eksperter.  

5. Hvis [!INCLUDE[d365fin](includes/cds_long_md.md)]-synkronisering ikke allerede er satt opp, vil du bli spurt om du vil bruke standard synkroniseringsoppsett. Avhengig av om du vil beholde postene som er justert i [!INCLUDE[d365fin](includes/cds_long_md.md)] og [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du **Ja** eller **Nei**.

> [!Note]
> Tilkobling til [!INCLUDE[d365fin](includes/cds_long_md.md)] ved hjelp av siden **Konfigurasjon for CDS-tilkobling** kan kreve at du tilordner sikkerhetsrollene Integrasjonsadministrator og Integrasjonsbruker til kontoen som brukes til integrasjon i Dynamics 365 Sales. Hvis du vil ha mer informasjon, kan du se [Tilordne en sikkerhetsrolle til en bruker](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#assign-a-security-role-to-a-user.md).

### <a name="to-disconnect-from-d365fin"></a>For å koble fra [!INCLUDE[d365fin](includes/cds_long_md.md)]  
1. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konfigurasjon for CDS-tilkobling**, og velg deretter den relaterte koblingen.
2. På siden **Konfigurasjon for CDS-tilkobling** deaktiverer du alternativet **Aktivert**.  

## <a name="see-also"></a>Se også  
[Vise statusen for en synkronisering](admin-how-to-view-synchronization-status.md)  
