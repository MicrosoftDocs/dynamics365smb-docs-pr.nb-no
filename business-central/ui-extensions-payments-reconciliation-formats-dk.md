---
title: Bruke utvidelsen Betalinger og avstemminger (Danmark) | Microsoft-dokumentasjon
description: Utvidelsen gjør det enkelt å eksportere filer som er formatert på forhånd for å oppfylle bankens krav til elektroniske innsendinger.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 13ef7eb6cdda472d68758e7e6ef5cb7d73d9fba4
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384077"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="e263d-103">Utvidelsen Betalinger og avstemminger (Danmark)</span><span class="sxs-lookup"><span data-stu-id="e263d-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="e263d-104">Betal fort og uten feil ved å eksportere filer som er formatert spesielt for utveksling med leverandører eller banken.</span><span class="sxs-lookup"><span data-stu-id="e263d-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="e263d-105">Filene øker hastigheten til betalings- og avstemmingsprosessen, og du unngår feil som kan skje når du angir informasjonen på bankens webområde manuelt.</span><span class="sxs-lookup"><span data-stu-id="e263d-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="e263d-106">Utvidelens støtter filformater for flere dansk banker.</span><span class="sxs-lookup"><span data-stu-id="e263d-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="e263d-107">Når du eksporterer betalingsinformasjon til en fil, sørger utvidelsen for at dataen får formatet som kreves av banken.</span><span class="sxs-lookup"><span data-stu-id="e263d-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="e263d-108">Formatene er blant annet Bankdata-V3, BEC, SDC og FIK, som brukes av mange forskjellige banker, og noen formater som er tilpasset bestemte banker, for eksempel Danske Bank og Nordea.</span><span class="sxs-lookup"><span data-stu-id="e263d-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="e263d-109">Utvidelsen inkluderer også noen formater for import og avstemming av bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="e263d-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="e263d-110">Hvis du vil bruke utvidelsen, må du vite formatet banken eller leverandøren krever.</span><span class="sxs-lookup"><span data-stu-id="e263d-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="e263d-111">Noen banker eller leverandører oppgir disse opplysningene på deres nettsteder. Det kan imidlertid være nødvendig å kontakte deres kundetjeneste for å få informasjonen.</span><span class="sxs-lookup"><span data-stu-id="e263d-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="e263d-112">Bankformater som støttes</span><span class="sxs-lookup"><span data-stu-id="e263d-112">Supported Bank Formats</span></span>
<span data-ttu-id="e263d-113">Utvidelsen kan bruke følgende filformater for betalingsfiler:</span><span class="sxs-lookup"><span data-stu-id="e263d-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="e263d-114">BANKDATA V3</span><span class="sxs-lookup"><span data-stu-id="e263d-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="e263d-115">BEC INDLAND</span><span class="sxs-lookup"><span data-stu-id="e263d-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="e263d-116">BEC CSV</span><span class="sxs-lookup"><span data-stu-id="e263d-116">BEC-CSV</span></span>  
* <span data-ttu-id="e263d-117">DANSKEBANK CMKV</span><span class="sxs-lookup"><span data-stu-id="e263d-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="e263d-118">DANSKEBANK CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="e263d-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="e263d-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="e263d-119">DANSKEBANK</span></span>  
* <span data-ttu-id="e263d-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="e263d-120">FIK71</span></span>  
* <span data-ttu-id="e263d-121">NORDEA-ERHVERV CSV</span><span class="sxs-lookup"><span data-stu-id="e263d-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="e263d-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="e263d-122">NORDEA</span></span>  
* <span data-ttu-id="e263d-123">NORDEA-UNITEL V3</span><span class="sxs-lookup"><span data-stu-id="e263d-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="e263d-124">SDC</span><span class="sxs-lookup"><span data-stu-id="e263d-124">SDC</span></span>  
* <span data-ttu-id="e263d-125">SDC CSV</span><span class="sxs-lookup"><span data-stu-id="e263d-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="e263d-126">Slik konfigurerer du filtypen</span><span class="sxs-lookup"><span data-stu-id="e263d-126">To set up the extension</span></span>

<span data-ttu-id="e263d-127">Det er noen trinn for å komme i gang.</span><span class="sxs-lookup"><span data-stu-id="e263d-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="e263d-128">Tillat eksport av betalingsdata.</span><span class="sxs-lookup"><span data-stu-id="e263d-128">Allow payment data exports.</span></span> <span data-ttu-id="e263d-129">For å beskytte dataene, er ikke dette lett tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e263d-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="e263d-130">Definere kjøps- og leverandørkonti slik at du ikke trenger eksterne bilagsnumre på fakturaer.</span><span class="sxs-lookup"><span data-stu-id="e263d-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="e263d-131">Du kan bruke referansenummeret for å referere til en bestemt faktura ved behov.</span><span class="sxs-lookup"><span data-stu-id="e263d-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="e263d-132">Angi betalingsmåten for hver leverandør.</span><span class="sxs-lookup"><span data-stu-id="e263d-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="e263d-133">Betalingsmåter definerer hvordan du betaler fakturaer fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="e263d-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="e263d-134">For eksempel i banken, kontant, med sjekk eller til konto.</span><span class="sxs-lookup"><span data-stu-id="e263d-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="e263d-135">Angi formatet som skal brukes for hver av bankkontiene dine.</span><span class="sxs-lookup"><span data-stu-id="e263d-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="e263d-136">Det kan for eksempel være NORDEA, DANSKEBANK, SDC og så videre.</span><span class="sxs-lookup"><span data-stu-id="e263d-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="e263d-137">I tillegg må du tilordne leverandørene til et innenlands **Bokføringsgruppe - firma** og en **Bokføringsgruppe - leverandør**.</span><span class="sxs-lookup"><span data-stu-id="e263d-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="e263d-138">Innstillingen land/region for leverandøren må være Danmark (dansk).</span><span class="sxs-lookup"><span data-stu-id="e263d-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="e263d-139">Hvis du vil ha mer informasjon, kan du se [Definere bokføringsgrupper](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="e263d-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-prod_short-to-export-payment-data"></a><span data-ttu-id="e263d-140">Tillat [!INCLUDE[prod_short](includes/prod_short.md)]å eksportere betalingsdata.</span><span class="sxs-lookup"><span data-stu-id="e263d-140">To allow [!INCLUDE[prod_short](includes/prod_short.md)] to export payment data</span></span>

1. <span data-ttu-id="e263d-141">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e263d-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e263d-142">Velg **Bank**-bunken på siden **Rediger betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="e263d-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="e263d-143">Velg avmerkingsboksen **Tillat betalingseksport**.</span><span class="sxs-lookup"><span data-stu-id="e263d-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="e263d-144">Angi betalingsmåten for en leverandør</span><span class="sxs-lookup"><span data-stu-id="e263d-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="e263d-145">Tabellen nedenfor viser kombinasjoner av FIK og GIRO betalingsmåter som støttes av [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="e263d-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[prod_short](includes/prod_short.md)] supports.</span></span>

|<span data-ttu-id="e263d-146">Kombinasjon</span><span class="sxs-lookup"><span data-stu-id="e263d-146">Combination</span></span>|<span data-ttu-id="e263d-147">Type 01</span><span class="sxs-lookup"><span data-stu-id="e263d-147">Type 01</span></span> | <span data-ttu-id="e263d-148">Type 04</span><span class="sxs-lookup"><span data-stu-id="e263d-148">Type 04</span></span> | <span data-ttu-id="e263d-149">Type 71</span><span class="sxs-lookup"><span data-stu-id="e263d-149">Type 71</span></span> | <span data-ttu-id="e263d-150">Type 73</span><span class="sxs-lookup"><span data-stu-id="e263d-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="e263d-151">Girokontonr. eller FIK kreditornr.?</span><span class="sxs-lookup"><span data-stu-id="e263d-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="e263d-152">Girokontonr.</span><span class="sxs-lookup"><span data-stu-id="e263d-152">Giro Account No.</span></span> | <span data-ttu-id="e263d-153">Girokontonr.</span><span class="sxs-lookup"><span data-stu-id="e263d-153">Giro Account No.</span></span> | <span data-ttu-id="e263d-154">FIK Kreditornr.</span><span class="sxs-lookup"><span data-stu-id="e263d-154">FIK Creditor No.</span></span> | <span data-ttu-id="e263d-155">FIK Kreditornr.</span><span class="sxs-lookup"><span data-stu-id="e263d-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="e263d-156">Tillater melding til mottaker?</span><span class="sxs-lookup"><span data-stu-id="e263d-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="e263d-157">Ja</span><span class="sxs-lookup"><span data-stu-id="e263d-157">Yes</span></span> |<span data-ttu-id="e263d-158">Nei</span><span class="sxs-lookup"><span data-stu-id="e263d-158">No</span></span> |<span data-ttu-id="e263d-159">Nei</span><span class="sxs-lookup"><span data-stu-id="e263d-159">No</span></span> | <span data-ttu-id="e263d-160">Ja</span><span class="sxs-lookup"><span data-stu-id="e263d-160">Yes</span></span> |
|<span data-ttu-id="e263d-161">Inneholder et betalingsreferansenummer?</span><span class="sxs-lookup"><span data-stu-id="e263d-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="e263d-162">Nei</span><span class="sxs-lookup"><span data-stu-id="e263d-162">No</span></span> | <span data-ttu-id="e263d-163">Ja, 16 sifre.</span><span class="sxs-lookup"><span data-stu-id="e263d-163">Yes, 16 digits.</span></span> | <span data-ttu-id="e263d-164">Ja, 15 sifre.</span><span class="sxs-lookup"><span data-stu-id="e263d-164">Yes, 15 digits.</span></span> | <span data-ttu-id="e263d-165">Nei</span><span class="sxs-lookup"><span data-stu-id="e263d-165">No</span></span>|

1. <span data-ttu-id="e263d-166">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e263d-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e263d-167">Åpne kortet, utvid **Betalinger**-kategorien, velg betalingsmåte i **Betalingsmåte** -feltet.</span><span class="sxs-lookup"><span data-stu-id="e263d-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="e263d-168">Avhengig av hva du velger, må du fylle ut andre felt.</span><span class="sxs-lookup"><span data-stu-id="e263d-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="e263d-169">Se i tabellen over for en beskrivelse av kombinasjonene.</span><span class="sxs-lookup"><span data-stu-id="e263d-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="e263d-170">Angi formatet som skal brukes for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="e263d-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="e263d-171">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e263d-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e263d-172">Åpne kortet for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="e263d-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="e263d-173">I **Betalingseksportformat**-feltet velger du formatet for eksportfilen.</span><span class="sxs-lookup"><span data-stu-id="e263d-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="e263d-174">Velge FIK eller Girobetalingsinformasjon for leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="e263d-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="e263d-175">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e263d-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="e263d-176">Velg leverandør.</span><span class="sxs-lookup"><span data-stu-id="e263d-176">Choose the vendor.</span></span> <span data-ttu-id="e263d-177">Husk at det må være en dansk leverandør med en adresse i Danmark.</span><span class="sxs-lookup"><span data-stu-id="e263d-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="e263d-178">Opprette en faktura.</span><span class="sxs-lookup"><span data-stu-id="e263d-178">Create an invoice.</span></span> <span data-ttu-id="e263d-179">Feltene **Betalingsmåte** og **Leverandørnummer** er fylt ut på grunnlag av innstillingene på leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="e263d-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="e263d-180">De kan endres.</span><span class="sxs-lookup"><span data-stu-id="e263d-180">You can change them if you want.</span></span>
4. <span data-ttu-id="e263d-181">I **Betalingsreferanse**-vinduet angir du nummeret med 15 sifre som står på leverandørens faktura.</span><span class="sxs-lookup"><span data-stu-id="e263d-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="e263d-182">Du trenger kun å legge inn de 11 siste sifrene i nummeret.</span><span class="sxs-lookup"><span data-stu-id="e263d-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[prod_short](includes/prod_short.md)] <span data-ttu-id="e263d-183">legger til fire nuller i begynnelsen av nummeret.</span><span class="sxs-lookup"><span data-stu-id="e263d-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="e263d-184">Bokfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e263d-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="e263d-185">Bruke utvidelsen til å eksportere betalingsdata</span><span class="sxs-lookup"><span data-stu-id="e263d-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="e263d-186">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e263d-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="e263d-187">Velg **Betalingskladdforslag - leverandør**.</span><span class="sxs-lookup"><span data-stu-id="e263d-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="e263d-188">Hvis du vil eksportere bare bestemte betalinger, må du bruke alternativene for å filtrere data.</span><span class="sxs-lookup"><span data-stu-id="e263d-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="e263d-189">Ved behov kan du legge til filtre for å eksportere kun bestemte betalinger.</span><span class="sxs-lookup"><span data-stu-id="e263d-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="e263d-190">I **Bankbetalingstype**-feltet velger du **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="e263d-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="e263d-191">Velg handlingen **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="e263d-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e263d-192">Se også</span><span class="sxs-lookup"><span data-stu-id="e263d-192">See also</span></span>

<span data-ttu-id="e263d-193">[Tilpasse Business Central for [!INCLUDE[prod_short](includes/prod_short.md)]med utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e263d-193">[Customizing Business Central for [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="e263d-194">Innkreve betalinger med SEPA direct debit</span><span class="sxs-lookup"><span data-stu-id="e263d-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="e263d-195">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="e263d-195">Working with General Journals</span></span>](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]