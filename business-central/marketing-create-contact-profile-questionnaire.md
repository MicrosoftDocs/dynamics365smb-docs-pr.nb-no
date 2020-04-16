---
title: Bruke profiler til å klassifisere kontakter
description: Konfigurere profilspørreskjemaer til å klassifisere forretningskontaktene
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 04/01/2020
ms.openlocfilehash: 9cf4817cd85951f193ffadbcd3e7ebc971bcca36
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181583"
---
# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="1106f-103">Bruke profilspørreskjemaer til å klassifisere forretningskontakter</span><span class="sxs-lookup"><span data-stu-id="1106f-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="1106f-104">Du kan definere profilspørreskjemaer du vil bruke når du angir opplysninger om profiler for kontaktene.</span><span class="sxs-lookup"><span data-stu-id="1106f-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="1106f-105">Du kan definere de ulike spørsmålene du vil spørre kontaktene om, i hvert enkelt spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="1106f-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="1106f-106">Du kan også kjøre spørreskjemaet for å besvare noen av spørsmålene automatisk basert på data om kontakter, kunder eller leverandører.</span><span class="sxs-lookup"><span data-stu-id="1106f-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="1106f-107">Slik legger du til et profilspørreskjema:</span><span class="sxs-lookup"><span data-stu-id="1106f-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="1106f-108">Velg ikonet ![Lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Spørreskjemaoppsett**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="1106f-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1106f-109">Velg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="1106f-109">Choose the **New** Action.</span></span>  
3.  <span data-ttu-id="1106f-110">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="1106f-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="1106f-111">Slik legger du til spørsmål i et profilspørreskjema:</span><span class="sxs-lookup"><span data-stu-id="1106f-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="1106f-112">Velg det aktuelle profilspørreskjemaet, og velg handlingen **Rediger spørreskjemaoppsett**.</span><span class="sxs-lookup"><span data-stu-id="1106f-112">Choose the relevant profile questionnaire, and then choose the **Edit Questionnaire Setup** action.</span></span>  
2.  <span data-ttu-id="1106f-113">På den første tomme linjen, i **Type**-feltet, velger du **Spørsmål** og skriver inn spørsmålet i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1106f-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="1106f-114">Fyll ut de andre feltene på denne linjen.</span><span class="sxs-lookup"><span data-stu-id="1106f-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="1106f-115">På den neste tomme linjen, i **Type**-feltet, velger du **Svar** og skriver inn svaret i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1106f-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="1106f-116">Velg prioriteten i **Prioritet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1106f-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="1106f-117">Definer et punktområde i feltene **Fra verdi** og **Til verdi**.</span><span class="sxs-lookup"><span data-stu-id="1106f-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="1106f-118">Kontakter som får poeng innenfor det definerte intervallet, vil motta svaret.</span><span class="sxs-lookup"><span data-stu-id="1106f-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="1106f-119">Gjenta disse trinnene hvis du vil angi alle spørsmål og svar i profilspørreskjemaene.</span><span class="sxs-lookup"><span data-stu-id="1106f-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="1106f-120">Når du har opprettet et spørreskjema, må du opprette kontaktrangeringer for å klassifisere kontaktene dine.</span><span class="sxs-lookup"><span data-stu-id="1106f-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="1106f-121">Du kan også lage spørsmål som rangeres automatisk basert på informasjon på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="1106f-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="1106f-122">Hvis du angir et spørsmål som skal besvares automatisk, velger du <STRONG>Linje</STRONG>, og deretter velger du <STRONG>Spørsmålsopplysninger</STRONG> for å angi hvilke kriterier som skal brukes til å besvare spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="1106f-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="1106f-123">Automatisk klassifisering av kontakter</span><span class="sxs-lookup"><span data-stu-id="1106f-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="1106f-124">Du kan klassifisere kontaktene automatisk etter opplysninger om kunde, leverandør og kontakt. Det gjør du ved å definere automatisk besvarte profilspørsmål på siden **Profilspørreskjema - oppsett**.</span><span class="sxs-lookup"><span data-stu-id="1106f-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions on the **Profile Questionnaire Setup** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="1106f-125">Det er bare kontakter som er registrert som kunder og leverandører, som kan tilordnes en klassifisering som er basert på henholdsvis kunde- og leverandørdata.</span><span class="sxs-lookup"><span data-stu-id="1106f-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="1106f-126">Den automatiske klassifiseringen blir ikke automatisk oppdatert.</span><span class="sxs-lookup"><span data-stu-id="1106f-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="1106f-127">Du bør derfor oppdatere profilspørreskjemaene etter at du har oppdatert kunde-, leverandør- eller kontaktdataene som skjemaene er basert på.</span><span class="sxs-lookup"><span data-stu-id="1106f-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="1106f-128">Etter at du har definert automatisk besvaring av profilspørsmål, tilordner [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk riktige svar for en kontakt hvis du tilordner profilspørreskjemaet som inneholder disse spørsmålene, til kontakten.</span><span class="sxs-lookup"><span data-stu-id="1106f-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="1106f-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="1106f-129">Example</span></span>
<span data-ttu-id="1106f-130">Du kan klassifisere kontakter etter hvor mye de handler:</span><span class="sxs-lookup"><span data-stu-id="1106f-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1106f-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="1106f-132"><strong>Gjelder</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1106f-133">A</span><span class="sxs-lookup"><span data-stu-id="1106f-133">A</span></span></p></td>
<td><p><span data-ttu-id="1106f-134">kontakter som kjøpte for NOK 500 000 eller mer</span><span class="sxs-lookup"><span data-stu-id="1106f-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1106f-135">B</span><span class="sxs-lookup"><span data-stu-id="1106f-135">B</span></span></p></td>
<td><p><span data-ttu-id="1106f-136">kontakter som kjøpte for NOK 100 000 til 499 999</span><span class="sxs-lookup"><span data-stu-id="1106f-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1106f-137">U</span><span class="sxs-lookup"><span data-stu-id="1106f-137">C</span></span></p></td>
<td><p><span data-ttu-id="1106f-138">kontakter som kjøpte for NOK 99 999 eller mindre</span><span class="sxs-lookup"><span data-stu-id="1106f-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1106f-139">Du gjør dette ved å fylle ut siden **Profilspørreskjema - oppsett** slik:</span><span class="sxs-lookup"><span data-stu-id="1106f-139">To do this, fill on the **Profile Questionnaire Setup** page as follows:</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1106f-140"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="1106f-141"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="1106f-142"><strong>Automatisk klassifisering</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="1106f-143"><strong>Fra verdi</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="1106f-144"><strong>Til verdi</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1106f-145">Spørsmål</span><span class="sxs-lookup"><span data-stu-id="1106f-145">Question</span></span></p></td>
<td><p><span data-ttu-id="1106f-146">ABC-klassifisering</span><span class="sxs-lookup"><span data-stu-id="1106f-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="1106f-147">Klikk for å sette en hake</span><span class="sxs-lookup"><span data-stu-id="1106f-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1106f-148">Svar</span><span class="sxs-lookup"><span data-stu-id="1106f-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="1106f-149">A</span><span class="sxs-lookup"><span data-stu-id="1106f-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1106f-150">500,000</span><span class="sxs-lookup"><span data-stu-id="1106f-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1106f-151">Svar</span><span class="sxs-lookup"><span data-stu-id="1106f-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="1106f-152">B</span><span class="sxs-lookup"><span data-stu-id="1106f-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1106f-153">100,000</span><span class="sxs-lookup"><span data-stu-id="1106f-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="1106f-154">499,999</span><span class="sxs-lookup"><span data-stu-id="1106f-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1106f-155">Svar</span><span class="sxs-lookup"><span data-stu-id="1106f-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="1106f-156">U</span><span class="sxs-lookup"><span data-stu-id="1106f-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="1106f-157">99,999</span><span class="sxs-lookup"><span data-stu-id="1106f-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1106f-158">Fyll deretter ut siden **Profilspørsmålsopplysninger** på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="1106f-158">Then fill on the **Profile Question Details** page as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1106f-159"><strong>Felt</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="1106f-160"><strong>Verdi</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1106f-161"><strong>Kundeklassifiseringsfelt</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="1106f-162"><emphasis>Salg (NOK)</emphasis></span><span class="sxs-lookup"><span data-stu-id="1106f-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1106f-163"><strong>Klassifiseringsmåte</strong></span><span class="sxs-lookup"><span data-stu-id="1106f-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="1106f-164"><emphasis>Definert verdi</emphasis></span><span class="sxs-lookup"><span data-stu-id="1106f-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1106f-165">Når du tilordner profilspørreskjemaet som inneholder dette spørsmålet, til en kontakt, angir programmet automatisk riktig svar for denne kontakten på profillinjene på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="1106f-165">When you assign the profile questionnaire containing this question to a contact, application automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="1106f-166">Se også</span><span class="sxs-lookup"><span data-stu-id="1106f-166">See Also</span></span>
[<span data-ttu-id="1106f-167">Opprette kontakter</span><span class="sxs-lookup"><span data-stu-id="1106f-167">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
