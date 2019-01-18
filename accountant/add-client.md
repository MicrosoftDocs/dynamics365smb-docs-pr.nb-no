---
title: "Hente klienter i regnskapsføreropplevelsen i Dynamics 365 | Microsoft-dokumentasjon"
description: "Lær hvordan du legger til eksisterende klienter i Accountant Hub for Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 11/23/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: c7f0af8d3535f558567cd40c841909cd151ce313
ms.contentlocale: nb-no
ms.lasthandoff: 11/26/2018

---
# <a name="add-clients-to-your-dashboard-in-include-d365acclongincludesd365acclongmdmd"></a>Legge til klienter i instrumentbordet i [!INCLUDE [d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE [d365fin_early_release](includes/d365fin_early_release.md.md)]

Du kan legge til en klient ved å bruke **Klienter**-siden, som du kan åpne ved å velge handlingen **Administrer klienter** på båndet. Velg ganske enkelt **Ny**, og fyll deretter ut feltene.  

> [!div class="mx-imgBorder"]
> ![Legg til en klient](./media/accountant-add-client/manage-client.png)

Dataene på kortet for hver klient angis av deg, og du kan endre dem etter behov. Feltet **URL-adresse til klient** er avgjørende – det er slik du får tilgang til hver klients [!INCLUDE [d365fin](includes/d365fin_md.md)]. Bruk handlingen **Valider URL-adresse for klient** på båndet for å teste at du har angitt riktig kobling. URL-adressen som du må du angi, peker til klientens [!INCLUDE [d365fin](includes/d365fin_md.md)] og inneholder domeneadressen. Hvis de for eksempel har angitt domenet mittfirma.com, vil koblingen til [!INCLUDE [d365fin](includes/d365fin_md.md)] være *https://businesscentral.dynamics.com/mybusiness.com?redirectedfromsignup=1*.  

> [!NOTE]
>  Før oppdateringen i mai 2018 hadde URL-adressen du angav et annet format med kundens selskapsnavn i begynnelsen. I gjeldende versjon av [!INCLUDE [d365fin](includes/d365fin_md.md)] er formatet ```https://businesscentral.dynamics.com/clientdomain?redirectedfromsignup=1```, der ```clientdomain``` representerer domenet til klienten.  

Denne URL-adressen for klient brukes deretter når du velger menyelementet **Gå til selskap** på instrumentbordet [!INCLUDE [d365acc](includes/d365acc_md.md)].  

### <a name="get-invited-to-a-clients-include-d365finlongincludesd365finlongmdmd"></a>Bli invitert til en klients [!INCLUDE [d365fin_long](includes/d365fin_long_md.md)]
Et selskap som bruker [!INCLUDE [d365fin](includes/d365fin_md.md)], kan invitere deg til [!INCLUDE [d365fin](includes/d365fin_md.md)] som deres eksterne regnskapsfører. Hvis du vil bli invitert, må du gi dem e-postadressen du brukte med [!INCLUDE [d365acc](includes/d365acc_md.md)], for eksempel <em>me@accountant.com</em>. Klientens administrator kan deretter legge deg til i systemet ved å kjøre veiviseren **Inviter ekstern regnskapsfører**.  

Derfor vil du motta e-post fra klienten med koblinger til deres [!INCLUDE [d365fin](includes/d365fin_md.md)]. Den første koblingen er en invitasjon for å få tilgang til selskapet. Åpne koblingen og godta trinnene som legger deg til i klientens [!INCLUDE [d365fin](includes/d365fin_md.md)]. Den andre koblingen er for å legge til denne klienten på instrumentbordet i [!INCLUDE [d365acc](includes/d365acc_md.md)] som beskrevet ovenfor.  

Når du har godtatt invitasjonen, logges du på og har tilgang til klienten økonomiske data fra **Regnskapsfører**-rollesenteret. Hvis du vil ha mer informasjon, se [Regnskapsføreropplevelser [!INCLUDE[d365fin](includes/d365fin_md.md)]](/dynamics365/business-central/finance-accounting?toc=/dynamics365/accountants/toc.json).  

## <a name="see-also"></a>Se også
[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Feilsøking [!INCLUDE[d365acc](includes/d365acc_md.md)]](troubleshooting.md)  

