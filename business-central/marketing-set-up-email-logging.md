---
title: Konfigurere loggføring av e-post| Microsoft Docs
description: Lær hvordan du kan gjøre om e-postinteraksjon mellom selgere og kunder til reelle salgsmuligheter.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 08/26/2019
ms.author: bholtorf
ms.openlocfilehash: e42618be17ff4f9bfe0d54a88e70d5a1841568c1
ms.sourcegitcommit: 8d9f08304b2f3b5504332bc626383797564ac5e3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/26/2019
ms.locfileid: "1920469"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="d23b8-103">Spor utveksling av e-postmeldinger mellom selgere og kontakter</span><span class="sxs-lookup"><span data-stu-id="d23b8-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>
<span data-ttu-id="d23b8-104">Få mer ut av kommunikasjonen mellom selgere og de eksisterende eller potensielle kundene ved å spore e-postutvekslinger og deretter gjøre dem om til salgsmuligheter.</span><span class="sxs-lookup"><span data-stu-id="d23b8-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d23b8-105">fungerer med Exchange Online for å føre en logg over innkommende og utgående meldinger.</span><span class="sxs-lookup"><span data-stu-id="d23b8-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="d23b8-106">Du kan vise og analysere innholdet i hver enkelt melding på siden **Samhandlingsposter**.</span><span class="sxs-lookup"><span data-stu-id="d23b8-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-included365finincludesd365fin_mdmd-to-log-email-messages"></a><span data-ttu-id="d23b8-107">Konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] for å logge e-postmeldinger</span><span class="sxs-lookup"><span data-stu-id="d23b8-107">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>
<span data-ttu-id="d23b8-108">Kom i gang med e-postpålogging med to enkle trinn:</span><span class="sxs-lookup"><span data-stu-id="d23b8-108">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="d23b8-109">Koble [!INCLUDE[d365fin](includes/d365fin_md.md)] til Exchange Online for Office 365-abonnementet.</span><span class="sxs-lookup"><span data-stu-id="d23b8-109">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="d23b8-110">Exchange Online behandler e-postmeldingene.</span><span class="sxs-lookup"><span data-stu-id="d23b8-110">Exchange Online handles your email messages.</span></span> <span data-ttu-id="d23b8-111">Vi har gjort dette trinnet enkelt ved å tilby en veiledning for assistert oppsett.</span><span class="sxs-lookup"><span data-stu-id="d23b8-111">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="d23b8-112">Du trenger bare administratorlegitimasjon for administratorkontoen i Office 365.</span><span class="sxs-lookup"><span data-stu-id="d23b8-112">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="d23b8-113">Gå til **Assistert oppsett** og velg deretter **Konfigurer loggføring av e-post**.</span><span class="sxs-lookup"><span data-stu-id="d23b8-113">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span> 
2. <span data-ttu-id="d23b8-114">Kontroller at det er angitt gyldige e-postadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] for selgere og kontakter, avhengig av om de er potensielle eller eksisterende kunder.</span><span class="sxs-lookup"><span data-stu-id="d23b8-114">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="d23b8-115">For hver kunde eller selger åpner du **Kontakt** eller **Selger/innkjøper**-kortet og ser i **E-post** -feltet.</span><span class="sxs-lookup"><span data-stu-id="d23b8-115">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="d23b8-116">Når du har fullført trinnene i guiden, kan du kontrollere om tilkoblingen var vellykket.</span><span class="sxs-lookup"><span data-stu-id="d23b8-116">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="d23b8-117">Søk etter **Markedsføringsoppsett**, velg **Behandle**, og velg deretter **Funksjoner** og deretter **Valider oppsett for loggføring av e-post**.</span><span class="sxs-lookup"><span data-stu-id="d23b8-117">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="d23b8-118">Vise utvekslinger av e-postmeldinger i samhandlingsloggen</span><span class="sxs-lookup"><span data-stu-id="d23b8-118">Viewing Email Message Exchanges in the Interaction Log</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="d23b8-119">oppretter en post på siden **Samhandlingslogg** hver gang en selger og en kontakt utveksler en e-postmelding.</span><span class="sxs-lookup"><span data-stu-id="d23b8-119">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="d23b8-120">Hvis du vil vise samhandlingsloggen, åpner du **Kontakter** eller **Selger/innkjøper**-kortet for personen, og deretter velger du **Naviger**, **Logg** og deretter **Samhandlingsposter**.</span><span class="sxs-lookup"><span data-stu-id="d23b8-120">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="d23b8-121">Det er et par ting vi kan gjøre med hver oppføring i loggen, for eksempel:</span><span class="sxs-lookup"><span data-stu-id="d23b8-121">There are a few things we can do with each entry in the log, for example:</span></span>

* <span data-ttu-id="d23b8-122">Vis innholdet i e-postmeldingen som ble utvekslet, ved å klikke handlingen **Vis vedlegg**.</span><span class="sxs-lookup"><span data-stu-id="d23b8-122">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
* <span data-ttu-id="d23b8-123">Gjør en e-postutveksling om til en salgsmulighet – Hvis en oppføring ser lovende ut, kan du gjøre den om til en salgsmulighet og deretter håndtere fremdriften for den mot et salg.</span><span class="sxs-lookup"><span data-stu-id="d23b8-123">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="d23b8-124">Velg oppføringen for å gjøre dette, og velg deretter handlingen **Opprett salgsmulighet**.</span><span class="sxs-lookup"><span data-stu-id="d23b8-124">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="d23b8-125">Hvis du vil ha mer informasjon, kan du se [Håndtere salgsmuligheter](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="d23b8-125">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d23b8-126">Se også</span><span class="sxs-lookup"><span data-stu-id="d23b8-126">See Also</span></span>
[<span data-ttu-id="d23b8-127">Administrere forbindelser</span><span class="sxs-lookup"><span data-stu-id="d23b8-127">Managing Relationships</span></span>](marketing-relationship-management.md)

