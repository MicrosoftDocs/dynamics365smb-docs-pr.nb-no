---
title: "Bruke profiler til å klassifisere kontakter"
description: "Konfigurere profilspørreskjemaer til å klassifisere forretningskontaktene"
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, profiles
ms.author: edupont
ms.date: 05/09/2018
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 00cfce8b467040a4de419c1b59a258c0eacf0b9a
ms.contentlocale: nb-no
ms.lasthandoff: 05/15/2018

---

# <a name="use-profile-questionnaires-to-classify-business-contacts"></a><span data-ttu-id="9666b-103">Bruke profilspørreskjemaer til å klassifisere forretningskontakter</span><span class="sxs-lookup"><span data-stu-id="9666b-103">Use Profile Questionnaires to Classify Business Contacts</span></span>
<span data-ttu-id="9666b-104">Du kan definere profilspørreskjemaer du vil bruke når du angir opplysninger om profiler for kontaktene.</span><span class="sxs-lookup"><span data-stu-id="9666b-104">You can set up profile questionnaires that you want to use when entering information about your contacts' profiles.</span></span> <span data-ttu-id="9666b-105">Du kan definere de ulike spørsmålene du vil spørre kontaktene om, i hvert enkelt spørreskjema.</span><span class="sxs-lookup"><span data-stu-id="9666b-105">Within each questionnaire, you can set up the different questions you intend to ask your contacts.</span></span>  

<span data-ttu-id="9666b-106">Du kan også kjøre spørreskjemaet for å besvare noen av spørsmålene automatisk basert på data om kontakter, kunder eller leverandører.</span><span class="sxs-lookup"><span data-stu-id="9666b-106">You can also run the questionnaire to answer some of the questions based on contact, customer, or vendor data automatically.</span></span>  

## <a name="to-add-a-profile-questionnaire"></a><span data-ttu-id="9666b-107">Slik legger du til et profilspørreskjema:</span><span class="sxs-lookup"><span data-stu-id="9666b-107">To add a profile questionnaire</span></span>
1.  <span data-ttu-id="9666b-108">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Søk etter side eller rapport"), angi **Spørreskjemaoppsett.**, og velg den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="9666b-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Questionnaire Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9666b-109">I fanen **Hjem** under **Ny** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9666b-109">On the **Home** tab, in the **New** group, choose **New**.</span></span>  
3.  <span data-ttu-id="9666b-110">Fyll ut feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="9666b-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-add-questions-to-a-profile-questionnaire"></a><span data-ttu-id="9666b-111">Slik legger du til spørsmål i et profilspørreskjema:</span><span class="sxs-lookup"><span data-stu-id="9666b-111">To add questions to a profile questionnaire</span></span>
1.  <span data-ttu-id="9666b-112">Velg det aktuelle profilspørreskjemaet, og velg **Rediger spørreskjemaoppsett** under **Prosess** i fanebladet **Hjem**.</span><span class="sxs-lookup"><span data-stu-id="9666b-112">Choose the relevant profile questionnaire, and then on the **Home** tab, in the **Process** group, choose **Edit Questionnaire Setup**.</span></span>  
2.  <span data-ttu-id="9666b-113">På den første tomme linjen, i **Type**-feltet, velger du **Spørsmål** og skriver inn spørsmålet i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9666b-113">On the first empty line, in the **Type** field, choose **Question** and type your question in the **Description** field.</span></span> <span data-ttu-id="9666b-114">Fyll ut de andre feltene på denne linjen.</span><span class="sxs-lookup"><span data-stu-id="9666b-114">Fill in the other fields on this line.</span></span>  
3.  <span data-ttu-id="9666b-115">På den neste tomme linjen, i **Type**-feltet, velger du **Svar** og skriver inn svaret i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9666b-115">On the next empty line, in the **Type** field, choose **Answer** and type your answer in the **Description** field.</span></span>  
4.  <span data-ttu-id="9666b-116">Velg prioriteten i **Prioritet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9666b-116">In the **Priority** field, select the priority.</span></span> <span data-ttu-id="9666b-117">Definer et punktområde i feltene **Fra verdi** og **Til verdi**.</span><span class="sxs-lookup"><span data-stu-id="9666b-117">In the **From Value** and **To Value** fields, define a point range.</span></span> <span data-ttu-id="9666b-118">Kontakter som får poeng innenfor det definerte intervallet, vil motta svaret.</span><span class="sxs-lookup"><span data-stu-id="9666b-118">Contacts that receive points within the defined range will get the answer.</span></span>  

<span data-ttu-id="9666b-119">Gjenta disse trinnene hvis du vil angi alle spørsmål og svar i profilspørreskjemaene.</span><span class="sxs-lookup"><span data-stu-id="9666b-119">Repeat these steps to enter all the questions and answers within the profile questionnaire.</span></span>

<span data-ttu-id="9666b-120">Når du har opprettet et spørreskjema, må du opprette kontaktrangeringer for å klassifisere kontaktene dine.</span><span class="sxs-lookup"><span data-stu-id="9666b-120">After you have created a questionnaire, you must create contact ratings to classify your contacts.</span></span> <span data-ttu-id="9666b-121">Du kan også lage spørsmål som rangeres automatisk basert på informasjon på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="9666b-121">You can also set up questions that are rated automatically based on information in the contact card.</span></span>  

> [!NOTE]
> <span data-ttu-id="9666b-122">Hvis du angir et spørsmål som skal besvares automatisk, velger du <STRONG>Linje</STRONG>, og deretter velger du <STRONG>Spørsmålsopplysninger</STRONG> for å angi hvilke kriterier som skal brukes til å besvare spørsmålet.</span><span class="sxs-lookup"><span data-stu-id="9666b-122">If you enter a question that is automatically answered, choose <STRONG>Line</STRONG>, and then choose <STRONG>Question Details</STRONG>, to enter the criteria to automatically answer the question.</span></span>

## <a name="the-automatic-classification-of-contacts"></a><span data-ttu-id="9666b-123">Automatisk klassifisering av kontakter</span><span class="sxs-lookup"><span data-stu-id="9666b-123">The Automatic Classification of Contacts</span></span>
<span data-ttu-id="9666b-124">Du kan klassifisere kontaktene automatisk etter opplysninger om kunde, leverandør og kontakt. Det gjør du ved å definere automatisk besvarte profilspørsmål i vinduet **Profilspørreskjema - oppsett**.</span><span class="sxs-lookup"><span data-stu-id="9666b-124">You can automatically classify your contacts according to customer, vendor, and contact information, by setting up automatically answered profile questions in the **Profile Questionnaire Setup** window.</span></span>  

> [!NOTE]
> <span data-ttu-id="9666b-125">Det er bare kontakter som er registrert som kunder og leverandører, som kan tilordnes en klassifisering som er basert på henholdsvis kunde- og leverandørdata.</span><span class="sxs-lookup"><span data-stu-id="9666b-125">Only contacts that are recorded as customers can be assigned a classification based on customer data and only contacts that are recorded as vendors can be assigned a classification based on vendor data.</span></span> <span data-ttu-id="9666b-126">Den automatiske klassifiseringen blir ikke automatisk oppdatert.</span><span class="sxs-lookup"><span data-stu-id="9666b-126">The automatic classification is not updated automatically.</span></span> <span data-ttu-id="9666b-127">Du bør derfor oppdatere profilspørreskjemaene etter at du har oppdatert kunde-, leverandør- eller kontaktdataene som skjemaene er basert på.</span><span class="sxs-lookup"><span data-stu-id="9666b-127">Consequently, you may want to update the profile questionnaires, after you have updated the customer, vendor or contact data they are based on.</span></span>  

<span data-ttu-id="9666b-128">Etter at du har definert automatisk besvaring av profilspørsmål, tilordner [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk riktige svar for en kontakt hvis du tilordner profilspørreskjemaet som inneholder disse spørsmålene, til kontakten.</span><span class="sxs-lookup"><span data-stu-id="9666b-128">After you have set up automatically answered profile questions, if you assign the profile questionnaire containing these questions to a contact, [!INCLUDE[d365fin](includes/d365fin_md.md)] will automatically assign the right answers for the contact.</span></span>  

## <a name="example"></a><span data-ttu-id="9666b-129">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9666b-129">Example</span></span>
<span data-ttu-id="9666b-130">Du kan klassifisere kontakter etter hvor mye de handler:</span><span class="sxs-lookup"><span data-stu-id="9666b-130">You can classify your contacts according to how much they bought from you:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9666b-131"><strong>Svar</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-131"><strong>Answer</strong></span></span></th>
<th><span data-ttu-id="9666b-132"><strong>Gjelder</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-132"><strong>Applies to</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9666b-133">A</span><span class="sxs-lookup"><span data-stu-id="9666b-133">A</span></span></p></td>
<td><p><span data-ttu-id="9666b-134">kontakter som kjøpte for NOK 500 000 eller mer</span><span class="sxs-lookup"><span data-stu-id="9666b-134">contacts who bought for 500,000 LCY or more</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9666b-135">B</span><span class="sxs-lookup"><span data-stu-id="9666b-135">B</span></span></p></td>
<td><p><span data-ttu-id="9666b-136">kontakter som kjøpte for NOK 100 000 til 499 999</span><span class="sxs-lookup"><span data-stu-id="9666b-136">contacts who bought for 100,000 up to 499,999 LCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9666b-137">C</span><span class="sxs-lookup"><span data-stu-id="9666b-137">C</span></span></p></td>
<td><p><span data-ttu-id="9666b-138">kontakter som kjøpte for NOK 99 999 eller mindre</span><span class="sxs-lookup"><span data-stu-id="9666b-138">contacts who bought for 99,999 LCY or less</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9666b-139">Du gjør dette ved å fylle ut vinduet **Profilspørreskjema - oppsett**:</span><span class="sxs-lookup"><span data-stu-id="9666b-139">To do this, fill in the **Profile Questionnaire Setup** window as follows:</span></span>


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
<th><span data-ttu-id="9666b-140"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-140"><strong>Type</strong></span></span></th>
<th><span data-ttu-id="9666b-141"><strong>Beskrivelse</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-141"><strong>Description</strong></span></span></th>
<th><span data-ttu-id="9666b-142"><strong>Automatisk klassifisering</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-142"><strong>Automatic Classification</strong></span></span></th>
<th><span data-ttu-id="9666b-143"><strong>Fra verdi</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-143"><strong>From Value</strong></span></span></th>
<th><span data-ttu-id="9666b-144"><strong>Til verdi</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-144"><strong>To Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9666b-145">Spørsmål</span><span class="sxs-lookup"><span data-stu-id="9666b-145">Question</span></span></p></td>
<td><p><span data-ttu-id="9666b-146">ABC-klassifisering</span><span class="sxs-lookup"><span data-stu-id="9666b-146">ABC Classification</span></span></p></td>
<td><p><span data-ttu-id="9666b-147">Klikk for å sette en hake</span><span class="sxs-lookup"><span data-stu-id="9666b-147">Click to insert a check mark</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9666b-148">Svar</span><span class="sxs-lookup"><span data-stu-id="9666b-148">Answer</span></span></p></td>
<td><p><span data-ttu-id="9666b-149">A</span><span class="sxs-lookup"><span data-stu-id="9666b-149">A</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9666b-150">500 000</span><span class="sxs-lookup"><span data-stu-id="9666b-150">500,000</span></span></p></td>
<td><p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9666b-151">Svar</span><span class="sxs-lookup"><span data-stu-id="9666b-151">Answer</span></span></p></td>
<td><p><span data-ttu-id="9666b-152">B</span><span class="sxs-lookup"><span data-stu-id="9666b-152">B</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9666b-153">100 000</span><span class="sxs-lookup"><span data-stu-id="9666b-153">100,000</span></span></p></td>
<td><p><span data-ttu-id="9666b-154">499,999</span><span class="sxs-lookup"><span data-stu-id="9666b-154">499,999</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9666b-155">Svar</span><span class="sxs-lookup"><span data-stu-id="9666b-155">Answer</span></span></p></td>
<td><p><span data-ttu-id="9666b-156">L</span><span class="sxs-lookup"><span data-stu-id="9666b-156">C</span></span></p></td>
<td><p> </p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="9666b-157">99 999</span><span class="sxs-lookup"><span data-stu-id="9666b-157">99,999</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9666b-158">Fyll deretter ut vinduet **Profilspørsmålsopplysninger** på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="9666b-158">Then fill in the **Profile Question Details** window as follows:</span></span>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9666b-159"><strong>Felt</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-159"><strong>Field</strong></span></span></th>
<th><span data-ttu-id="9666b-160"><strong>Verdi</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-160"><strong>Value</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9666b-161"><strong>Kundeklassifiseringsfelt</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-161"><strong>Customer Classification Field</strong></span></span></td>
<td><span data-ttu-id="9666b-162"><emphasis>Salg (NOK)</emphasis></span><span class="sxs-lookup"><span data-stu-id="9666b-162"><emphasis>Sales (LCY)</emphasis></span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9666b-163"><strong>Klassifiseringsmåte</strong></span><span class="sxs-lookup"><span data-stu-id="9666b-163"><strong>Classification Method</strong></span></span></td>
<td><span data-ttu-id="9666b-164"><emphasis>Definert verdi</emphasis></span><span class="sxs-lookup"><span data-stu-id="9666b-164"><emphasis>Defined Value</emphasis></span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9666b-165">Når du tilordner profilspørreskjemaet som inneholder dette spørsmålet til en kontakt, angir programmet automatisk riktig svar for denne kontakten på profillinjene på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="9666b-165">When you assign the profile questionnaire containing this question to a contact, the program automatically enters the relevant answer for this contact on the profile lines of the contact card.</span></span>

## <a name="see-also"></a><span data-ttu-id="9666b-166">Se også</span><span class="sxs-lookup"><span data-stu-id="9666b-166">See Also</span></span>
[<span data-ttu-id="9666b-167">Opprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="9666b-167">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="9666b-168">Opprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="9666b-168">Create Contact Persons</span></span>](marketing-how-create-contact-persons.md)  
[<span data-ttu-id="9666b-169">Opprette kontaktselskaper</span><span class="sxs-lookup"><span data-stu-id="9666b-169">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  

