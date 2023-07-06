---
title: Behandle lagrede innstillinger for rapporter og satsvise jobber
description: Beskriver hvordan administratoren kan konfigurere forhåndsdefinerte alternativer og filtre for en rapport og dele disse innstillingene med én eller alle brukerne.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customization, personalization'
ms.date: 12/21/2021
ms.author: edupont
---
# <a name="manage-saved-settings-for-reports-and-batch-jobs"></a><a name="manage-saved-settings-for-reports-and-batch-jobs"></a><a name="manage-saved-settings-for-reports-and-batch-jobs"></a>Behandle lagrede innstillinger for rapporter og satsvise jobber

Når en rapport skal kjøres, ser brukere vanligvis en side der de kan velge alternativer og angi filtre for å endre dataene som er inkludert i den genererte rapporten. Denne siden kalles *forespørselssiden*. En rapport kan inneholde en eller flere *lagrede innstillinger* som brukere kan bruke på rapporten fra forespørselssiden. *Lagrede innstillinger* er i hovedsak forhåndsdefinerte alternativer og filtre. Lagrede innstillinger er en rask, pålitelig og konsekvent metode for å generere rapporter som inneholder de riktige dataene. Hvis du vil ha mer informasjon, kan du se [Bruk lagrede innstillinger](ui-work-report.md#SavedSettings).

> [!NOTE]
> Dette emnet refererer til *rapporter*, men lignende informasjon gjelder for *kjørsler*.

Hvis du har riktige tillatelser, kan du vise, opprette og endre de lagrede innstillingene for alle rapporter for alle brukere i et selskap. Du kan tilordne lagrede innstillingene for en rapport til enkeltbrukere eller til alle brukerne i selskapet.

## <a name="manage-saved-settings"></a><a name="manage-saved-settings"></a><a name="manage-saved-settings"></a>Administrere lagrede innstillinger

Du kan administrere lagrede innstillinger på siden **Rapportinnstillinger**. Det er to måter å åpne en side på:

- Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") og angi **Rapportinnstillinger**, og velg deretter den relaterte koblingen.
- På forespørselssiden for en rapport velger du oppslaget i feltet **Bruk standardverdi fra** og deretter handlingen **Velg fra hele listen**.

    Dette feltet vises bare hvis du har kjørt rapporten minst én gang tidligere. Listen viser bare innstillinger som er tilgjengelige for deg, enten fordi de er dine egne innstillinger, eller fordi de deles med deg.

**Rapportinnstillinger**-siden viser alle eksisterende lagrede innstillinger for alle brukere. Hvis det er et brukernavn i feltet **Tilordnet**, kan bare den brukeren bruke innstillingene som er lagret for den tilknyttede rapporten. Hvis det er en hake i feltet **Del med alle brukerne**, kan alle brukere bruke innstillingene som er lagret i rapporten.  

> [!TIP]
> Når en bruker har kjørt en rapport som støtter delte innstillinger, blir innstillingene lagret og lagt til i denne listen. Administratoren kan i de fleste tilfeller redigere disse innstillingene og deretter velge å dele dem med alle brukerne.
>
> I noen tilfeller kan imidlertid innstillingene ikke deles, og administratoren kan heller ikke endre dem. De fleste kjørslene støtter ikke delte innstillinger.  

## <a name="create-or-modify-saved-settings-for-all-users"></a><a name="create-or-modify-saved-settings-for-all-users"></a><a name="create-or-modify-saved-settings-for-all-users"></a>Opprette eller endre lagrede innstillinger for alle brukere

Fra siden **Rapportinnstillinger**-siden kan du:

- Velg handlingen **Ny** for å opprette en helt ny post med lagrede innstillinger.
- Velg en post med lagrede innstillinger fra oversikten, og velg handlingen **Kopier** for å lage en kopi.
- Velg en post med lagrede innstillinger fra oversikten, og velg handlingen **Rediger** for å endre en post med lagrede innstillinger.

> [!Important]
> Vurder navnet som du gir en post med lagrede innstillinger. Hvis du oppretter en post med lagrede innstillinger for alle brukere, og den har samme navn som en eksisterende post med lagrede innstillinger som er tilordnet en bestemt bruker, kan brukeren ikke bruke posten med lagrede innstillinger som er tilordnet til alle.  I delen **Lagrede innstillinger** på rapportforespørselssiden vil brukeren se to lagrede innstillingsposter med samme navn. Uansett hvilket alternativ som velges, vil imidlertid den brukerspesifikke posten med lagrede innstillingene bli brukt.

> [!NOTE]
> Funksjonen for å lagre innstillinger er bare tilgjengelig i rapporter der [SaveValues-egenskapen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-savevalues-property) for forespørselssiden i rapporten er satt til **Ja**. **SaveValues**-egenskapen angis av utvikleren.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Arbeid med rapporter, satsvise jobber og XMLport-er](ui-work-report.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
