---
title: "Metoder for å feilsøke eller omgå problemer | Microsoft-dokumentasjon"
description: "Lær å omgå problemer i Accountant Hub for Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: nb-no
ms.lasthandoff: 12/14/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a>Feilsøke [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

Registrering for [!INCLUDE[d365acc](includes/d365acc_md.md)] er enkelt og kan gjøres svært raskt. Det er også lett å legge til klienter på instrumentbordet, men denne artikkelen tar opp problemer du kan møte underveis.

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a>Hvilken e-postadresse kan jeg bruke med [!INCLUDE[d365acc](includes/d365acc_md.md)]?
[!INCLUDE[d365acc](includes/d365acc_md.md)] krever at du bruker en e-postadresse for arbeid eller skole for å registrere deg. [!INCLUDE[d365acc](includes/d365acc_md.md)] støtter ikke e-postadressene levert av e-posttjenester for forbrukere eller telekommunikasjonsleverandører. Dette inkluderer outlook.com, hotmail.com, gmail.com og andre.  

Hvis du prøver å registrere deg med en personlig e-postadresse, får du en melding om å bruke en e-postadresse for arbeid eller skole.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Hvorfor kan jeg ikke koble til klientens data?
Det kan være et par årsaker, blant annet følgende:

- URL-adressen i feltet **URL-adresse for klient** er ikke gyldig  

  Gå til **Administrer klienter**, åpne klienten du ikke kan koble til, og velg deretter **Test URL-adresse for klient**.  
- Klientens selskapet er frakoblet for øyeblikket, for eksempel hvis det blir oppgradert

  På instrumentpanelet velger du **Verktøy**-menyelementet, og deretter **Sjekk feil**. Dermed åpnes en liste med tekniske opplysninger, så du vil kanskje kontakte systemansvarlig hvis du ser feil. Feilmeldingen «Serveren har avvist klientlegitimasjonen» antyder at du ikke har tilgang.  
- Du ikke har mottatt en e-post fra klienten som inviterer dem til [!INCLUDE[d365fin](includes/d365fin_md.md)], eller du åpnet ikke koblingen i e-posten, eller du godtok ikke invitasjonen.

  Du må åpne koblingen i invitasjonen og godta trinnene som legger deg til i klientens [!INCLUDE[d365fin](includes/d365fin_md.md)]. Før det har du ikke tilgang til dataene.  
- Du har ikke tilgang til alle selskapene i klientens [!INCLUDE[d365fin](includes/d365fin_md.md)]

  Klienten kan ha flere selskaper eller konsern i [!INCLUDE[d365fin](includes/d365fin_md.md)], og invitasjonen omfatter ikke alltid alle selskapene. Kontakt klienten for å sikre at du har tilgang til selskapene som klienten vil du skal arbeide i.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Hvorfor oppdateres ikke dataene på instrumentbordet mitt?
Når du legger til en klient eller ber om en oppdatering av dataene, henter [!INCLUDE[d365acc](includes/d365acc_md.md)] dataene. Men du må oppdatere vinduet selv, for eksempel velge handlingen Vis alle selskap på nytt, oppdatere leservinduet, navigere fra instrumentbordet og deretter tilbake igjen, eller lignende. Dette er et kjent problem som vi arbeider med å forbedre i en senere oppdatering.  

## <a name="see-also"></a>Se også
[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Legge til klienter på skrivebordet i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  

