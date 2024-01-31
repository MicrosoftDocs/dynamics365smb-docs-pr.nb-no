---
title: Slett godkjenningsarbeidsflyter
description: 'Hvis du er sikker på at en arbeidsflyt ikke lenger er i bruk, kan du slette den. Alle forekomster av arbeidsflyttrinn definert i arbeidsflyten må ha statusen **Fullført**.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '1500,'
ms.date: 09/08/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Slett godkjenningsarbeidsflyter

Hvis du er sikker på at en arbeidsflyt ikke lenger er i bruk, kan du slette den. Alle forekomster av arbeidsflyttrinn definert i arbeidsflyten må ha statusen **Fullført**.

> [!CAUTION]
> Når du sletter en arbeidsflyt, går all informasjon i arbeidsflyten tapt.

På **Arbeidsflyt**-siden oppretter du en arbeidsflyt ved å føre opp de involverte trinnene på linjene. Hvert trinn består av en arbeidsflythendelse, endret av hendelsesbetingelsene, og et arbeidsflytsvar, endret av svaralternativer. Du definerer arbeidsflyttrinn ved å fylle ut felter på arbeidsflytlinjer ved å bruke faste lister over verdier for hendelse og svar som representerer scenarioer som støttes av programkoden. Finn ut mer under [Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md).

## Slett en arbeidsflyt

1. Velg ikonet ![Lyspære som åpner funksjonen Fortell meg.](media/ui-search/search_small.png "Fortell hva du vil gjøre") , angi **Arbeidsflyter**, og velg deretter den relaterte koblingen.
2. Velg arbeidsflyten du vil slette.
3. Velg handlingen **Slett**.
4. Åpne eventuelt arbeidsflyten du vil slette.
5. Velg **Slett**-handlingen på **Arbeidsflyt**-siden.

> [!NOTE]
> Sletting av en arbeidsflyt krever at den deaktiveres. Du deaktiverer en arbeidsflyt ved å åpne den på siden **Arbeidsflyter** og deretter slå av vekslebryteren **Aktivert**.

## Se også

[Opprett godkjenningsarbeidsflyter](across-how-to-create-workflows.md)  
[Aktiver godkjenningsarbeidsflyter](across-how-to-enable-workflows.md)  
[Bruk godkjenningsarbeidsflyter](across-use-workflows.md)  
[Vis arkiverte forekomster av arbeidsflyttrinn](across-how-to-view-archived-workflow-step-instances.md)  
[Gjennomgang: Definer og bruk en arbeidsflyt for kjøpsgodkjenning](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)  
[Konfigurer godkjenningsarbeidsflyter](across-set-up-workflows.md)  
[Arbeidsflyt](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
