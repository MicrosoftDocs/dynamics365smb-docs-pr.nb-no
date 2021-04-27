---
title: Felt som kreves for å fullføre prosesser | Microsoft-dokumentasjon
description: Les om felt som er markert med en rød stjerne, som betyr at de er obligatoriske og må fylles ut for at prosesser skal kunne fullføres.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: solsen
ms.openlocfilehash: 386025d90301f780f8bf5927de495658a100825f
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775278"
---
# <a name="detecting-mandatory-fields"></a><span data-ttu-id="f5d9a-103">Registrere obligatoriske felt</span><span class="sxs-lookup"><span data-stu-id="f5d9a-103">Detecting Mandatory Fields</span></span>
<span data-ttu-id="f5d9a-104">Når du angir data på sider i [!INCLUDE[prod_short](includes/prod_short.md)], merkes bestemte felt med en rød stjerne.</span><span class="sxs-lookup"><span data-stu-id="f5d9a-104">When you enter data on pages in [!INCLUDE[prod_short](includes/prod_short.md)], certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="f5d9a-105">Den røde stjernen betyr at feltet må fylles ut for å fullføre en bestemt prosess som bruker feltet, for eksempel bokføre en transaksjon som bruker verdien i feltet.</span><span class="sxs-lookup"><span data-stu-id="f5d9a-105">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>

<span data-ttu-id="f5d9a-106">Selv om feltet inneholder en rød stjerne, er du ikke nødt til å fylle ut feltet før du går videre til andre felt eller lukker siden.</span><span class="sxs-lookup"><span data-stu-id="f5d9a-106">Even though the field contains a red asterisk, you are not forced to fill in the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="f5d9a-107">Stjernen bare fungerer som en påminnelse om at du vil bli blokkert fra å fullføre en bestemt prosess.</span><span class="sxs-lookup"><span data-stu-id="f5d9a-107">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>

## <a name="examples"></a><span data-ttu-id="f5d9a-108">Eksempler</span><span class="sxs-lookup"><span data-stu-id="f5d9a-108">Examples</span></span>
<span data-ttu-id="f5d9a-109">På siden **Kundekort** vises den røde stjernen i **Navn**-feltet, i **Mva-områdekode**-feltet og de tre bokføringsgruppefeltene for å angi at du ikke kan bokføre en salgstransaksjon for kunden med mindre feltene fylles ut.</span><span class="sxs-lookup"><span data-stu-id="f5d9a-109">On the **Customer Card** page, the red asterisk appears in the **Name** field, in the **Tax Area Code** field, and in the posting group fields to indicate that you cannot post a sales transaction for the customer unless the fields are filled.</span></span>

<span data-ttu-id="f5d9a-110">Den røde stjernen vises i feltet **Beskrivelse** på siden **Varekort** for å angi at du ikke kan registrere varen på en dokumentlinje, for eksempel en ordre, med mindre dette feltet fylles ut.</span><span class="sxs-lookup"><span data-stu-id="f5d9a-110">On the **Item Card** page, the red asterisk appears in the **Description** field to indicate that you cannot enter the item on a document line, such as a sales order, unless this field is filled.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5d9a-111">Se også</span><span class="sxs-lookup"><span data-stu-id="f5d9a-111">See Also</span></span>
<span data-ttu-id="f5d9a-112">[Arbeide med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5d9a-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]