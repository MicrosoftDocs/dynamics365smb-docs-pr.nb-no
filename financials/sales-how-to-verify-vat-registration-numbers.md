---
title: Bekrefte organisasjonsnumre | Microsoft-dokumentasjon
description: "Du kan bruke en EU-webtjeneste til å bekrefte at organisasjonsnumre du angir på kunde-, leverandør- eller kontaktkort, er gyldige."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: nb-no
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="e543b-103">Bekrefte organisasjonsnumre</span><span class="sxs-lookup"><span data-stu-id="e543b-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="e543b-104">Du kan bruke en EU-webtjeneste til å bekrefte at organisasjonsnumre du angir på kunde-, leverandør- eller kontaktkort, er gyldige.</span><span class="sxs-lookup"><span data-stu-id="e543b-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="e543b-105">Når du endrer feltet **Organisasjonsnummer** på et kort der verdien i feltet **Lands-/regionskode** er et EU-land/område, logges det nye organisasjonsnummeret og bruker-ID-en din i vinduet **Organisasjonsnummerlogg**.</span><span class="sxs-lookup"><span data-stu-id="e543b-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="e543b-106">Du bekrefter et organisasjonsnummer ved å klikke knappen **Bekreft registreringsnummer** i vinduet **Organisasjonsnummerlogg**.</span><span class="sxs-lookup"><span data-stu-id="e543b-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="e543b-107">Det opprettes en ny linje hver gang du bruker funksjonen for bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="e543b-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="e543b-108">Hvis nummeret kan bekreftes, inneholder **Status**-feltet **Gyldig**.</span><span class="sxs-lookup"><span data-stu-id="e543b-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="e543b-109">Hvis nummeret ikke kan bekreftes, inneholder **Status**-feltet **Ugyldig**, og du må deretter endre nummeret i **Organisasjonsnummer**-feltet på kortet og starte funksjonen for bekreftelse på nytt.</span><span class="sxs-lookup"><span data-stu-id="e543b-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="e543b-110">Nettadressen for standard webtjeneste er definert i feltet **URL-adresse for validering av organisasjonsnummer** i vinduet **Finansoppsett**.</span><span class="sxs-lookup"><span data-stu-id="e543b-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="e543b-111">I tabellen **Format for organisasjonsnr.** kan du endre de ulike formatene for organisasjonsnummer som brukerne kan angi i feltet **Organisasjonsnr.**, for hvert landregion.</span><span class="sxs-lookup"><span data-stu-id="e543b-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="e543b-112">Denne webtjenesten bruker HTTP-protokollen, som betyr at data som overføres via tjenesten, ikke er kryptert.</span><span class="sxs-lookup"><span data-stu-id="e543b-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e543b-113">Denne tjenesten er en del av et omfattende EU-nettverk av nasjonale mva-registre, og du kan oppleve nedetid som Microsoft ikke er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="e543b-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="e543b-114">Slik bekrefter du et organisasjonsnummer fra et kundekort:</span><span class="sxs-lookup"><span data-stu-id="e543b-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="e543b-115">Nedenfor beskrives hvordan du bekrefter et organisasjonsnummer for en kunde.</span><span class="sxs-lookup"><span data-stu-id="e543b-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="e543b-116">Trinnene er de samme for en leverandør og en kontakt.</span><span class="sxs-lookup"><span data-stu-id="e543b-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="e543b-117">Velg ikonet ![Søk etter side eller rapport](media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Kunder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="e543b-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="e543b-118">Åpne kortet til en kunde der du vil bekrefte organisasjonsnummeret.</span><span class="sxs-lookup"><span data-stu-id="e543b-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="e543b-119">Feltet **Lands-områdekode** på kundekortet må inneholde EU-land-område.</span><span class="sxs-lookup"><span data-stu-id="e543b-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="e543b-120">Velg DrillDown-knappen ved siden av **Organisasjonsnr.**-feltet i hurtigfanen **Fakturering**.</span><span class="sxs-lookup"><span data-stu-id="e543b-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="e543b-121">Vinduet **Organisasjonsnummerlogg** åpnes og viser én linje der **Status**-feltet inneholder **Ikke bekreftet**.</span><span class="sxs-lookup"><span data-stu-id="e543b-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="e543b-122">Velg handlingen **Bekreft registreringsnummer**.</span><span class="sxs-lookup"><span data-stu-id="e543b-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="e543b-123">Det opprettes en ny linje der **Status**-feltet inneholder enten **Gyldig** eller **Ugyldig**.</span><span class="sxs-lookup"><span data-stu-id="e543b-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="e543b-124">Hvis **Status**-feltet inneholder **Ugyldig**, endrer du nummeret i **Organisasjonsnummer**-feltet på kortet, og deretter gjentar du trinn 3 og 4.</span><span class="sxs-lookup"><span data-stu-id="e543b-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e543b-125">Se også</span><span class="sxs-lookup"><span data-stu-id="e543b-125">See Also</span></span>  
[<span data-ttu-id="e543b-126">Finans</span><span class="sxs-lookup"><span data-stu-id="e543b-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="e543b-127">Registrere nye kunder</span><span class="sxs-lookup"><span data-stu-id="e543b-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="e543b-128">Registrere nye leverandører</span><span class="sxs-lookup"><span data-stu-id="e543b-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="e543b-129">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="e543b-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

