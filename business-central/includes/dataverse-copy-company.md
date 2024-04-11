---
author: brentholtorf
ms.topic: include
ms.date: 03/08/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

> [!NOTE]
> Når du kopierer et selskap i et miljø der Dataverse- eller Sales-integrering er aktivert, fjerner [!INCLUDE [prod_short](prod_short.md)] følgende innstillinger under kopiering til målselskapet:
>
> * Dataverse- og Dynamics-tilkoblingsinnstillinger for å sikre at integreringen starter på riktig måte i målselskapet.
> * Integreringsposter for å sikre at målselskapet ikke peker til poster som er koblet til kildeselskapet.
> * Integreringssynkronisering for å stoppe bakgrunnsjobber for synkronisering.
> * Synkroniseringsfeil, hvis de eksisterer, fordi de peker på feil i kildeselskapet og bare blir ansett som støy i målselskapet.