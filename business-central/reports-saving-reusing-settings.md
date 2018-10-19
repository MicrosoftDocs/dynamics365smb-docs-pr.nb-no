---
title: Bruke og endre lagrede innstillinger i rapporter | Microsoft-dokumentasjon
description: "Beskriver hvordan du bruker forhåndsdefinerte alternativer og filtre til å tilpasse rapporter og generere riktige data."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 6027ba17868aca0a6571e059c9d157c542d12823
ms.contentlocale: nb-no
ms.lasthandoff: 09/28/2018

---
# <a name="managing-saved-settings-on-reports"></a>Administrere lagrede innstillinger i rapporter
Når en rapport skal kjøres, ser brukere vanligvis en side der de kan angi bestemte alternativer og filtre for å endre dataene som er inkludert i den genererte rapporten. Denne siden kalles rapportforespørselssiden. En rapport kan inneholde en eller flere *lagrede innstillinger* som brukere kan bruke på rapporten fra forespørselssiden. *Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre. Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene. Hvis du vil ha mer informasjon om hvordan lagrede innstillingene brukes, kan du se [Bruke lagrede innstillinger](ui-work-report.md#SavedSettings).

Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i firmaet. Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller alle brukerne i firmaet.

<!-- 
## Apply saved settings to a report
1. Open the report.

   The report request page appears.    
2. In the **Saved Settings** section of the page, set the **Name** field  to the saved settings that you want to use.

   The **Saved Settings** section only appears if the report has been run before or if there are existing saved settings entries. The saved settings entry called **Last used options and filters** is always available. These settings are the option and filter values that were used the last time you ran the report.

-->

## <a name="create-and-modify-saved-settings-for-all-users"></a>Opprette og endre lagrede innstillinger for alle brukere
Du kan administrere lagrede innstillinger fra siden **1560 Rapportinnstillinger**. Det er to måter å åpne en side på:
-   Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Rapportinnstillinger**, og velg deretter den relaterte koblingen.
-   Åpne en rapport, velg oppslag ved siden av boksen **Bruk standardverdi fra:**, og velg **Velge fra hele listen**.

Siden viser alle eksisterende lagrede innstillinger for alle brukere. Hvis det er et brukernavn i kolonnen **Tilordnet**, kan bare den brukeren bruke innstillingene som er lagret for den tilknyttede rapporten. Hvis det er en hake i kolonnen **Del med alle brukerne**, kan alle brukere bruke innstillingene som er lagret i rapporten.

Fra vinduet **Rapportinnstillinger** kan du:
-   Velg **Ny** for å opprette en helt ny post med lagrede innstillinger.
-   Velg en post med lagrede innstillinger fra oversikten, og velg **Kopier** for å lage en kopi.
-   Velg en post med lagrede innstillinger fra oversikten, og velg **Rediger** for å endre en post med lagrede innstillinger.


> [!Important]
> Vurder navnet som du gir en post med lagrede innstillinger. Hvis du oppretter en post med lagrede innstillinger for alle brukere, og den har samme navn som en eksisterende post med lagrede innstillinger som er tilordnet en bestemt bruker, kan brukeren ikke bruke posten med lagrede innstillinger som er tilordnet til alle.  I **Lagrede innstillinger** på rapportforespørselssiden, vil brukeren se to lagrede innstillingsposter med samme navn. Uansett hvilket alternativ som velges, vil imidlertid den brukerspesifikke posten med lagrede innstillingene bli brukt.

> [!NOTE]
> Funksjonen for lagrede innstillinger i rapporter er kun tilgjengelig når [SaveValues-egenskapen](https://docs.microsoft.com/en-us/dynamics-nav/savevalues-property) for forespørselssiden er satt til `Yes`. **SaveValues**-egenskapen angis i utviklingsmiljøet.  

## <a name="see-also"></a>Se også
[Arbeide med rapporter](ui-work-report.md)  

