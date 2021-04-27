---
title: Bruke Word-maler til massekommunikasjon | Microsoft-dokumentasjon
description: Word-maler kan gjøre det enkelt å opprette dokumenter som er tilpasset for bestemte enheter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788572"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="53f39-103">Bruke Word-maler til massekommunikasjon</span><span class="sxs-lookup"><span data-stu-id="53f39-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="53f39-104">Microsoft Word-maler kan gjøre det enklere å massekommunisere med enheter som kunder og leverandører.</span><span class="sxs-lookup"><span data-stu-id="53f39-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="53f39-105">Du kan for eksempel opprette brosjyrer for å varsle kunder om en salgskampanje, brev til å informere leverandører om en ny kjøpspolicy, eller invitasjoner til å tiltrekke kontakter til et kommende arrangement.</span><span class="sxs-lookup"><span data-stu-id="53f39-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

<span data-ttu-id="53f39-106">Du kan bruke enheter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for malen, og legge til flettefelt for å tilpasse dokumenter for hver enhet.</span><span class="sxs-lookup"><span data-stu-id="53f39-106">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="53f39-107">Flettefeltene kommer fra enheten i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="53f39-107">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="53f39-108">Når du bruker en Word-mal på en enhet, settes det inn data fra flettefeltene i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="53f39-108">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="53f39-109">På siden **Word-maler** kan du bruke en veiledning for assistert installasjon for å laste ned en ZIP-fil som inneholder filen DataSource.txt og en Word-malfil for en enhet.</span><span class="sxs-lookup"><span data-stu-id="53f39-109">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="53f39-110">Når du har definert malen og lagt til flettefelt, bruker du den samme håndboken til å laste opp malen.</span><span class="sxs-lookup"><span data-stu-id="53f39-110">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="53f39-111">Du kan bare bruke Word-maler og datakildefiler du laster ned fra [!INCLUDE[prod_short](includes/prod_short.md)], og du må lagre filene på samme sted.</span><span class="sxs-lookup"><span data-stu-id="53f39-111">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="53f39-112">Når du velger en enhet du vil opprette en mal for, viser listen alle enhetene i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="53f39-112">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="53f39-113">Du kan imidlertid ikke opprette maler for alle enheter.</span><span class="sxs-lookup"><span data-stu-id="53f39-113">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="53f39-114">Hvis navnet på en enhet inneholder spesialtegn, for eksempel **/**, **.**, **_** eller **-**, kan du ikke opprette en mal for den.</span><span class="sxs-lookup"><span data-stu-id="53f39-114">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="53f39-115">Navnet på enheten vises i kolonnen **Objekttittel**.</span><span class="sxs-lookup"><span data-stu-id="53f39-115">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="53f39-116">Når du definerer malen i Word, kan du legge til flettefelt ved å velge **Sett inn flettefelt** i fanen **Masseutsendelser**.</span><span class="sxs-lookup"><span data-stu-id="53f39-116">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="53f39-117">Du kan ikke bruke flettefelt hvis navnet på feltet inneholder 40 tegn eller mer.</span><span class="sxs-lookup"><span data-stu-id="53f39-117">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="53f39-118">Du kan for eksempel ikke feltet bruke Company__Information_Customs_Permit_Date, fordi det har 40 tegn.</span><span class="sxs-lookup"><span data-stu-id="53f39-118">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="53f39-119">Når Word-malen er klar, kan du velge **Bruk** på siden **Word-maler** for å generere dokumentene.</span><span class="sxs-lookup"><span data-stu-id="53f39-119">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="53f39-120">Du kan enten opprette ett dokument som inneholder inndelinger for hver enkelt enhet, eller dele opp operasjonen for å opprette et nytt dokument for hver enhet.</span><span class="sxs-lookup"><span data-stu-id="53f39-120">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="53f39-121">Slik oppretter du en Word-mal</span><span class="sxs-lookup"><span data-stu-id="53f39-121">To create a Word template</span></span>
1. <span data-ttu-id="53f39-122">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Word-maler**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="53f39-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="53f39-123">Følg trinnene i den assisterte oppsettsveiledningen.</span><span class="sxs-lookup"><span data-stu-id="53f39-123">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="53f39-124">Se også</span><span class="sxs-lookup"><span data-stu-id="53f39-124">See Also</span></span>
[<span data-ttu-id="53f39-125">Administrere rapport- og dokumentoppsett</span><span class="sxs-lookup"><span data-stu-id="53f39-125">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
