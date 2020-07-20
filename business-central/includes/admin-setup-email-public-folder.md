---
author: edupont04
ms.service: dynamics365-accountant
ms.topic: include
ms.date: 06/25/2020
ms.author: edupont
ms.openlocfilehash: 8c5f4205128d52ec88f432cea7ece98e0310546d
ms.sourcegitcommit: 3e9c89f90db5eaed599630299353300621fe4007
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/01/2020
ms.locfileid: "3528013"
---
<span data-ttu-id="078c8-101">Før du kan opprette e-postpålogging må du klargjøre Exchange Online med [fellesmapper](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="078c8-101">Before you can set up email logging, you must prepare your Exchange Online with [public folders](/exchange/collaboration/public-folders/public-folders?view=exchserver-2019).</span></span> <span data-ttu-id="078c8-102">Du kan gjøre dette i [Administrasjonssenter for Exchange](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), eller du kan bruke [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="078c8-102">You can do this in the [Exchange admin center](/Exchange/architecture/client-access/exchange-admin-center?view=exchserver-2019), or you can use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps).</span></span>  

> [!TIP]
> <span data-ttu-id="078c8-103">Hvis du vil bruke [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), kan du finne inspirasjon for hvordan du konfigurerer skriptet i et eksempelskript som vi publiserte i [BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span><span class="sxs-lookup"><span data-stu-id="078c8-103">If you want to use the [Exchange Management Shell](/powershell/exchange/exchange-management-shell?view=exchange-ps), you can find inspiration for how to set up your script in a sample script that we published to [the BCTech repo](https://github.com/microsoft/BCTech/tree/master/samples/EmailLogging).</span></span>

<span data-ttu-id="078c8-104">Listen nedenfor beskriver de viktigste trinnene med koblinger for å finne ut mer.</span><span class="sxs-lookup"><span data-stu-id="078c8-104">The following list describes the main steps with links to learn more.</span></span>  

- <span data-ttu-id="078c8-105">Opprett en administratorrolle for fellesmapper basert på informasjonen i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="078c8-105">Create an admin role for public folders based on the information in the following table:</span></span>

  |<span data-ttu-id="078c8-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="078c8-106">Property</span></span>        |<span data-ttu-id="078c8-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="078c8-107">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="078c8-108">Name</span><span class="sxs-lookup"><span data-stu-id="078c8-108">Name</span></span>            |<span data-ttu-id="078c8-109">Administrasjon av fellesmapper</span><span class="sxs-lookup"><span data-stu-id="078c8-109">Public Folders Management</span></span> |
  |<span data-ttu-id="078c8-110">Valgte roller</span><span class="sxs-lookup"><span data-stu-id="078c8-110">Selected roles</span></span>  |<span data-ttu-id="078c8-111">Fellesmapper</span><span class="sxs-lookup"><span data-stu-id="078c8-111">Public Folders</span></span>            |
  |<span data-ttu-id="078c8-112">Valgte medlemmer</span><span class="sxs-lookup"><span data-stu-id="078c8-112">Selected members</span></span>|<span data-ttu-id="078c8-113">E-postadressen til brukerkontoen som Business Central bruker til å kjøre loggføringsjobben for e-post</span><span class="sxs-lookup"><span data-stu-id="078c8-113">The email of the user account that Business Central will use to run the email logging job</span></span>|

  <span data-ttu-id="078c8-114">Hvis du vil ha mer informasjon, kan du se [Administrere rollegrupper](/exchange/permissions/role-groups?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="078c8-114">For more information, see [Manage role groups](/exchange/permissions/role-groups?view=exchserver-2019).</span></span>

- <span data-ttu-id="078c8-115">Opprett en ny postboks for fellesmapper basert på informasjonen i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="078c8-115">Create a new public folder mailbox based on the information in the following table:</span></span>

  |<span data-ttu-id="078c8-116">Egenskap</span><span class="sxs-lookup"><span data-stu-id="078c8-116">Property</span></span>        |<span data-ttu-id="078c8-117">Verdi</span><span class="sxs-lookup"><span data-stu-id="078c8-117">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="078c8-118">Name</span><span class="sxs-lookup"><span data-stu-id="078c8-118">Name</span></span>            |<span data-ttu-id="078c8-119">Fellespostboks</span><span class="sxs-lookup"><span data-stu-id="078c8-119">Public MailBox</span></span>            |

  <span data-ttu-id="078c8-120">Hvis du vil ha mer informasjon, kan du se [Opprette en postboks for fellesmapper i Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span><span class="sxs-lookup"><span data-stu-id="078c8-120">For more information, see [Create a public folder mailbox in Exchange Server](/exchange/collaboration/public-folders/create-public-folder-mailboxes).</span></span>  

- <span data-ttu-id="078c8-121">Opprette nye fellesmapper</span><span class="sxs-lookup"><span data-stu-id="078c8-121">Create new public folders</span></span>

  - <span data-ttu-id="078c8-122">Opprett en ny fellesmappe med navnet *Loggføring av e-post* i roten, slik at hele banen til mappen blir ```\Email Logging\```</span><span class="sxs-lookup"><span data-stu-id="078c8-122">Create a new public folder with the name *Email Logging* in the root so that the full path to the folder becomes ```\Email Logging\```</span></span>
  - <span data-ttu-id="078c8-123">Opprett to undermapper slik at resultatet er følgende fullstendige baner til mappene:</span><span class="sxs-lookup"><span data-stu-id="078c8-123">Create two subfolders so that the the result is the following full paths to the folders:</span></span>
    - ```\Email Logging\Queue\```
    - ```\Email Logging\Storage\```

  <span data-ttu-id="078c8-124">Hvis du vil ha mer informasjon, kan du se [Opprette en fellesmappe](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span><span class="sxs-lookup"><span data-stu-id="078c8-124">For more information, see [Create a public folder](/exchange/collaboration/public-folders/create-public-folders?view=exchserver-2019).</span></span>

- <span data-ttu-id="078c8-125">Aktiver e-post for fellesmappen *Kø*</span><span class="sxs-lookup"><span data-stu-id="078c8-125">Mail-enable the *Queue* public folder</span></span>

  <span data-ttu-id="078c8-126">Hvis du vil ha mer informasjon, kan du se [Aktivere eller deaktivere e-post for en fellesmappe](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span><span class="sxs-lookup"><span data-stu-id="078c8-126">For more information, see [Mail-enable or mail-disable a public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019)</span></span>

- <span data-ttu-id="078c8-127">Aktivere e-post for å sende e-post til fellesmappen *Kø* ved bruk av Outlook eller Exchange Management Shell</span><span class="sxs-lookup"><span data-stu-id="078c8-127">Mail-enable sending emails to the *Queue* public folder using Outlook or the Exchange Management Shell</span></span>

  <span data-ttu-id="078c8-128">Hvis du vil ha mer informasjon, kan du se [Tillat at anonyme brukere kan sende e-post til en fellesmappe som e-post er aktivert for](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span><span class="sxs-lookup"><span data-stu-id="078c8-128">For more information, see [Allow anonymous users to send email to a mail-enabled public folder](/exchange/collaboration/public-folders/mail-enable-or-disable?view=exchserver-2019#allow-anonymous-users-to-send-email-to-a-mail-enabled-public-folder)</span></span>

- <span data-ttu-id="078c8-129">Angi brukeren for loggføring av e-post som eier av fellesmappene *Kø* og *Lagring* ved hjelp av Outlook eller Exchange Management Shell, basert på informasjonen i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="078c8-129">Set the email logging user as an owner of both public folders, *Queue* and *Storage* public folders  using Outlook or the Exchange Management Shell based on the information in the following table:</span></span>

  |<span data-ttu-id="078c8-130">Egenskap</span><span class="sxs-lookup"><span data-stu-id="078c8-130">Property</span></span>        |<span data-ttu-id="078c8-131">Verdi</span><span class="sxs-lookup"><span data-stu-id="078c8-131">Value</span></span>                     |
  |----------------|--------------------------|
  |<span data-ttu-id="078c8-132">Bruker</span><span class="sxs-lookup"><span data-stu-id="078c8-132">User</span></span>            |<span data-ttu-id="078c8-133">E-postadressen til brukerkontoen som Business Central bruker til å kjøre loggføringsjobben for e-post</span><span class="sxs-lookup"><span data-stu-id="078c8-133">The email of the user account that Business Central will use to run the email logging job</span></span>|
  |<span data-ttu-id="078c8-134">Tillatelsesnivå</span><span class="sxs-lookup"><span data-stu-id="078c8-134">Permission level</span></span>|<span data-ttu-id="078c8-135">Eier</span><span class="sxs-lookup"><span data-stu-id="078c8-135">Owner</span></span>                     |

  <span data-ttu-id="078c8-136">Hvis du vil ha mer informasjon, kan du se [Tilordne tillatelser til fellesmapper](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span><span class="sxs-lookup"><span data-stu-id="078c8-136">For more information, see [Assign permissions to the public folder](/exchange/collaboration-exo/public-folders/set-up-public-folders#step-3-assign-permissions-to-the-public-folder).</span></span>

- <span data-ttu-id="078c8-137">Opprett to nye regler for e-postflyt basert på informasjonen i følgende tabell:</span><span class="sxs-lookup"><span data-stu-id="078c8-137">Create two mail flow rules based on the information in the following table</span></span>

  |<span data-ttu-id="078c8-138">Formål</span><span class="sxs-lookup"><span data-stu-id="078c8-138">Purpose</span></span>  |<span data-ttu-id="078c8-139">Name</span><span class="sxs-lookup"><span data-stu-id="078c8-139">Name</span></span> |<span data-ttu-id="078c8-140">Betingelser</span><span class="sxs-lookup"><span data-stu-id="078c8-140">Conditions</span></span>                        |<span data-ttu-id="078c8-141">Handling</span><span class="sxs-lookup"><span data-stu-id="078c8-141">Action</span></span>                                       |
  |---------|-----|----------------------------------|---------------------------------------------|
  |<span data-ttu-id="078c8-142">Regel for innkommende e-post</span><span class="sxs-lookup"><span data-stu-id="078c8-142">A rule for incoming email</span></span> |<span data-ttu-id="078c8-143">Logge e-post sendt til denne organisasjonen</span><span class="sxs-lookup"><span data-stu-id="078c8-143">Log Email Sent to This Organization</span></span>|<span data-ttu-id="078c8-144">*Avsenderen* befinner seg *utenfor organisasjonen*, og *mottakeren* befinner seg *i organisasjonen*</span><span class="sxs-lookup"><span data-stu-id="078c8-144">*The sender* is located *Outside the organization*, and *the recipient* is located *Inside the organization*</span></span>|<span data-ttu-id="078c8-145">Sende blindkopi til e-postkontoen som er angitt for fellesmappen *Kø*</span><span class="sxs-lookup"><span data-stu-id="078c8-145">BCC the email account that is specified for the *Queue* public folder</span></span>|
  |<span data-ttu-id="078c8-146">Regel for utgående e-post</span><span class="sxs-lookup"><span data-stu-id="078c8-146">A rule for outgoing email</span></span> | <span data-ttu-id="078c8-147">Logge e-post sendt fra denne organisasjonen</span><span class="sxs-lookup"><span data-stu-id="078c8-147">Log Email Sent from This Organization</span></span> |<span data-ttu-id="078c8-148">*Avsenderen* befinner seg *i organisasjonen*, og *mottakeren* befinner seg *utenfor organisasjonen*</span><span class="sxs-lookup"><span data-stu-id="078c8-148">*The sender* is located *Inside the organization*, and *the recipient* is located *Outside the organization*</span></span>|<span data-ttu-id="078c8-149">Sende blindkopi til e-postkontoen som er angitt for fellesmappen *Kø*</span><span class="sxs-lookup"><span data-stu-id="078c8-149">BCC the email account that is specified for the *Queue* public folder</span></span>|
  
  <span data-ttu-id="078c8-150">Hvis du vil ha mer informasjon, kan du se [Administrere regler for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) og [Regelhandlinger for e-postflyt i Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span><span class="sxs-lookup"><span data-stu-id="078c8-150">For more information, see [Manage mail flow rules in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules) and [Mail flow rule actions in Exchange Online](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rule-action).</span></span>

> [!NOTE]
> <span data-ttu-id="078c8-151">Hvis du utfører endringer i Exchange Management Shell, blir endringene synlige i Administrasjonssenter for Exchange etter en forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="078c8-151">If you make changes in the Exchange Management Shell, the changes become visible in the Exchange admin center after a delay.</span></span> <span data-ttu-id="078c8-152">Endringene som er gjort i Exchange, vil også være tilgjengelige i [!INCLUDE[prodshort](prodshort.md)] etter en forsinkelse.</span><span class="sxs-lookup"><span data-stu-id="078c8-152">Also, the changes made in Exchange will be available in [!INCLUDE[prodshort](prodshort.md)] after a delay.</span></span>
