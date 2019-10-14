---
title: Konfigurere e-post i Business Central | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker firmaets SMTP-serveren til å sende og motta e-postmeldinger i Business Central, eller alternativt hvordan du bruker innstillingene for e-postserver som ble opprettet med Office 365-abonnementet.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: SMTP, mail, Office 365
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 90e119dc44a23bcd9dca7920d05538ac685a44f6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304615"
---
# <a name="set-up-email"></a>Konfigurer e-post
Hvis du vil sende og motta e-postmeldinger fra [!INCLUDE[d365fin](includes/d365fin_md.md)], må du fylle ut feltene på Oppsett for SMTP-e-post-siden.

I stedet for å skrive inn detaljene for SMTP-serveren manuelt, kan du bruke funksjonen **Bruk Office 365-serverinnstillinger** til å angi dem med informasjon fra Office 365-abonnementet.

Du kan enten definere e-post manuelt, som beskrevet nedenfor, eller du kan få hjelp ved å bruke den assisterte oppsettveiledningen **E-postoppsett**. Hvis du vil ha mer informasjon, kan du se [Bli klar til å gjøre forretninger](ui-get-ready-business.md).  

## <a name="to-set-up-email"></a>Konfigurere e-post
1. Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Oppsett for SMTP-e-post**, og velg deretter den relaterte koblingen.
2. Fyll ut feltene etter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]
    > Hvis du bruker en konto som krever godkjenning med to faktorer, må passordet du angir i **Passord**-feltet, være det samme som du bruker for Office 365-abonnementet, og det må være av typen **App-passord**.
3. Du kan også velge handlingen **Bruk Office 365-serverinnstillinger** for å sette inn informasjon som allerede er definert for Office 365-abonnementet.
4. Når alle feltene er fylt ut riktig, velger du **Test e-postoppsett**.
5. Når testen er vellykket, lukker du siden.

## <a name="using-a-substitute-sender-address-on-outbound-email-messages"></a>Bruke en erstatningsavsenderadresse i utgående e-postmeldinger
Alle utgående e-postmeldinger fra [!INCLUDE[d365fin](includes/d365fin_md.md)] bruker standardadressen for kontoen du angav på siden Oppsett for SMTP-e-post, som beskrevet ovenfor. Du kan imidlertid bruke funksjonene **Send som** eller **Send på vegne av** på Exchange-serveren til å endre avsenderadressen i utgående meldinger. [!INCLUDE[d365fin](includes/d365fin_md.md)] bruker standardkontoen til å godkjenne til Exchange, men erstatter avsenderadressen med den du angir, eller endrer den med "på vegne av".

Følgende er eksempler på hvordan Send som og Send på vegne av brukes i [!INCLUDE[d365fin](includes/d365fin_md.md)]:

 * Når du sender dokumenter som for eksempel bestillinger eller ordrer til leverandører og kunder, vil du kanskje at de skal se ut som om de kommer fra en _ikkesvar@dittselskapsnavn.com_-adresse.
 * Når arbeidsflyten sender en godkjenningsforespørsel via e-post ved hjelp av e-postadressen til anmoderen.

> [!Note]
> Du kan bare bruke én konto til å erstatte avsenderadresser. Det vil si at du ikke kan ha én erstatningsadresse for innkjøpsprosesser og en annen for salgsprosesser.

### <a name="to-set-up-the-substitute-sender-address-for-all-outbound-email-messages"></a>Sette opp erstatningsavsenderadresse for alle utgående e-postmeldinger
1. I **Administrasjonssenter for Exchange** for Office 365-kontoen finner du e-postboksen som skal brukes som erstatningsadresse, og deretter kopierer eller noterer du adressen. Hvis du trenger en ny adresse, går du til administrasjonssenteret for Microsoft 365 for å opprette en ny bruker og konfigurere postboksen.
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ![lyspæren som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Oppsett for SMTP-e-post**, og deretter velger du den relaterte koblingen.
3. I **Send som**-feltet angir du erstatningsadressen.
4. Kopier eller noter adressen i feltet **Bruker-ID**.
5. I **Administrasjonssenter for Exchange** finner du postboksen som skal brukes som erstatningsadresse, og deretter angir du adressen fra **Bruker-ID**-feltet i **Send som**-feltet. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser for mottakere](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019#use-the-eac-to-assign-permissions-to-individual-mailboxes).

### <a name="to-use-the-substitute-address-in-approval-workflows"></a>Slik bruker du erstatningsadressen i arbeidsflyter for godkjenning
1. I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ![lyspæren som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Oppsett for SMTP-e-post**, og deretter velger du den relaterte koblingen.
2. Kopier eller noter adressen i feltet **Bruker-ID**.
3. Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Brukeroppsett for godkjenning**, og velg deretter den relaterte koblingen.
4. I **Administrasjonssenter for Exchange** finner du postboksene for hver bruker i **Brukeroppsett for godkjenning**, og i feltet **Send som** angir du adressen fra feltet **Bruker-ID** fra siden **Oppsett for SMTP-e-post** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis du vil ha mer informasjon, kan du se [Administrere tillatelser for mottakere](https://docs.microsoft.com/en-us/Exchange/recipients/mailbox-permissions?view=exchserver-2019).
5. I [!INCLUDE[d365fin](includes/d365fin_md.md)] velger du ![lyspæren som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Oppsett for SMTP-e-post**, og deretter velger du den relaterte koblingen.
6. For å aktivere erstatning slår du på aktivering/deaktivering av **Tillat avsendererstatning**.

> [!Note]
> [!INCLUDE[d365fin](includes/d365fin_md.md)] vil avgjøre hvilken adresse som skal vises i følgende rekkefølge: <br><br> 1. Adressen som er angitt i feltet **E-post** på siden **Brukeroppsett for godkjenning** for meldinger i en arbeidsflyt. <br> 2. Adressen som er angitt i **Send som**-feltet på siden **Oppsett for SMTP-e-post**. <br> 3. Adressen som er angitt i **Bruker-ID**-feltet på siden **Oppsett for SMTP-e-post**.


## <a name="see-also"></a>Se også  
[Delte postbokser i Exchange Online](https://docs.microsoft.com/en-us/exchange/collaboration-exo/shared-mailboxes)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Sende dokumenter i e-post](ui-how-send-documents-email.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)  
[Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] som innboks for virksomheten i Outlook](admin-outlook.md)  
[Få [!INCLUDE[d365fin](includes/d365fin_md.md)] på mobilenheten min](install-mobile-app.md)
