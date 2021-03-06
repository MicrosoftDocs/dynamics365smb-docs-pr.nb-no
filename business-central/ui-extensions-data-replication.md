---
title: Skyoverføringsutvidelser
description: Bruk skyoverføringsutvidelsene til å overføre de lokale dataene til Business Central på nettet. Disse utvidelsene flytter de lokale dataene til skyen, slik at du kan bruke Business Central på nettet med de eksisterende dataene.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f02face497affd1fd1467c118e10e69f2be39b85
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889127"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a>Skyoverføringsutvidelser for overføring til Business Central Online

Avhengig av din lokale løsning må du bruke ulike utvidelser for å koble data til lokal [!INCLUDE[prod_short](includes/prod_short.md)] for å overføre løsningen til skyen.  

Hvis du bruker én av de støttede lokale produktene, kan du konfigurere skymiljøet basert på en produktspesifikk utvidelse. Når skymiljøet er konfigurert, vil du kunne overføre data fra den lokale løsningen til [!INCLUDE[prod_short](includes/prod_short.md)]. Dette gjør at du kan dra nytte av hva skyen har å tilby bedriften din, for eksempel utvidet innsikt i din bedrift, AI, tilgang til flere enheter og tilgang når og hvor som helst.  

Hvis du vil ha mer informasjon, kan du se [Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrasjonsinnholdet for [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="business-central-on-premises"></a>Business Central lokalt

Hvis du bruker en lokal distribusjon av [!INCLUDE[prod_short](includes/prod_short.md)], hent utvidelsen for **Intelligent skybase** og utvidelsen for **Intelligent sky for Business Central**, og kjør deretter den assisterte oppsettsveiledningen **Oppsett av skyoverføring**.  

## <a name="dynamics-gp"></a>Dynamics GP

Hvis du bruker Dynamics GP, hent utvidelsen for **Intelligent skybaseutvidelse** og utvidelsen for **Intelligent sky for Dynamics GP** , og kjør deretter den assisterte oppsettsveiledningen **Oppsett av skyoverføring**.  

> [!IMPORTANT]
> Migrering fra Dynamics GP med den assisterte oppsettsveiledningen **Oppsett av skyoverføring** støttes for øyeblikket bare for følgende markeder: USA, Canada, Storbritannia.

## <a name="dynamics-sl"></a>Dynamics SL

Hvis du bruker Dynamics SL, hent utvidelsen for **Intelligent skybase**, utvidelsen for **Microsoft Dynamics SL intelligent sky** og utvidelsen for **Microsoft Dynamics SL historikksmartlister**, og kjør deretter den assisterte oppsettsveiledningen **Oppsett av skyoverføring**.  

## <a name="see-also"></a>Se også

[Utvidelse for skyoverføringsbase](ui-extensions-intelligent-cloud.md)  
[Overføre lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]