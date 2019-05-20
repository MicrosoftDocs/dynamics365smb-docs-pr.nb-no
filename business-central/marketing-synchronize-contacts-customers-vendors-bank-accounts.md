---
title: Synkronisere kontakter med kunder og leverandører | Microsoft-dokumentasjon
description: Du kan koble eller synkronisere kontaktinformasjon for kontakter som også er kunder, leverandører eller bankkonti, så du oppdaterer informasjon bare på ett sted.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, CRM, integration, couple
ms.date: 04/01/2019
ms.author: edupont
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: 96ec0862cf93cf9b0bf240ef65bc7ff79b3ccfb5
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/29/2019
ms.locfileid: "1242275"
---
# <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="211bf-103">Synkronisere kontakter med kunder, leverandører og bankkonti</span><span class="sxs-lookup"><span data-stu-id="211bf-103">Synchronizing Contacts With Customers, Vendors, and Bank Accounts</span></span>
<span data-ttu-id="211bf-104">Hvis en del av kontaktene også er kunder, leverandører eller bankkonti, kan du synkronisere kontaktinformasjonen med relatert kunde, leverandør eller bankkonto.</span><span class="sxs-lookup"><span data-stu-id="211bf-104">If some of your contacts are also customers, vendors, or bank accounts, you can synchronize the contact information with the related customer, vendor, or bank account.</span></span> <span data-ttu-id="211bf-105">Synkronisering gjør at informasjon som er felles mellom kontakter og kunder, leverandører eller bankkonto, er den samme.</span><span class="sxs-lookup"><span data-stu-id="211bf-105">Synchronization makes information that is common between contacts and customers, vendors, or bank account the same.</span></span>  

## <a name="different-ways-to-synchronize-contacts-with-customers-vendors-and-bank-accounts"></a><span data-ttu-id="211bf-106">Ulike metoder for å synkronisere kontakter med kunder, leverandører og bankkonti</span><span class="sxs-lookup"><span data-stu-id="211bf-106">Different Ways to Synchronize Contacts with Customers, Vendors and Bank Accounts</span></span>
<span data-ttu-id="211bf-107">Du kan synkronisere kontaktene med kunder, leverandører eller bankkonti ved hjelp av tre metoder:</span><span class="sxs-lookup"><span data-stu-id="211bf-107">You can synchronize your contacts with customers, vendors, or bank accounts by three methods:</span></span>

* <span data-ttu-id="211bf-108">Koble kontakter til eksisterende kunder, leverandører og/eller bankkonti fra kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="211bf-108">Link contacts with existing customers, vendors, or bank accounts from the contact card.</span></span> <span data-ttu-id="211bf-109">Hvis du vil ha mer informasjon, kan du se [Knytte kontakter til kunder, leverandører og bankkonti](marketing-how-link-contact.md).</span><span class="sxs-lookup"><span data-stu-id="211bf-109">For more information, see [Link Contacts With Customers, Vendors, and Bank Accounts](marketing-how-link-contact.md).</span></span>
* <span data-ttu-id="211bf-110">Opprett kunder, leverandører eller bankkonti fra kontakten.</span><span class="sxs-lookup"><span data-stu-id="211bf-110">Create customers, vendors, or bank accounts from the contact.</span></span> <span data-ttu-id="211bf-111">Hvis du vil ha mer informasjon, kan du se [Opprette en kunde, leverandør eller bankkonto fra en kontakt](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="211bf-111">For more information, see [Create a Customer, Vendor, or Bank Account From a Contact](marketing-how-create-contacts-new-customers-vendors-bank-accounts.md).</span></span>
* <span data-ttu-id="211bf-112">Opprett kontakter fra kunder, leverandører eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="211bf-112">Create contacts from customers, vendors or bank accounts.</span></span> <span data-ttu-id="211bf-113">Hvis du vil ha mer informasjon, kan du se [Opprette en selskapskontakt fra kunde, leverandør eller bankkonto](marketing-how-create-contact-companies.md).</span><span class="sxs-lookup"><span data-stu-id="211bf-113">For more information, see [Create a company contact from a customer, vendor, or bank account](marketing-how-create-contact-companies.md).</span></span>

## <a name="consequences-of-synchronization"></a><span data-ttu-id="211bf-114">Konsekvensene av synkronisering</span><span class="sxs-lookup"><span data-stu-id="211bf-114">Consequences of Synchronization</span></span>
<span data-ttu-id="211bf-115">Når kontakten synkroniseres med kunde, leverandør, bankkonto:</span><span class="sxs-lookup"><span data-stu-id="211bf-115">When the contact is synchronized with the customer, vendor, bank account:</span></span>

* <span data-ttu-id="211bf-116">Du trenger du bare å oppdatere opplysninger på ett sted.</span><span class="sxs-lookup"><span data-stu-id="211bf-116">You only have to update information in one place.</span></span> <span data-ttu-id="211bf-117">Hvis du for eksempel endrer telefonnummeret på kontakten, blir telefonnummeret automatisk oppdatert med de samme endringene på kunden, leverandøren eller bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="211bf-117">For example, if you modify the phone number on the contact, the phone number is automatically updated with the same modification on the customer, the vendor, or the bank account.</span></span>
* <span data-ttu-id="211bf-118">Hvis du har angitt en nummerserie for kontakter, opprettes det automatisk et kontaktkort for kunden, leverandøren eller bankkontoen når du oppretter et kundekort, leverandørkort eller bankkontokort.</span><span class="sxs-lookup"><span data-stu-id="211bf-118">If you have specified a number series for contacts, when you create a customer card, a vendor card, or a bank account card, a contact card is automatically created for the customer, vendor or bank account.</span></span>
* <span data-ttu-id="211bf-119">Du kan du opprette tilbud og ordrer og forespørsler og bestillinger fra kontakten.</span><span class="sxs-lookup"><span data-stu-id="211bf-119">You can create sales quotes and orders, and purchase quotes and orders from the contact.</span></span>
* <span data-ttu-id="211bf-120">Du kan angi at samhandlinger registreres når du utfører handlinger, for eksempel når du skriver ut ordrer, rammeordrer, oppretter serviceordrer, sender e-post og så videre.</span><span class="sxs-lookup"><span data-stu-id="211bf-120">You can have your interactions recorded when you perform actions such as printing orders, blanket orders, creating sales service orders, sending e-mails, and so on.</span></span>
* <span data-ttu-id="211bf-121">Hvis du sletter en kontakt som er koblet til en kunde, leverandør eller bankkonto, er det bare kontakten som fjernes.</span><span class="sxs-lookup"><span data-stu-id="211bf-121">If you delete a contact linked to a customer, vendor or bank account, only the contact is removed.</span></span> <span data-ttu-id="211bf-122">Kunden, leverandøren eller bankkontoen beholdes.</span><span class="sxs-lookup"><span data-stu-id="211bf-122">The customer, vendor, or bank account remains.</span></span>
* <span data-ttu-id="211bf-123">Hvis du sletter en kunde, leverandør eller bankkonto som er koblet til en kontakt, beholdes kontakten.</span><span class="sxs-lookup"><span data-stu-id="211bf-123">If you delete a customer, vendor, bank account linked to a contact, the contact remains.</span></span>

> [!NOTE]  
>   <span data-ttu-id="211bf-124">Noen detaljer, for eksempel fakturerings- og bokføringsopplysninger, vises ikke på kontaktkortet.</span><span class="sxs-lookup"><span data-stu-id="211bf-124">Some details, such as invoicing and posting details, do not appear on the contact card.</span></span> <span data-ttu-id="211bf-125">Du vil derfor kanskje legge dem til manuelt på kundekortet, leverandørkortet eller bankkontokortet når du oppretter kontakter som kunder, leverandører eller bankkonti.</span><span class="sxs-lookup"><span data-stu-id="211bf-125">Therefore, you may want to add them manually on the customer card, vendor card, or bank account card when you create contacts as customers, vendors or bank accounts.</span></span>

## <a name="see-also"></a><span data-ttu-id="211bf-126">Se også</span><span class="sxs-lookup"><span data-stu-id="211bf-126">See Also</span></span>
[<span data-ttu-id="211bf-127">Administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="211bf-127">Managing Contacts</span></span>](marketing-contacts.md)  
<span data-ttu-id="211bf-128">[Arbeide med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="211bf-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
