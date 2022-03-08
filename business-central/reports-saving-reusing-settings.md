---
title: Bruke og endre lagrede innstillinger i rapporter | Microsoft-dokumentasjon
description: Beskriver hvordan du bruker forhåndsdefinerte alternativer og filtre til å tilpasse rapporter og generere riktige data.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: a9bb72a85fb49b4316af2160e5823fbf77a18cbf
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2881404"
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Behandle lagrede innstillinger for rapporter og satsvise jobber
Når en rapport skal kjøres, ser brukere vanligvis en side der de kan velge alternativer og angi filtre for å endre dataene som er inkludert i den genererte rapporten. Denne siden kalles forespørselssiden. En rapport kan inneholde en eller flere *lagrede innstillinger* som brukere kan bruke på rapporten fra forespørselssiden. *Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre. Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene. Hvis du vil ha mer informasjon, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).

> [!NOTE]
> Dette emnet dreier seg hovedsakelig om "rapport", men lignende informasjon gjelder kjørsler.

Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i et selskap. Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller til alle brukerne i selskapet.

<!--
## Apply saved settings to a report
1. Open the report.

   The request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="to-create-and-modify-saved-settings-for-all-users"></a>Opprette og endre lagrede innstillinger for alle brukere
Du kan administrere lagrede innstillinger på siden **Rapportinnstillinger**. Det er to måter å åpne en side på:
-   Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportinnstillinger**, og velg deretter den relaterte koblingen.
-   Åpne en rapport, velg oppslag i feltet **Bruk standardverdi fra:**, og velg handlingen **Velge fra hele listen**.

Siden viser alle eksisterende lagrede innstillinger for alle brukere. Hvis det er et brukernavn i feltet **Tilordnet**, kan bare den brukeren bruke innstillingene som er lagret for den tilknyttede rapporten. Hvis det er en hake i feltet **Del med alle brukerne**, kan alle brukere bruke innstillingene som er lagret i rapporten.

Fra siden **Rapportinnstillinger**-siden kan du:
-   Velg handlingen **Ny** for å opprette en helt ny post med lagrede innstillinger.
-   Velg en post med lagrede innstillinger fra oversikten, og velg handlingen **Kopier** for å lage en kopi.
-   Velg en post med lagrede innstillinger fra oversikten, og velg handlingen **Rediger** for å endre en post med lagrede innstillinger.

> [!Important]
> Vurder navnet som du gir en post med lagrede innstillinger. Hvis du oppretter en post med lagrede innstillinger for alle brukere, og den har samme navn som en eksisterende post med lagrede innstillinger som er tilordnet en bestemt bruker, kan brukeren ikke bruke posten med lagrede innstillinger som er tilordnet til alle.  I delen **Lagrede innstillinger** på rapportforespørselssiden vil brukeren se to lagrede innstillingsposter med samme navn. Uansett hvilket alternativ som velges, vil imidlertid den brukerspesifikke posten med lagrede innstillingene bli brukt.

> [!NOTE]
> Funksjonen Lagrede innstillinger er bare tilgjengelig i rapporter der [SaveValues-egenskapen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) for forespørselssiden er satt til **Ja**. **SaveValues**-egenskapen angis i utviklingsmiljøet.  

## <a name="see-also"></a>Se også
[Arbeide med rapporter, satsvise jobber og XML-porter](ui-work-report.md)  
