---
title: Betalingsavstemming med Envestnet Yodlee Bank Feeds-utvidelsen | Microsoft Docs
description: Beskriver Envestnet Yodlee Bank Feeds-utvidelsen, som kobles til bankkonti, slik at du raskt kan avstemme betalinger.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6089a51a0ef27175988ed0c00fdb353cd3c7e96c
ms.sourcegitcommit: c6e28db8f78fa21db064c9b8a8d742f49d7db3ae
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2019
ms.locfileid: "2692947"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a>Envestnet Yodlee Bank Feeds-utvidelsen
Hvis du raskt vil avstemme betalinger til bankkonti, lar tjenesten Envestnet Yodlee Bank Feeds deg koble systembankkontoen din til nettbankkontoen. Dette betyr at det siste bankkontoutdraget automatisk eller manuelt mates inn i avstemmingskladden, noe som sikrer at du alltid behandler de siste betalingene med minimal risiko for feil.

Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.

> [!NOTE]
> Envestnet Yodlee Bank Feeds-tjenesten støttes bare i den elektroniske versjonen av Business Central. Hvis du vil bruke denne funksjonaliteten lokalt, må du hente en cobrand-konto fra Envestnet Yodlee.<br /><br />
> Envestnet Yodlee Bank Feeds-tjenesten støttes bare i USA og Canada.
> Det er bare banker som befinner seg i disse landene, som støttes, selv om banker fra andre land kan vises i vinduet for valg av bank Envestnet Yodlee Bank Feeds i [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!IMPORTANT]
> På grunn av det nye direktivet for betalingstjenester i Europa (PSD2), vil du ikke lenger kunne importere bankkontoutdrag fra banker i Stobritannia i [!INCLUDE[d365fin](includes/d365fin_md.md)] etter 14. september 2019. Vi undersøker muligheten for å tilby denne funksjonen igjen senere.

Envestnet Yodlee Bank Feeds-tjenesten gir følgende fordeler:

* Fjerner behovet for manuell registrering.
* Forbedrer effektivitet og nøyaktighet når du utfører betalingsavstemming.
* Støtter et stort antall banker.
* Gir oppdatert informasjon om banktransaksjoner fra [!INCLUDE[d365fin](includes/d365fin_md.md)].
* Støtter manuelle og automatiske bankfeeder.
* Tillater outsourcing av betalingsavstemming til en regnskapsfører ved å gi tilgang til bankkontoutdrag.

Hvis du vil ha mer informasjon, kan du se [Konfigurere Envestnet Yodlee Bank Feeds-tjenesten](bank-how-setup-bank-statement-service.md).

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjelp av utvidelser](ui-extensions.md)    
[Utligne betalinger automatisk og avstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
