---
title: Sammenkoble og synkronisere poster manuelt | Microsoft Docs
description: Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster i en tabell i Business Central og Dynamics 365 Sales-enhet som er koblet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 0c70b1ba34af32b7cf542149c8f15cb191761358
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308119"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="1ca1d-103">Sammenkoble og synkronisere poster manuelt</span><span class="sxs-lookup"><span data-stu-id="1ca1d-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="1ca1d-104">Dette emnet beskriver hvordan du kobler sammen én eller flere poster i [!INCLUDE[d365fin](includes/d365fin_md.md)] med poster i [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1ca1d-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="1ca1d-105">Kobling av poster lar deg vise [!INCLUDE[crm_md](includes/crm_md.md)]-informasjon fra [!INCLUDE[d365fin](includes/d365fin_md.md)], og omvendt.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="1ca1d-106">Kopling lar deg også synkronisere data mellom postene.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="1ca1d-107">Du kan koble eksisterende poster, eller du kan opprette og koble nye poster.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="1ca1d-108">Koble og synkronisere data med [!INCLUDE[crm_md](includes/crm_md.md)] er bare tilgjengelig hvis systemansvarlig har opprettet en kobling mellom [!INCLUDE[d365fin](includes/d365fin_md.md)] og [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1ca1d-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="1ca1d-109">En rask måte å kontrollere på, er å åpne **Kunde**-kortet og se etter handlingen **Konfigurer kobling**.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="1ca1d-110">Hvis handlingen er tilgjengelig, er appene koblet.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-110">If the action is available, the apps are connected.</span></span>   

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="1ca1d-111">Koble en post</span><span class="sxs-lookup"><span data-stu-id="1ca1d-111">To couple a record</span></span>  
1.  <span data-ttu-id="1ca1d-112">I [!INCLUDE[d365fin](includes/d365fin_md.md)] åpner du kortet for posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="1ca1d-113">For eksempel kunde- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="1ca1d-114">Du kan også bare åpne listesiden og velge posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="1ca1d-115">Velg handlingen **Konfigurer kobling**.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="1ca1d-116">Fyll ut feltene, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="1ca1d-117">Synkronisere en enkeltoppføring</span><span class="sxs-lookup"><span data-stu-id="1ca1d-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="1ca1d-118">I [!INCLUDE[d365fin](includes/d365fin_md.md)] åpner du kortet for posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="1ca1d-119">For eksempel kunde- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="1ca1d-120">Velg **Synkroniser nå**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="1ca1d-121">Hvis en post kan synkroniseres fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="1ca1d-122">Synkronisere flere poster</span><span class="sxs-lookup"><span data-stu-id="1ca1d-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="1ca1d-123">I [!INCLUDE[d365fin](includes/d365fin_md.md)] åpner du listesiden for posten, for eksempel listesiden for kunder eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="1ca1d-124">Velg postene som skal synkroniseres, og velg deretter **Synkroniser nå**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="1ca1d-125">Hvis postene kan synkroniseres fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til [!INCLUDE[crm_md](includes/crm_md.md)] eller fra [!INCLUDE[crm_md](includes/crm_md.md)] til [!INCLUDE[d365fin](includes/d365fin_md.md)], velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**-knappen.</span><span class="sxs-lookup"><span data-stu-id="1ca1d-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1ca1d-126">Se også</span><span class="sxs-lookup"><span data-stu-id="1ca1d-126">See Also</span></span>  
[<span data-ttu-id="1ca1d-127">Bruke Dynamics 365 Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="1ca1d-127">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
