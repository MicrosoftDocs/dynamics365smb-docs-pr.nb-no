---
title: Felt som kreves for å fullføre prosesser | Microsoft-dokumentasjon
description: Les om felt som er markert med en rød stjerne, som betyr at de er obligatoriske og må fylles ut for at prosesser skal kunne fullføres.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 6778536df70ef70b1e3e67e956768b0a474acd89
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "853238"
---
# <a name="detecting-mandatory-fields"></a>Registrere obligatoriske felt
Når du angir data på sider i [!INCLUDE[d365fin](includes/d365fin_md.md)], merkes bestemte felt med en rød stjerne. Den røde stjernen betyr at feltet må fylles ut for å fullføre en bestemt prosess som bruker feltet, for eksempel bokføre en transaksjon som bruker verdien i feltet.

Selv om feltet inneholder en rød stjerne, er du ikke nødt til å fylle ut feltet før du går videre til andre felt eller lukker siden. Stjernen bare fungerer som en påminnelse om at du vil bli blokkert fra å fullføre en bestemt prosess.

## <a name="examples"></a>Eksempler
På siden **Kundekort** vises den røde stjernen i **Navn**-feltet, i **Mva-områdekode**-feltet og de tre bokføringsgruppefeltene for å angi at du ikke kan bokføre en salgstransaksjon for kunden med mindre feltene fylles ut.

Den røde stjernen vises i feltet **Beskrivelse** på siden **Varekort** for å angi at du ikke kan registrere varen på en dokumentlinje, for eksempel en ordre, med mindre dette feltet fylles ut.

## <a name="see-also"></a>Se også
[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
