---
title: Koble fra poster til ekstern informasjon eller eksterne programmer | Microsoft-dokumentasjon
description: Legg til en hyperkobling i et dokument eller et webområde til en bestemt post, for eksempel en kunde eller et dokument.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 781f43daf6482c7e29696dc7a03aa021550cde7d
ms.sourcegitcommit: f2e3b571eab6e01d9f5aa8ef47056b6bd313dcbd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/13/2019
ms.locfileid: "1629760"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="0d7c5-103">Legge til koblinger i webområder, dokumenter eller programmer i poster</span><span class="sxs-lookup"><span data-stu-id="0d7c5-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="0d7c5-104">Du kan legge til en kobling i et eksternt dokument, et webområde eller et program i en bestemt post som kunde, dokument eller ordre.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="0d7c5-105">Du kan også legge til en kobling som du kan velge for å åpne en ny, tom e-post til en bestemt mottaker.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="0d7c5-106">Kortsiden for noen poster, for eksempel kunde- og leverandørkort, har et **Hjemmeside**-felt der du kan angi en nettadresse (URL).</span><span class="sxs-lookup"><span data-stu-id="0d7c5-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="0d7c5-107">Du kan bruke metoden som er beskrevet i denne artikkelen, for å inkludere andre koblinger.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="0d7c5-108">Nå er denne funksjonen bare er tilgjengelig i lokale distribusjoner av [!INCLUDE [prodshort](includes/prodshort.md)] med den gamle Dynamics NAV Windows-klienten.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="0d7c5-109">Et annet eksempel kan være når du mottar papirfakturaer fra leverandører.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="0d7c5-110">Du kan skanne og lagre dem som PDF-filer på et SharePoint-område.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="0d7c5-111">Deretter kan du opprette en kobling fra en kjøpsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] til den tilsvarende fakturaen på SharePoint.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="0d7c5-112">Du kan også opprette en kobling fra et varekort til den tilsvarende siden i leverandørens elektroniske katalog.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="0d7c5-113">Slik legger du til en kobling i en post</span><span class="sxs-lookup"><span data-stu-id="0d7c5-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="0d7c5-114">Åpne posten du vil knytte koblingen til, for eksempel et kundekort eller en ordre.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="0d7c5-115">Hvis du vil knytte koblingen til en bestemt linje, for eksempel en kladdelinje, merker du linjen.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="0d7c5-116">Velg **Koblinger** for å åpne **Koblinger**-sider som viser alle gjeldende koblinger som er lagt til posten.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="0d7c5-117">Hvis du vil legge til en ny kobling, velger du **+ny**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="0d7c5-118">I vinduet **Koblingsadresse** angir du</span><span class="sxs-lookup"><span data-stu-id="0d7c5-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="0d7c5-119">Hvis du vil koble til en fil på datamaskinen eller nettverket, angir du fullstendig bane og filnavn, for eksempel **C:\My Documents\invoice1.doc**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:\My Documents\invoice1.doc**.</span></span>
    -   <span data-ttu-id="0d7c5-120">Hvis du vil koble til et webområde, angir du Internett-adressen (URL-adressen), for eksempel **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="0d7c5-121">Hvis du vil koble til et program, angir du en bestemt streng for å åpne programmet.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="0d7c5-122">Hvis du for eksempel vil åpne OneNote på en bestemt side, skriver du inn **onenote:///C:\My Documents/test.one**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-122">For example, to open OneNote with a specific page, enter **onenote:///C:\My Documents/test.one**.</span></span> <span data-ttu-id="0d7c5-123">Eller hvis du vil åpne Outlook med en ny, tom e-post til et bestemt alias, skriver du inn **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="0d7c5-124">Fyll ut **Beskrivelse**-feltet med informasjon om koblingen.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="0d7c5-125">Velg **Lagre**-knappen.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="0d7c5-126">Slik sletter du en kobling fra en post</span><span class="sxs-lookup"><span data-stu-id="0d7c5-126">To delete a link from a record</span></span>  

<span data-ttu-id="0d7c5-127">Hvis du vil slette en kobling, gå til siden **Koblinger** og velg **...** og deretter **Slett**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-127">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="0d7c5-128">Hvis du sletter én enkelt post, for eksempel en ordrelinje, en ordre eller en kunde, slettes alle koblingene som er knyttet til posten.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="0d7c5-129">Hvis du imidlertid sletter poster ved å bruke en kjørsel, for eksempel kjørselen **Slett fakturerte ordrer**, lagres koblingene i databasen.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="0d7c5-130">Hvis du vil slette koblingene fra databasen, kjører du kodeenheten **Slett koblinger til løse poster**.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="0d7c5-131">For å gjøre dette velger du ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angir **Slett koblinger til løse poster** og velger deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="0d7c5-131">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="0d7c5-132">Se også</span><span class="sxs-lookup"><span data-stu-id="0d7c5-132">See Also</span></span>  
<span data-ttu-id="0d7c5-133">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0d7c5-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
