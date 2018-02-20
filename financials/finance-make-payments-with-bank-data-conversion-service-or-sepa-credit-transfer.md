---
title: "Betale med tjenesten for bankdatakonvertering eller SEPA-kredittoverføring | Microsoft-dokumentasjon"
description: "Behandle betalinger til leverandører i -vinduet ved å eksportere en fil sammen med betalingsinformasjonen fra kladdelinjene."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/17/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d9388a99585eea4e9e229a2f47982f9f690e3001
ms.contentlocale: nb-no
ms.lasthandoff: 01/30/2018

---
# <a name="making-payments-with-bank-data-conversion-service-or-sepa-credit-transfer"></a><span data-ttu-id="8f158-103">Betale med tjenesten for bankdatakonvertering eller SEPA-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="8f158-103">Making Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>
<span data-ttu-id="8f158-104">Nå kan du behandle betalinger til leverandører i vinduet **Betalingskladd** ved å eksportere en fil sammen med betalingsinformasjonen fra kladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="8f158-104">In the **Payment Journal** window, you can process payments to your vendors by exporting a file together with the payment information from the journal lines.</span></span> <span data-ttu-id="8f158-105">Du kan deretter laste opp filen til nettbanken der de relaterte pengeoverføringene behandles.</span><span class="sxs-lookup"><span data-stu-id="8f158-105">You can then upload the file to your electronic bank where the related money transfers are processed.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="8f158-106"> støtter formatet for SEPA-kreidttoverføring, men andre formater for elektroniske betalinger kan være tilgjengelige i ditt land/region.</span><span class="sxs-lookup"><span data-stu-id="8f158-106"> supports the SEPA Credit Transfer format, but in your country/region, other formats for electronic payments may be available.</span></span>   

 <span data-ttu-id="8f158-107">Hvis du vil gjøre det mulig å foreta SEPA-kredittoverføringer, må du først opprette en bankkonto, en leverandør og finanskladden som utbetalingskladden er basert på.</span><span class="sxs-lookup"><span data-stu-id="8f158-107">To enable SEPA credit transfers, you must first set up a bank account, a vendor, and the general journal batch that the payment journal is based on.</span></span> <span data-ttu-id="8f158-108">Deretter gjør du klar betalinger til leverandører ved å fylle ut vinduet **Betalingskladd** med forfalte betalinger som har angitte bokføringsdatoer.</span><span class="sxs-lookup"><span data-stu-id="8f158-108">You then prepare payments to vendors by automatically filling the **Payment Journal** window with due payments with specified posting dates.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="8f158-109">Når du har bekreftet at betalingene er behandlet av banken, kan du begynne å bokføre utbetalingskladdelinjene.</span><span class="sxs-lookup"><span data-stu-id="8f158-109">When you have verified that the payments are successfully processed by the bank, you can proceed to post the payment journal lines.</span></span>  

 <span data-ttu-id="8f158-110">Tabellen nedenfor beskriver en sekvens av oppgaver, og har koblinger til emnene som beskriver dem.</span><span class="sxs-lookup"><span data-stu-id="8f158-110">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="8f158-111">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="8f158-111">**To**</span></span>|<span data-ttu-id="8f158-112">**Se**</span><span class="sxs-lookup"><span data-stu-id="8f158-112">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="8f158-113">Aktiverer tjenesten for bankdatakonvertering for å konvertere en kontoutdragsfil til et format du kan importere, eller konvertere den eksporterte betalingsfilen til formatet som banken krever.</span><span class="sxs-lookup"><span data-stu-id="8f158-113">Activate the Bank Data Conversion Service feature to have any bank statement file converted to a format that you can import or to have your exported payment files converted to the format that your bank requires.</span></span>|[<span data-ttu-id="8f158-114">Konfigurere tjeneste for konvertering av bankdata</span><span class="sxs-lookup"><span data-stu-id="8f158-114">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)|  
|<span data-ttu-id="8f158-115">Definere en bankkonto, leverandør og en utbetalingskladd for SEPA-kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="8f158-115">Set up a bank account, a vendor, and a payment journal for SEPA credit transfer.</span></span>|[<span data-ttu-id="8f158-116">Definere SEPA-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="8f158-116">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)|  
|<span data-ttu-id="8f158-117">Fylle ut utbetalingskladden med linjer for utestående leverandørfordringer, med mulighet til å sette inn bokføringsdatoer basert på forfallsdatoen til de relaterte kjøpsdokumentene.</span><span class="sxs-lookup"><span data-stu-id="8f158-117">Fill the payment journal with lines for due payments to vendors, with the option to insert posting dates based on the due date of the related purchase documents.</span></span>|[<span data-ttu-id="8f158-118">Administrere skyldige beløp</span><span class="sxs-lookup"><span data-stu-id="8f158-118">Managing Payables</span></span>](payables-manage-payables.md)|  
|<span data-ttu-id="8f158-119">Eksportere utbetalingskladdelinjer til en fil i SEPA-kredittoverføringsformatet.</span><span class="sxs-lookup"><span data-stu-id="8f158-119">Export payment journal lines to a file in the SEPA Credit Transfer format.</span></span>|[<span data-ttu-id="8f158-120">Eksportere betalinger til en bankfil</span><span class="sxs-lookup"><span data-stu-id="8f158-120">Export Payments to a Bank File</span></span>](payables-how-export-payments-bank-file.md)|  
|<span data-ttu-id="8f158-121">Bokfør betalingene når den elektroniske betalingen er behandlet av banken.</span><span class="sxs-lookup"><span data-stu-id="8f158-121">When the electronic payment is successfully processed by the bank, post the payments.</span></span>|[<span data-ttu-id="8f158-122">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="8f158-122">Working with General Journals</span></span>](ui-work-general-journals.md)|  

## <a name="see-also"></a><span data-ttu-id="8f158-123">Se også</span><span class="sxs-lookup"><span data-stu-id="8f158-123">See Also</span></span>  
[<span data-ttu-id="8f158-124">Konfigurere tjeneste for konvertering av bankdata</span><span class="sxs-lookup"><span data-stu-id="8f158-124">Set Up the Bank Data Conversion Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="8f158-125">Definere SEPA-kredittoverføring</span><span class="sxs-lookup"><span data-stu-id="8f158-125">Set Up SEPA Credit Transfer</span></span>](finance-how-to-set-up-sepa-credit-transfer.md)  
<span data-ttu-id="8f158-126">[Administrere skyldige beløp](payables-manage-payables.md) </span><span class="sxs-lookup"><span data-stu-id="8f158-126">[Managing Payables](payables-manage-payables.md) </span></span>  
[<span data-ttu-id="8f158-127">Arbeide med finanskladder</span><span class="sxs-lookup"><span data-stu-id="8f158-127">Working with General Journals</span></span>](ui-work-general-journals.md)  
[<span data-ttu-id="8f158-128">Innkreve betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="8f158-128">Collecting Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)   

