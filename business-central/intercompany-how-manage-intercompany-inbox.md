---
title: Behandle inngående og utgående KI-transaksjoner | Microsoft-dokumentasjon
description: Konserninterne transaksjoner du mottar fra de konserninterne partnerne dine, er oppført i den konserninterne innboksen der du behandler dem manuelt eller automatisk.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: incoming document
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: c7bf0c1c22d2f43220d9b101a1a54757add900e9
ms.sourcegitcommit: d09f5ee0e164c7716f4ccb2ed71e2f9732a1f4f9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "853284"
---
# <a name="manage-the-intercompany-inbox-and-outbox"></a><span data-ttu-id="12c45-103">Administrere den konserninterne innboksen og utboksen</span><span class="sxs-lookup"><span data-stu-id="12c45-103">Manage the Intercompany Inbox and Outbox</span></span>
<span data-ttu-id="12c45-104">Alle de konserninterne transaksjonene du mottar elektronisk fra de konserninterne partnerne, er oppført i den konserninterne innboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-104">All of the intercompany transactions that you receive electronically from your intercompany partners are listed in the intercompany Inbox.</span></span>  

## <a name="organizing-the-inbox"></a><span data-ttu-id="12c45-105">Ordre innboksen</span><span class="sxs-lookup"><span data-stu-id="12c45-105">Organizing the Inbox</span></span>  
 <span data-ttu-id="12c45-106">Du kan bruke filterfeltene øverst på innbokssiden til å bestemme hvilke transaksjoner som skal vises på siden.</span><span class="sxs-lookup"><span data-stu-id="12c45-106">You can use the filter fields at the top of the inbox page to determine which transactions are shown on the page.</span></span> <span data-ttu-id="12c45-107">Hvis du for eksempel bare vil se på transaksjoner som en bestemt partner har opprettet, kan du angi filtre i filtrene for **transaksjonskilde** og **kode for konsernintern partner**.</span><span class="sxs-lookup"><span data-stu-id="12c45-107">For example, if you only want to look at transactions a particular partner created, you can enter filters in the **Transaction Source** and **Intercompany Partner Code** filters.</span></span>  

### <a name="transaction-source"></a><span data-ttu-id="12c45-108">Transaksjonskilde</span><span class="sxs-lookup"><span data-stu-id="12c45-108">Transaction Source</span></span>  
<span data-ttu-id="12c45-109">Hva du kan gjøre med en transaksjon, avhenger av om den ble:</span><span class="sxs-lookup"><span data-stu-id="12c45-109">What you can do with a transaction depends whether it was:</span></span>  

- <span data-ttu-id="12c45-110">Opprettet av den konserninterne partneren</span><span class="sxs-lookup"><span data-stu-id="12c45-110">Created by your intercompany partner</span></span>  
- <span data-ttu-id="12c45-111">Avvist av den konserninterne partneren og returnert til deg</span><span class="sxs-lookup"><span data-stu-id="12c45-111">Rejected by your intercompany partner and returned to you</span></span>  

<span data-ttu-id="12c45-112">Du kan bruke feltet **Vis transaksjonskilde** til å filtrere siden **Konserninterne inngående transaksjoner** slik at det bare viser én av disse transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="12c45-112">You can use the **Show Transaction Source** field to filter the **Intercompany Inbox Transactions** page so that it displays only one of these types of transactions.</span></span> <span data-ttu-id="12c45-113">(Du kan også filtrere etter konsernintern partner eller etter innholdet i **Linjehandling**-feltet.)</span><span class="sxs-lookup"><span data-stu-id="12c45-113">(You can also filter by intercompany partner, or by the contents of the **Line Action** field.)</span></span>  

#### <a name="created-by-intercompany-partner"></a><span data-ttu-id="12c45-114">Opprettet av konsernintern partner</span><span class="sxs-lookup"><span data-stu-id="12c45-114">Created by Intercompany Partner</span></span>  
 <span data-ttu-id="12c45-115">Når du mottar en ny transaksjon som ble opprettet av partneren, kan du velge å:</span><span class="sxs-lookup"><span data-stu-id="12c45-115">When you receive a new transaction that was created by your partner, you can choose to either:</span></span>

- <span data-ttu-id="12c45-116">Godta transaksjonen</span><span class="sxs-lookup"><span data-stu-id="12c45-116">Accept the transaction</span></span>  
- <span data-ttu-id="12c45-117">Avvise transaksjonen (returnere den til partneren)</span><span class="sxs-lookup"><span data-stu-id="12c45-117">Reject the transaction (Return to partner)</span></span>  
- <span data-ttu-id="12c45-118">Avbryte transaksjonen (slette transaksjonen, men ikke returnere den til partneren)</span><span class="sxs-lookup"><span data-stu-id="12c45-118">Cancel the transaction (Delete the transaction but do not return it to your partner)</span></span>  

#### <a name="returned-from-intercompany-partner"></a><span data-ttu-id="12c45-119">Returnert fra konsernintern partner</span><span class="sxs-lookup"><span data-stu-id="12c45-119">Returned from Intercompany Partner</span></span>  
 <span data-ttu-id="12c45-120">Hvis transaksjonen ble avvist av den konserninterne partneren, kan du bare avbryte transaksjonen i innboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-120">If the transaction was rejected by your intercompany partner, your only choice is to cancel the transaction in the inbox.</span></span> <span data-ttu-id="12c45-121">Deretter må du opprette korrigeringslinjer eller reversere kladden eller bilaget i selskapet.</span><span class="sxs-lookup"><span data-stu-id="12c45-121">Then you must create correction lines or reverse the journal or document in your company.</span></span>  

## <a name="recreating-inbox-entries"></a><span data-ttu-id="12c45-122">Opprette innboksposter på nytt</span><span class="sxs-lookup"><span data-stu-id="12c45-122">Recreating Inbox Entries</span></span>  
 <span data-ttu-id="12c45-123">Hvis du godtok en transaksjon i innboksen, men deretter slettet bilaget eller kladden i stedet for å bokføre det/den, kan du opprette innboksposten på nytt og godta den på nytt.</span><span class="sxs-lookup"><span data-stu-id="12c45-123">If you accepted a transaction in your inbox but then deleted the document or journal instead of posting it, you can re-create the inbox entry and accept it again.</span></span>  

## <a name="getting-an-overview-of-intercompany-transactions-for-a-period"></a><span data-ttu-id="12c45-124">Få oversikt over konserninterne transaksjoner for en periode</span><span class="sxs-lookup"><span data-stu-id="12c45-124">Getting an Overview of Intercompany Transactions for a Period</span></span>  
 <span data-ttu-id="12c45-125">Du kan få oversikt over alle de konserninterne transaksjonene du har sendt og mottatt i en periode.</span><span class="sxs-lookup"><span data-stu-id="12c45-125">You can get an overview of all of the intercompany transactions that you have sent and received in a period.</span></span> <span data-ttu-id="12c45-126">Rapporten **Konserninterne transaksjoner** viser alle konserninterne finansposter, kundeposter og leverandørposter.</span><span class="sxs-lookup"><span data-stu-id="12c45-126">The **Intercompany Transactions** report lists all intercompany G/L entries, customer ledger entries, and vendor ledger entries.</span></span>

 > [!NOTE]  
 > <span data-ttu-id="12c45-127">Hvis de konserninterne partnerne er i samme database, overføres transaksjoner uten å måtte filen eller e-post.</span><span class="sxs-lookup"><span data-stu-id="12c45-127">If the intercompany partners are in the same database, then transactions are transferred without the need for file or email.</span></span> <span data-ttu-id="12c45-128">Se feltet **Overføringstype** på siden **Konsernintern partner**.</span><span class="sxs-lookup"><span data-stu-id="12c45-128">See the **Transfer Type** field on the **Intercompany Partner** page.</span></span> <br /><br />
<span data-ttu-id="12c45-129">I så fall kan du konfigurere systemet til å hoppe over innboksen og utboksen ved å merke av for henholdsvis **Godta transaksjoner automatisk** på siden **Konsernintern partner** og **Send transaksjoner automatisk** på siden **Konserninternt oppsett**.</span><span class="sxs-lookup"><span data-stu-id="12c45-129">In that case, you can set the system up to bypass the inbox and outbox by selecting the **Auto. Accept Transactions** check box on the **Intercompany Partner** page and the **Auto. Send Transactions** check box on the **Intercompany Setup** page respectively.</span></span>

## <a name="to-import-intercompany-transactions-from-a-file"></a><span data-ttu-id="12c45-130">Slik importerer du konserninterne transaksjoner fra en fil</span><span class="sxs-lookup"><span data-stu-id="12c45-130">To import intercompany transactions from a file</span></span>  
<span data-ttu-id="12c45-131">Hvis du har en konsernintern partner som ikke er i samme database som selskapet ditt, kan du motta konserninterne transaksjoner fra partneren i en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="12c45-131">If you have an intercompany partner that is not in the same database as your company, you can receive intercompany transactions from that partner in an .xml file.</span></span> <span data-ttu-id="12c45-132">Deretter må du importere transaksjonene til innboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-132">Then you must import the transactions into your inbox.</span></span>  

1.  <span data-ttu-id="12c45-133">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Selskapsopplysninger**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12c45-133">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information** , and then choose the related link.</span></span>
2. <span data-ttu-id="12c45-134">Lagre filen på lokasjonen du har angitt i feltet **Detaljer om konsernintern innboks** på siden **Selskapsopplysninger**.</span><span class="sxs-lookup"><span data-stu-id="12c45-134">Save the file to the location that you specified in the **Intercompany Inbox Details** field on the **Company Information** page.</span></span>  
3. <span data-ttu-id="12c45-135">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konserninterne inngående transaksjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12c45-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Intercompany Inbox Transactions**, and then choose the related link.</span></span>
4. <span data-ttu-id="12c45-136">På siden **Konserninterne inngående transaksjoner** velger du **Importer transaksjonsfil**.</span><span class="sxs-lookup"><span data-stu-id="12c45-136">On the **Intercompany Inbox Transactions** page, choose the **Import Transaction File** action.</span></span>  
5. <span data-ttu-id="12c45-137">På siden som vises, velger du XML-filen som inneholder transaksjonene, og deretter velger du **Åpne**-knappen.</span><span class="sxs-lookup"><span data-stu-id="12c45-137">on the page that appears, select the .xml file that contains the transactions, and then choose the **Open** button.</span></span>  

<span data-ttu-id="12c45-138">Transaksjonene importeres til innboksen, og du kan nå behandle dem.</span><span class="sxs-lookup"><span data-stu-id="12c45-138">The transactions are imported into the inbox and you can now process them.</span></span>

## <a name="to-process-incoming-intercompany-transactions"></a><span data-ttu-id="12c45-139">Slik behandler du inngående konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="12c45-139">To process incoming intercompany transactions</span></span>  
<span data-ttu-id="12c45-140">Når de konserninterne partnerne sender deg konserninterne transaksjoner, ender transaksjonene opp i den konserninterne innboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-140">When your intercompany partners send you intercompany transactions, the transactions end up in your intercompany inbox.</span></span> <span data-ttu-id="12c45-141">Du må vurdere hver transaksjon i innboksen og utføre de nødvendige handlingene.</span><span class="sxs-lookup"><span data-stu-id="12c45-141">You must evaluate each transaction in your inbox and act upon it.</span></span>  

1. <span data-ttu-id="12c45-142">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konserninterne inngående transaksjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12c45-142">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Intercompany Inbox Transactions**, and then choose the related link.</span></span>  
2. <span data-ttu-id="12c45-143">På siden **Konserninterne inngående transaksjoner** velger du en linje og velger en handling som **Godta**, for å behandle linjen.</span><span class="sxs-lookup"><span data-stu-id="12c45-143">On the **Intercompany Inbox Transactions** page, select a line, and then choose an action, such as **Accept**, to process the line.</span></span>
3. <span data-ttu-id="12c45-144">På siden **Fullfør KI-innbokshandling** fyller du ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="12c45-144">On the **Complete IC Inbox Action** page, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="12c45-145">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="12c45-145">Choose the **OK** button.</span></span>  

<span data-ttu-id="12c45-146">For linjer som du behandlet med **Godta**-handlingen, bilag eller kladdelinjer vil bli opprettet i selskapet.</span><span class="sxs-lookup"><span data-stu-id="12c45-146">For lines that you processed with the **Accept** action, document or journal lines will be created in your company.</span></span> <span data-ttu-id="12c45-147">Åpne hvert bilag eller hver kladd, gjør de nødvendige endringene, og bokfør dem.</span><span class="sxs-lookup"><span data-stu-id="12c45-147">Open each document or journal, make any necessary changes, and then post them.</span></span>  

<span data-ttu-id="12c45-148">Linjene som du behandlet med **Gå tilbake til partner**-handlingen, vil bli flyttet til utboksen fra der du kan deretter sende dem til partneren.</span><span class="sxs-lookup"><span data-stu-id="12c45-148">Lines that you processed with the **Return to Partner** action will be moved to the outbox from where you can then send them to your partner.</span></span>

<span data-ttu-id="12c45-149">For linjer du behandlet med **Returnert av partner**-handlingen, må du nå bokføre en korreksjon av den opprinnelige transaksjonen du bokførte i selskapet ditt.</span><span class="sxs-lookup"><span data-stu-id="12c45-149">For lines that you processed with the **Returned by Partner** action, you must now post a correction to the original transaction that you posted in your company.</span></span>

## <a name="to-process-outgoing-intercompany-transactions"></a><span data-ttu-id="12c45-150">Slik behandler du utgående konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="12c45-150">To process outgoing intercompany transactions</span></span>  
<span data-ttu-id="12c45-151">Når du bokfører konserninterne kladder eller bilag eller sender en konsernintern bestillingsbekreftelse, sendes transaksjonene til den konserninterne utboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-151">When you post an intercompany journal or document, or send an intercompany order confirmation, the transactions are sent to your intercompany outbox.</span></span> <span data-ttu-id="12c45-152">Du må åpne utboksen og behandle dem for at de skal bli sendt videre til de konserninterne partnerne.</span><span class="sxs-lookup"><span data-stu-id="12c45-152">In order for them to be sent on to your intercompany partners, you must open the outbox and process them.</span></span>  

1.  <span data-ttu-id="12c45-153">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Konserninterne utgående transaksjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12c45-153">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Intercompany Outbox Transactions**, and then choose the related link.</span></span>  
2. <span data-ttu-id="12c45-154">På siden **Konserninterne utgående transaksjoner** velger du en linje og velger en handling som **Gå tilbake til innboks**, for å behandle linjen.</span><span class="sxs-lookup"><span data-stu-id="12c45-154">On the **Intercompany Outbox Transactions** page, select a line, and then choose an action, such as **Return to Inbox**, to process the line.</span></span>

<span data-ttu-id="12c45-155">Linjene som du behandlet med **Send til konsernintern partner**-handlingen, vil bli sendt til innboksen til den relevante partneren.</span><span class="sxs-lookup"><span data-stu-id="12c45-155">Lines that you processed with the **Send to Intercompany Partner** action will be sent to the relevant partner's inbox.</span></span>

<span data-ttu-id="12c45-156">Linjene som du behandlet med **Gå tilbake til innboks**-handlingen, vil bli flyttet til innboksen der du kan godta dem til å opprette bilag eller kladdelinjer i selskapet.</span><span class="sxs-lookup"><span data-stu-id="12c45-156">Lines that you processed with the **Return to Inbox** action will be moved to the inbox where you can then accept them to create documents or journal lines in your company.</span></span>  

<span data-ttu-id="12c45-157">For linjer du behandlet med **Avbryt**-handlingen, må du nå bokføre en korreksjon av den opprinnelige transaksjonen du bokførte i selskapet ditt.</span><span class="sxs-lookup"><span data-stu-id="12c45-157">For lines that you processed with the **Cancel** action, you must now post a correction to the original transaction that you posted in your company.</span></span>  

## <a name="to-recreate-intercompany-inbox-transactions"></a><span data-ttu-id="12c45-158">Slik oppretter du konserninterne innbokstransaksjoner på nytt:</span><span class="sxs-lookup"><span data-stu-id="12c45-158">To recreate intercompany inbox transactions</span></span>  
<span data-ttu-id="12c45-159">Noen ganger vil du kanskje opprette en transaksjon på nytt i innboksen eller utboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-159">Occasionally, you may want to re-create a transaction in the inbox or outbox.</span></span> <span data-ttu-id="12c45-160">Hvis du for eksempel godtok en transaksjon i innboksen, men deretter slettet bilaget eller kladden i stedet for å bokføre det/den, kan du opprette innboksposten på nytt og godta den på nytt.</span><span class="sxs-lookup"><span data-stu-id="12c45-160">For example, if you accepted a transaction in your inbox but then deleted the document or journal instead of posting it, you can re-create the inbox entry and accept it again.</span></span>  

<span data-ttu-id="12c45-161">Følgende fremgangsmåte beskriver hvordan du oppretter innbokstransaksjoner på nytt, men de samme trinnene gjelder også for utboksen.</span><span class="sxs-lookup"><span data-stu-id="12c45-161">The following procedure describes to re-create inbox transactions, but the same steps also apply to the outbox.</span></span>

  1.  <span data-ttu-id="12c45-162">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Håndterte inngående KI-transaksjoner**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="12c45-162">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Handled IC Inbox Transactions**, and then choose the related link.</span></span>  

  2.  <span data-ttu-id="12c45-163">På siden **Håndterte inngående KI-transaksjoner** velger du linjen med transaksjonen du vil opprette på nytt i innboksen, og velger deretter **Opprett inngående transaksjon på nytt**.</span><span class="sxs-lookup"><span data-stu-id="12c45-163">On the **Handled IC Inbox Transactions** page, select the line with the transaction that you want to re-create in the inbox, and then choose the **Re-create Inbox Transaction** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="12c45-164">Se også</span><span class="sxs-lookup"><span data-stu-id="12c45-164">See Also</span></span>
[<span data-ttu-id="12c45-165">Behandle konserninterne transaksjoner</span><span class="sxs-lookup"><span data-stu-id="12c45-165">Managing Intercompany Transactions</span></span>](intercompany-manage.md)  
[<span data-ttu-id="12c45-166">Finans</span><span class="sxs-lookup"><span data-stu-id="12c45-166">Finance</span></span>](finance.md)  
[<span data-ttu-id="12c45-167">Konfigurere finans</span><span class="sxs-lookup"><span data-stu-id="12c45-167">Setting Up Finance</span></span>](finance-setup-finance.md)  
[<span data-ttu-id="12c45-168">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="12c45-168">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="12c45-169">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="12c45-169">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>