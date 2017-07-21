---
title: Koble dataene med Flow | Microsoft-dokumentasjon
description: "Du kan gjøre Financials-dataene tilgjengelige som en datakilde og angi en OData-URL-adresse til webtjenestene dine for å utvikle automatisk arbeidsflyt."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: nb-no
ms.lasthandoff: 07/07/2017


---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruke [!INCLUDE[d365fin](includes/d365fin_md.md)] i en automatisk arbeidsflyt
Du kan bruke dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del av en arbeidsflyt i Microsoft Flow.  

> [!NOTE]  
>   Du må ha en gyldig konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] og med Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Legge til [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. I leseren, kan du gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/), og deretter logge på.
2. Velg **Mine Flow-er** fra båndet øverst på siden.
3. I vinduet **Mine Flow-er** velger du **Opprett fra tom**.
4. Fra listen over tilgjengelige utløsere velger du en av de to [!INCLUDE[d365fin](includes/d365fin_md.md)]-utløserne tilgjengelig: *Når en oppføring opprettes* eller *Når en oppføring endres*.
5. Flow vil vise en tilkoblingsside som ber deg om informasjonen som kreves for å koble til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Hvis du vil koble til, må du angi et navn for tilkoblingen, en OData URL-adresse, brukernavn, passord og selskapsnavn.

   For *OData URL-adressen*, kan du kopiere OData V4 URL-adressen for web-tjenester som er oppført på siden **Web Services** i [!INCLUDE[d365fin](includes/d365fin_md.md)], som `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   For *Selskapsnavn*, bruk navnet som vises i **Navn**-feltet i vinduet **Selskapsopplysninger** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] inneholder flere selskaper, velger du det relevante selskapsnavnet fra listen i **Selskaper**-vinduet. I begge tilfeller må du kontrollere at navnet du angir i veiviseren for PowerApps tilsvarer teksten som vises i [!INCLUDE[d365fin](includes/d365fin_md.md)], som `My Company`.

   Om brukernavn og passord, kan du bruke navnet og web service hurtigtast som er angitt for kontoen i **Brukere**-vinduet i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ditt brukernavn er for eksempel *ADMIN*, og web service hurtigtast som fungerer som passordet ditt er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU =*. Hvis du vil ha mer informasjon, kan du se [Administrere brukere og tillatelser](ui-how-users-permissions.md).
6. Velg **Opprett**-knappen nederst på siden for å fortsette.

   Flow vil vise en liste over tabeller som er tilgjengelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse tabellene eller endepunktene, representerer alle web-tjenester som du har publisert fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Alternativt, opprette en ny web service URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av **Opprett datasett** i siden **Web Services** ved hjelp av **Sett opp rapportering** assistert installasjonsveiledningen eller ved å velge **Rediger i Excel** i lister.
7. Velg dataene du vil bruke i Flow.

Nå har du koblet til Dynamics 365-dataene og er klar til å begynne å bygge din flyt. Hvis du ønsker mer informasjon, se [Flow-dokumentasjonen](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere forretningsdata fra andre økonomisystemer](upload-data.md)  
[Administrere brukere og tillatelser](ui-how-users-permissions.md)    
[Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

