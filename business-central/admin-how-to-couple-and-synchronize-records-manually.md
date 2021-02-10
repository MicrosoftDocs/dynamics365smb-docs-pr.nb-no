---
title: Kobling og synkronisering| Microsoft Docs
description: Synkronisering av en integrert tabelltilordning gjør det mulig å synkronisere data i alle poster i en tabell i Business Central og Dynamics 365 Sales-tabell som er koblet.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: fa4d6cfe13662613a73c14d68542f8319798ea80
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752678"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="f66f7-103">Kobling og synkronisering</span><span class="sxs-lookup"><span data-stu-id="f66f7-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="f66f7-104">Dette emnet beskriver hvordan du kobler sammen én eller flere poster i [!INCLUDE[prod_short](includes/prod_short.md)] med poster i Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f66f7-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="f66f7-105">Kobling av poster lar deg vise Dataverse-informasjon fra [!INCLUDE[prod_short](includes/prod_short.md)], og omvendt.</span><span class="sxs-lookup"><span data-stu-id="f66f7-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="f66f7-106">Kopling lar deg også synkronisere data mellom postene.</span><span class="sxs-lookup"><span data-stu-id="f66f7-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="f66f7-107">Du kan koble eksisterende poster, eller du kan opprette og koble nye poster.</span><span class="sxs-lookup"><span data-stu-id="f66f7-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="f66f7-108">Kobling og synkronisering av data er bare tilgjengelig hvis systemansvarlig har opprettet en kobling mellom [!INCLUDE[prod_short](includes/prod_short.md)] og Dataverse eller [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f66f7-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="f66f7-109">En rask måte å kontrollere på, er å åpne **Kunde**-kortet og se etter handlingen **Konfigurer kobling**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="f66f7-110">Hvis handlingen er tilgjengelig, er appene koblet.</span><span class="sxs-lookup"><span data-stu-id="f66f7-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="f66f7-111">Videoeksempel</span><span class="sxs-lookup"><span data-stu-id="f66f7-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="f66f7-112">Koble en post</span><span class="sxs-lookup"><span data-stu-id="f66f7-112">To couple a record</span></span>  
1.  <span data-ttu-id="f66f7-113">I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du kortet for posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="f66f7-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="f66f7-114">For eksempel kunde- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="f66f7-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="f66f7-115">Du kan også bare åpne listesiden og velge posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="f66f7-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="f66f7-116">Velg handlingen **Konfigurer kobling**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="f66f7-117">Fyll ut feltene, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="f66f7-118">Synkronisere en enkeltoppføring</span><span class="sxs-lookup"><span data-stu-id="f66f7-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="f66f7-119">I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du kortet for posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="f66f7-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="f66f7-120">For eksempel kunde- eller kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="f66f7-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="f66f7-121">Velg **Synkroniser nå**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="f66f7-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="f66f7-122">Hvis en post kan synkroniseres i én retning, velger du alternativet som angir retningen for dataoppdatering, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="f66f7-123">Slik synkroniserer du en enkeltoppføring fra [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="f66f7-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="f66f7-124">I [!INCLUDE[crm_md](includes/crm_md.md)] åpner du skjemaet for posten du vil koble.</span><span class="sxs-lookup"><span data-stu-id="f66f7-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="f66f7-125">Det kan for eksempel være skjema for kontokort eller kontaktkort.</span><span class="sxs-lookup"><span data-stu-id="f66f7-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="f66f7-126">Velg **[!INCLUDE[prod_short](includes/prod_short.md)]-** handlingen på båndet for å åpne og koble til posten automatisk.</span><span class="sxs-lookup"><span data-stu-id="f66f7-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="f66f7-127">Du kan synkronisere én post fra [!INCLUDE[crm_md](includes/crm_md.md)] automatisk bare når det ikke er merket av for **Synkroniser bare koblede poster** og synkroniseringsretningen er satt til Toveis eller Fra integreringstabell på siden **Tilordning for integreringstabell** for posten.</span><span class="sxs-lookup"><span data-stu-id="f66f7-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="f66f7-128">Hvis du vil ha mer informasjon, kan du se [Tilordne tabellene og feltene som skal synkroniseres](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="f66f7-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="f66f7-129">Synkronisere flere poster</span><span class="sxs-lookup"><span data-stu-id="f66f7-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="f66f7-130">I [!INCLUDE[prod_short](includes/prod_short.md)] åpner du listesiden for posten, for eksempel listesiden for kunder eller kontakter.</span><span class="sxs-lookup"><span data-stu-id="f66f7-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="f66f7-131">Velg postene som skal synkroniseres, og velg deretter **Synkroniser nå**-handlingen.</span><span class="sxs-lookup"><span data-stu-id="f66f7-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="f66f7-132">Hvis poster kan synkroniseres i én retning, velger du alternativet som angir retningen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="f66f7-133">Oppheve kobling av poster</span><span class="sxs-lookup"><span data-stu-id="f66f7-133">Uncoupling Records</span></span>
<span data-ttu-id="f66f7-134">Du kan slette én eller flere poster fra listesider eller siden **Feil ved synkronisering av koblede data** ved å velge én eller flere linjer og velge **Slett kobling**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="f66f7-135">Du kan også fjerne alle koblingene for én eller flere tabelltilordninger på siden **Tilordninger for integreringstabell**.</span><span class="sxs-lookup"><span data-stu-id="f66f7-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="f66f7-136">Se også</span><span class="sxs-lookup"><span data-stu-id="f66f7-136">See Also</span></span>  
[<span data-ttu-id="f66f7-137">Bruke Dynamics 365 Sales fra Business Central</span><span class="sxs-lookup"><span data-stu-id="f66f7-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
