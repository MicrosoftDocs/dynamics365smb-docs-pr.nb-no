---
title: Bruke utvidelsen Betalinger og avstemminger (Danmark) | Microsoft-dokumentasjon
description: Utvidelsen gjør det enkelt å eksportere filer som er formatert på forhånd for å oppfylle bankens krav til elektroniske innsendinger.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, bank, formats
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: 1afd60dc4c9c86b476c3c2c80974ce805b19a4ca
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912324"
---
# <a name="the-payments-and-reconciliations-dk-extension"></a><span data-ttu-id="2c4f0-103">Utvidelsen Betalinger og avstemminger (Danmark)</span><span class="sxs-lookup"><span data-stu-id="2c4f0-103">The Payments and Reconciliations (DK) Extension</span></span>

<span data-ttu-id="2c4f0-104">Betal fort og uten feil ved å eksportere filer som er formatert spesielt for utveksling med leverandører eller banken.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-104">Make fast, error-free payments by exporting files that are formatted specifically for exchanges with your vendor or bank.</span></span> <span data-ttu-id="2c4f0-105">Filene øker hastigheten til betalings- og avstemmingsprosessen, og du unngår feil som kan skje når du angir informasjonen på bankens webområde manuelt.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-105">These files speed up the payment and reconciliation processes, and eliminate errors that can happen when you manually enter the information on a bank website.</span></span>  

<span data-ttu-id="2c4f0-106">Utvidelens støtter filformater for flere dansk banker.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-106">This extension supports file formats for several Danish banks.</span></span> <span data-ttu-id="2c4f0-107">Når du eksporterer betalingsinformasjon til en fil, sørger utvidelsen for at dataen får formatet som kreves av banken.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-107">When you export payment information to a file, the extension packages the data into the format that your bank requires.</span></span> <span data-ttu-id="2c4f0-108">Formatene er blant annet Bankdata-V3, BEC, SDC og FIK, som brukes av mange forskjellige banker, og noen formater som er tilpasset bestemte banker, for eksempel Danske Bank og Nordea.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-108">For example, the formats include Bankdata-V3, BEC, SDC, and FIK, which many different banks use, and some that are more specialized for certain banks, for example, Danske Bank and Nordea.</span></span> <span data-ttu-id="2c4f0-109">Utvidelsen inkluderer også noen formater for import og avstemming av bankkontoutdrag.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-109">The extension also includes some formats for importing and reconciling bank statements.</span></span>  

> [!Note]
> <span data-ttu-id="2c4f0-110">Hvis du vil bruke utvidelsen, må du vite formatet banken eller leverandøren krever.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-110">To use the extension, you must know the format that your bank or vendor requires.</span></span> <span data-ttu-id="2c4f0-111">Noen banker eller leverandører oppgir disse opplysningene på deres nettsteder. Det kan imidlertid være nødvendig å kontakte deres kundetjeneste for å få informasjonen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-111">Some banks or vendors provide this information on their websites; however, you might need to contact their customer service to get the information.</span></span>  

## <a name="supported-bank-formats"></a><span data-ttu-id="2c4f0-112">Bankformater som støttes</span><span class="sxs-lookup"><span data-stu-id="2c4f0-112">Supported Bank Formats</span></span>
<span data-ttu-id="2c4f0-113">Utvidelsen kan bruke følgende filformater for betalingsfiler:</span><span class="sxs-lookup"><span data-stu-id="2c4f0-113">This extension can apply the following file formats for payment files:</span></span>  

* <span data-ttu-id="2c4f0-114">BANKDATA V3</span><span class="sxs-lookup"><span data-stu-id="2c4f0-114">BANKDATA-V3</span></span>  
* <span data-ttu-id="2c4f0-115">BEC INDLAND</span><span class="sxs-lookup"><span data-stu-id="2c4f0-115">BEC-INDLAND</span></span>  
* <span data-ttu-id="2c4f0-116">BEC CSV</span><span class="sxs-lookup"><span data-stu-id="2c4f0-116">BEC-CSV</span></span>  
* <span data-ttu-id="2c4f0-117">DANSKEBANK CMKV</span><span class="sxs-lookup"><span data-stu-id="2c4f0-117">DANSKEBANK-CMKV</span></span>  
* <span data-ttu-id="2c4f0-118">DANSKEBANK CMKXKSX</span><span class="sxs-lookup"><span data-stu-id="2c4f0-118">DANSKEBANK-CMKXKSX</span></span>  
* <span data-ttu-id="2c4f0-119">DANSKEBANK</span><span class="sxs-lookup"><span data-stu-id="2c4f0-119">DANSKEBANK</span></span>  
* <span data-ttu-id="2c4f0-120">FIK71</span><span class="sxs-lookup"><span data-stu-id="2c4f0-120">FIK71</span></span>  
* <span data-ttu-id="2c4f0-121">NORDEA-ERHVERV CSV</span><span class="sxs-lookup"><span data-stu-id="2c4f0-121">NORDEA-ERHVERV-CSV</span></span>  
* <span data-ttu-id="2c4f0-122">NORDEA</span><span class="sxs-lookup"><span data-stu-id="2c4f0-122">NORDEA</span></span>  
* <span data-ttu-id="2c4f0-123">NORDEA-UNITEL V3</span><span class="sxs-lookup"><span data-stu-id="2c4f0-123">NORDEA-UNITEL-V3</span></span>  
* <span data-ttu-id="2c4f0-124">SDC</span><span class="sxs-lookup"><span data-stu-id="2c4f0-124">SDC</span></span>  
* <span data-ttu-id="2c4f0-125">SDC CSV</span><span class="sxs-lookup"><span data-stu-id="2c4f0-125">SDC-CSV</span></span>  

## <a name="to-set-up-the-extension"></a><span data-ttu-id="2c4f0-126">Slik konfigurerer du filtypen</span><span class="sxs-lookup"><span data-stu-id="2c4f0-126">To set up the extension</span></span>

<span data-ttu-id="2c4f0-127">Det er noen trinn for å komme i gang.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-127">There are a few steps to get started.</span></span>  

* <span data-ttu-id="2c4f0-128">Tillat eksport av betalingsdata.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-128">Allow payment data exports.</span></span> <span data-ttu-id="2c4f0-129">For å beskytte dataene, er ikke dette lett tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-129">To help protect your data, this is not readily available.</span></span>  
* <span data-ttu-id="2c4f0-130">Definere kjøps- og leverandørkonti slik at du ikke trenger eksterne bilagsnumre på fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-130">Set up purchase and payables so that you do not require external document numbers on invoices.</span></span> <span data-ttu-id="2c4f0-131">Du kan bruke referansenummeret for å referere til en bestemt faktura ved behov.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-131">If needed, you can use the reference number to refer to a specific invoice.</span></span>  
* <span data-ttu-id="2c4f0-132">Angi betalingsmåten for hver leverandør.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-132">Specify the payment method for each vendor.</span></span> <span data-ttu-id="2c4f0-133">Betalingsmåter definerer hvordan du betaler fakturaer fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-133">Payment methods define how you pay invoices from the vendor.</span></span> <span data-ttu-id="2c4f0-134">For eksempel i banken, kontant, med sjekk eller til konto.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-134">For example, Bank, Cash, Check, or Account.</span></span>  
* <span data-ttu-id="2c4f0-135">Angi formatet som skal brukes for hver av bankkontiene dine.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-135">Specify the type of format to use for each of your bank accounts.</span></span> <span data-ttu-id="2c4f0-136">Det kan for eksempel være NORDEA, DANSKEBANK, SDC og så videre.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-136">For example, NORDEA, DANSKEBANK, SDC, and so on.</span></span>  

<span data-ttu-id="2c4f0-137">I tillegg må du tilordne leverandørene til et innenlands **Bokføringsgruppe - firma** og en **Bokføringsgruppe - leverandør**.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-137">Additionally, you must assign vendors to a domestic **Gen. Bus. Posting Group** and a **Vendor Posting Group**.</span></span> <span data-ttu-id="2c4f0-138">Innstillingen land/region for leverandøren må være Danmark (dansk).</span><span class="sxs-lookup"><span data-stu-id="2c4f0-138">The Country/Region setting for the vendor must be Denmark (DK).</span></span> <span data-ttu-id="2c4f0-139">Hvis du vil ha mer informasjon, kan du se [Definere bokføringsgrupper](finance-posting-groups.md).</span><span class="sxs-lookup"><span data-stu-id="2c4f0-139">For more information, see [Setting Up Posting Groups](finance-posting-groups.md).</span></span>  

### <a name="to-allow-d365fin-to-export-payment-data"></a><span data-ttu-id="2c4f0-140">Tillat [!INCLUDE[d365fin](includes/d365fin_md.md)]å eksportere betalingsdata.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-140">To allow [!INCLUDE[d365fin](includes/d365fin_md.md)] to export payment data</span></span>

1. <span data-ttu-id="2c4f0-141">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladd**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-141">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2c4f0-142">Velg **Bank**-bunken på siden **Rediger betalingskladd**.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-142">On the **Edit Payment Journal** page, choose the **Bank** batch.</span></span>  
3. <span data-ttu-id="2c4f0-143">Velg avmerkingsboksen **Tillat betalingseksport**.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-143">Choose the **Allow Payment Export** check box.</span></span>  

### <a name="to-specify-a-payment-method-for-a-vendor"></a><span data-ttu-id="2c4f0-144">Angi betalingsmåten for en leverandør</span><span class="sxs-lookup"><span data-stu-id="2c4f0-144">To specify a payment method for a vendor</span></span>

<span data-ttu-id="2c4f0-145">Tabellen nedenfor viser kombinasjoner av FIK og GIRO betalingsmåter som støttes av [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="2c4f0-145">The following table shows the combinations of FIK and GIRO payment methods that [!INCLUDE[d365fin](includes/d365fin_md.md)] supports.</span></span>

|<span data-ttu-id="2c4f0-146">Kombinasjon</span><span class="sxs-lookup"><span data-stu-id="2c4f0-146">Combination</span></span>|<span data-ttu-id="2c4f0-147">Type 01</span><span class="sxs-lookup"><span data-stu-id="2c4f0-147">Type 01</span></span> | <span data-ttu-id="2c4f0-148">Type 04</span><span class="sxs-lookup"><span data-stu-id="2c4f0-148">Type 04</span></span> | <span data-ttu-id="2c4f0-149">Type 71</span><span class="sxs-lookup"><span data-stu-id="2c4f0-149">Type 71</span></span> | <span data-ttu-id="2c4f0-150">Type 73</span><span class="sxs-lookup"><span data-stu-id="2c4f0-150">Type 73</span></span> |
|----|--------|---------|---------|---------|
|<span data-ttu-id="2c4f0-151">Girokontonr. eller FIK kreditornr.?</span><span class="sxs-lookup"><span data-stu-id="2c4f0-151">Giro Account No. or FIK Creditor No.?</span></span> | <span data-ttu-id="2c4f0-152">Girokontonr.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-152">Giro Account No.</span></span> | <span data-ttu-id="2c4f0-153">Girokontonr.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-153">Giro Account No.</span></span> | <span data-ttu-id="2c4f0-154">FIK Kreditornr.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-154">FIK Creditor No.</span></span> | <span data-ttu-id="2c4f0-155">FIK Kreditornr.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-155">FIK Creditor No.</span></span>|
|<span data-ttu-id="2c4f0-156">Tillater melding til mottaker?</span><span class="sxs-lookup"><span data-stu-id="2c4f0-156">Allows Message to Recipient?</span></span> | <span data-ttu-id="2c4f0-157">Ja</span><span class="sxs-lookup"><span data-stu-id="2c4f0-157">Yes</span></span> |<span data-ttu-id="2c4f0-158">Nei</span><span class="sxs-lookup"><span data-stu-id="2c4f0-158">No</span></span> |<span data-ttu-id="2c4f0-159">Nei</span><span class="sxs-lookup"><span data-stu-id="2c4f0-159">No</span></span> | <span data-ttu-id="2c4f0-160">Ja</span><span class="sxs-lookup"><span data-stu-id="2c4f0-160">Yes</span></span> |
|<span data-ttu-id="2c4f0-161">Inneholder et betalingsreferansenummer?</span><span class="sxs-lookup"><span data-stu-id="2c4f0-161">Contains Payment Reference number?</span></span> | <span data-ttu-id="2c4f0-162">Nei</span><span class="sxs-lookup"><span data-stu-id="2c4f0-162">No</span></span> | <span data-ttu-id="2c4f0-163">Ja, 16 sifre.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-163">Yes, 16 digits.</span></span> | <span data-ttu-id="2c4f0-164">Ja, 15 sifre.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-164">Yes, 15 digits.</span></span> | <span data-ttu-id="2c4f0-165">Nei</span><span class="sxs-lookup"><span data-stu-id="2c4f0-165">No</span></span>|

1. <span data-ttu-id="2c4f0-166">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Leverandører**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-166">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2c4f0-167">Åpne kortet, utvid **Betalinger**-kategorien, velg betalingsmåte i **Betalingsmåte** -feltet.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-167">Open the card, expand the **Payments** tab, in the **Payment Method** field choose the payment method.</span></span>  
3. <span data-ttu-id="2c4f0-168">Avhengig av hva du velger, må du fylle ut andre felt.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-168">Depending on your selection, you must complete other fields.</span></span> <span data-ttu-id="2c4f0-169">Se i tabellen over for en beskrivelse av kombinasjonene.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-169">See the table above for a description of the combinations.</span></span>  

### <a name="to-specify-the-format-to-use-for-a-bank-account"></a><span data-ttu-id="2c4f0-170">Angi formatet som skal brukes for en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-170">To specify the format to use for a bank account</span></span>

1. <span data-ttu-id="2c4f0-171">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Bankkonti**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-171">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Bank Accounts**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2c4f0-172">Åpne kortet for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-172">Open the card for the bank account.</span></span>  
3. <span data-ttu-id="2c4f0-173">I **Betalingseksportformat**-feltet velger du formatet for eksportfilen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-173">In the **Payment Export Format** field, choose the format for your export file.</span></span>  

## <a name="choosing-the-fik-or-giro-payment-information-for-vendor-invoices"></a><span data-ttu-id="2c4f0-174">Velge FIK eller Girobetalingsinformasjon for leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="2c4f0-174">Choosing the FIK or Giro payment information for vendor invoices</span></span>

1. <span data-ttu-id="2c4f0-175">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Kjøpsfakturaer**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-175">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="2c4f0-176">Velg leverandør.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-176">Choose the vendor.</span></span> <span data-ttu-id="2c4f0-177">Husk at det må være en dansk leverandør med en adresse i Danmark.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-177">Remember, this must be a Danish vendor with an address in Denmark.</span></span>
3. <span data-ttu-id="2c4f0-178">Opprette en faktura.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-178">Create an invoice.</span></span> <span data-ttu-id="2c4f0-179">Feltene **Betalingsmåte** og **Leverandørnummer** er fylt ut på grunnlag av innstillingene på leverandørkortet.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-179">The **Payment Method** and **Vendor Number** fields are filled in based on settings on the Vendor card.</span></span> <span data-ttu-id="2c4f0-180">De kan endres.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-180">You can change them if you want.</span></span>
4. <span data-ttu-id="2c4f0-181">I **Betalingsreferanse**-vinduet angir du nummeret med 15 sifre som står på leverandørens faktura.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-181">In the **Payment Reference** field, enter the 15-digit number from the vendor invoice.</span></span>  

    > [!Tip]
    > <span data-ttu-id="2c4f0-182">Du trenger kun å legge inn de 11 siste sifrene i nummeret.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-182">You only have to add the last 11 digits of the number.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="2c4f0-183">legger til fire nuller i begynnelsen av nummeret.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-183">will add four zeros to the beginning of the number.</span></span>  

5. <span data-ttu-id="2c4f0-184">Bokfør fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-184">Post the invoice.</span></span>

## <a name="to-use-the-extension-to-export-payment-data"></a><span data-ttu-id="2c4f0-185">Bruke utvidelsen til å eksportere betalingsdata</span><span class="sxs-lookup"><span data-stu-id="2c4f0-185">To use the extension to export payment data</span></span>

1. <span data-ttu-id="2c4f0-186">Velg ikonet ![lyspære som åpner Fortell meg-funksjonen](media/ui-search/search_small.png "Fortell hva du vil gjøre"), angi **Utbetalingskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-186">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2c4f0-187">Velg **Betalingskladdforslag - leverandør**.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-187">Choose the **Suggest Vendor Payment Journals** action.</span></span>  

    > [!Tip]
    > <span data-ttu-id="2c4f0-188">Hvis du vil eksportere bare bestemte betalinger, må du bruke alternativene for å filtrere data.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-188">If you want to export only specific payments, use the options for filtering the data.</span></span>  

3. <span data-ttu-id="2c4f0-189">Ved behov kan du legge til filtre for å eksportere kun bestemte betalinger.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-189">If needed, you can add filters to export only specific payments.</span></span>  
4. <span data-ttu-id="2c4f0-190">I **Bankbetalingstype**-feltet velger du **Elektronisk betaling**.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-190">In the **Bank Payment Type** field, choose **Electronic Payment**.</span></span>  
5. <span data-ttu-id="2c4f0-191">Velg handlingen **Eksporter**.</span><span class="sxs-lookup"><span data-stu-id="2c4f0-191">Choose the **Export** action.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2c4f0-192">Se også</span><span class="sxs-lookup"><span data-stu-id="2c4f0-192">See also</span></span>

<span data-ttu-id="2c4f0-193">[Tilpasse Business Central for [!INCLUDE[d365fin](includes/d365fin_md.md)]med utvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2c4f0-193">[Customizing Business Central for [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="2c4f0-194">Innkreve betalinger med SEPA direct debit</span><span class="sxs-lookup"><span data-stu-id="2c4f0-194">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="2c4f0-195">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="2c4f0-195">Working with General Journals</span></span>](ui-work-general-journals.md)  
