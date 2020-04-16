---
title: Lønnsdatadefinisjoner (NO) | Microsoft-dokumentasjon
description: Denne utvidelsen gjør det enkelt å utveksle data med lønnstjenesteleverandøren i Norge.
author: edupont04
manager: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: a294ca42a45792a465ae62e03662c79b19d73e74
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181003"
---
# <a name="the-payroll-data-definitions-no-extension"></a><span data-ttu-id="ff8de-103">Utvidelsen Lønnsdatadefinisjoner (NO)</span><span class="sxs-lookup"><span data-stu-id="ff8de-103">The Payroll Data Definitions (NO) Extension</span></span>

<span data-ttu-id="ff8de-104">Hvis bedriften din bruker Huldt & Lillevik Lønn - Visma-lønnstjenesteleverandørene i Norge kan utvidelsen **Lønnsdatadefinisjoner (NO)** hjelpe deg med å registrere lønnstransaksjoner fra disse leverandørene raskt og nøyaktig.</span><span class="sxs-lookup"><span data-stu-id="ff8de-104">If your business uses the Huldt & Lillevik Lønn - Visma payroll service provider in Norway, the **Payroll Data Definitions (NO)** extension can help you quickly and accurately register payroll transactions from these providers.</span></span> <span data-ttu-id="ff8de-105">Utvidelsen inneholder datautvekslingsdefinisjoner som lar deg lese inn lønnstransaksjoner i filer som leverandørene sender til deg.</span><span class="sxs-lookup"><span data-stu-id="ff8de-105">The extension contains data exchange definitions that enable you to import payroll transactions in files that the providers send to you.</span></span> <span data-ttu-id="ff8de-106">Hvis du vil ha mer informasjon om datautvekslingsdefinisjoner, kan du se [Definere datautvekslingsdefinisjoner](../../across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="ff8de-106">For more information about data exchange definitions, see [Set Up Data Exchange Definitions](../../across-how-to-set-up-data-exchange-definitions.md).</span></span>   

## <a name="getting-started"></a><span data-ttu-id="ff8de-107">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="ff8de-107">Getting Started</span></span>

<span data-ttu-id="ff8de-108">Det første trinnet er å tilordne typer lønnstransaksjoner til finanskontiene som du ønsker å bokføre dem til, i [!INCLUDE[prodshort](../../includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="ff8de-108">The first step is to map the types of payroll transactions to the general ledger accounts that you want to post them to in [!INCLUDE[prodshort](../../includes/prodshort.md)].</span></span> <span data-ttu-id="ff8de-109">Du kan for eksempel bokføre pensjonsbidrag til en konto med navnet Pensjon, og skatt betalt på bidragene til en konto med navnet Pensjonsskatt.</span><span class="sxs-lookup"><span data-stu-id="ff8de-109">For example, you might want to post retirement plan contributions to an account named Pension, and the taxes paid on the contributions to an account named Pension Tax.</span></span> <span data-ttu-id="ff8de-110">Dette skjer utenfor [!INCLUDE[prodshort](../../includes/prodshort.md)]. Du kan for eksempel bruke et Excel-regneark for å visualisere tilordningen.</span><span class="sxs-lookup"><span data-stu-id="ff8de-110">This happens outside of [!INCLUDE[prodshort](../../includes/prodshort.md)], for example, you might use an Excel worksheet to visualize the mapping.</span></span> <span data-ttu-id="ff8de-111">Arbeid med lønnstjenesteleverandøren for å være sikker på at filen de eksporterer, inneholder tilordningen.</span><span class="sxs-lookup"><span data-stu-id="ff8de-111">Work with the payroll service provider to ensure that the file they export contains the mapping.</span></span> <span data-ttu-id="ff8de-112">Vanligvis kan du finne informasjon om hvordan du konfigurerer eksportfiler på leverandørens nettsted.</span><span class="sxs-lookup"><span data-stu-id="ff8de-112">Typically, you can find information about how to configure export files on the provider's website.</span></span>  

<span data-ttu-id="ff8de-113">Når du har installert utvidelsen, er neste trinn å angi formatet for lønnsdatafilen fra lønnstjenesteleverandøren.</span><span class="sxs-lookup"><span data-stu-id="ff8de-113">After you install the extension, the next step is to specify the format for the payroll data file from the payroll service provider.</span></span> <span data-ttu-id="ff8de-114">Hvis du vil gjøre dette, kan du gå til **Finansoppsett**-siden og velge leverandøren i feltet **Importformat for lønnstransaksjon**.</span><span class="sxs-lookup"><span data-stu-id="ff8de-114">To do that, go to the **General Ledger Setup** page and choose the provider in the **Payroll Trans. Import Format** field.</span></span>  

## <a name="to-import-a-payroll-file"></a><span data-ttu-id="ff8de-115">Slik importerer du en lønnsfil</span><span class="sxs-lookup"><span data-stu-id="ff8de-115">To import a payroll file</span></span>

1.  <span data-ttu-id="ff8de-116">Velg ikonet ![Søk etter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søk etter side eller rapport"), angi **Finanskladder**, og velg deretter den relaterte koblingen.</span><span class="sxs-lookup"><span data-stu-id="ff8de-116">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>   
2.  <span data-ttu-id="ff8de-117">Velg kladden som skal brukes, og bruk deretter handlingen **Importer lønnsfil** til å importere datafilen fra lønnstjenesteleverandøren.</span><span class="sxs-lookup"><span data-stu-id="ff8de-117">Choose the journal to use, and then use the **Import Payroll File** action to import the data file from the payroll service provider.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ff8de-118">Se også</span><span class="sxs-lookup"><span data-stu-id="ff8de-118">See Also</span></span>
[<span data-ttu-id="ff8de-119">Funksjonalitet som er spesifikk for norske brukere</span><span class="sxs-lookup"><span data-stu-id="ff8de-119">Norway Local Functionality</span></span>](norway-local-functionality.md)   
