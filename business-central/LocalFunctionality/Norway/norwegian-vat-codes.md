---
title: Norske mva-koder
description: I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan mva-behandlingsinformasjon enkelt defineres ved hjelp av norske standard mva-koder..
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 78cb55d0c53db5b0a8252ffae6316a537be25459
ms.openlocfilehash: ab6d96312d4098a00c456386c4cfff2134f81a0a
ms.contentlocale: nb-no
ms.lasthandoff: 10/15/2018

---
# <a name="norwegian-vat-codes"></a><span data-ttu-id="bcc75-103">Norske mva-koder</span><span class="sxs-lookup"><span data-stu-id="bcc75-103">Norwegian VAT Codes</span></span>
<span data-ttu-id="bcc75-104">I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan mva-behandlingsinformasjon enkelt defineres ved hjelp av norske standard mva-koder..</span><span class="sxs-lookup"><span data-stu-id="bcc75-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], VAT processing information can be easily set up using standard Norwegian VAT codes.</span></span> <span data-ttu-id="bcc75-105">Tabellen nedenfor viser norske standard mva-koder.</span><span class="sxs-lookup"><span data-stu-id="bcc75-105">The following table shows the standard Norwegian VAT codes.</span></span>  

|<span data-ttu-id="bcc75-106">**Kode**</span><span class="sxs-lookup"><span data-stu-id="bcc75-106">**Code**</span></span>|<span data-ttu-id="bcc75-107">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="bcc75-107">**Description**</span></span>|  
|--------------|-------------------------------------------|  
|<span data-ttu-id="bcc75-108">**0**</span><span class="sxs-lookup"><span data-stu-id="bcc75-108">**0**</span></span>|<span data-ttu-id="bcc75-109">Salg - ingen mva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-109">Sale - No VAT</span></span>|  
|<span data-ttu-id="bcc75-110">**1**</span><span class="sxs-lookup"><span data-stu-id="bcc75-110">**1**</span></span>|<span data-ttu-id="bcc75-111">Innkjøp - mva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-111">Purchase - VAT</span></span>|  
|<span data-ttu-id="bcc75-112">**2**</span><span class="sxs-lookup"><span data-stu-id="bcc75-112">**2**</span></span>|<span data-ttu-id="bcc75-113">Innkjøp - mva. og inv.avg.</span><span class="sxs-lookup"><span data-stu-id="bcc75-113">Purchase - VAT and Inv. Tax</span></span>|  
|<span data-ttu-id="bcc75-114">**3**</span><span class="sxs-lookup"><span data-stu-id="bcc75-114">**3**</span></span>|<span data-ttu-id="bcc75-115">Salg - mva</span><span class="sxs-lookup"><span data-stu-id="bcc75-115">Sale - VAT</span></span>|  
|<span data-ttu-id="bcc75-116">**4**</span><span class="sxs-lookup"><span data-stu-id="bcc75-116">**4**</span></span>|<span data-ttu-id="bcc75-117">Innkjøp - mva. og 0% lageravg.</span><span class="sxs-lookup"><span data-stu-id="bcc75-117">Purchase - VAT and 0% Inv. Tax</span></span>|  
|<span data-ttu-id="bcc75-118">**11**</span><span class="sxs-lookup"><span data-stu-id="bcc75-118">**11**</span></span>|<span data-ttu-id="bcc75-119">Innkjøp - full mva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-119">Purchase - Full VAT</span></span>|  
|<span data-ttu-id="bcc75-120">**13**</span><span class="sxs-lookup"><span data-stu-id="bcc75-120">**13**</span></span>|<span data-ttu-id="bcc75-121">Salg - full mva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-121">Sale - Full VAT</span></span>|  
|<span data-ttu-id="bcc75-122">**14**</span><span class="sxs-lookup"><span data-stu-id="bcc75-122">**14**</span></span>|<span data-ttu-id="bcc75-123">Innkjøp - snudd avregning</span><span class="sxs-lookup"><span data-stu-id="bcc75-123">Purchase - Reverse Charge VAT</span></span>|  

<span data-ttu-id="bcc75-124">Vanligvis angir du feltet **Mva-bokf.gruppe - firma** og **Mva-bokf.gruppe - vare** når du angir mva-behandlingen.</span><span class="sxs-lookup"><span data-stu-id="bcc75-124">Typically, you enter the **VAT Bus. Posting Group** and **VAT Prod. Posting Group** fields when you specify the VAT handling process.</span></span>  

<span data-ttu-id="bcc75-125">Hvis du bare ønsker å bruke **Mva-kode**-feltet når du angir mva-behandlingen, kan du tilordne en mva-kode i **Mva-bokføringsoppsett**-tabellen, og bruke denne koden i stedet for bokføringsgruppefeltene.</span><span class="sxs-lookup"><span data-stu-id="bcc75-125">If you want to use only the **VAT Code** field when you specify the VAT handling process, you can assign a VAT code in the **VAT Posting Setup** table, and use this code instead of the posting group fields.</span></span> <span data-ttu-id="bcc75-126">Mva-koden kan brukes som en snarvei i **Mva-bokføringsoppsett**-tabellen, og du kan bruke norske standard mva-koder samtidig,.</span><span class="sxs-lookup"><span data-stu-id="bcc75-126">The VAT code can be used as a shortcut in the **VAT Posting Setup** table and at the same time, you can use standard Norwegian VAT codes.</span></span>  

## <a name="set-up-of-norwegian-vat-codes"></a><span data-ttu-id="bcc75-127">Definere norske mva-koder</span><span class="sxs-lookup"><span data-stu-id="bcc75-127">Set Up of Norwegian VAT Codes</span></span>  
<span data-ttu-id="bcc75-128">Du må opprette norske mva-koder i **Mva-koder**-vinduet.</span><span class="sxs-lookup"><span data-stu-id="bcc75-128">You must create the Norwegian VAT codes in the **VAT Codes** window.</span></span> <span data-ttu-id="bcc75-129">Deretter tilordner du mva-kodene i **Mva-bokføringsoppsett**-tabellen ved hjelp av **Mva-kode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="bcc75-129">Then assign the VAT codes in the **VAT Posting Setup** table, using the **VAT Code** field.</span></span> <span data-ttu-id="bcc75-130">Hvis du vil ha mer informasjon, kan du se [Bruke én mva-kode i kladder](how-to-use-one-vat-code-in-journals.md).</span><span class="sxs-lookup"><span data-stu-id="bcc75-130">For more information, see [Use One VAT Code in Journals](how-to-use-one-vat-code-in-journals.md).</span></span>  

## <a name="use-of-vat-codes"></a><span data-ttu-id="bcc75-131">Bruk av mva-koder</span><span class="sxs-lookup"><span data-stu-id="bcc75-131">Use of VAT Codes</span></span>  
<span data-ttu-id="bcc75-132">Når du angir en mva-kode, kan du velge informasjonen for mva-bokføringsoppsett for denne koden.</span><span class="sxs-lookup"><span data-stu-id="bcc75-132">When you specify a VAT code, you can select the VAT posting setup information for this code.</span></span> <span data-ttu-id="bcc75-133">Denne informasjonen brukes i kladder eller på dokumentlinjer når du angir mva-oppsettsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="bcc75-133">This information will be used in journals or on document lines when you specify the VAT setup information.</span></span> <span data-ttu-id="bcc75-134">Hvis du bruker mva-koden i disse tilfellene, brukes bokføringsgruppefeltene med opplysningene fra tilsvarende opplysninger for mva-bokføringsoppsett.</span><span class="sxs-lookup"><span data-stu-id="bcc75-134">If you use the VAT code in these cases, the posting group fields are used with the information from the corresponding VAT posting setup information.</span></span>  

<span data-ttu-id="bcc75-135">Eventuelt må du angi både feltet **Mva-bokf.gruppe - firma** og **Mva-bokf.gruppe - vare** når du velger eller endrer informasjon for mva-bokføringsoppsett på kladdelinjen eller dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="bcc75-135">Alternatively, you will have to specify both the **VAT Bus. Posting Group** and the **VAT Prod. Posting Group** fields when you select or change the VAT posting setup information on the journal line or the document line.</span></span>  

### <a name="example-using-vat-codes"></a><span data-ttu-id="bcc75-136">Eksempel: Bruke mva-koder</span><span class="sxs-lookup"><span data-stu-id="bcc75-136">Example: Using VAT Codes</span></span>  
<span data-ttu-id="bcc75-137">Det er to forskjellige forekomster av mva-bokføringsoppsett som kan brukes når du bokfører et salgsdokument.</span><span class="sxs-lookup"><span data-stu-id="bcc75-137">There are two different VAT posting setup instances that can be used when you post a sales document.</span></span>  

<span data-ttu-id="bcc75-138">Ett scenario for mva-bokføringsoppsett beregner 24 prosent mva for innenlandske kunder:</span><span class="sxs-lookup"><span data-stu-id="bcc75-138">One VAT posting setup scenario will calculate 24 percent VAT for domestic customers:</span></span>  

- <span data-ttu-id="bcc75-139">Mva-bokf.gruppe - firma: INNLAND</span><span class="sxs-lookup"><span data-stu-id="bcc75-139">VAT Bus. Posting Group: DOMESTIC</span></span>  
- <span data-ttu-id="bcc75-140">Mva-bokføringsgruppe - vare: NORMAL</span><span class="sxs-lookup"><span data-stu-id="bcc75-140">VAT Prod. Posting Group: NORMAL</span></span>  
- <span data-ttu-id="bcc75-141">Mva-%: 24</span><span class="sxs-lookup"><span data-stu-id="bcc75-141">VAT %: 24</span></span>  
- <span data-ttu-id="bcc75-142">Mva-kode: 3</span><span class="sxs-lookup"><span data-stu-id="bcc75-142">VAT Code: 3</span></span>  

<span data-ttu-id="bcc75-143">Ett scenario for mva-bokføringsoppsett vil beregne uten mva for internasjonale kunder:</span><span class="sxs-lookup"><span data-stu-id="bcc75-143">One VAT posting setup scenario will calculate without VAT for international customers:</span></span>  

- <span data-ttu-id="bcc75-144">MVA-bokf.gruppe – firma: EKSPORT</span><span class="sxs-lookup"><span data-stu-id="bcc75-144">VAT Bus. Posting Group: EXPORT</span></span>  
- <span data-ttu-id="bcc75-145">Mva-bokføringsgruppe - vare: NORMAL</span><span class="sxs-lookup"><span data-stu-id="bcc75-145">VAT Prod. Posting Group: NORMAL</span></span>  
- <span data-ttu-id="bcc75-146">Mva-%: 0</span><span class="sxs-lookup"><span data-stu-id="bcc75-146">VAT %: 0</span></span>  
- <span data-ttu-id="bcc75-147">Mva-kode: 1</span><span class="sxs-lookup"><span data-stu-id="bcc75-147">VAT Code: 1</span></span>  

<span data-ttu-id="bcc75-148">Vanligvis når du angir mva-oppsettsinformasjon på en kladdelinje, må feltet **Mva-bokf.gruppe - firma** angis til **INNENLANDS** og feltet **Mva-bokf.gruppe - vare** angis til **NORMAL** for å kunne velge det innenlandske oppsettet.</span><span class="sxs-lookup"><span data-stu-id="bcc75-148">Typically, when you specify the VAT setup information on a journal line, the **VAT Bus. Posting Group** field must be set to **DOMESTIC** and the **VAT Prod. Posting Group** field must be set to **NORMAL** in order to choose the domestic setup.</span></span>  

<span data-ttu-id="bcc75-149">Hvis du bruker norske standard mva-koder, kan du angi **Mva-kode 3** for den innenlandske mva-bokføringsoppsettsinformasjonen, og **Mva-kode 1** for den internasjonale mva-bokføringsoppsettsinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="bcc75-149">If you use standard Norwegian VAT codes, you could specify **VAT Code 3** for the domestic VAT posting setup information, and **VAT Code 1** for the international VAT posting setup information.</span></span> <span data-ttu-id="bcc75-150">Dermed kan du velge mellom mva-bokføringsoppsettsinformasjonen ved hjelp av bare ett felt og de kjente norske mva-standardkodene.</span><span class="sxs-lookup"><span data-stu-id="bcc75-150">This lets you choose between the VAT posting setup information using only one field and the familiar standard Norwegian VAT codes.</span></span>  

### <a name="example-restricting-the-use-of-vat-codes"></a><span data-ttu-id="bcc75-151">Eksempel: Begrense bruken av mva-koder</span><span class="sxs-lookup"><span data-stu-id="bcc75-151">Example: Restricting the Use of VAT Codes</span></span>  
<span data-ttu-id="bcc75-152">Standard norsk **mva-kode 3** brukes for salg inklusiv mva.</span><span class="sxs-lookup"><span data-stu-id="bcc75-152">The standard Norwegian **VAT Code 3** is used for sales inclusive of VAT.</span></span> <span data-ttu-id="bcc75-153">Med mindre du begrenser bruken av denne mva-koden, kan den brukes for både salg og kjøp i [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc75-153">Unless you restrict the use of this VAT code, it can be used for both sales and purchases in [!INCLUDE[d365fin](../../includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="bcc75-154">Du kan definere feltet **Bokføringstype** som et salg i **Finanskonto (analysevisning)**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="bcc75-154">You can define the **Gen. Posting Type** field as a sale in the **G/L Account (Analysis View)** table.</span></span> <span data-ttu-id="bcc75-155">Denne generelle bokføringstypen vil brukes sammen med **Mva-kode 3**.</span><span class="sxs-lookup"><span data-stu-id="bcc75-155">This general posting type will be used together with **VAT Code 3**.</span></span>  

<span data-ttu-id="bcc75-156">Bokføringstypen behandles på to måter, avhengig av verdien i feltet **Test bokføringstype**.</span><span class="sxs-lookup"><span data-stu-id="bcc75-156">The general posting type will be handled in two ways, depending on the value in the **Test Gen. Posting Type** field.</span></span>  

|<span data-ttu-id="bcc75-157">Alternativ</span><span class="sxs-lookup"><span data-stu-id="bcc75-157">Option</span></span>|<span data-ttu-id="bcc75-158">Description</span><span class="sxs-lookup"><span data-stu-id="bcc75-158">Description</span></span>|  
|-----------------------------------------|-------------------------------------------|  
|<span data-ttu-id="bcc75-159">**Obligatorisk**</span><span class="sxs-lookup"><span data-stu-id="bcc75-159">**Mandatory**</span></span>|<span data-ttu-id="bcc75-160">Bokføringstypen settes automatisk til **Salg** på kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="bcc75-160">The general posting type is automatically set to **Sale** on journal lines.</span></span> <span data-ttu-id="bcc75-161">Før du bokfører, verifiserer [!INCLUDE[d365fin](../../includes/d365fin_md.md)] om bokføringstypen er angitt, men det er ingen kontroll av om feltet settes til **Salg**.</span><span class="sxs-lookup"><span data-stu-id="bcc75-161">Before you post, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] verifies if the general posting type is specified, but there is no verification if the field is set to **Sale**.</span></span><br /><br /> <span data-ttu-id="bcc75-162">**Mva-kode 3** kan brukes for både salgs- og kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcc75-162">**VAT Code 3** can be used for both sales and purchase documents.</span></span>|  
|<span data-ttu-id="bcc75-163">**Samme**</span><span class="sxs-lookup"><span data-stu-id="bcc75-163">**Same**</span></span>|<span data-ttu-id="bcc75-164">Bokføringstypen settes automatisk til **Salg** på kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="bcc75-164">The general posting type is automatically set to **Sale** on journal lines.</span></span> <span data-ttu-id="bcc75-165">Før du bokfører verifiserer [!INCLUDE[d365fin](../../includes/d365fin_md.md)] om bokføringstypen er satt til **Salg**.</span><span class="sxs-lookup"><span data-stu-id="bcc75-165">Before you post, [!INCLUDE[d365fin](../../includes/d365fin_md.md)] verifies if the general posting type is set to **Sale**.</span></span><br /><br /> <span data-ttu-id="bcc75-166">**Mva-kode 3** kan brukes for salgsdokumenter, men ikke på kjøpsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="bcc75-166">**VAT Code 3** can be used for sales documents, but not on purchase documents.</span></span><br /><br /> <span data-ttu-id="bcc75-167">Dette gjør det mulig å begrense bruken av mva-koder til forhåndsdefinerte bokføringstyper.</span><span class="sxs-lookup"><span data-stu-id="bcc75-167">This enables you to restrict the use of VAT codes to predefined general posting types.</span></span>|  

## <a name="see-also"></a><span data-ttu-id="bcc75-168">Se også</span><span class="sxs-lookup"><span data-stu-id="bcc75-168">See Also</span></span>  
 [<span data-ttu-id="bcc75-169">Norsk mva-rapportering</span><span class="sxs-lookup"><span data-stu-id="bcc75-169">Norwegian VAT Reporting</span></span>](norwegian-vat-reporting.md)

