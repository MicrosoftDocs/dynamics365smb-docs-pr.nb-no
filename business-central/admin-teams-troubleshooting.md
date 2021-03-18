---
title: Feilsøke Microsoft Teams-integrering
description: Finn ut hva du kan gjøre som administrator for å styre Microsoft Teams-integreringen.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, troubleshooting, errors
ms.date: 01/20/2021
ms.author: jswymer
ms.openlocfilehash: 7a98b53a34ddf403cf6507da7740b97924d4c81c
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385202"
---
# <a name="troubleshooting-microsoft-teams-integration-with-prod_short"></a>Feilsøke Microsoft Teams-integrering med [!INCLUDE [prod_short](includes/prod_short.md)]

[!INCLUDE [online_only](includes/online_only.md)]

Denne artikkelen inneholder informasjon om hvordan du kan identifisere og løse problemer som kan oppstå når du bruker Microsoft Teams sammen med [!INCLUDE [prod_short](includes/prod_short.md)], som en vanlig bruker eller administrator.

## <a name="none-of-my-links-expand-into-a-card"></a>Ingen av koblingene utvides til et kort 

Her er noen ting du kan prøve hvis du får dette problemet:

1. Først kontrollerer du at [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams er installert.

    Du kan kontrollere dette ved å logge deg på Teams-skrivebordsappen eller Teams i nettleseren. Deretter velger du **Apper** på venstre side og søker etter **[!INCLUDE [prod_short](includes/prod_short.md)]**. Når du finner **[!INCLUDE [prod_short](includes/prod_short.md)]**-appen, velger du den for å åpne siden med appdetaljer. Hvis knappen **Legg til for meg** vises, er ikke [!INCLUDE [prod_short](includes/prod_short.md)]-appen installert. Hvis du vil ha mer informasjon om hvordan du installerer appen, kan du se [Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md).

    > [!NOTE]
    > Gjestebrukere kan ikke installere apper umiddelbart. Hvis du vil ha mer informasjon om gjestebrukere, kan du se vanlige spørsmål om samarbeid med gjester. 

2. Kontroller deretter at du har logget på med riktig identitet.

    Gå til en chat i Teams, og velg [!INCLUDE [prod_short](includes/prod_short.md)]-ikonet under meldingsboksen. Når vinduet vises, må du kontrollere om brukeren den sier at du er tilkoblet som, samsvarer med den du bruker til å koble deg til [!INCLUDE [prod_short](includes/prod_short.md)].

3. Kontroller at codeunit 2718 **Page Summary Provider** publiseres som en nettjeneste.

    Teams kobles til [!INCLUDE [prod_short](includes/prod_short.md)] med et endepunkt til denne codeunit på [!INCLUDE [prod_short](includes/prod_short.md)]-tjenesten. Hvis du vil ha informasjon om publisering av nettjenester, kan du se [Publiser en nettjeneste](across-how-publish-web-service.md).

4. Det kan også hende at organisasjonen din hindrer innliming av koblinger som utvides til kort. Kontakt administratoren for å forstå organisasjonspolicyene for Teams som kan gjelde for deg.

## <a name="my-link-sometimes-doesnt-expand-into-a-card"></a>Koblingen utvides noen ganger ikke til et kort 

En kobling utvides ikke til et kort i følgende situasjoner:

- Koblingen er rettet mot en side av en type som ikke representerer en post. Det kan for eksempel være en kobling til rollesenteret for [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollere sidetypen ved hjelp av sideinspeksjonsruten i nettklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon om sideinspeksjon, kan du se [Inspisere sider](across-inspect-page.md).
- Koblingen er rettet mot en side som (på et teknisk nivå) ikke er koblet til en kildetabell i [!INCLUDE [prod_short](includes/prod_short.md)]. Du kan kontrollere om en side har en kildetabell ved hjelp av sideinspeksjonsruten i nettklienten i [!INCLUDE [prod_short](includes/prod_short.md)]. Hvis du vil ha mer informasjon om sideinspeksjon, kan du se [Inspisere sider](across-inspect-page.md). 
- Teams støtter ikke koblingsforhåndsvisninger i enkelte funksjoner. Når du for eksempel skal løsne en chat, er du på et møte eller du er en gjest til en annen organisasjon.
- Teams forlater lydløst forsøk på å vise kortet etter 15 sekunder, for eksempel på grunn av nettverksproblemer.
- Teams kan ikke utvide koblingen hvis du allerede har limt inn en kobling i samme meldingsboks og slettet kortet.

Koblingen må også inneholde all nødvendig informasjon for å finne posten og vise det tilsvarende kortet. Denne informasjonen omfatter:

- Miljønavnet ved å ta det med i URL-banen. Hvis du ikke angir miljønavnet, antar Teams at du prøver å nå miljøet som heter Produksjon.
- Selskapsnavnet ved hjelp av parameteren *company=*
- Sideidentifikatoren ved hjelp av parameteren *page=*
- Bokmerket til posten, ved hjelp av parameteren *bookmark=*

Eksempel:

`https://businesscentral.dynamics.com/?environmentname=Production&company=CRONUS%20USA%2C%20Inc.&page=21&dc=0&bookmark=21%3bEgAAAAJ7BTEAMAAwADAAMA%3d%3d`

Du finner tekniske detaljer om [!INCLUDE [prod_short](includes/prod_short.md)]-URL-adresser i [Nettklientens URL-adresse](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls)i hjelpen for [!INCLUDE [prod_short](includes/prod_short.md)]-utviklere og IT-eksperter.

## <a name="the-card-is-displayed-in-the-message-compose-box-but-selecting-the-details-button-does-nothing"></a>Kortet vises i meldingsboksen, men når du velger Detaljer-knappen, skjer det ingenting 

Når en kobling blir utvidet til et kort i meldingsboksen, må du sende meldingen til chatten før du kan bruke **Detaljer**-knappen.

## <a name="the-details-window-opens-but-shows-an-error-before-details-are-shown"></a>Detaljer-vinduet åpnes, men viser en feil før detaljene vises

Dette problemet kan skyldes et par ting: manglende tillatelser i [!INCLUDE [prod_short](includes/prod_short.md)] eller nettleserinnstillinger (når du bruker Teams i nettleseren).

1. Kontroller tillatelsene dine i [!INCLUDE [prod_short](includes/prod_short.md)].

    Hvis du vil vise detaljer for et kort, kontrollerer [!INCLUDE [prod_short](includes/prod_short.md)] om lisensen og tillatelsene for å vise den bestemte posten og den bestemte siden i det bestemte selskapet og miljøet. Hvis du ikke er autorisert for noen av disse tingene, vises standard [!INCLUDE [prod_short](includes/prod_short.md)]-feilmeldinger om tillatelser i Detaljer-vinduet. 

    Hvis du vil ha mer informasjon om tillatelser, kan du se [Tilordne tillatelser til brukere og grupper](ui-define-granular-permissions.md)

2. Kontroller nettleserinnstillingene hvis du bruker Teams i nettleseren.

    - Popup-blokkering må enten være deaktivert eller angitt til å tillate popup-vinduer fra domenene *businesscentral.dynamics.com* eller *bc.dynamics.com*. Hvis du vil ha informasjon om hvordan du tillater popup-vinduer for [!INCLUDE [prod_short](includes/prod_short.md)], kan du se [Konfigurere nettleseren](across-browser-settings.md#popup).
    - Nettleseren må ha tilgang til lokal nettleserlagring for informasjonskapsler og innstillinger mens du arbeider.
    - Unngå å bruke gjestesurfing eller privat surfing med mindre det er nødvendig, fordi de kan forkaste eller blokkere visse deler i enkelte nettlesere.

    Hvis du vil ha mer informasjon om minimumskrav til nettlesere, kan du se [Minimumskrav for å bruke [!INCLUDE [prod_short](includes/prod_short.md)]](product-requirements.md#browsers) 

## <a name="im-having-problems-with-the-camera-or-location-in-teams"></a>Jeg har problemer med kameraet eller plasseringen i Teams 

Når du bruker [!INCLUDE [prod_short](includes/prod_short.md)]-funksjoner i detaljvinduet som krever tilgang til plasseringen eller enhetskameraet, må du først gi samtykke til at Teams får tilgang til disse enhetsegenskapene.  

- For Teams i nettleseren må du kontrollere at nettleserinnstillingene gir tilgang til kamera og plassering for https://teams.microsoft.com. 

- For Teams for iOS eller Android må du kontrollere at enhetsinnstillingene gir tilgang til kamera og plassering for Teams-mobilappen. 

Hvis du trenger hjelp til å endre disse innstillingene, kan du se at [Kameraet fungerer ikke i Teams](https://support.microsoft.com/office/my-camera-isn-t-working-in-teams-9581983b-c6f9-40e3-b0d8-122857972ade?ns=msftteams&version=16&ui=en-us&rs=en-us&ad=us) på Microsoft Kundestøtte.

[!INCLUDE [prod_short](includes/prod_short.md)]-appen støtter ikke plassering i Teams-skrivebordsappen.. Hvis du vil ha mer informasjon om plassering, kan du se [Vanlige spørsmål om Teams](teams-faq.md#location).

Med noen nettlesere, som nye Microsoft Edge, kan du velge hvilket enhetskamera som skal brukes når enheten støtter flere kameraer. 

## <a name="teams-displays-mixed-languages-for-my-cards-and-card-details"></a>Teams viser blandede språk for kort og kortdetaljer

Hvis kort og kortdetaljer skal vise samme språk i Teams, må språket for Teams-klienten og språket du bruker i [!INCLUDE [prod_short](includes/prod_short.md)]-nettklienten, samsvare.

- Hvis du vil vite mer om hvordan du endrer språk i Teams, kan du se [Endre innstillinger i Teams](https://support.microsoft.com/en-us/office/change-settings-in-teams-b506e8f1-1a96-4cf1-8c6b-b6ed4f424bc7) på Microsoft Kundestøtte. 

- Hvis du vil vite mer om hvordan du endrer språket i [!INCLUDE [prod_short](includes/prod_short.md)], kan du se [Endre grunnleggende innstillinger – språk](ui-change-basic-settings.md#language).

Hvis du vil ha mer informasjon om hvordan språk fungerer mellom Teams og [!INCLUDE [prod_short](includes/prod_short.md)], kan du se [Vanlige spørsmål om Teams](teams-faq.md#language).

## <a name="i-edited-a-field-in-the-details-window-but-my-change-wasnt-saved"></a>Jeg redigerte et felt i detaljvinduet, men endringen ble ikke lagret

Endringer du gjør i et felt i detaljvinduene, lagres automatisk når du forlater feltet. Før du lukker vinduet etter at du har endret et felt, trykker du Tab-tasten eller klikker/trykker utenfor feltet.

## <a name="a-new-tile-appeared-in-the-app-launcher-how-do-i-remove-it"></a>En ny flis ble vist i appstarteren. Hvordan fjerner jeg den?

Når du viser appene på Office 365-hjemmesiden (https://home.office.com) eller i appstarteren, vises en ny flis med navnet "Business Central Teams Integration Service Connector" når du har installert [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Teams. Denne flisen har ingen verdi i seg selv, og kan trygt skjules.

Som en administrator, som har Azure Active Directory-administratorrettigheter, kan du skjule flisen ved å gjøre følgende:

1. Logg på [Azure Active Directory-administrasjonssenteret](https://aad.portal.azure.com/).
2. Velg **Enterprise-apper**, og velg deretter **Business Central Teams Integration Service Connector**.
3. Velg **Egenskaper**, og sett deretter bryteren **Synlig for brukere** til **Nei**.
4. Velg **Lagre**.

> [!NOTE]
> Det tar en liten stund før endringen trer i kraft.


## <a name="see-also"></a>Se også

[Oversikt over [!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams-integrering](across-teams-overview.md)  
[Installer [!INCLUDE [prod_short](includes/prod_short.md)]-appen for Microsoft Teams](across-install-app-for-teams.md)  
[Vanlige spørsmål om Teams](teams-faq.md)  
[Utvikle for Teams-integrering](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]